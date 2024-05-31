pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // Build the code with Maven or similar build automation tool.
                echo "Build Stage"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Run unit tests with JUnit or similar test automation tool.
                // Run integration tests with Selenium or another integration testing tool.
                echo "Testing Stage"
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrate a code analysis tool like Checkstyle or SonarQube.
                echo "Code Analysis Stage"
            }
        }
        stage('Security Scan') {
            steps {
                //Run a security scan with tools like OWASP ZAP or SonarQube.
                echo "Security Stage"
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Set up a staging server.
                echo "Deployment Stage"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Utilise the staging area to carry out validation tests
                echo "Integration Stage"
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy the application to the production server.
                echo "Production Stage"
            }

             post {
                success {
                    // Send email notification on successful deployment
                    emailext (
                        to: 'vin.rohatgi@gmail.com',
                        subject: 'Successful Deployment ',
                        body: 'The deployment was successful. Please verify.',
                        attachmentsPattern:'/*.log'
                    )
                }
            }
        }
    }
}
