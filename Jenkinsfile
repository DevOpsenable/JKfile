pipeline {
agent any

environment{
    branch1 = 'stack'
    branch2 = 'over'
    branch3 = 'flow'
}

stages {
    stage('Stage-One') {
        steps {
            script {                
                env.BRANCHDEPLOY = input message: 'User input required',
                ok: 'Deploy!',
                parameters: [choice(name: 'Branch to deploy', choices: "${branch1}\n${branch2}\n${branch3}", description: 'What branch you wont deploy?')]
            }
        }
    }
    stage('Stage-Two'){
        steps{
             echo "hello Master"
        }
    }
}
}
