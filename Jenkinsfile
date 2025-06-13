flag=true

pipeline {
    agent any
    parameters {
        // These are types of parameters
        choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: 'Version to deploy on prod')
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Whether to execute tests')
    }
    environment {
        // Variables defined here can be used by any stage
        HEL_VERSION = '1.3.0'
    }
    stages {
        stage('build') {
            steps {
                echo 'Building Project'
            }
        }
        stage('test') {
            when {
                expression {
                    params.executeTests
                }
            }
            steps {
                echo 'Testing Project'
            }
        }
    }
}
