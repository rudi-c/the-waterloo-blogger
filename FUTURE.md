# Future plans

Let me know if you are interested in working on one of these. I think they can be accessible and very useful side projects.

## Blog feed

It would be nice to scrape the websites on the list and create a feed that people can subscribe to.

Challenges:
- Not all blogs have an RSS feed (todo: write instructions on how to setup one)
- May need a way to parse arbitrary web pages (find an open-source tool?)

On the other hand, half the entries are from Medium so it's fine if we don't have data for all blogs.

Notes on scraping: apparently using a browser like Selenium tends to give better results? See https://lord.io/blog/2015/elixir-scraping/

## Automatic integration

We could setup automatic integration on PRs to make sure everyone follows the same formatting when adding blog posts. This could probably be implemented as a single regex (and maybe a few lines of code to deal with section headers).

## Web interface

It would be nice to have a website where you can filter by activity, tags, etc.

I didn't build it initially as a website to avoid dependencies on a single (or small set of) maintainers, the text approach is fine to start. We could make the website a view of the Github repo itself (make it update itself when there's a new commit). This avoids dealing with databases and stateful things. People have done this before and apparently it works well. An example would be pyvideo.org where the data is located at https://github.com/pyvideo/data and the website source code is located at https://github.com/pyvideo/pyvideo. Search could be (not) implemented via Algolia (https://blog.algolia.com/instant-search-blog-documentation-jekyll-plugin/).

The web interface could have a way of searching by blog and by post (which is probably more useful). We could also highlight 2-3 posts per blog to make the list more useful. This could be done via upvotes or some sort of recommendation system.

Prior work to look into that could be useful for semantic parsing of pages: Mercury by Postlight, Mobile Safari's readability feature
