pipeline {
    agent any
    stages {
        stage('One') {
                steps {
                        echo 'Hi, this is Zulaikha from edureka'
			
                }
		post {
       			always {
           			jiraSendBuildInfo branch: '', site: 'navjit.atlassian.net'
       			}
       		}
      	}
        stage('Two'){	    
		steps {
			input('Do you want to proceed?')
        	}
	}
        stage('Three') {
                when {
                        not {
                                branch "master"
                        }
                }
                steps {
			echo "Hello"
                        }
        }
        stage('Four') {
                parallel {
                        stage('Unit Test') {
                                steps{
                                        echo "Running the unit test..."
                                }
                        }
                        }  
	}
        
    }
}

