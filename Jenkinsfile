#!groovy

pipeline
{
    agent any 
    stages
    {
        stage('configure')
        {
            steps
            {
                sh 'cmake .'
            }
        }
        stage('build')
        {
            steps
            {
                sh 'make -j8'
            }
        }
    }
}
