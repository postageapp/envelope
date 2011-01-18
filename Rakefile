require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "envelope"

  gem.homepage = "http://github.com/twg/envelope"
  gem.license = "MIT"

  gem.summary = %Q{Simple library for constructing emails}
  gem.description = %Q{This is a simple library for constructing RFC-compliant emails}
  gem.email = "scott@twg.ca"
  gem.authors = [ "Scott Tadman" ]

  gem.add_runtime_dependency 'mail', '> 2.2.1'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end

task :default => :test
