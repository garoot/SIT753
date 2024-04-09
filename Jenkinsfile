pipeline {
    agent any
    environment {
            DIRECTORY_PATH = "/path/to/code"
            TESTING_ENVIRONMENT = "TestingEnv"
            PRODUCTION_ENVIRONMENT = "ProductionEnv"
    }
    stages {
        stage('Build'){
            steps{
                echo 'Fetching the source code from the directory path specified by DIRECTORY_PATH environment variable'
                echo 'Compiling the code and generating any necessary artifacts'
            }
        }
        stage('Test') {
            steps{
                echo 'Running unit tests'
                echo 'Running integration tests'
            }
        }
        stage('Code Quality Check'){
            steps{
                echo 'Checking the quality of the code'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying the application to a testing environment'
            }
        }
        stage('Approval'){
            steps{
                echo 'Waiting for manual approval'
                sleep 10
            }
        }
        stage('Deploy to Production'){
            steps{
                echo 'Deploying the code to the production environment using the environment variable specifying the environment name'
            }
        }
    }
}