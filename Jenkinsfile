pipeline{
    agent any
    stages{
        stage("Fortis-Development-server"){
            when {
                // This works only in multi branch pipeline
                branch 'dev-1'
            }
            steps{
                echo "Deploying to Dev environment"
            }
        }
        stage("Fortis-Staging-server"){
            when {
                branch 'master'
            }
            steps{
                echo "Deploying to Staging environment"
            }
        }
    }
}
