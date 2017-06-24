# Future plans

## Blog feed

It would be nice to scrape the websites on the list and create a feed that people can subscribe to.

Challenges:
- Not all blogs have a RSS feed
- May need a way to parse arbitrary web pages

## Automatic integration

We could setup automatic integration on PRs to make sure everyone follows the same formatting when adding blog posts. This could probably be implemented as a single regex (and maybe a few lines of code to deal with section headers).

## Web interface

It would be nice to have a website where you can filter by activity, tags, etc.

I didn't build it initially as a website to avoid dependencies on a single (or small set of) maintainers, the text approach is fine to start. We could make the website a view of the Github repo itself (make it update itself when there's a new commit). This avoids dealing with databases and stateful things.
