pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''hostname
date
systemctl status jenkins

'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'This is new code from blue ocean on test'
          }
        }

        stage('test par') {
          steps {
            echo 'Code test parallelly '
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'Deploy on prod if all ok in test'
        sleep 5
      }
    }

    stage('print all') {
      steps {
        mail(subject: 'Deployment successful', body: 'Hi, Test is successful', from: 'satish.chikkadi@gmail.com', to: 'satish.chikkadi@gmail.com', charset: 'successful')
      }
    }

  }
}