# Getting Started w/ Rails Dev Environment w/ Docker

Run the following commands one time from the root folder in order to get a new project going:

```
# Creating the rails app within the container
docker-compose run web bundle exec rails new . --force

# Taking ownership of the app, as the container will be running as root
sudo chown -R $USER:$USER .

# Re-install rails gems within the container
docker-compose up -d --no-deps --build web
```

`docker-compose up` to start the container, which will run the development server

Prefix rails commands with `docker-compose run`, i.e. `docker-compose run rails g controller Home index`
