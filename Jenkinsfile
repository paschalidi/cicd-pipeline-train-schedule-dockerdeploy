node {
    checkout scm

        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
        def customImage = docker.build("cpaschalidi/docker-test${env.BUILD_ID}")

        /* Push the container to the custom Registry */
        customImage.push()
    }
}