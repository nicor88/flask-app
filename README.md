# flask-app
Simple flask boilerplate.


## Running Locally

### Requirements
* python >= 3.6
* pip
* install requirements running `pip install -r requirements.txt`

### Run the app

Run the app with Python:
<pre>
python app.py
</pre>

You can use gunicorn to spin up multiple workers, and make the app faster:
<pre>
gunicorn app:app --chdir src --bind 0.0.0.0:5000 --workers 4
</pre>

The Flask App will be available at: [localhost:5000](http://localhost:5000)

## Running with Docker

### Requirements
* Docker

### TODO
* Add a Dockerimage to the repo to package the app and all the necessary dependencies to run it
    * Base the docker image on the official [Python docker images](https://hub.docker.com/_/python), consider to use at least Python 3.7

* Provide a simply way to run the app via docker-run
* Provide a docker-compose to package and run the app
  
#### Add-ons
* Extend the app to provide another endpoint that return a list of users fetched from a DB
    * Endpoint available at [localhost:5000/users](http://localhost:5000/users)
    * Use Postgres >= 11.6
    * Table entity can be defined from you as you wish
    * provide a version of docker-compose to run the DB and the app
