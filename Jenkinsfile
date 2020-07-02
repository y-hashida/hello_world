pipeline {
    agent any 
    environment {
        GIT_TOKEN = credentials('github-token')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Build' 
            }
        }
        stage('Test') {
            steps {
                echo 'Test' 
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() // clean up our workspace
        }
        /*
        success {
            echo 'I succeeeded!'
            curl -X POST -H "Authorization: token ${GIT_TOKEN}" "https://api.github.com/repos/y-hashida/hello_world/statuses/$(git rev-parse HEAD)" \
            -d "{
              \"state\": \"success\",
              \"description\": \"The build has succeeded!\"
            }"
        }
        failure {
            echo 'I failure'
            curl -X POST -H "Authorization: token ${GIT_TOKEN}" "https://api.github.com/repos/y-hashida/hello_world/statuses/$(git rev-parse HEAD)" \
            -d "{
              \"state\": \"failure\",
              \"description\": \"The build has failed!\"
            }"
        }
        */
    }
}