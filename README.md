# Cryptocurrency Investment Collections Project Docker Configuration

This repository contains Docker configuration files for running [project](https://github.com/a3naumov/cryptocurrency-investment-collections) using the following services:

| Service    | Version |
|------------|---------|
| Nginx      | 1.25    |
| PHP        | 8.2     |
| PostgreSQL | 16.1    |

## Getting Started

Follow these steps to set up and run the project using Docker and Docker Compose.

1) Follow the instructions from the main repository

2) Make Scripts Executable

```shell
chmod +x ./bin/*
```

3) Add SSL Certificates

Generate SSL certificates and place them in the **./docker/nginx/certs** directory.
```shell
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./docker/nginx/certs/server.key -out ./docker/nginx/certs/server.crt
```

4) Configure PHP

Copy the appropriate PHP configuration file (**php.ini-development** or **php.ini-production**) to **./docker/php/conf/php.ini** and adjust the settings as needed.
```shell
cp ./docker/php/conf/php.ini-development ./docker/php/conf/php.ini
```

5) Set Environment Variables

Copy the **.env.example** file to **.env** and fill in the necessary values.
```shell
cp .env.example .env
```

## Running the Project

Refer to the project repository for specific instructions on running the project. The Docker configuration provided here ensures the required services are set up for your project.

For detailed instructions on running the project, please visit the [main repository](https://github.com/a3naumov/cryptocurrency-investment-collections).