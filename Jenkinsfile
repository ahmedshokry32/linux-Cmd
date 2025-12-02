pipeline {
    
    agent {
        label 'sshagent'
    }
    
    stages {
        stage('build') {
            steps {
                echo 'make all'
            }
        }

      stage('test') {
            steps {
                echo 'mkdir bins'
                echo 'cp *.out bins'
                echo 'ls bins | wc -l'
            }
        }

      stage('package') {
            steps {
                echo 'tar zcf commands.tar.gz bins'
            }
        }
    }
}
