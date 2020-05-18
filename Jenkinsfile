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

    stage('message') {
      steps {
        echo 'Ready '
      }
    }

    stage('image') {
      steps {
        sh 'docker build -t zouppa/webserver .'
      }
    }

    stage('container') {
      steps {
        sh 'docker run -d -p 80:80 zouppa/webserver'
      }
    }

    stage('') {
      steps {
        echo 'end'
      }
    }

  }
}