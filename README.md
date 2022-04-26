# README

Our flask server connects the frontend with the Neo4j database.
It is adopted from a template at https://github.com/neo4j-examples/neo4j-movies-template.
We just amended the Python/Flask backend at `/flask-api` from the template.
The web frontend can be found at `/web`. 
We just put the Heroku Deployable version of the flask API in this repo.  
Feel encouraged to fork and update this repo!

## The Model

### Nodes

* `Document`
* `User`

### Relationships

* `(:User)-[:FAVOURITE]->(:Document)`

## Database Setup: Sandbox

Go to https://sandbox.neo4j.com/?usecase=recommendations&ref=movie-app-tutorial, pick "Recommendations", and press play to start the database.

Make sure to edit the file `flask-api/.env` or `api/.env` and update the `MOVIE_DATABASE_USERNAME`, 
`MOVIE_DATABASE_PASSWORD`, and `MOVIE_DATABASE_URL` of your chosen backend to connect to your instance.

## Flask API

First, configure your `flask-api/.env` file to point to your database. 

Then, from the root directory of this project:

```
cd flask-api
python3 -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
export FLASK_APP=app.py
flask run
```

* Take a look at the docs at [http://localhost:5000/docs](http://localhost:5000/docs)


