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

    stage('Deploy ') {
      steps {
        echo 'HEllo World'
      }
    }

  }
}