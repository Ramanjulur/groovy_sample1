pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
             }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
}
       post ('Notification') {
             success {
                 mail to: 'ramanjulureddy.p@gmail.com',
                       subject: "Failed Pipeline: ${currentBuild.fullDisplayName}",
                       body: "Something is wrong with ${env.BUILD_URL}"
               }
          }
    }


