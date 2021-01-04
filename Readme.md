
# [Installing jekyll on WSL Ubuntu 20.x](https://jekyllrb.com/docs/installation/ubuntu/)

1. [Setup Windows Subsystem for Linux (WSL)](https://docs.microsoft.com/en-us/windows/wsl/install-win10) 
2. [Install Ubuntu in WSL](https://ubuntu.com/wsl)
3. [Install ruby](https://www.ruby-lang.org/en/documentation/installation/#apt)
```
sudo apt-get update
sudo apt-get install ruby-full build-essential zlib1g-dev
ruby -v
```

4. Install Ruby Gems to user dir
```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

5. Install Jekyll & [Bundler](https://bundler.io/)
```
gem install jekyll bundler
```

# Create your first site

1. Check out [Ruby 101](https://jekyllrb.com/docs/ruby-101/)

2. Init a working dir for your first site
```
mkdir testsite
cd testsite
bundle init
vim Gemfile
# Append the row `gem "jekyll"`
# save and run
bundle
```
Now run `bundle exec` befor all jekyll commands to make sure you use the jekyll version defined in the `Gemfile`.

3. [Create file index.html](https://jekyllrb.com/docs/step-by-step/01-setup/#create-a-site)

4. Build and run the site
```
bundle exec jekyll build
```
Your site is generated to dir `./_site`  
Run a local dev-site at http://localhost:4000 by executing 
```
jekyll serve
```
5. Continue with the step-by-step tutorial

Check out step 2 - 10 in the [jekyll step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/02-liquid/)

6. Checkout Jekyll default theme on github [minima](https://github.com/jekyll/minima)


