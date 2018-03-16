namespace :greeting do 

  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end
  
  desc 'outputs hole to the temrinal'
  task :hola do 
    puts 'hola de Rake!'
  end
end

desc 'drop into the Pry console'
task :console => :environment do 
  Pry.start 
end

task :environment do 
  require_relative './config/environment'
end

namespace :db do 
  desc ' migate change to databse'
  task :migrate => :environment do 
    Student.create_table
  end
  
  desc 'seed the database with some data'
  task :seed do 
    require_relative './db/seeds.rb'
  end
end