PROJECTS = 'http://localhost:8080/dashboard/cctray.xml' #'http://taney.thoughtworks.com:8080/dashboard/cctray.xml'

namespace :db do
  namespace :migrate do
    task :reset do
      require 'migrations/project'
      Project.down
      Project.up
    end
  end
end

namespace :monitor do
  task :start do
    require 'start'
    start
  end
  
  task :clean => ['db:migrate:reset']  
end