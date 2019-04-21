pipeline{
  agent {
     label 'master' 
  }
  tools {
    maven 'apache-maven'
	jdk 'java'
   }  
  stages{
     stage (github) {
	  steps {
	 git (
	     branch: 'master' ,
	     url: 'https://github.com/santhi-94/repo-3.git'
	     )
	        }
	 }
     stage (compile) {
	    steps{
		 sh  'mvn clean compile' 
		     }
	 }
	 stage (test) {
	  steps{
	   sh 'mvn test'
	        }
	 }
	 
  }
}
