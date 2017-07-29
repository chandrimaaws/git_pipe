pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
  }

  stages {
    stage('Cloning....') {
      agent any

      steps {
         echo "My Branch Name: ${env.BRANCH_NAME}:${env.BUILD_NUMBER}"
      }
    }
    
    stage('Deploying using chef....') {
      agent any

      steps {
         echo "deploying..."
      }
    }
  }
}
