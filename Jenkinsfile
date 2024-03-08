pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/Keyzoneeee/AKINS-REVISION.git'
              }
          }
          stage('Compile'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code repository
                git 'https://github.com/Keyzoneeee/AKINS-REVISION.git'
            }
        }
        
        stage('Build') {
            steps {
                // Execute Maven package command
                sh 'mvn package'
            }
        }
    }
    

