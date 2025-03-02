pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'your-dockerhub-username/your-app'
        DOCKER_TAG = 'latest'
    }

    stages {

        stage('Build with Maven') {
            steps {
                script {
                    sh 'mvn clean package -DskipTests'
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh "sudo -S docker build -t petclinic:v1 ."
                }
            }
        }
  }
}
