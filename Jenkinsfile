@Library("mySharedLibrary")
import com.yoav.jenkins.deployment

def pipe = new deployment()

node {
  checkout scmGit(branches: [[name: 'refs/tags/1.0']], extensions: [], userRemoteConfigs: [[credentialsId: 'github_user_pass1', url: 'https://github.com/yoav-klein/jenkins-shared-library.git']])
  sh 'ls'
  pipe.flow()
}
