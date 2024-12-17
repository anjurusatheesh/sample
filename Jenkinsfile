pipeline {
    agent any

    stages {
        stage('git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/anjurusatheesh/sample.git'
            }
        }
        
        stage('image build') {
            steps {
                sh 'docker build -t node .'
            }
        }
        
        stage('image run') {
            steps {
                sh 'docker run -itd -p 3002:3000 node'
            }
        }
    }
}
