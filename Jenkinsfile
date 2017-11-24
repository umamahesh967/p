pipeline {
    agent any

    stages {
 
        stage('Build'){
            steps {
                sh 'printenv'
                sh 'mvn clean package'
 
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose -f docker-compose.yml -f docker-compose-dev.yml up   --build --remove-orphans '
            }
        }
    }
}
