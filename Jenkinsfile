pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
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
}
