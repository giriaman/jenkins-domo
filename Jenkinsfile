pipeline {
    agent any

    stages {
        stage ('Compile Stage') {
          git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {
git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            git url: 'https://github.com/cyrille-leclerc/multi-module-maven-project'
            steps {
                withMaven(maven : 'maven_3_8_2') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
