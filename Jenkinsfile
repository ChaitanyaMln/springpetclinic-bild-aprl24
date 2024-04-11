pipeline{
   agent{
     label 'spc'
	 }
	 stages{
	    stage('git'){
		  steps{
		   git url:'https://github.com/spring-projects/spring-petclinic.git', branch:'main'
                  }
            }
            stage('build'){
                steps{
                 sh 'mvn clean package'
                 junit testResults: '**/surefire-reports/*.xml'
         }
     }
    }
}
