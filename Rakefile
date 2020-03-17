require 'rake/testtask'
require 'bundler/gem_tasks'

desc 'say hello'
task :hello do
  puts 'Hello there. This is from the hello task'
end

desc 'run tests'
task :test do
  sh 'ruby ./test/todolist_project_test.rb'
end

desc 'run tests'
task :default => :test

Rake::TestTask.new(:task) do |t|
  t.libs << 'test'
  t.libs << 'lib'
  t.test_files = FileList['test/**/*_test.rb']
end

desc 'Display Inventory of All Files'
task :inventory do 
  Find.find('.') do |name|
    next if name.include?('/.')
    puts name if File.file?(name)
  end
end
