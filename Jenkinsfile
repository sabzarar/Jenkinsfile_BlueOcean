pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
ls
date'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing stage'
          }
        }

        stage('Integration testing') {
          steps {
            echo 'Integration testing'
          }
        }

      }
    }

    stage('Sonar') {
      steps {
        echo 'code quality'
      }
    }

    stage('deploy') {
      steps {
        echo 'deployment'
      }
    }

  }
}