pipeline {
    
    agent {
        label 'sshagent'
    }
    
    stages {
        stage('build') {
            steps {
                sh 'make all'
            }
        }

      stage('test') {
            steps {
                sh 'mkdir bins'
                sh 'cp *.out bins'
                sh 'ls bins | wc -l'
            }
        }

      stage('package') {
            steps {
                sh 'tar zcf commands.tar.gz bins'
            }
        }
    }
}
