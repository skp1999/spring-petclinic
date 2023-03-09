pipeline {
  agent {
    docker { image 'maven:3.5.0'}
  }
  stages {
    stage('maven-build') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Docker build') {
      agent any
      steps {
        sh 'docker build -t demo/spring-petclinic:latest'
      }
    }
  }
}
