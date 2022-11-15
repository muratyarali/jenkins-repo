pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn -f hello-app/pom.xml -B -DskipTests clean package'   /* -f,--file <arg> Force the use of an alternate POM file (or directory with pom.xml)
                                                                                -B,--batch-mode Run in non-interactive (batch) mode (disables output color) */
            }
            post {
                success {
                    echo "Now Archiving the Artifacts....."
                    archiveArtifacts artifacts: '**/*.jar'   /* /home/* is saying every file directly in the /home directory.
                                                                               /home/** is saying every file in a ny directory inside /home. */
                }
            }
        }
        stage('Test') {
            steps {
                sh 'mvn -f hello-app/pom.xml test'
            }
            post {
                always {
                    junit 'hello-app/target/surefire-reports/*.xml'
                }
            }
        }
    }
}