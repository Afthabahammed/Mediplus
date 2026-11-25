# Mediplus

## About the Project

Mediplus is a healthcare-oriented web application developed using Python and Django. It provides a website interface for healthcare-related information and services.

The application uses SQLite for database storage and Django to handle its backend functionality. I used this project as part of my DevSecOps assignment to practise securing, building, and deploying a web application.

## Technologies Used

- **Python** – Programming language
- **Django** – Backend web framework
- **SQLite** – Database
- **HTML, CSS and JavaScript** – Frontend development
- **Git and GitHub** – Source code management
- **Semgrep** – Static Application Security Testing (SAST)
- **Trivy** – Dependency vulnerability scanning
- **OWASP ZAP** – Dynamic Application Security Testing (DAST)
- **Jenkins** – CI/CD automation
- **Docker** – Application containerization
- **Amazon ECR** – Container image storage
- **Kubernetes (K3s)** – Application deployment
- **Argo CD** – GitOps-based deployment management

## Running the Application Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Afthabahammed/Mediplus.git
cd Mediplus
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure the Django Secret Key

Set the `DJANGO_SECRET_KEY` environment variable before starting the application.

### 4. Apply Database Migrations

```bash
python manage.py migrate
```

### 5. Start the Development Server

```bash
python manage.py runserver
```

Open the following URL in your browser:

`http://127.0.0.1:8000/index`

## DevSecOps Implementation

I integrated Mediplus into an automated DevSecOps pipeline to understand how security testing and deployment automation work together.

The workflow includes:

1. **GitHub:** Stores and manages the application source code.
2. **Semgrep:** Scans the source code for potential security issues.
3. **Trivy:** Checks project dependencies for known vulnerabilities.
4. **Jenkins:** Automates the CI/CD pipeline.
5. **Docker:** Builds a container image of the application.
6. **Amazon ECR:** Stores the Docker image.
7. **Kubernetes:** Runs and manages the application.
8. **Argo CD:** Synchronizes Kubernetes configurations using GitOps.
9. **OWASP ZAP:** Performs dynamic security testing against the running application.

## Deployment

The application is packaged as a Docker image and deployed on Kubernetes. The image is stored in Amazon ECR, and Argo CD manages the deployment using configuration files maintained in a separate GitOps repository.

## Project Goal

Through this project, I gained hands-on experience with application security scanning, Jenkins pipeline automation, Docker image management, Kubernetes deployment, and GitOps using Argo CD.
