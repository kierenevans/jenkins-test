pipeline {
    agent { label "my127ws" }
    environment {
        MY127WS_ENV = "pipeline"
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo $GIT_COMMIT'
                milestone(10)
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
