pipeline {
  agent any

  triggers {
    pollSCM('* * * * *')
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', 
        url: 'https://github.com/goldrako/source-maven-java-spring-hello-webapp.git'
      }
    }
    stage('Build') {
      steps {
        sh '<COMMAND>'
      }
    }
    stage('Test') {
      steps {
        sh '<COMMAND>'
      }
    }
    stage('Deploy') {
      steps {
        deploy adapters: [tomcat9(credentialsId: 'tomcat-manager', url: 'http://3.35.5.232:8080/')], contextPath: null, war: 'target/hello-world.war'
      }
    }
  }
}