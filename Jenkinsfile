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
        sh '''echo "FROM centos:7" > Dockerfile
echo " RUN yum install httpd -y" >> Dockerfile

docker build -t pipelineimg .'''
      }
    }

    stage('Deployment') {
      steps {
        sh '''echo "Creating container" 

docker run -itd -p 89:80 pipelineimg'''
      }
    }

  }
}