pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/rajuramachandra/Ansible.git',
                    ]]
                ])
            }
        }
        
        stage('Process Payload') {
            steps {
                script {
                    def payloadData = env.payload
                    def repository = payloadData.repository.full_name
                    def commitMessage = payloadData.head_commit.message
                    // Process the extracted data as needed
                    
                    println "payloadData"
                }
            }
        }
    }
}
