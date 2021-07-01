pipeline {
  agent any
  stages {
    stage('Build start') {
      steps {
        sh 'echo " Build Start"'
      }
    }

    stage('image Building') {
      steps {
        sh 'echo "FROM centos:7" > Dockerfile'
      }
    }

    stage('Deployment') {
      steps {
        sh 'echo "Creating container" '
      }
    }

  }
}