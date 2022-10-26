pipeline {
    agent any

    stages {
        stage("Using curl example") {
            steps {
                script {
                        final String url = "https://raw.githubusercontent.com/Ismail-Elyaakouby/groovy/main/aghouchaf.txt"

                    final String response = sh(script: "curl -s $url", returnStdout: true).trim()

                    echo response
                }
            }
        }
    }
}
