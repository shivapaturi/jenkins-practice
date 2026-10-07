pipeline {
    agent {
        node {
            label 'AGENT-1'
    }
}

    stages {
        stage('Build') {
            steps {
                scrpit{
                    echo 'Building..'
                }
            }
        }
        stage('Test') {
            steps {
                scrpit{
                    echo 'Testing..'
                }    
            }
        }
        stage('Deploy') {
            steps {
                scrpit{
                    echo 'Deploying....'
                }
                
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        }
        success { 
            echo 'Hello success!'
        }
        failure { 
            echo 'Hello failure!'
        }
    }
}