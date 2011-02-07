$LOAD_PATH << '.'
require 'rake'
require 'rake/rdoctask'
#require 'spec/rake/spectask'
require 'lib/metric_fu'

MetricFu::Configuration.run do |config|
  config.roodi    = config.roodi.merge(:roodi_config => 'config/roodi_config.yml')
  config.churn    = { :start_date => "1 year ago", :minimum_churn_count => 10}
  config.hotspots = { :start_date => "1 year ago", :minimum_churn_count => 10}
end

task :default => :spec
