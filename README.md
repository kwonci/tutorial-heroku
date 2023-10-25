## 10/24 Heroku based docker application deployments

### Deploy explanation based on time

1. docker build

2. create heroku app by command(`heroku create`),

then automatically, heroku app registry is created.

3. tag docker image based on app name + process types, then deploy(`heroku container:push`)

4. deploy push(`heroku container:release`)

### Model

1. It has web/worker model(process model). Web for request handling, and worker for CPU intensive/blocking operations.

2. I saw that two operations communicate with "postgres-queue"..

### Pricing?

1. Pricing is based on dynos,

if deployed, default dyno is `basic`(0.010$/hour). Increased by time
Also there's Eco pricing, which has flat fee(5$/month).
