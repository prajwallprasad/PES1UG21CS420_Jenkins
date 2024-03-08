pipeline {
  agent any  // Potential error: Unrestricted agent could lead to resource exhaustion

  stages {
    stage('Build') {
      steps {
        build 'PES1UG21CS420-1' // Potential error: Missing or incorrect build job name
        sh 'g++ cccc.cpp -o output' // Potential error: Missing header files or libraries
      }
    }

    stage('Test') {
      steps {
        sh './output' // Potential error: No error handling for test execution
      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }

  post {
    failure {
      error 'Pipeline failed'  // Potential error: Uninformative error message
    }
  }
}
