// pipeline {
//    agent any

//    stages {

//        stage('Build') {
//            steps {
//                sh 'npm install'
//            }
//        }

//        stage('Run') {
//            steps {
//                sh 'node index.js'
//            }
//        }

//    }
// }


// pipeline {

//     agent any

//     stages {

//         stage('Build Stage') {

//             steps {

//                 sh 'npm install'

//             }
//         }
//         stage('Deploy Stage') {

//             steps {

//                 sh '''

//                 /usr/local/bin/pm2 delete myapp || true

//                 /usr/local/bin/pm2 start index.js --name myapp

//                 /usr/local/bin/pm2 save

//                 '''
                

//             }
//         }
//     }
// }


pipeline {
agent any
stages {

    stage('Build Docker Image') {
        steps {
            sh 'docker build -t nodeapp:${BUILD_NUMBER} .'
        }
    }
}
}

