FROM nginx:1.15.2-alpine

RUN mkdir -p /code/node_modules

WORKDIR /code

COPY . ./

RUN apk --no-cache --virtual build-dependencies add \
	nodejs nodejs-npm \
    python \
    make \
    gcc \
    g++ \
    zlib-dev \
    && npm install

RUN npm install -f --unsafe-perm

RUN ls

# RUN npm run build

# COPY nginx.conf /etc/nginx/nginx.conf

# RUN cp -r build /var/www

EXPOSE 3000

#ENTRYPOINT ["nginx","-g","daemon off;"]

