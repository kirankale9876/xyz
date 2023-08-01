pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'building a code'
        sh '''pwd
ls'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'This test case'
            sleep 10
          }
        }

        stage('Test Parallel') {
          steps {
            sh '''whoami
hostname -f'''
          }
        }

      }
    }

    stage('Prod') {
      steps {
        sh '''ls
sleep 15
'''
      }
    }

  }
}