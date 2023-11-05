def gv

pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "testing the app"
                    echo "executing pipeline for branch $BRANCH_NAME"
                    //gv.buildJar()
                }
            }
        }
        stage("build image") {
            when {
                expression {
                    BRANCH_NAME == 'main'
                }
            steps {
                script {
                    echo "building image"
                    //gv.buildImage()
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    //gv.deployApp()
                }
            }
        }
    }   
}
