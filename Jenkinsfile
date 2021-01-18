pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'echo "artifact file" > generatedFile.txt'
        archiveArtifacts(artifacts: 'generatedFile.txt', fingerprint: true)
      }
    }

  }
}