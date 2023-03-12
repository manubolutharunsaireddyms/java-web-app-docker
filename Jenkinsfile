pipeline{
    agent any

    stages{
        stage('Git Clone')
        {
            steps{
            git branch: 'main', credentialsId: 'afdd31f6-eed3-41b1-99fa-255552ce90d9', url: 'https://github.com/manubolutharunsaireddyms/java-web-app-docker.git'
            }
        }
        stage('Maven Clean Package')
        {
            steps{
                 sh 'mvn clean package'
            }
        }
        stage('Build Docker Image')
        {
            steps{
                script{
                     docker.build("java-web-app:${env.BUILD_NUMBER}")
                }
               
            }
        }
    }
}