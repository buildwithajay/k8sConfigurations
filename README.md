**MongoDB on Kubernetes **
A hands-on project to learn Kubernetes fundamentals by deploying MongoDB with a web interface.
**What I Built**
This project deploys a complete MongoDB setup on Kubernetes consisting of:
MongoDB database (internal service)
mongo-express web interface (external access via LoadBalancer)
Secure configuration management using ConfigMaps and Secrets

**Technologies Used**
Kubernetes - Container orchestration
MongoDB - NoSQL database
mongo-express - Web-based MongoDB admin interface
Docker - Containerization
YAML - Configuration files

**What I Learned**
Through this project, I gained hands-on experience with:
Creating and managing Kubernetes Deployments
Setting up internal and external Services
Using ConfigMaps for configuration data
Managing sensitive data with Secrets
Service discovery within Kubernetes clusters
Basic Kubernetes networking concepts

**Quick Start**
bash# Apply all configurations
kubectl apply -f .

# Access mongo-express web interface
kubectl get svc mongo-express-service
Login credentials:

Username: admin
Password: pass

Project Structure
├── mongodb-secret.yaml           # Database credentials
├── mongodb-configmap.yaml        # Configuration data
├── mongodb-deployment.yaml       # MongoDB deployment & service
└── mongo-express-deployment.yaml # Web interface deployment & service
Key Concepts Demonstrated

Service Types: ClusterIP for internal communication, LoadBalancer for external access
Configuration Management: Separating config from code using ConfigMaps and Secrets
Security: Proper credential management with base64 encoded secrets
Inter-service Communication: How services discover and communicate within the cluster
