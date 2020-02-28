desc 'exists'
task :console do
  "Make sure you have a 'console' rake task"
end

desc 'creates environment'
task :environment do
  require_relative './config/environment'
end

namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'puts hola to the terminal'
  task :hola do
    puts 'hola de Rake!'
  end

end

namespace :db do
  desc 'invokes :environment task as a dependency'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds database with dummy date from seed file'
  task :seed do
    require_relative './db/seeds.rb'
  end

end