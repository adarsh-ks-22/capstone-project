FROM node:18 AS base

WORKDIR /app

COPY package.json yarn.lock* package-lock.json* ./

RUN  \
    if [ -f yarn.lock ]; then yarn --frozen-lockfile; \
    elif [ -f package-lock.json ]; then npm install; \
    else echo "Error: Lockfile not found" && exit 1; \
    fi

COPY . .

RUN npm run build

EXPOSE 3000

CMD [ "npm", "start" ]