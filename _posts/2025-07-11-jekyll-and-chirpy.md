---
layout: post
title: Creating my blog through Jekyll and GitHub Pages
categories: notes
tags: jekyll
description: A description of the process of creating this page for future me.
image:
    path: /assets/posts/jekyll-and-chirpy/jekyll-chirpy.png
    alt: Jekyll and Chirpy
---

I came across the idea of creating a blog recently, and decided to take it upon my hands and build one from scratch. At first, I wanted to create a blog with an admin page so I could create posts without having to go into the codebase. But quickly, I saw the challenge of creating HTML of a posts' text and image exactly how the user envisioned it. 

Not keen on creating my own content management system for one blog, I decided to scrap that idea and work on a static site. But the idea of modifying HTML for every post seemed inefficient. What is some way I could type content up quickly and have it render the correct HTML?

[Jekyll](https://jekyllrb.com/) seems to be a good answer to this, and is used a lot for blogs, portfolios, class websites, and more. This website uses the Chirpy theme. Setting up was very easy thanks to this [Chirpy starter](https://github.com/cotes2020/chirpy-starter). Installing Ruby and Jekyll were relatively easy, and serving the site was a quick two step process. 

## Instructions

Run ```bundle``` in the your project root to install all dependencies.

Run ```bundle exec jekyll serve``` to serve the site to [localhost:4000](http://localhost:4000).

Now, deploying on GitHub Pages was also very easy! Simply enablign GitHub Actions in the repository settings will cause deployments to be triggered automatically with each commit. Make sure to change the ```url``` field in ```_config.yml``` to your GitHub url, in my case I used https://username.github.io.

## A slight issue

I wanted the host my blog at https://username.github.io/blog. I was able to do this for both local and GitHub pages deployment, although I ran into a ton of issues before resolving it! You have to be very precise with the fields `url` and `baseurl`. In `_config.yml`, I had:
```
url: "https://nleobandung.github.io"
baseurl: "/blog"
```

If your CSS or assets don't render, or your build fails because it can't find certain resources, your URL paths are probably the problem.

## Conclusion

Using Jekyll themes will add some inflexibility in your blog design, but at least for Chirpy it is really easy to customize the things you do have control over. The `.yml` files provide many options to modify your page to how you like it. Check out my repository to see how this blog was set up!

That's all there is to it! I plan to document more of the things I do just in case I ever need to look back at what I did, but maybe this will help someone else encountering the same niche problems I do!