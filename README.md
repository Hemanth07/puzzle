This is a sample nodejs express app based on
http://expressjs.com/en/starter/hello-world.html

To configure:

* install https://nodejs.org/en/ (we tested with v6.9.1)
* `npm install`
* edit `config.json` to change the message or port as needed

To start the app:

```
node app.js
```

# How to

* build the docker image ` docker build -t <image_name>:<tag_name> .`

* run the contianer `docker container run -p 80:3000 <image_name>:<tag_name>`

I choose docker due to the following reasons:

1. easily shippable 
2. testing made easy 
3. carry out the same working env across multiple stages

---

## In production 

1. build the image via jenkins/codebild-pipeline.
2. push it to artifactory or any private registries.
3. pull to any COE(Container Orchestration Engines).
4. Run the container.