pipeline{
    agent any 
    // here any = any available server that jenkins can connect to
    // that means the agent is current server only
    
    tools{
        maven 'mymaven'
    }
    stages{
        stage('Checkout code'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Compile code'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Review code'){
            steps{
                sh 'mvn pmd:pmd'
            }
        }
        stage('Test code'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package code'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy code'){
            steps{
               echo 'deploy the code...'
            }
        }
    }
}
