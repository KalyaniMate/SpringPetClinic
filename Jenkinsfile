pipeline{
    agent{labe; 'master'}
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/KalyaniMate/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steos{
                sh 'mvn compile'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /var/lib/jenkins/workspace/PetclinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
