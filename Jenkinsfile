pipeline {
    agent any

    stages {
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
        stage('Sonarqube') {
            steps {
                sonar-scanner 
                  -Dsonar.projectKey=Prueba 
                  -Dsonar.sources=Jenkinsfile 
                  -Dsonar.host.url=ec2-18-222-163-216.us-east-2.compute.amazonaws.com:9000
                  -Dsonar.login=7650e8fd49440f9aa9b4659ac7d4196024b576b4

            }
        }
    }
}
