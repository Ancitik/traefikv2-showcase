# Traefik v2.2 sample

## Features

- Local, trusted, selfsigned certificates using [mkcert](https://github.com/FiloSottile/mkcert)

## Requirements

- [mkcert](https://github.com/FiloSottile/mkcert)

## Usage

### Cert generation

We will use mkcert to generate self-signed and trusted certificates

- Create local trusted authority

      mkcert -install
- Generate certs

      mkcert -cert-file certs/local-cert.pem -key-file certs/local-key.pem "traefik.localhost" "whoami.localhost" "*.localhost" 

### Run

- Edit `.env`
- Launch the stack `docker-compose up -d`
- Open http://whoami.localhost