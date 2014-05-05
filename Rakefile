desc "Setup GitHub Pages Branch"
task :setup_github do
  system "git checkout -b gh-pages"
  system "git checkout master"
end

desc "Generate site and deploy to GitHub Pages"
task :deploy_github do
  system "jekyll build"
  system "cp -rp _site/ ../tmp/"
  system "git checkout gh-pages"
  system "rm -rf _includes"
  system "rm -rf _layouts"
  system "rm -rf _posts"
  system "rm -rf _site"
  system "rm -rf css"
  system "rm -rf font"
  system "rm -rf js"
  system "rm -rf jekyll"
  system "rm .gitignore"
  system "rm _config.yml"
  system "rm CNAME"
  system "rm index.md"
  system "rm Rakefile"
  system "rm index.html"
  system "cp -r ../tmp/ ./"
  system "rm -rf ../tmp"
  system "git add --all && git commit -m 'Update site' && git push origin gh-pages"
  system "git checkout master"
end