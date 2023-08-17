pipeline{
    agent any
    stages{
        stage("Provision"){
            steps{
                /* delete everything in jenkins job workspace*/
                sh 'rm -r *'
                /* delete everything inside html/ */        
                sh 'rm -r ../../../../www/html/*'
            }  
        }
        stage("Deploy"){
            steps{
                /* Checking my directory*/
                sh 'pwd'
                /*Cloning all my files from gitlab*/
                sh 'git clone https://gitlab.com/pradyumna1990/hotstar.git -b master'
            }  
        }
        stage("Build"){
            steps{
                /* Moving cloned files to running directory*/
                sh 'mv hotstar/* ../../../../www/html/'
            }  
        }
    }
}