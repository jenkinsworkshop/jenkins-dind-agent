pipeline {
  options {
    buildDiscarder(logRotator(numToKeepStr: '7')) 
    skipDefaultCheckout() 
  }
  agent none
  stages {
    stage('Setup') {
      steps {
        script {
          dockerBuildDockerHubPush {
            dockerHubCredentialsId = 'docker-hub-beedemo'
          }
        }
      }
    }
  }
}