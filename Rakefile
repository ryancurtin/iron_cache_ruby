require 'rubygems'
require 'rake'

begin
  require 'jeweler2'
  Jeweler::Tasks.new do |gem|
    gem.name = "iron_cache"
    gem.summary = "Ruby client for IronCache by www.iron.io"
    gem.description = "Ruby client for IronCache by www.iron.io"
    gem.email = "travis@iron.io"
    gem.homepage = "http://www.iron.io"
    gem.authors = ["Travis Reeder"]
    gem.add_dependency 'iron_core'
    gem.add_dependency 'rest-client'
    gem.add_dependency 'rest', '>= 0.1.2'
    #gem.add_dependency 'typhoeus'
    gem.required_ruby_version = '>= 1.9'
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler2"
end

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test

require 'rdoc/task'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'doc'
  rdoc.title = "iron_cache #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
