pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                git branch: 'release/java11'
		    url: 'https://github.com/spring-petclinic/spring-petclinic-microservices.git'
                sh './mvnw clean install -P buildDocker'
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
