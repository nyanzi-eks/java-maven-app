pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "Testing the application..."
                    echo "Executing pipeline for branch ${env.GIT_BRANCH} "
                }
            }
        }
        stage("build") {
            when {
                expression {
                    env.GIT_BRANCH == "master"
                }
            }
            steps {
                script {
                    echo "Building the application..."
                }
            }
        }
        stage("deploy") {
            when {
                expression {
                    env.GIT_BRANCH == "master"
                }
            }
            steps {
                script {
                    echo "Deploying the application..."
                }
            }
        }
    }
}