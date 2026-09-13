pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile the source code and package it into a deployable artifact.'
                echo 'Tool: Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests on individual components, then integration tests to confirm modules work together.'
                echo 'Tools: JUnit for unit tests, TestNG for integration tests'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse the source code against industry coding standards to detect code smells and maintainability issues.'
                echo 'Tool: SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Task: Scan the code and its dependencies for known vulnerabilities and produce a findings report.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the packaged application to the staging server.'
                echo 'Tool: AWS CLI deploying to an EC2 staging instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests against the staging environment to confirm correct behaviour in a production-like setup.'
                echo 'Tool: Selenium'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Task: Promote the same verified artifact to the production server.'
                echo 'Tool: AWS CLI deploying to an EC2 production instance'
            }
        }
    }
}