%w[rubygems rake rake/clean rake/testtask fileutils].each { |f| require f }
require File.dirname(__FILE__) + '/lib/qadmin'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = %q{qadmin}
    s.version = "0.2.3"
    s.authors = ["Aaron Quint"]
    s.date = %q{2009-04-07}
    s.description = %q{An [almost] one command solution for adding admin interfaces/resources to a Rails app.}
    s.email = ["aaron@quirkey.com"]
    s.homepage = %q{http://github.com/quirkey/qadmin}
    s.post_install_message = %q{PostInstall.txt}
    s.rubyforge_project = %q{quirkey}
    s.summary = %q{An [almost] one command solution for adding admin interfaces/resources to a Rails app.}
    s.add_runtime_dependency(%q<activesupport>, [">= 2.3.2"])
    s.add_runtime_dependency(%q<will_paginate>, [">= 2.3.7"])
    s.add_runtime_dependency(%q<restful_query>, [">= 0.2.0"])
    s.add_development_dependency(%q<Shoulda>, [">= 1.2.0"])
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: sudo gem install jeweler"
end

Rake::TestTask.new do |t|
  t.libs << "test"
  t.test_files = FileList['test/test*.rb']
  t.verbose = true
end

Dir['tasks/**/*.rake'].each { |t| load t }

# TODO - want other tests/tasks run by default? Add them to the list
# task :default => [:spec, :features]
