# JS-Tricks.com

> JS-Tricks.com provides tips, tricks, and techniques on JavaScript running on node.js and in the browser in the form of snippets and tutorials.

JS-Tricks.com aims to become a collection of tiny JavaScript snippets that not only show what JS can do, but also describe best practices and principles every good developer should know and understand. It’s about teaching the audience using small and compressed pieces of information (i.e. code snippets) on very specific tasks. 

Every JS developer once had to dig in [reference docs and guides](https://developer.mozilla.org/en/docs/Web/JavaScript) in order to learn how to code JavaScript. But these docs usually don’t include hints on how a specific feature is implemented the best way possible. Often we only head for code that just *works* without thinking about maintainability, performance, compatibility, and so on. We learn these things later on, often because we find out that code doesn’t work in a specific environment. Of course there is lots of information available on the [web](http://google.com/), especially [StackOverflow](http://stackoverflow.com/questions/tagged/javascript), and there are also [good](http://amzn.com/0596517742) [books](http://amzn.com/0596809484) that you should definitely read. Nonetheless we think it’s time to collect all the **small stuff**, which is learnt quickly, for everyone to look up [at a central place](http://js-tricks.com/).

That’s why [we](http://fapprik.com/) started JS-Tricks as an experiment on Tumblr. However, we quickly realized that Tumblr isn’t the best place to start a blog about coding with lots of code snippets. Thus we decided to move the blog to a file-based content management system in order to be able to manage the whole content community-driven on GitHub. Feel free to contribute!

## Getting started

	git clone --recursive https://github.com/fapprik/js-tricks.com
	cd js-tricks.com
	npm install gulp -g  # if not already installed on your system
	npm install  # will probably show some warnings, see below
	gulp build

Note that you need to clone the repository recursively in order to include all required submodules as well. Moreover we make use of [Bower](http://bower.io/) and [gulp.js](http://gulpjs.com/) for frontend asset generation, concatenation, uglification, image minification, and so on—so don’t forget to run `gulp build` at least once after cloning.

JS-Tricks.com is built using [PRONTO](http://prontocms.com/). If you want to run the site locally, that’s pretty easy:

    php -S localhost:8080

If you prefer to use Apache or nginx, check out the [»Getting started« section on the PRONTO website](http://prontocms.com/docs/getting-started).

Besides the `gulp build` task, there is `gulp dev`, which does exactly the same but additionally starts watching the file system for changes and rebuilds every time a change occurs.

### Issues with `npm install`

**The warnings are normal!** Because of the way how [spritesmith](https://github.com/Ensighten/spritesmith) (one of our dependencies that conveniently generates sprites) works, you will most certainly encounter some warnings when you run `npm install`. This is due to the fact, that `spritesmith` has several *optional* dependencies itself, which may fail. Nonetheless `npm` will continue to install everything else. This is also explained in spritesmith’s [README](https://github.com/Ensighten/spritesmith/blob/master/README.md#installation), albeit very short.

## Contributing

Well, that’s easy! First, head over to our [GitHub](https://github.com/fapprik/js-tricks.com) repository and fork it. Then make your contributions, and send a pull request. Please note that writing articles and hacking on the JS-Tricks.com source are two different things. Therefore, please send separate pull requests according to what you’ve done. It will be helpful to use distinct branches in your fork to accomplish that.

## Writing articles

If you find out that there’s no article on a specific topic you are currently into, but there should be one, go ahead and write about it! Here are some guidelines for you to keep in mind. Note that we use these guidelines to review your article and will give you hints in the PR chat on what’s missing.

While JS-Tricks.com itself is released under the MIT license, all articles are published under [CC-BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/).

### Primer

* **The PRONTO style.** If you’ve never worked with PRONTO before, check out their [»Managing content« section](http://prontocms.com/docs/managing-content) in order to get started.

* **Markdown format.** If that’s new for you, PRONTO provides a [short introduction](http://prontocms.com/docs/formatting-text) on that. There’s also a [short writing](https://help.github.com/articles/markdown-basics/) by the GitHub staff. For correct syntax highlighting, please use the [GitHub style](https://help.github.com/articles/github-flavored-markdown/#syntax-highlighting). On JS-Tricks.com you may use `javascript`, `css` and `html`.

### Guidelines

* **Choose a short, but descriptive headline.**

* **Be distinct and precise.** Your article should be readable within two to three minutes and should only contain what’s needed to concisely describe your chosen topic, no more, no less. The reader should be able to get the idea, but not always want’s to know the whole story.

* **Refer to other resources when needed.** Going into detail is honourable. But before writing too much, it’s almost always better to refer to external resources that one may consume later.

* **Use a neutral style of writing.** JS-Tricks is a community project. That means anyone can provide content by writing new articles as well as improve existing ones. We kindly ask you to write in a neutral style to maintain a common style of writing across the site. 

* **Show some respect.** If you did not invent a certain programming feature you are writing about, but you know that someone else deserves credit, do not hesitate to include the inventor’s name (even if it’s just a nickname!) and link to his/her blog or GitHub profile.

* **If you want, you may add your name to the contributors list.** Feel free to add your GitHub username to the `Contributors` field (comma-separated list) in your `post.md` to be listed on the site’s [contributors list](http://js-tricks.com/contributors).

* **When it’s online: spread the word!**

## License

Copyright (c) 2014 [fapprik](http://fapprik.com/)  
Licensed under the MIT license.

See LICENSE for more info.
