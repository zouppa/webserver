pipeline {
  agent any
  stages {
    stage('Content') {
      parallel {
        stage('Content') {
          steps {
            sh 'ls -lrt'
          }
        }

        stage('Version ') {
          steps {
            sh 'git --version'
          }
        }

        stage('Docker') {
          steps {
            sh 'docker -v'
          }
        }

      }
    }

    stage('error') {
      steps {
        echo 'Ready '
      }
    }

  }
}