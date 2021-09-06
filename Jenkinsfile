pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
         
            steps {
                 git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
         
            steps {
                git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
