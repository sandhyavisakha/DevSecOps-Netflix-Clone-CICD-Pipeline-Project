Set Up Build-

1.	Created a t2.large EC2 instance where we install Jenkins, SonarQube and Trivy.
2.	In the security group, opened the ports 22 for SSH, 443, for HTTPS, 80 for HTTP, 8080 for Jenkins, and 9000 for SonarQube.
3.	Connected to the server and cloned the code from my GitHub repository.
4.	To test if the application is running locally, installed Docker, built the Netflix image, and ran the Netflix app on a container on port 8081.
5.	Created an API key on TMDB (The Movie Database).
6.	Recreated the Docker image with the API key and ran the container again and saw that the Netflix app is showing the list of movies.
7.	Installed SonarQube by running it as a container and it runs o port 9000.
8.	Installed Trivy to scan the files. To test it, scanned the Docker image which was created locally.
9.	Installed Jenkins for automation and installed all the necessary plugins like node.js, eclipse, temurin, sonarqube scanner. Also set up the tools nodejs and jdk17.
10.	Configured Sonar credentials, tools, and system configuration for Sonar Scanner in Jenkins for integration.
11.	Created a new job in Jenkins with pipeline script with stages to clean the Jenkins workspace, check out the code from Git repository, run SonarQube analysis on the checkout code using the Sonar Scanner tool, wait for the quality gate to pass, install node.js dependencies using npm.
12.	Installed OWASP dependency check and Docker plugins in Jenkins and configured Docker Hub credentials in Jenkins credentials section.
13.	Configured dependency check and Docker in tools.
14.	Updated the pipeline script with OWASP dependency check and Docker stages and configured the Jenkins build to push the Docker image to Docker Hub.

Moniotoring-

15.	To set up monitoring, created a new EC2 instance of type t2.medium to install Prometheus, Node Exporter and Grafana.
16.	Configured Grafana with Node Exporter and integrated with Prometheus to create dashboards.
17.	Configured Prometheus with Jenkins by installing plugins.

Set Up Kubernetes Cluster-

18.	Installed Kubectl on Jenkins server.
19.	Created two t2.medium EC2 instances for K8s master node and K8s worker node.
20.	Set up Kubernetes cluster on both master and worker nodes.
21.	Installed Kubernetes plugins on Jenkins, and configured credentials.
22.	Installed Node Exporter on master and worker nodes to monitor.
23.	Configured prometheus.yml file with master and worker nodes IP addresses to monitor.
24.	Configured the Kubernetes deployment stage in Jenkins pipeline script and built the pipeline and successfully deployed the Netflix app on Kubernetes.
