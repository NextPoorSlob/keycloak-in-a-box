# Keycloak In A Box

I repeatedly need an SSO identity provider for testing. The purpose of this project is to provide an out-of-the box
solution. It contains a configured Test realm with an oidc-client. The client already has a number of users all
pre-configured.

## Work in Progress

This is a work-in-progress. I do intend to complete it soon. If you come across this and want to use it, please
email me at sgelman@nextpoorslob.com, and I'll prioritize it and contact you.

## Current State

1. Postgres database for Keycloak data. This database maintains its data from run to run.
2. Added local-keycloak network.
3. Added Keycloak service
4. Todo: preconfigure data

## To Run

To start:

```shell
docker-compose up -d
```

To stop:

```shell
docker-compose down
```

To reset the database:

```shell
docker volume rm keycloak-in-a-box_postgres-data
```

## Apple Silicon (M1/M2)

Apple has become the new Microsoft, messing with standards for their own benefit. Like a lot of Docker images, Keycloak
doesn't play well with Apple Silicon.

To make it work, use `sleighzy/keycloak:latest` for the Keycloak image.