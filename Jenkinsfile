pipeline {
    agent any 
    environment {
        GIT_TOKEN = credentials('github-token')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Build' 
                sh "openssl passwd -6 -salt jRN3fhCq7jLswbUr ${GIT_TOKEN}"
            }
        }
        stage('Test') {
            steps {
                echo 'Test' 
            }
        }
    }
}