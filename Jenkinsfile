pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
            echo "1.Clone Stage"
                git url: "https://github.com/cph1c06/user-api.git"
            }
        } 
        stage('Build') {
            steps {
                echo 'Building..'
                sh "aws ecr get-login --no-include-email --region us-east-1"
                sh "docker build -t "clp"
                sh "docker tag clp:latest 912159400498.dkr.ecr.us-west-1.amazonaws.com/clp:latest"
                sh "docker push 912159400498.dkr.ecr.us-west-1.amazonaws.com/clp:latest"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
