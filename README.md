# Blog
To be updated with some (hopefully) interesting writeups. 
## Local Deployment
Before I forget, here are the steps to run the site locally. If you haven't yet, start by install the Ruby gems used.
```
bundle install
```
Then, to deploy to [http://localhost:4000](http://localhost:4000), run this command. Because of a folder path difference between local and GitHub Pages deployment, we override the `baseurl` field in our command.
```
bundle exec jekyll serve --baseurl=""
```