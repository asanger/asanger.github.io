---
layout: post
title: "Hello World"
date: 2016-08-18T10:55:42-04:00
---

# Personal Blogging
How many times in a month do you find yourself looking for some information and stumble upon someone's personal blog where they are explaining how they overcame the exact situation that you're haveing trouble with?

Personal developer blogs serve two purposes:

1. They serve as a "rubber ducky" of sorts because we need to be able to explain what we did in plain english. The simple act of doing this really helps to reinforce the concepts that you're writing about.
2. The serve as documentation for the next time you run into a similar problem. A blog that you personally wrote is going to be much easier to find than that one stack overflow question that helped point you in the right direction.
3. They give back to the community. In an industry where 95% of us are just taking information, code snippets, open source software, etc, it feels good to be able to give something back, however small. Maybe it will help someone on the other side of the country and make their day a little less stressful.

# Creating Your First Jekyll Blog

We're going to set up a simple blog and get it hosted using Github pages.

 
### Install the `octopress` gem. 

We can do this by installing the gem globally with `gem install octopress`, or we can put it in a `Gemfile` and install it with `bundler`. For now, we will just install it globally:

{% highlight bash %}
  $ gem install octopress
{% endhighlight %}


### Verify

Open a new terminal window and check to make sure that `octopress` has been installed correctly.

{% highlight bash %}
  $ octopress --help
{% endhighlight %}

You should see a list of available commands. If you don't, then you done goofed...


### Create blog

Create a new blog in you preferred location. In the command below, replace `~/dev/blog` with the directory that you want to be your blog's root.

{% highlight bash %}
  $ octopress new ~/dev/blog
{% endhighlight %}

Check out all the files that were created. Running `octopress new` is the same as running `jekyll new` and `octopress init`, so you'll see a bunch of jekyll-specific files (remember, octopress is just something built on top of jekyll).


### Test

To quickly test the default blog, run the following:

{% highlight bash %}
  $ bundle install
  $ jekyll serve
{% endhighlight %}

Open `http://localhost:4000` and make sure that you see something! If you don't, you done goofed!


### Create a Post

Let's create our very first post:

{% highlight bash %}
  $ octopress new post "Hello World"
{% endhighlight %}

The new post that was created can be found in the `_posts` directory.  Right now, it's nothing more than [Front Matter](https://jekyllrb.com/docs/frontmatter/), which is Jekyll's way of defining special variables for the post to use.
Some of these variables are special, such as `layout`, which Jekyll uses to decide which template should be used for laying out the content of your post.
Run `jekyll serve` again and refresh the browser to see your new post.


### Add Content

It's super boring now, so let's add some content to it. The blog uses Markdown by default, so there's no need to worry about adding a bunch of `html` (though you can if you want).