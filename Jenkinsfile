def flag = true

pipeline {
    agent any
    environment {
    NEW_VERSION = '1.3.0'
}

    stages {
        stage('build') {
            steps {
                echo 'Building Project'
                    echo "Building Version ${NEW_VERSION}"
            }
        }

        stage('test') {
            when {
                expression {
                    flag == false
                }
            }
            steps {
                echo 'Testing Project'
            }
        }
    }
}
