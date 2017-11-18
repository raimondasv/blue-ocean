pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        git(url: 'https://github.com/raimondasv/blue-ocean-rails-demo', branch: 'master', changelog: true, poll: true)
        sh '''rbenv exec gem install bundler
rbenv exec bundle install
rbenv exec bundle exec rspec spec/'''
      }
    }
  }
}
