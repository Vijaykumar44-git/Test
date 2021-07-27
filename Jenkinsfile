pipeline {
    agent any
    environment {
        Name="VijayKumar"
        secret=credentials('Test')
    }
    parameters {
        choice(name: 'VERSION', choices: ['1.0','2.0','3.0'], description: 'Choices given')
        booleanParam(name: 'et', defaultValue: true, description: 'Boolean Valuue....')
    }
    stages {
        stage ('Build') {
            when {
                expression {
                    params.et
                }
            }
            steps {
                sh 'echo "building...by $Name, $secret"'
            }
        }
    }
    post {
        always {
            echo "I will always executed...."
        }
        success {
            echo " I will only executed when job is success"
        }
    }
}
