# 🚀 DevOps Task 8 - Run a Simple Java Maven Build Job in Jenkins

## Objective
Learn how to use Jenkins to build a simple Java application using Maven.

## Tools & Technologies
- Jenkins
- Docker
- Java JDK
- Maven
- Git & GitHub

## Project Overview
This project contains a basic Java HelloWorld application that prints "Hello, Jenkins + Maven!" using Maven as the build tool.

## Project Files
- `src/main/java/HelloWorld.java` – The Java source file.
- `pom.xml` – Maven configuration file.
- `jenkins-build-success.png` – Screenshot of the Jenkins build console showing BUILD SUCCESS.

## Jenkins Build Process (if Code is in GitHub)
1. A Freestyle Jenkins job was created to pull this repository.
2. The build step used was "Invoke top-level Maven targets" with the goal `clean package`.
3. The build was triggered manually, and the console output confirmed a successful build.

- Jenkins run using Docker:
  ```bash
  docker run -d --name jenkins -p 8080:8080 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts


## Jenkins Build Process (if Code is in your local/EC2)
1. Select **Jenkins Freestyle Project**.
2. The build step used was "Invoke top-level Maven targets" with the goal: 
   ```bash
   -f /var/jenkins_home/hello-java-maven/pom.xml clean package
3. The build was triggered manually, and the console output confirmed a successful build.

- Jenkins run using Docker:
  ```bash
  docker run -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock -v /home/ubuntu/hello-java-maven:/var/jenkins_home/hello-java-maven --name jenkins jenkins/jenkins:lts

## ✅ Outcome
- Jenkins successfully built the project using Maven.
- Console output showed BUILD SUCCESS.
