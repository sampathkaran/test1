pipeline {
  agent any
  stages {
    stage('Download') {
      steps {
        sh 'echo "artifact file" > generatedFile.txt'
        archiveArtifacts(artifacts: 'generatedFile.txt', fingerprint: true)
      }
    }

    stage('Download-2') {
      steps {
        sh '''mkdir js
echo "not a artifact file" > js/build.js
echo "artifact file" > js/build.min.js

mkdir css
echo "not a artifact file" > css/build.css
echo "artifact file" > css/build.min.css

'''
        archiveArtifacts(artifacts: '**/*.min.*', fingerprint: true)
      }
    }

  }
}