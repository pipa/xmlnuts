$KCODE = 'u'

require 'rubygems'
require 'rake'
require 'rake/clean'
require 'rake/gempackagetask'
require 'rake/rdoctask'
require 'rake/testtask'

Rake::GemPackageTask.new(Gem::Specification.load('xmlnuts.gemspec')) do |p|
  p.need_tar = true
  p.need_zip = true
end

Rake::RDocTask.new do |rdoc|
  files =['README.rdoc', 'MIT-LICENSE', 'lib/**/*.rb']
  rdoc.rdoc_files.add(files)
  rdoc.main = "README.rdoc" # page to start on
  rdoc.title = "XmlNuts Documentation"
  rdoc.rdoc_dir = 'doc/rdoc' # rdoc output folder
  rdoc.options << '--line-numbers' << '--inline-source'
end

Rake::TestTask.new do |t|
  t.test_files = FileList['test/**/*.rb']
end
