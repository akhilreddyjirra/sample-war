pipeline {
  agent {
    docker {
      image 'maven'
      args '-v C:\\mvn\\bin:/root/.m2'
    }
    
  }
  stages {
    stage('Init') {
      steps {
        sh '''echo $PATH
echo PATH={path}
mvn clean'''
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}