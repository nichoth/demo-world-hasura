# hasura
What is hasuram? I think its a graphql API that you can add to a database.

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

-------------------------------------------

## admin key
> If you want to make API calls from outside the console, you need to pass the admin secret as the `x-hasura-admin-secret` request header

> Once an admin secret is added, we need to configure Hasura to use the Auth0 public keys. An easier way to generate the config for JWT is to use the following link -- https://hasura.io/jwt-config/

Great! Now your Hasura instance is secured using Auth0.

----------------------------------------------

> Auth0 has rules that can be set up to be called on every login request.
> need to set up a rule in Auth0 which allows the users of Auth0 to be in sync with the users in our database

-------------------------------------------------

> let's test this setup by getting the access token from Auth0 and making GraphQL queries with the Authorization headers to see if the permissions are applied.

> In the Hasura Console GraphiQL tab, you can add a header `Authorization: Bearer <access_token>` for making such requests.


```
  "access_token": "eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IlJVVXlRVFpFUXpZeFJqZzRNak0zUXpKRU56ZEdOMFU0T1RaR056VkNNMEUwTWpZeVJqZzFPUSJ9.eyJodHRwczovL2hhc3VyYS5pby9qd3QvY2xhaW1zIjp7IngtaGFzdXJhLWRlZmF1bHQtcm9sZSI6InVzZXIiLCJ4LWhhc3VyYS1hbGxvd2VkLXJvbGVzIjpbInVzZXIiXSwieC1oYXN1cmEtdXNlci1pZCI6ImF1dGgwfDVmOTlhZmYwNmIxNDM1MDA3N2YwYmY1YSJ9LCJpc3MiOiJodHRwczovL2Rldi1wYmJxMDZzby5hdXRoMC5jb20vIiwic3ViIjoiYXV0aDB8NWY5OWFmZjA2YjE0MzUwMDc3ZjBiZjVhIiwiYXVkIjpbImh0dHBzOi8vaGFzdXJhLmlvL2xlYXJuIiwiaHR0cHM6Ly9kZXYtcGJicTA2c28uYXV0aDAuY29tL3VzZXJpbmZvIl0sImlhdCI6MTYwMzkwNzU2OSwiZXhwIjoxNjAzOTE0NzY5LCJhenAiOiJBdmtJM2syWU1jdFc5N2w2T1NrOElsdzRFQm5uVDd5SyIsInNjb3BlIjoib3BlbmlkIGVtYWlsIn0.WrdfwfUf9rsuxv3kKQI6DsL3bImtcMdpdvROd9Q3vHARJrhz-eok3QI0p-YnlCEl73Vs9btSstFdC2r2P9GtfFQuxtIHZkI6PuiyWysHs7_ZqwRRySI83yDPY2b5y7v2J8a-hTU1OmtDhOlu9y4G6I14YexWRps_98Ise2ZPWabvrPv1-yJ6D0rWFEpABgEqN23tgQiRtTR_q7e_i3xW2nvcvcxETIEoUuF_FhDAVnTYvWmiVFqWLeIC3DSorVmgIBhT0X_UTGkQSpDIUaavEtI-BM1yyKfhJiXTS_MYHUemgBmXd5gDgp9B-8MuAJ1ZcNabBtUGSUHydoMvPqEi0Q",
```

### Custom busniess logic
> in the todo app that we are building, before inserting todos into the public feed we want to validate the text for profanity.

> Actions can be added to Hasura to handle various use cases such as data validation, data enrichment from external sources and any other complex business logic.

* Use Remote Schemas if you have a GraphQL server or if you're comfortable building one yourself.
* Use Actions if you need to call a REST API


> fetching profile information from Auth0.




