pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
  }

  stages {
    stage('Say Hello') {
      agent any

      steps {
         echo "My Branch Name: ${env.BRANCH_NAME}"
      }
    }
  }
}
