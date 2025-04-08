pipeline{
    agent any
    stages{
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/faisaliqbal-dev/elevate-app.git'
            }
        }
        stage("build"){
            steps{
                echo 'installing dependencies'
                sh 'npm install'
            }
        }
         stage("test"){
            steps{
                echo 'Running tests'
                sh 'npm test'
            }
        }
         stage("deploy"){
            steps{
                echo 'deploying Node.js App for Elevate Lab Internship'
                echo 'created by Mohammed Faisal Iqbal'
                sh 'npm start &'
            }
        }
    }
    post{
        always{
            echo " always "
        }
        success{
            echo " pipeline executed successfully "
        }
        failure{
            echo " pipeline execution failed "
        }
    }
}