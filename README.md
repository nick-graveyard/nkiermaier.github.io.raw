### Jekyll blog code

This is the custom code for my jekyll pages blog:  
  * https://nkiermaier.github.io

I use a plugin for category indexes and pagination which isnt supported natively by Github.

So, I maintain my code here, rebuild my blog locally on changes, and update my blog repo with the
newly updated `_site` folder.   

This combined with a `.nojekyll` file in the blog repo allows hosting without build in github jekyll. 

The advantage of this custom jekyll configuration:  

1. All of my categories are dynamically generated, have their own home page, and are paginated.
      * thanks to the sweet plugin from here: https://github.com/midnightSuyama/jekyll-paginate-category
2. Archives are dynamically generated.
3. Pages in their own folder: `_pages`.
4. Assets in their own folder
5. HTML5 boilerplate, Jquery, Bootstrap included. 


Note: Really hoping Octopress 3.0 will have category homepages and pagination included, b/c it looks awesome an would solve all my problems.
  * https://github.com/imathis/octopress




