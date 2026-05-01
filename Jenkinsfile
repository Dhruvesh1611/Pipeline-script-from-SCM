pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Dhruvesh1611/Pipeline-script-from-SCM.git'
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

// This Jenkinsfile defines a pipeline with four stages: Clone Code, Build, Test, and Package. It uses Maven as the build tool and checks out the code from the specified Git repository. Each stage executes the corresponding Maven commands to compile, test, and package the application.