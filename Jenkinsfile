pipeline {
	agent any
	stages{
	    stage('Resync Build'){
	        steps{
	           sh "cd /var/www/html/api_dentalhut"
		                   
	        }
		
	        post {
	           success {
	              echo 'Resync Build Success'

	           }
	        }
	    }
			    stage('Inprogress') {
            steps{
                sh '''
                #sudo npm i --save-dev
                sudo npm i
                sudo chown ubuntu:ubuntu -R /var/www/html/
                sudo pm2 stop server.js
                sudo pm2 start server.js
                '''
                echo 'Done'
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
