pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(branch: 'main', url: 'https://github.com/AHmedsalem256/Jenkins_Test_Github.git')
      }
    }

    stage('Test') {
      steps {
        bat 'robot -d results tests/'
      }
    }

    stage('Report') {
      steps {
        publishHTML([
                              reportDir: 'results',
                              reportFiles: 'report.html',
                              alwaysLinkToLastBuild: true,
                              keepAll: true,
                              allowMissing: false,
                              reportName: 'Robot Test Report'
                          ])
        }
      }

    }
  }