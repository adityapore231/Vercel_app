Introducing Project Vercel Clone 👨‍💻  

As you might know vercel is a PaaS which takes care of hosting your application with one click. Versel only need a url of your github repository.

I tried to build vercel app that accepts React project and builds and deploys the application.



Architecting Vercel Clone : 

👉High level system design : 

Services:

👉1. Build Service - This service helps to build react project with npm build and the project converts into html, css, javascript. For website hosting ,we are using object store such as amazon aws s3 to store html, css, javascript. 



👉2. Request Handler Service - The service used to route the request traffic to particular s3 bucket and folder. Service is used to call (get_object) to serve index.html to user



👉Tech stack :

1. AWS s3 - for storing static websites

2. ECS + Fargate - used by building service to build project.

3. Docker

4. Javascript
