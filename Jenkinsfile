pipeline {
  agent any
  stages {
    stage('Fetch dependencies') {
      steps {
        sh 'sudo docker pull nginx:latest'
      }
    }

    stage('Build docker image') {
      steps {
        sh 'sudo docker build . -t customnginx:1'
      }
    }

    stage('Test image') {
      steps {
        sh '''sudo docker run -d -it -p 1234:80 customnginx:1
'''
      }
    }

  }
}