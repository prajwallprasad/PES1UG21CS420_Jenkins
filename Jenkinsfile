pipeline {
  // Consider using a dedicated agent or labels for controlled execution
  agent any

  stages {
    stage('Build') {
  steps {
    noCache true  // Disable caching for this step
    build 'PES1UG21CS420-1'
    // ... (rest of your build steps)
  }
}

    stage('Test') {
      steps {
        // Execute the test and check for failures (e.g., exit code or output parsing)
        sh './output'
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
      // Provide more informative error message
      error '''Pipeline failed. 
      Check the stage and step logs for details.'''
    }
  }
}
