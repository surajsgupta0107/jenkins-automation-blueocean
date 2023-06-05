pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        sh 'echo "Jai Shri Ram"'
        sh '''ls
pwd
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test'
          }
        }

        stage('Configure') {
          steps {
            echo 'Configure'
          }
        }

      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build'
          }
        }

        stage('Code Quality') {
          steps {
            echo 'Code Quality'
          }
        }

      }
    }

    stage('Deploy on Test') {
      steps {
        echo 'Deploy on Test'
        sleep 5
      }
    }

    stage('Deploy on Production') {
      steps {
        echo 'Deploy on Production'
        sleep 5
      }
    }

  }
}