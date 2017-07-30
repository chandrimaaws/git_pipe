pipeline {
  agent none
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
  
  post {
        success {
          emailext(
            subject: "${env.JOB_NAME} [${env.BUILD_NUMBER}] Development Promoted to Master",
            body: """<p>'${env.JOB_NAME} [${env.BUILD_NUMBER}]' Development Promoted to Master":</p>
            <p>Check console output at &QUOT;<a href='${env.BUILD_URL}'>${env.JOB_NAME} [${env.BUILD_NUMBER}]</a>&QUOT;</p>""",
            to: "chandrimaaws2@gmail.com"
          )
        }
      }
  
}
