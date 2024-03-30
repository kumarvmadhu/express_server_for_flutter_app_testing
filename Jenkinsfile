pipeline{
    agent any
    tools {nodejs "Node"}
    stages {
        stage('Clone Repository'){
            steps{
                git branch: 'main',
                    url: 'https://github.com/MIRTAHAALI/express_server_for_flutter_app_testing.git'
            }
        }
        
        stage('Install Dependencies'){
            steps {
                'npm install'
            }
        }
         stage('Install pm2'){
            steps {
                'npm install pm2 -g'
            }
        }
        
        stage('Deploy'){
            steps {
                'pm2 startOrRestart pm2.config.json'
            }
        }
    }
}
