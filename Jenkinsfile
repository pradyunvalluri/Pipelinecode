pipeline {


  agent any

  
  options {
    timestamps()
  }


  stages {
    stage('Build') {
      
      steps {
           sh 'echo "build step"
        }
       }
    stage('Test') {
      
      steps {
           sh 'echo "Test step"
        }
       }
      }
      post {
        success {
         sh 'echo "build success"
        }
      }
    }
