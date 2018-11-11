pipeline {
  agent {
      docker {
          image 'maven:3.5.4-jdk-10-slim'
          args '-v $HOME/.m2:/root/.m2'
      }
  }
  stages {
    stage('Build Package') {
      steps {
          echo "Building package ..."
      }
    }
  }
  stage('Deploy Approval'){
    steps {
      input "Deploy to Production?"
    }
  }
  stage('Deploy to Production') {
    steps {
      echo "Deploying to Production environment ..."
    }
  }
  stage('Clean up') {
    steps {
      echo "Have a nice day!"
    }
  }
}