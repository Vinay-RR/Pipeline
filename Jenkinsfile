pipeline {
  agent any
  parameters {
  string defaultValue: 'TEST', description: 'Environment to deploy the application', name: 'ENV', trim: true
   choice choices: ['main', 'master'], description: 'environment to deploy application', name: 'BRANCH'
}
   stages {
    stage ('BUILD') {
      steps {
        sh '''
		sleep 5
		echo deploying to $ENV
		echo deploying to $BRANCH
		exit 0
		'''
		}
	}
     }
  }
