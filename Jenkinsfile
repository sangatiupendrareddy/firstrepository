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
        sh 'docker build -t pipelineimg2 .'
      }
    }

    stage('Deployment') {
      steps {
        sh '''echo "Creating container" 

docker run -itd -p 84:80 --name jenkinscontainer pipelineimg2'''
      }
    }

  }
}