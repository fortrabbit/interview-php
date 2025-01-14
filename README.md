# PHP Interview Task

Build a simple REST API from scratch using Symfony and Doctrine ORM, using a preferred database backend of your choice.

## Entities

`app` is an entity stored in database with these properties:

- id - numeric database id (should never be returned in api response)
- publicId - random 6 character string
- name - textfield 20 characters
- environments - one-to-many relation to environment entities

`environment` is an entity stored in database with these properties:

- id - numeric database id (should never be returned in api response)
- publicId - random 6 character string
- name - textfield 20 characters
- phpVersion - one of these: 8.1, 8.2, 8.3
- app - many-to-one relation to app entity

## Methods

The API should have five methods.

- Add app with arguments
    - name
- Add environment with arguments
    - name
    - phpVersion
    - appPublicId - which app this environment belongs to
- Delete environment
- Delete app (should also delete linked environments)
- List apps and environments in hierarchical array

## Commands
Create a Symfony CLI command to seed the database with a few randomized objects

## Additional tips
- Demonstrate best practices (e.g. OOP, tests, docs), but be pragmatic about effort.
- Provide instructions for how to run the project in a local environment (using docker, ddev or similar)
- Ask early if things are not clear, it's not a shame to ask for help.

## When you are done
- Upload your code to a fork of this repo, or to a private personal repo and add @erinbit as collaborator
- Send us an email and we will review the code and then invite you to a short video call about it
