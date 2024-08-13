pipeline{
    agent any
    stages{
        stage('checkout the code from github'){
            steps{
                 git url: 'https://github.com/Soumyaranjan-Rout/temp0.git'
                 echo 'github url checkout'
            }
        }
        stage('Maven codecompile'){
            steps{
                echo 'starting compiling'
                sh 'mvn compile'
            }
        }
        stage('Maven codetesting'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Maven qa'){
            steps{
                sh 'mvn checkstyle:checkstyle'
            }
        }
        stage('Maven package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Docker Login'){
            steps{
                withCredentials([string(credentialsId: 'dockerhub', variable: 'dockerhubpassword')]) {
    // some block
               }
            }
        } 
    }
}
