pipeline {
    agent any

    stages {
       
        
        stage('Build') {
            when {
                // Only run this stage if files under 'src/' have changed
                changeset "/home/ec2-user/docker/ELA/**"
            }
            steps {
                echo 'Building because src directory has changed'
                // Add your build steps here
            }
        }

        stage('Deploy') {
            when {
                branch 'main' // Only run on the 'main' branch
            }
            steps {
                echo 'Deploying as we are on the main branch'
                // Add your deploy steps here
            }
        }
    }
}
