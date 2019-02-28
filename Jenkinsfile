properties([pipelineTriggers([githubPush()])])

  node ('linux'){

    
    stage ("Unit Test") {
	
       
		
		git 'https://github.com/chak1581/jenkinsTest.git'
		
		   sh "ant -f test.xml -v"
		   
			
		
	}
	stage ("Build") {
	
	sh "ant -f build.xml -v"

	
	}
	
	stage ("Copy") {
	
	
	
	
	sh "aws s3 cp /workspace/jenkinsTest/dist/rectangle-${env.BUILD_NUMBER}.jar s3://cf-templates-ika2ur4lmnvx-us-east-1/"
	
	
	}
	

  
} 	
