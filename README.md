# DevOps and Deployment Assessment

* In this assessment, you'll be answering some questions on the devops material that we went over.
* Answers to your written questions should be recorded in _Answers.md_.
* This assessment is to be worked on alone, but you can use outside resources and reference old repositories.
* Please refrain from copying and pasting any answers you previously wrote as an answer for a question on this assessment. Try and understand the question and put your responses in your own words. Be as thorough as possible when explaining something.
* **Friendly reminder:** Don't fret or get anxious about this assessment. This is a no-pressure assessment that is only going to help show you where you need to brush up on when reviewing. This is NOT a pass/fail situation.

## Assessment Questions

* **RESEARCH AND THOROUGHLY** Answer these questions. This shouldn't take just a trivial amount of time. You should spend some signifigant time on this.

1. Describe the differences between a Docker container and a virtual machine. What makes a container more aptly-suited for portability?

Docker container provides a way to virtualize an OS in order for multiple workloads to run on a single OS instance. Compared with Virtual Machine, the hardware is being virtualize to run multiple OS instances.

Docker images are stored in a repository, either the Docker Hub (a public set of repositories) or advanced features like Docker Data center, where images are stored in the Docker Trusted Registry. It's easy to see how having an efficient distribution mechanism allows up to many thousands of servers hosts to run Docker images without having to download the entire image content each time code changes. It's particularly valuable when containers move around the physical infrastructure; getting the latest version of an application image needs to be achieved as quickly as possible.

2. Using the command `docker run -p 49160:8080 -d <your_docker_username>/<your_docker_image_name>`, what does `49160:8080` specify?

It specifies that the public port is redirected to a private port inside the docker container.

3. What is the main purpose of using a "container orchestration platform" such as Kubernetes or Docker Swarm?

When the application keeps growing and needs to be divided into smaller chunks as micro services. We now need a caching layer to increase performance,be able to process tasks asynchronously and quickly share data among the services. We will face some challanges like: service discovery, load balancing, secrets configuration, health checks, auto-scaling of containers, and zero-downtime deploys. The container orchestration platform is to provide automating deployments, scaling and operations of application containers across clusters of hosts, providing container-centric infrastructure.

4. How do you change the number of replicas in a Kubernetes cluster?

We will have to write a yml file for deployment configuration. Inside the yml file, we will specify the replica numbers under the spec: replicas. And submitting this file to a Kubernetes cluster should create the defined ReplicaSet and pods that it manages using `kubectl create -f *.yml`.

5. What does it mean to scale a deployed application 'horizontally'? What does it mean to scale 'vertically'?

scaling horizontally affords the ability to scale wider to deal with traffic. It is the ability to connect multiple hardware or software entities, such as servers, so that they work as a single logical unit.

Scaling vertically resizes the server with no change to the code. It is the ability to increase the capacity of existing hardware or software by adding resources. it is limited by the fact that you can only get as big as the size of the server. 

6. Heroku also utilizes software containers for deployment. What is the main difference between the 'free' tier of containers on Heroku vs. the paid tiers?

 Free tier doesn't offer the auto-scaling, horizontal scaling, and zero-downtime deployment features that will boost the application performance tremendously.

## Post Assessment

1. Now that you have spent the week learning about some deployment options, the main goal here is to get your personal projects up on the world wide web for all to see!
2. Once you get your project hosted, clean it up so people can interact with it at least a little bit. And if you feel so inclined, solicit feedback in the `show-it-off` channel in slack.
3. Another task you can do once you are done hosting your project is craft some really great documentation.
4. Lastly, continue pushing forward on your personal projects! Build features, figure out problems etc.
