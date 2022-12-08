namespace :greeting do
  desc 'logs hello from task'
  task :hello do
    puts "hello from Rake!"
  end
  desc 'logs hola from task'
  task :hola do
    puts "hola de Rake!"
  end
end

desc 'connect migrate to environment'
task :environment do
  require_relative './config/environment'
end

namespace :db do
  desc 'migrate changes to database'
  task migrate: :environment do 
    Student.create_table
  end
  desc 'seed the database with dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
end
desc 'drop into pry'
task console: :environment do 
  Pry.start
end