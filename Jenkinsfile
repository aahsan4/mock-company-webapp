pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // TODO: Add build step
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                // TODO: Add test step
                sh './gradlew test'
            }
        }
    }

    post {
        failure {
            // Add a post-build step to handle failures
            script {
                withCredentials([[$class: 'GitHubAppCredentials', credentialsId: 'your-credentials-id', owner: 'aahsan4', appid: 'your-app-id']]) {
                    // You can use the GitHub App Credentials here
                    echo "Failed: Check the build logs for details."
                }
            }
        }
    }
}
