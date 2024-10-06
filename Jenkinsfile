pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                // Example: Build with Maven
                sh 'mvn clean package'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
                // Example: Run tests
                sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Performing code analysis...'
                // Example: SonarQube
                sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running security scan...'
                // Example: OWASP Dependency Check
                sh 'dependency-check --scan ./ --out ./reports'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
                // Example: Deploy using AWS CLI or Ansible
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
                // Example: Selenium or Postman
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
                // Example: Deploy to AWS EC2 or Kubernetes
            }
        }
    }

    post {
        always {
            echo 'Sending notifications...'
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
 
