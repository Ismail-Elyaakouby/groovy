def BRANCH_NAMES = sh (script: 'curl -s https://raw.githubusercontent.com/Ismail-Elyaakouby/groovy/main/aghouchaf.txt' ', returnStdout:true).trim()
pipeline {

    agent any

    parameters {
        choice(
            name: 'BranchName',
            choices: "${BRANCH_NAMES}",
            description: 'to refresh the list, go to configure, disable "this build has parameters", launch build (without parameters)to reload the list and stop it, then launch it again (with parameters)'
        )
    }

    stages {
        stage("Run Tests") {
            steps {
                sh "echo SUCCESS on ${BranchName}"
            }
        }
    }
}
