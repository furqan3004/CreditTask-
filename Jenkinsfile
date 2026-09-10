pipeline {
    agent any

    triggers {
        pollSCM('H/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven to compile and package the application.'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit tests and integration tests using JUnit to verify code functionality and component interaction.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analysing code quality and standards using SonarQube.'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Scanning the code for vulnerabilities using OWASP Dependency-Check.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to a staging server (AWS EC2 instance) using AWS CLI.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium to confirm production-like behaviour.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to the production server (AWS EC2 instance) using AWS CLI.'
            }
        }
    }
}
