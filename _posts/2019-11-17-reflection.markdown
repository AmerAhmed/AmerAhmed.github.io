---
layout: post
title: "Reflektion"
date: 2019-11-17 14:31:16
---

- What do you think about pre-compiling your CSS?
- Compared to regular CSS?
- What techniques did you use?
- Advantages / Disadvantages?

  At first I thought it was quite complicated with pre-compiling. I felt that you first have to lookthrough all the files, or start all over again from the beginning, to understand what to do.
  However, every time you sat down with this task it became easier and even after looking at <https://jekyllrb.com/>. What we did in the course (1ME321) before I thought it was a little easier to understand the CSS code right away.I main.css skapade jag variablar för de färger jag skulle använda till min webbplats. Flera mediaquerys för att kunna få en responsiv design, som även ska se snygg ut på mobila enheter.

  The advantage or disadvantage, a little depending on what you yourself think, is that there are quite a few files. Personally, I like to be able to have more files, with a little less information than to package all the code into one file.

  If you are going to do a smaller project then pre-compiling may feel a little unnecessary.
  One disadvantage is also that if you are a larger team that is going to work, everyone needs to know how it works. If someone starts to go in and change and doesn't understand pre-compiling, it can create problems instead. However, it can also be an advantage when working in larger teams for everyone to work with their own files. For example, if you are a developer and a designer, then the designer has his css files and does not need to be affected by javascript, but only the files the developer needs to move.

- What do you think of static site generators?

- What kind of project is it suitable for?

  I think it works well, but they may not be suitable for all websites.
  A good feature of static site generators is how fast they load and when everything is static, it is packed into files, which means that there are as few calls as possible to the server.
  When I created my website I used "npm run watch" to see the changes in the browser all the time, however this becomes a problem if you want to see, for example, how the site looks in something other than the computer. Then you have to upload the website first.
  Because static site generators do not require as much maintenance, this is probably something you save time and money on, which is always positive.

* What is robots.txt and how have you configured it for your site?

  Robots.txt is a text file that search engines and "robots" download to control which folders they can access. You can freely control what you want to block and not.
  On my site I have chosen to block all "robots" from the entire site with:
  But you can also give "bots" access to the entire site, block / allow certain parts of the site, block / allow certain crawlers, etc.

  {% highlight ruby %}
  User-agent: \*
  Disallow: /
  {% endhighlight %}

- What is humans.txt and how did you configure it for your site?

  Humans.txt is an easily accessible and easily read text file containing information about who built the site. For example, Humans.txt may contain contact information, special thanks or software information.
  Actually, you can add whatever information you want that is relevant to the site. In my humans.txt I have only used information about myself and where I am in the world.

  {% highlight ruby %}
  /_ TEAM _/
  Owner: Amer Ahmed
  Contact: Amer [at] AmerAhmed.github.io
  Twitter: @amer_ahmed345
  Github: @AmerAhmed
  From: Kalmar, Sweden
  Location: Kalmar, Sweden

  /_ THANKS _/
  Education: https://lnu.se/student/

  /_ SITE _/
  Last update: 2019/11/17
  Standards: HTML5, CSS3 JavaScript
  Components: Disqus
  Software: Jekyll, Sass, Vscode, Sublime Text 3, Photoshop, IIlustrator
  {% endhighlight %}

- How did you implement comments on your blog posts?

  I used disqus which was the recommendation. Adding disqus was not difficult at all. After I registered, I used "universal code" and where you were given instructions on where to enter the code.
  However, I also tried to add that on the page with all the blog posts, it would appear how many comments there were on the posts (before going into the post or you could press comments to jump directly to the comments field).However, this only works on some posts and is only visible occasionally, has tried to solve the problem, but unfortunately does not know where the error lies when I followed the instructions for this and it still does not work.Below is the code I implemented in post.html.

  {% highlight ruby %}
  (function() { // DON'T EDIT BELOW THIS LINE
  var d = document, s = d.createElement('script');
  s.src = 'https://https-amerahmed-github-io.disqus.com/embed.js';
  s.setAttribute('data-timestamp', +new Date());
  (d.head || d.body).appendChild(s);
  })();
  {% endhighlight %}

- What is Open Graph and how do you get something out of it?

  Open graph is placed in meta tags in your HTML head. In Open graph you can enter information how you want your website to be presented when it is linked to for example Facebook or Twitter.
  For example, you can control the title, image and description of your website.
  If you use Open Graph, it will be a lot better looking when you share your site. Unfortunately, visitors can get a little tricked when some post information that is irrelevant to their website, just to get more visitors.
