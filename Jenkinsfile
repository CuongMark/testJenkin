pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'echo "Fail!"; exit 1'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {pipeline {
2
    agent any
3
    stages {
4
        stage('Build') {
5
            steps {
6
                sh 'echo "Hello World"'
7
                sh '''
8
                    echo "Multiline shell steps works too"
9
                    ls -lah
10
                '''
11
            }
12
        }
13
    }
14
}
15

            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
