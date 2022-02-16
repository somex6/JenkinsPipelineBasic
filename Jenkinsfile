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
            echo "Get chrome driver ${ChromeDriverPath}"
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying the app in IIS server'
        input(message: 'Do you want to deploy', id: 'yes')
      }
    }

  }
  environment {
    ChromeDriverPath = 'C:\\path\\chrome.exe'
  }
}