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
	
	script{
	
	def foo = ${env.BUILD_NUMBER}
	
	sh "aws s3 cp /workspace/jenkinsTest/dist/rectangle-${foo}.jar s3://cf-templates-ika2ur4lmnvx-us-east-1/"
	}
	
	}
	

  
} 	
