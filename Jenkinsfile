pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                (maven : 'maven_3_6_3') {
                     mvn clean compile
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                (maven : 'maven_3_6_3') {
                    mvn test
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                (maven : 'maven_3_6_3') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
