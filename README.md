Example how to set up DB on localhost:
```
make run-database
docker exec -it forfeater_db bash
psql -U postgres -h localhost
CREATE DATABASE forfeaterjs;
CREATE USER forfeater WITH PASSWORD 'secret';
GRANT ALL PRIVILEGES ON DATABASE forfeaterjs TO forfeater;
```

# forfeater flow:

# ALL:
#### get access token
> `POST /auth/login`
```
Content-Type: application/x-www-form-urlencoded

grant_type: password
client_id: forfeaterWeb
client_secret: forfeaterSecret
username: test@rst-it.com
password: secret
```
#### get user details by token (examplary route with authentitacion)
> `/auth/user`
```
Content-Type: application/x-www-form-urlencoded
Authorization = Bearer
```

API is available at `/doc/index.html`, unless
```
make api-doc
```

## License

forefeater is Copyright © 2018 SoftwareBrothers.co. It is free software, and may be redistributed under the terms specified in the [LICENSE](LICENSE) file.

## About SoftwareBrothers.co

<img src="https://softwarebrothers.co/assets/images/software-brothers-logo-full.svg" width=240>


We are a software company who provides web and mobile development and UX/UI services, friendly team that helps clients from all over the world to transform their businesses and create astonishing products.

* We are available to [hire](https://softwarebrothers.co/contact).
* If you want to work for us - checkout the [career page](https://softwarebrothers.co/career).
