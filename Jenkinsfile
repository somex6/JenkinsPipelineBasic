pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'building the .NET core application'
          }
        }

        stage('Test') {
          steps {
            echo 'Testing the operation'
            echo '"Get chrome driver ${ChromeDriverPath}"'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app in IIS server'
      }
    }

  }
  environment {
    ChromeDriverPath = 'C:\\path\\chrome.exe'
  }
}