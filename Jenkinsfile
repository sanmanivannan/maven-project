pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
                echo 'Building..'
            }
            post{
                success{
                    echo 'success building and archiving now'
                    archiveArtificats artifacts: '**/target/*.war'
            }
            
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
}
