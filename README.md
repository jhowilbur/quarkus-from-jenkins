                                                   
# Reactive hello world project (Quarkus and WebFlux) for deploy automation with Jenkins and everything working with containerization 
# in Docker and orchestration with k8s.

#-----------------
### for running local:
#### mvn package -Pnative -Dquarkus.native.container-build=true
### and after
#### docker build -f src/main/docker/Dockerfile.native -t quarkus-example:0.0.1 .
#-----------------
### for generate a image:
#### docker run -d -p 9000:9000 quarkus-example
#-----------------

#*****************
## see applications that have automation and their files Jenkinsfile, Dockerfile and more ...
#### git clone https://github.com/jhowilbur/webflux-from-jenkins.git
#### git clone https://github.com/jhowilbur/quarkus-from-jenkins.git
#### git clone https://github.com/jhowilbur/setup-jenkins.git
#*****************

##### ~ 🅦🅘🅛🅑🅤🅡 ~

 - Tanks for your attention!