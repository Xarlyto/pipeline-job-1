pipeline {
    agent any

    stages 
    {
        stage('Start') {
            steps {
                echo "Multibranch Pipeline Job 1 Starts"
            }
        }

        stage ('Invoke_pipeline') {
            steps {
                build job: 'pipeline-job-2', parameters: [
                string(name: 'param1', value: "value1")
                ], propagate: true, wait: true
            }
        }

        stage('End') {
            steps {
                echo "Multibranch Pipeline Job 1 Ends"
            }
        }
    }
}
