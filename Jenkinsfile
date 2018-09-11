pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'source ~/.bashrc && mvn clean package'
      }

      post {
        archiveArtifacts artifacts: "**/target/*.war"
      }

    }

  }

}
