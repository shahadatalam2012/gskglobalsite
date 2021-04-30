# Setup

1. Enable WSL windows component
2. Install Ubuntu 18.04 LTS
3. Launch Ubuntu and then following this guide (https://jekyllrb.com/docs/installation/ubuntu/)
- `sudo apt-get update`
- `sudo apt-get install ruby-full build-essential zlib1g-dev`
- following commands to update your `~/.bashrc` file
```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
- `gem install jekyll bundler`

# Running
- `bundle exec jekyll build` to build
- `bundle exec jekyll serve` to serve

# Resources
- https://pages.github.com/versions/

# @applyfiles error on jekyll build
- `sudo umount /mnt/e`
- `sudo mount -t drvfs E: /mnt/e -o metadata` here E: is drive that has my gskglobalsite folder. specify your drive.
- `sudo chmod -R 777 /mnt/e/GSK/gskglobalsite/` or `sudo chown -R gursharan /mnt/e/GSK/gskglobalsite/` here /mn/e/GSK/gskglobalsite is path to my site. specify your path. Here gursharan is my account name. specify your account name
- Refer stackoverflow - https://stackoverflow.com/questions/57243299/jekyll-operation-not-permitted-apply2files and https://stackoverflow.com/questions/46610256/chmod-wsl-bash-doesnt-work