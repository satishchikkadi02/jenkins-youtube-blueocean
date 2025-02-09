pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date
'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test step from blue ocean'
          }
        }

        stage('test par') {
          steps {
            echo 'test par'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 10
      }
    }

  }
}