pipeline {
  agent any
  stages {
    stage('plan') {
      steps {
        echo 'plan the project'
      }
    }

    stage('code') {
      steps {
        echo 'write the code'
      }
    }

    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'build the code'
          }
        }

        stage('deploy') {
          steps {
            echo 'deploy the code'
          }
        }

        stage('operate') {
          steps {
            echo 'run the application'
          }
        }

      }
    }

  }
}