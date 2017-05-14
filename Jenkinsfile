pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo Building'
            catchError() {
              sh '''echo "burnning man"
exit 1'''
            }
            
            
          },
          "Test": {
            sh 'echo "Test"'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploy"'
      }
    }
  }
}