pipeline {
  agent {
    docker {
      args '-v maven-repo:/root/.m2'
      image 'maven:3-jdk-8-slim'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
  }
}