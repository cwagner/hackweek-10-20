# Load some gem-supplied rake tasks to allow for project configuration
require 'rubyprobot'
spec = Gem::Specification.find_by_name 'rubyprobot'
rakefile = "#{spec.gem_dir}/lib/tasks/Rakeloader"
load rakefile
namespace :server do
  require_relative 'lib/inclusive_language_bot'

  desc 'Start development smee.io listener and web server'
  task :start do
    app_instance = InclusiveLanguageBot.new
    app_instance.start_dev_server
  end
end

APP_CLASS = InclusiveLanguageBot
