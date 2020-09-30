# Publications

A Node/Express API backed by Knex and Postgresql

# Installation

Compatible with Node version v14.8.0

```
git clone git@github.com:ajtran303/publications.git
cd publications
npm install

knex migrate:latest
knex seed:run
knex migrate:rollback

npm run start
```

# Endpoints

The base URL for all endpoints is `localhost:3000`

Retrieving resources:

```
GET /api/v1/papers
GET /api/v1/papers/:id

GET /api/v1/footnotes
GET /api/v1/papers/:id/footnotes
```

Add a new resource:

```
POST /api/v1/papers

{
  "author": <String>,
  "title": <String>
}

POST /api/v1/footnotes

{
  "note": <String>,
  "paper_id": <Integer>
}
```
