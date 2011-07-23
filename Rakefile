# encoding: utf-8

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
  # gem is a Gem::Specification... see http://docs.rubygems.org/read/chapter/20 for more options
  gem.name = "rubycliweather"
  gem.add_dependency 'nokogiri'
#  gem.add_dependency 'open-uri'
  gem.executables = ['rubycliweather']
  gem.homepage = "http://github.com/ip2k/rubycliweather"
  gem.license = "Creative Commons by-nc-sa"
  gem.summary = "Simple weather forecasts right in your terminal"
  gem.description = "rubycliweather provides an easy-to-use CLI that harnesses the Wunderground XML API and delivers pretty forecasts FAST right to your terminal"
  gem.email = "github@seanp2k.endjunk.com"
  gem.authors = ["ip2k"]
  # dependencies defined in Gemfile
end
Jeweler::RubygemsDotOrgTasks.new

=begin
require 'rake/testtask'
Rake::TestTask.new(:test) do |test|
  test.libs << 'lib' << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
end
=end

require 'rcov/rcovtask'
Rcov::RcovTask.new do |test|
  test.libs << 'test'
  test.pattern = 'test/**/test_*.rb'
  test.verbose = true
  test.rcov_opts << '--exclude "gems/*"'
end

task :default => :test

=begin
require 'rdoc/task'
RDoc::Task.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "rubycliweather #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
=end
