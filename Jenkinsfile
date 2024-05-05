pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build the code using Maven
                echo 'mvn clean package'
            }
        }
        stage('Unit and Integration Tests ') {
            steps {
                // Run unit tests
                echo 'running mvn test '

                // Run integration tests
                // Add commands for running integration tests
                echo 'running integration test '
            }
            post {
                success {
                    emailext subject: "Unit and Integration Tests - Success",
                            body: "The unit and integration tests passed successfully.",
                            to: "abdulmajeedgaroot@gmail.com",
                            attachLog: true
                }
                failure {
                    emailext subject: "Unit and Integration Tests - Failure",
                            body: "The unit and integration tests failed. Please check the logs for details.",
                            to: "abdulmajeedgaroot@gmail.com",
                            attachLog: true

                }
            }
        }
        stage('Code Analysis') {
            steps {
                // Analyze code using SonarQube
                // Add commands for code analysis
                echo 'running code analysis '

            }
        }
        stage('Security Scan ') {
            steps {
                // Perform security scan using OWASP ZAP
                // Add commands for security scan
                echo 'performing security scan using OWASP and Notify via E-mail '
            }
            post {
                success {
                    emailext subject: "Security Scan - Success",
                            body: "The security scan passed successfully.",
                            to: "abdulmajeedgaroot@gmail.com",
                            attachLog: true
                }
                failure {
                    emailext subject: "Security Scan - Failure",
                            body: "The security scan failed. Please check the logs for details.",
                            to: "abdulmajeedgaroot@gmail.com",
                            attachLog: true
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploy to staging server using AWS CodeDeploy
                // Add commands for deployment
                echo 'deploying to aws ec2 instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Run integration tests on staging environment
                // Add commands for running integration tests
                echo 'running integration tests on staging '
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploy to production server using AWS CodeDeploy
                // Add commands for deployment
                echo 'deploying to production'
            }
        }
    }
}
