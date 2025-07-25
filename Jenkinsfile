pipeline {
  agent any
  stages {
    stage('Branch Info') {
      steps {
        script {
          echo "현재 브랜치: ${env.BRANCH_NAME}"

          if (env.BRANCH_NAME == 'main') {
            echo "🚀 배포 준비"
          } else if (env.BRANCH_NAME == 'dev') {
            echo "🔧 개발 테스트 수행"
          } else if (env.BRANCH_NAME.startsWith('feature/')) {
            echo "🧪 기능 개발 중 (${env.BRANCH_NAME})"
          } else {
            echo "📦 기타 브랜치"
          }
        }
      }
    }
  }
}

