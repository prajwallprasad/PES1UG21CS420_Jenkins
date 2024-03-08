pipeline {
  // Consider using a dedicated agent or labels for controlled execution
  agent any

  stages {
    stage('Build') {
      steps {
        // Ensure the build job name exists
        build 'PES1UG21CS420-1' // This job likely doesn't exist, causing an error

        // Add steps to install dependencies if needed (e.g., npm install)

        // Compile the code, consider adding checks for missing headers/libraries
        sh 'g++ cccc.cpp -o output'
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
