require 'rubygems'
#Gem::manage_gems
require 'rubygems/package_task'


spec = Gem::Specification.new do |s|
  s.name = "libacl"
  s.version = "0.0.1"
  s.author = "Zachris Trolin"
  s.email = "zachris.trolin@gmail.com"
  s.homepage = "http://github.com/zachris/libacl-ruby"
  #s.platform = Gem::Platform.new 'linux-gnu'
  s.platform  =   Gem::Platform::RUBY
  s.summary = "Linux ACL for ruby using ffi"
  s.files = FileList["lib/*rb",'test/*'].to_a
  s.require_path = "lib"
  s.autorequire = "libacl"
  #s.test_files = FileList["{test}/**/*test.rb"].to_a
  s.has_rdoc = true
  s.extra_rdoc_files = ["README"]
  s.add_dependency("ffi")
  s.add_dependency("nice-ffi")
  s.description = <<-EOF
An implementation of linux ACL (posix1e).
Provides more convenience than ruby-acl, and uses FFI so it requires no
extra compilation of c files, and works with jruby.
  EOF
  s.licenses = ['GPL', 'Ruby']
end

Gem::PackageTask.new(spec) do |pkg|
  pkg.need_tar = true
end

task :default => "pkg/#{spec.name}-#{spec.version}.gem" do
    puts "generated latest version"
end
