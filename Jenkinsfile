@Library("mySharedLibrary")
import com.yoav.jenkins.deployment

String isThisAvailableInLibrary = "kuku"

def pipe = new deployment()


node {
  properties([parameters([choice(choices: ['main', 'develop'], name: 'version')])])
  checkout scmGit(branches: [[name: 'refs/heads/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_user_pass1', url: 'https://github.com/yoav-klein/jenkins-shared-library.git']])
  sh 'ls'
  pipe.flow()
}
