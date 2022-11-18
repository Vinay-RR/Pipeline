pipeline {
  agent any	
  environment {
  NAME = 'Vinay'
  }
  stages {
    stage ('BUILD') {
      steps {
        echo "$NAME"
        sh '''
		sleep 5
		echo "$NAME"
		exit 0
		'''
      }  
    }  
      stage ('TEST PARALLEL') {
	   parallel {
	   stage ('TEST ON CHROME') {
      steps {
        echo "This is Test on chrome browser"
        sh 'sleep 5;'
      }  
    }  
	   
    stage ('TEST ON SAFARI') {
      steps {
        echo "This is Test on Safari browser"
        sh 'sleep 5;'
      }  
    }  
  } 
}
	  stage('DEPLOY') {
		  parallel {
			  stage ('SERVER 1') {
		  steps {
			  echo 'This is Deploy TO Server 1'
			  sh 'sleep 5'
		    }
		}
		  stage ('SERVER 2') {
		  steps {
			  echo 'This is to Deploy Server2'
			  sh 'sleep 5'
			  }
	  }
	  stage ('SERVER 3') {
	  steps {
		  echo 'This is to deploy server 3'
		  sh 'sleep 5'
	  }
  }
	stage ('SRVER 4') {
	       steps {
		       echo 'This stage is to deploy Server4'
		       sh 'sleep 5'
	        }
	       }
		}
	}
  }
}
