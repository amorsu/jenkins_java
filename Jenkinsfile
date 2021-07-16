pipeline {
    agent any
    stages {
        stage('No-op'){
            steps{
                sh 'ls'
            }
        }
    }
    post {
        always {
            echo "one way or another , I have finished"
            deleteDir()
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :<'
        }
        changed {
            echo 'things were changed......'
        }
    }
}