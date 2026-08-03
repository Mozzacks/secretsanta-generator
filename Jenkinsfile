node {

    def IMAGE = "username/santa:${env.BUILD_NUMBER}"

    stage("Checkout") {

        git 'https://github.com/sarikakalsait/secretsanta-generator.git'

    }

    stage("Build") {

        sh "mvn clean package"

    }

    stage("Docker Build") {

        sh "docker build -t ${IMAGE} ."

    }

}
