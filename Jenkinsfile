pipeline{
    agent any

    stages{
        stage('Git Clone')
        {
            steps{
            git branch: 'main', credentialsId: 'afdd31f6-eed3-41b1-99fa-255552ce90d9', url: 'https://github.com/manubolutharunsaireddyms/java-web-app-docker.git'
            }
        }
        stage('Build')
        {
            steps{
                echo 'Build'
            }
        }
    }
}