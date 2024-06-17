pipeline{
    tools{
        jdk 'java'
        maven 'maven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/adegokeobafemi/demo-project1.git'
              }
          }
          stage('Compile with mvn1'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with mvn2'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
         
          stage('Package with mvn'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
