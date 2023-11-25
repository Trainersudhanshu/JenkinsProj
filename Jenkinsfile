pipeline {
    agent {label "awsslave"}

    stages {
        stage("Checkout the code"){
            steps{
                git "https://github.com/Trainersudhanshu/JenkinsProj.git"
            }
        }
        stage('Deployment') {
            steps {
                echo 'Going to deploy the app'
                sh " docker rm -f mywebos"
                sh "docker pull jinny1/gfgflaskapp:latest"
                sh "docker run -d -p 80:80 --name mywebos jinny1/gfgflaskapp"
            }
        }
    }
}

