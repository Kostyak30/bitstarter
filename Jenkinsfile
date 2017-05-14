pipeline {
  agent {
    docker {
      image 'hello-world'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            sh 'echo Building'
            
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