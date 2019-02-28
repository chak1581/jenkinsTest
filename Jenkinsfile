properties([pipelineTriggers([githubPush()])])

  node ('linux'){

  stages {    
    stage ("Unit Test") {
	
       
		
		git 'https://github.com/chak1581/jenkinsTest.git'
		
		   sh "ant -f test.xml -v"
		   
			
		
	}
	stage ("Build") {
	
	sh "ant -f build.xml -v"

	
	}
	

  }
} 	
