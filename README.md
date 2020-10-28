# hasura

Trying things

Uses a heroku postgres database

https://cloud.hasura.io/projects

https://cloud.hasura.io/project/ef77bb8f-bf77-4b6c-ab08-1e9384066b0c/details

https://valued-haddock-79.hasura.app/console?auto_login=true


* https://hasura.io/learn/graphql/hasura/setup/

> Hasura requires a Postgres database to start with

Hasura Cloud will perform the following for you:

* Create an app on Heroku
* Install Postgres Add-on
* Fetch database URL that you can use to configure Hasura

> open the Hasura Console to get started.


## basic data modelling
> we will build the data model for a realtime todo app.

## rxdb
* Any code and assets used should be available offline
* Any data changes should be made locally First and then synced to the cloud.

> all changes and reads on the front end are made from a local database. The local database is then synced with the backend service.

>  we provide RxDB with a callback function to be called whenever there is a change 

> Hasura requires a Postgres database to start with

-----------------------------------
## auth0
> The basic idea is that, whenever a user authenticates with Auth0, the client app receives a token that can be sent in the Authorization headers of all GraphQL requests. Hasura GraphQL Engine would verify if the token is valid and allow the user to perform appropriate queries.






