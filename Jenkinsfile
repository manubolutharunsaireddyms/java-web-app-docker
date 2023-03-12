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
                sh 'docker build -t java-web-app:latest .'
            }
        }
        stage('Docker push')
        {
            steps{
                sh 'docker login -u awstharun -p Ur16cs035#'
                sh 'docker push awstharun/java-web-app:latest'
            }
        }
    }
}