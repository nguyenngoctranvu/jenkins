pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'source ~/.bashrc && mvn clean package'
      }

      post {
        success {
          echo "Now archiving..."
          archiveArtifacts artifacts: "**/target/*.war"
        }
      }
    }
  }
}
