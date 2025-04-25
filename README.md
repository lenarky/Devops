---Prerequisites: Before setting up the pipeline and running the project, make sure you have the following tools installed:

Jenkins: A popular automation tool for CI/CD pipelines.

Docker: Containerization platform used to build and deploy applications.

Minikube: A local Kubernetes environment to manage and deploy containers.

SonarQube: Static code analysis tool for detecting bugs, vulnerabilities, and code smells.

Prometheus: Monitoring and alerting toolkit, used for collecting and storing metrics.

Grafana: Open-source data visualization tool, used for building dashboards.

Installation
1. Install Jenkins
To install Jenkins locally, first download the Jenkins WAR file from the official Jenkins website. Once downloaded, navigate to the folder where the file is located, then run the following command in the terminal:

java -jar jenkins.war.

After it starts, Jenkins will be accessible via http://localhost:8080.

2. Git Repository
Your Git repository for this project is located at C:/Users/username/.git/. You can clone your repository by navigating to your preferred directory and using the command:

git clone https://github.com/yourusername/your-repo.git.

This will pull the project into your local environment, allowing you to work with it.

3. Build Docker Image
Next, navigate to your project directory (C:\Users\username\OneDrive\Desktop\my-python-app) and build the Docker image by running:

docker build -t web-app ..

This will create a Docker image called web-app based on your Dockerfile, allowing you to containerize your application.

4. Run Minikube
To start a local Kubernetes environment using Minikube, use the following command in your terminal:

minikube start.

Minikube will provision a virtual machine and start a Kubernetes cluster locally, enabling you to manage and deploy containers in a Kubernetes environment.

5. Run SonarQube
To run SonarQube, navigate to the SonarQube bin directory (C:\Programs\sonarqube\bin\windows-x86-64) and run the command:

StartSonar.bat.

Once SonarQube is up and running, you can access it via http://localhost:9000 to perform static code analysis.

6. Run Prometheus
To start Prometheus, navigate to the Prometheus directory (C:\Programs\prometheus) and run the following command:

prometheus.exe.

Prometheus will begin collecting and storing metrics, and you can view it at http://localhost:9090.

7. Run Grafana
Finally, to start Grafana for visualizing Prometheus metrics, go to the Grafana bin directory (C:\Programs\Grafana\grafana\bin) and execute:

grafana-server.exe.

This will start the Grafana server, and you can access it via http://localhost:3000 to set up your dashboards and visualizations.

Usage
Once all the tools are set up and running, follow these steps:

Jenkins CI/CD Pipeline: Jenkins will automatically trigger the CI/CD pipeline defined in the Jenkinsfile whenever code is pushed to your Git repository. The pipeline will:

Build the Docker image.

Run tests.

Perform vulnerability scanning using Trivy.

Analyze the code using SonarQube.

Kubernetes Deployment: The pipeline can also deploy your Docker container to your local Kubernetes cluster created by Minikube.

Monitoring: Prometheus will collect metrics, and Grafana will display them on a dashboard. This helps in monitoring the health of your application and the pipeline's performance.

Testing Strategy
This project includes several layers of testing integrated into the pipeline:

Unit Tests: These ensure that individual functions and components work as expected.

Integration Tests: These test interactions between components.

End-to-End Tests: These simulate real-world usage to ensure the entire application flows correctly.

These tests will run automatically as part of the Jenkins pipeline.

Contribution Guidelines
We welcome contributions to improve this project! Please fork the repository, create a new branch, and submit a pull request. Ensure that your contributions are well-tested and documented.

License
This project is licensed under the MIT License

---Using CMD run the following: username is what your using on your computer.

cd C:\Users\username\Downloads
java -jar jenkins.war                       - To Run Jenkins

C:/Users/username/.git/ - Git Repository

cd C:\Users\username\OneDrive\Desktop\my-python-app
docker build -t web-app .                   - To run Docker

minikube start

cd C:\Programs\sonarqube\bin\windows-x86-64
StartSonar.bat                              - To run Sonarqube

cd C:\Programs\prometheus
prometheus.exe

cd C:\Programs\Grafana\grafana\bin
grafana-server.exe

wsl.exe -d Ubuntu
