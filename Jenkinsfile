def application = 'boot'
def configFile = ''

node {
  pull(application)

  docker.image('tiangolo/node-frontend:10').inside() {
    stage ('Build docker') {
      sh "npm install"
    }
  }

  packageAndDeploy(application, configFile)
}
