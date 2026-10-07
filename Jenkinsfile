pipeline {
    agent {
        node {
            label 'AGENT-1'
        }
    }
    environment { 
        COURSE = 'jenkins'
    }
    options {
                // Timeout counter starts BEFORE agent is allocated
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }    
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                        echo "Building.."
                        sleep 10
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    echo 'Testing..'
                }    
            }
        }
        stage('Deploy') {
            steps {
                script {
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