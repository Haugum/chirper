# CHIRPER
Chirper is a social media platform where uers can post 140 character microposts to share their thoughts and rambles.

Chirper is built using Ruby on Rails, and runs as Docker containers using microservice architecture.

To run this webapp, complete the following steps in a terminal:

* `docker build -t {image_name:version_number} .` e.g. `docker build -t chirper:1.0 .` Note: Make sure to include the `.` at the end of the command. 
* (Optional: Configure custom database settings in `database.yml`, default uses postgres on port 5432, username `postgres` and blank password.

* Create and run the database container: `docker run -rm -d -p 5433:5432 -name localdb postgres`

* Run the app container: `docker run -p 3000:3000 --link localdb:toyappdb toy-app`

* Need to run db:create and db:migrate in postgres container (maybe this could be done in a Dockerfile or dtabase.yml somehow?)

* Verify that both containers are up and running: `docker ps`

* Navigate to `localhost:3000 (or 0.0.0.0:3000`


* ...
# chirper
