pipeline {
  agent {
  label 'jenkins'
}	
  stages {
    stage ('BUILD') {
      steps {
        git branch: 'main', credentialsId: 'privateidnw', url: 'https://github.com/Vinay-RR/Vinay_private.git'
        sh 'sleep 5'
      }  
    }  
     }
  }
