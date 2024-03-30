pipeline{
    agent any
    tools {nodejs "Node"}
    stages {
        stage('Clone Repository'){
            steps{
                git branch: 'main',
                    url: 'https://github.com/kumarvmadhu/express_server_for_flutter_app_testing.git'
            }
        }
        
        stage('Install Dependencies'){
            steps {
                sh 'npm install'
            }
        }
               
        stage('Deploy'){
            steps {
                sh 'npm start'
            }
        }
    }
}
