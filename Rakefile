require 'pry'

  task :environment do
    require_relative '/Users/Mimi/Development/code/intro-to-rake-web-100817/config/environment.rb'
  end

namespace :greeting do
    desc 'outputs hello to the terminal'
    task :hello do
      puts "hello from Rake!"
    end

    desc 'outputs hola to the terminal'
    task :hola do
        puts "hola de Rake!"
    end
  end

  namespace :db do
      desc 'migrate changes to your database'
      task :migrate => :environment do
        Student.create_table
      end

      desc 'seed the database with dummy date'
      task :seed do
        require_relative '/Users/Mimi/Development/code/intro-to-rake-web-100817/db/seeds.rb'
      end
  end

    desc 'drop into the Pry console'
    task :console => :environment do
      Pry.start
    end
