require 'rubygems'
require 'rake'

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gem|
    gem.name        = "client_side_validations"
    gem.summary     = %Q{Client Side Validations}
    gem.description = %Q{Client Side Validations for Rails 2.x and 3.x}
    gem.email       = "bcardarella@gmail.com"
    gem.homepage    = "http://github.com/dnclabs/client_side_validations"
    gem.authors     = ["Brian Cardarella"]
    gem.add_dependency 'validation_reflection-active_model', ' 0.2.0'
    gem.add_dependency 'json', '1.4.3'
    gem.files       = Dir.glob("lib/**/*") + Dir.glob("javascript/lib/**/*") + Dir.glob("generators/**/*") + %w(LICENSE README.markdown)
    gem.test_files  = []
    
    gem.add_development_dependency 'jspec'
    gem.add_development_dependency 'rspec'
    gem.add_development_dependency 'activerecord', '2.3.8'
    gem.add_development_dependency 'activemodel', '3.0.0.beta4'
    gem.add_development_dependency 'bson_ext', '1.0.4'
    gem.add_development_dependency 'mongoid', '2.0.0.beta11'
    gem.add_development_dependency 'crack'
    gem.add_development_dependency 'bourne'
    gem.add_development_dependency 'rack-test'
  end
  Jeweler::GemcutterTasks.new
rescue LoadError
  puts "Jeweler (or a dependency) not available. Install it with: gem install jeweler"
end

desc 'RSpec tests'
task :rspec do
  puts 'ActiveRecord 2.x'
  system('spec spec/active_record_2_spec.rb')
  
  puts 'ActiveModel 3.x'
  system('spec spec/active_model_3_spec.rb')
  
  puts 'ActionView 2.x'
  system('spec spec/action_view_2_spec.rb')

  puts 'ActionView 3.x'
  system('spec spec/action_view_3_spec.rb')
  
  puts 'Middleware'
  system('spec spec/middleware_spec.rb')
end

desc 'Default: the full test suite.'
task :default do
  system('rake rspec')
end