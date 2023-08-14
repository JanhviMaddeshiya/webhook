pipeline {
    agent any
    stages {
        stage("Clean-up") {
            steps {
                deleteDir()
            }
        }
        stage("Clone repo") {
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/JanhviMaddeshiya/webhook/'
            }
        }
      stage("Build Image") {
            steps {
                script {
                    sh "docker build -t webhook-img ."
                }
            }
        }
    }
}

