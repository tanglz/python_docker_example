# python_docker_example
example for docker beginners

### step 1 create files
touch app.py
touch Dockerfile
touch docker-compose.dev.yml

### step 2 basic application as an example (Flask web server + mysql)
pip3 install Flask
pip3 install mysql-connector-python
* after coding app.py
pip3 freeze > requirements.txt

### step 3 create docker image
docker build --tag python_docker_example .
* check image
docker images

### step 4 run by docker-compose
docker-compose -f docker-compose.dev.yml up --build
* check containers
docker ps

### step 5 Test application is running
curl http://localhost:5000
curl http://localhost:5000/initdb
curl http://localhost:5000/widgets

### 


