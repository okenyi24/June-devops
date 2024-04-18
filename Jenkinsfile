pipeline {
    agent any
    tools {
        jdk 'myjava'
        maven 'mymaven'
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository..'
                git 'https://github.com/Keyzoneeee/AKINS-REVISION.git'
            }
        }
        stage('Compile') {
            steps {
                echo 'Compiling..'
                sh 'mvn compile'
            }
        }
        stage('CodeReview') {
            steps {
                echo 'Performing code review..'
                sh 'mvn pmd:pmd'
            }
        }
        stage('Build') {
            steps {
                echo 'Building project..'
                sh 'mvn package'
            }
        }
    }
}

    

