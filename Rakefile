$gem_dirpath = "`ruby -r rubygems -e 'puts Gem.user_dir'`"
$bin_dirpath = "#{$gem_dirpath}/bin"
$bundle_binpath = "#{$bin_dirpath}/bundle"
$site_dirpath = "../gh-pages"

def jekyll(command)
  system "#{$bundle_binpath} exec jekyll #{command}"
end

task :default => [:serve]

task :serve do
  jekyll "serve --watch --incremental --destination _site"
end

task :clean do
  jekyll "clean --destination _site"
end

task :build do
  jekyll "build --destination #{$site_dirpath}"
end
