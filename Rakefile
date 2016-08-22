task default: %w(sass:compile)

multitask server: %w(ruby:server sass:watch)

namespace :ruby do
  task :server do
    sh 'ruby -run -e httpd -- -p 8000 web/'
  end
end

namespace :sass do
  task :compile do
    sh 'sass --update --force --style=compressed scss:web/css'
  end

  task :watch do
    sh 'sass --watch scss:web/css'
  end
end
