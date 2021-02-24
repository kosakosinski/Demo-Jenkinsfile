pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git clone https://github.com/spring-petclinic/spring-petclinic-microservices.git
                cd spring-petclinic-microservices
                sh ./mvnw clean install -P buildDocker
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