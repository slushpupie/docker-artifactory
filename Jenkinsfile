
node("docker") {
  checkout scm
  stage 'build'
  image = docker.build('localhost:6000/slushpupie/artifactory')

  if(env.GIT_BRANCH == 'origin/master'){
    stage 'publish'
    image.push()
  }
}

