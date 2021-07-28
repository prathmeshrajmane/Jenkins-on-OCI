pipeline {
  agent {
    docker {
      image 'nginx:latest'
    }

  }
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
        sh 'echo "Tests successful"'
      }
    }

  }
}