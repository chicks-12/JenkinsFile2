pipeline {
    agent any

    tools {
        maven 'Maven'  // The name must match the Maven tool name configured in Jenkins Global Tools
    }

    environment {
        // Variables defined here can be used in any stage
        NEW_VERSION = '1.3.0'
    }

    stages {
        stage('build') {
            steps {
                echo 'Building Project'

                // Using environment variable
                echo "Building version ${NEW_VERSION}"

                // Run Maven command
                sh 'mvn install'
            }
        }
    }
}
