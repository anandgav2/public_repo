
pipeline {
    agent any

    stages {
        stage('Create Log File') {
            steps {
                script {
                    def jobName = env.JOB_NAME
                    def logFileName = "${jobName}_log.log"
                    def logFilePath = "$HOME/${logFileName}"

                    echo "Creating log file: ${logFilePath}"

                    writeFile file: logFilePath, text: "Log file for Jenkins job: ${jobName}"

                    echo "Log file created successfully."
                }
            }
        }

        // Add more stages as needed
    }

    post {
        always {
            cleanWs()
        }
    }
}
