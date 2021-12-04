pipeline {
    agent{label 'master'}
    tools{maven 'M3'}

    stages {
        stage('checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/28rahulmukherjee94/SpringPetClinic.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn compile'
                
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
               
            }
        }
        stage('PACKAGE') {
            steps {
                sh 'mvn package'
                
            }
        }
        stage('DEPLOY') {
            steps {
                
                sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
                
            }
        }
    }
}
 
