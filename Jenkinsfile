pipeline{
    agent any
    stages{
        stage('make it possible to execute'){
            steps{
                sh 'chmod +x ./script/*'
            }
        }
        stage('Setting up environment'){
            steps{
                sh './script/before_installation.sh'
                sh './script/installation.sh'
                
            }
        }
        stage('Run the application'){
            steps{
                sh 'sudo systemctl restart flask.service'
            }
        }
    }
}