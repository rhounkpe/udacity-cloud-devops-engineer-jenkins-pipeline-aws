pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'us-east-2',credentials:'aws-static') {
                    sh 'echo "Uploading content with AWS creds"'
                    s3Upload(file:'index.html', bucket:'rufin-hounkpe-cloud-devops-engineer-jenkins-pipeline-aws')
                }
            }
        }
    }
}