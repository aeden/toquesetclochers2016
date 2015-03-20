require 'rubygems'
require 'bundler/setup'
require 'fileutils'

desc "Compile the site"
task :compile do
  puts "Compiling site"
  FileUtils.rm_r('_site') if File.exist?('_site')
  `jekyll build`
end

desc "Publish to Github Pages"
task :'publish' => :compile do
  puts "Publishing to Github Pages"
  `git push origin master:gh-pages`
  puts "Site published"
end
