# Python GraphQL server, built with Falcon and Graphene

To install dependencies:
```
python3 -m venv venv
source venv/bin/activate
pip3 install --upgrade pip
pip3 install -r requirements.txt
```

You need to have PostgreSQL installed, with the following parameters:
```
POSTGRES_PASSWORD=postgres
POSTGRES_USER=postgres
POSTGRES_DB=ms-airports
```

To run:
```
make start-app
```

To check if it's running, simply:

```
curl http://127.0.01:80/healthcheck
```


To call the GraphQL endpoints, use Postman. Check the collection inside the `postman` folder.


To exit the virtual env, run `deactivate`.


## Running with Docker ##

```
docker-compose build 
```
To build the image that includes the app and the DB.

```
docker-compose up
```
To deploy it to Docker (you should have Docker Desktop or other Docker tool running on your local)
The app will run on port 8008, so:
```
http://localhost:8008/docs
```
will bring you the FastAPI default page