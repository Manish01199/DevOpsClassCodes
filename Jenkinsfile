pipeline {
	agent any
	stages{
	    stage('Resync Build'){
	        steps{
	           sh 'cd /var/www/html/'
                   sh 'mkdir api_dehtalhut'
                 sh  'sudo rsync -a /var/lib/jenkins/workspace/api_dentalhut.in/. '
                  
	        }
		
	        post {
	           success {
	              echo 'Resync Build Success'

	           }
	        }
	    }

	    stage('Inprogress') {
            steps{
                echo 'Done'
            }
        }
        stage('Deploy'){
            steps{
              echo 'Build Successful'
        }
        }
	}
}
