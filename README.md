## Description

web-app ecommerce docker container

## env file

```env:.env
#PORT
PORT=5000

#Database
MONGO_INITDB_ROOT_USERNAME={YOUR_MONGO_INITDB_ROOT_USERNAME}
MONGO_INITDB_ROOT_PASSWORD={YOUR_MONGO_INITDB_ROOT_PASSWORD}
MONGO_INITDB_DATABASE={YOUR_MONGO_INITDB_DATABASE}
MONGO_INITDB_USERNAME={YOUR_MONGO_INITDB_PASSWORD}
MONGO_INITDB_PASSWORD={YOUR_MONGO_INITDB_PASSWORD}
DATABASE_URL='mongodb://{YOUR_MONGO_INITDB_ROOT_USERNAME}:{YOUR_MONGO_INITDB_ROOT_PASSWORD}@ecommerce_mongo:27017/ecommerce?authSource=admin'

#logging
DEBUG="debugging:*"

#Facebook Authentication
FACEBOOK_APP_ID={YOUR_FACEBOOK_APP_ID}
FACEBOOK_APP_SECRET={YOUR_FACEBOOK_APP_SECRET}
FACEBOOK_CALLBACK_ROUTE=/auth/facebook/callback

#Google Authentication
GOOGLE_CLIENT_ID={YOUR_GOOGLE_CLIENT_ID}
GOOGLE_CLIENT_SECRET={YOUR_GOOGLE_CLIENT_SECRET}
GOOGLE_CALLBACK_ROUTE=/auth/google/callback

#Github Authentication
GITHUB_CLIENT_ID={YOUR_GITHUB_CLIENT_ID}
GITHUB_CLIENT_SECRET={YOUR_GITHUB_CLIENT_SECRET}
GITHUB_CALLBACK_ROUTE=/auth/github/callback

#SECRET

#JWT
JWT_SECRET={YOUR_JWT_SECRET}

#Send Email
SENDGRID_API_KEY={YOUR_SENDGRID_API_KEY}

#Frontend URL
FRONTEND_URI=http://localhost:3000

```

```env:.env.local
NEXT_PUBLIC_BACKEND_URI='http://api:5000'
NEXT_PUBLIC_TOKEN_NAME='accessToken'
NEXT_PUBLIC_FACEBOOK_LOGIN_URI='http://api:5000/auth/facebook'
NEXT_PUBLIC_GOOGLE_LOGIN_URI='http://api:5000/auth/google'
NEXT_PUBLIC_GITHUB_LOGIN_URI='http://api:5000/auth/github'
```

## Installation

```bash
$ docker compose up -d
```

## PORT SERVICE

- front-end - [localhost:3000]
- back-end - [localhost:5000]
- mongoDB - [localhost:5001]
- elasticsearch - [localhost:9200]
- logstash - [localhost:8080] , [localhost:8081]
- kibana - [localhost:5601]