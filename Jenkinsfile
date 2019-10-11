pipeline {
   agent any
   stages {
      stage('Setup'){
         steps {
            sh 'ls'
            // sh 'python3 -m venv ~/.devops
            //    source ~/.devops/bin/activate
            //    make install
            //    brew install hadolint
            //    brew cask install virtualbox
            //    brew cask install minikube'
         }
      }
      stage('Lint Dockerfile') {
         steps {
            sh 'ls'
            // sh 'hadolint Dockerfile'
         }
      }
      stage('Build Image') {
         steps {
            script{
               sh 'ls'
               // sh 'docker build --tag=machine-learning-microservice .'
            }
         }
      }
      stage('Push Image'){
         steps {
            script{
               sh 'ls'
               // sh 'docker build --tag=machine-learning-microservice .'
            }
            // 	withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhub', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD']]){
            //    sh '''
            //       docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD
				// 		docker push ziyadmsq/machine-learning-microservice:$BUILD_ID
            //       '''
            //    // sh '''make docker-push"
            // }
         }
      }
      stage('Create Cluster'){
         steps{
            script{
               sh 'ls'
               // sh 'pip install awscli --upgrade
               //    curl --silent --location "https://github.com/weaveworks/eksctl/releases/download/latest_release/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp
               //    sudo mv /tmp/eksctl /usr/local/bin
               //    eksctl create cluster \
               //    --name prod \
               //    --version 1.14 \
               //    --nodegroup-name standard-workers \
               //    --node-type t3.medium \
               //    --nodes 3 \
               //    --nodes-min 1 \
               //    --nodes-max 4 \
               //    --node-ami auto
               //    kubectl get svc'
            }
         }
      }
      stage('kubectl config'){
         steps{
            script{
               sh 'ls'
               // sh 'aws eks --region us-east-1 update-kubeconfig --name prod'
            }
         }
      }
      stage('Deploy Kubernetes'){
        steps{
            script{
               sh 'ls'
               // sh "make kube-deploy"
            }
        }
      }

   }
}
// ======================== \\
// pipeline {
//      agent any
//      stages {
//          stage('Build') {
//              steps {
//                  sh 'echo "Hello World"'
//                  sh '''
//                      echo "Multiline shell steps works too"
//                      ls -lah
//                  '''
//              }
//          }
//          stage('Lint HTML') {
//               steps {
//                   sh 'tidy -q -e *.html'
//               }
//          }
//          stage('Upload to AWS') {
//               steps {
//                   withAWS(region:'us-east-1',credentials:'aws-creditional-ID') {
//                   sh 'echo "Uploading content with AWS creds"'
//                       s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'static')
//                   }
//               }
//          }
//      }
// }