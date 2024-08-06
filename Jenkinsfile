pipeline{
    agent any
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/SafwanMcQueen/SpringPetClinic.git' 
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('deploy'){
            steps{
                sh 'java -jar /home/coder/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
