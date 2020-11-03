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
