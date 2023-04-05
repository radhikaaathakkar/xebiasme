pipeline {
    agent any 

    stages{
        stage('GIT Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/radhikaaathakkar/xebiasme'
            }
        }

        stage('Unit Testing'){
            steps{
                sh 'mvn test'
            }
        }

        stage('Integration Testing'){
            steps{
                sh 'mvn verify -DskipunitTests'
            }
        }
    }
}