h1. How do I change the number of articles displayed? [todo]

Edit your *page template*, and change the @<txp:article />@ tag to include a @limit@ attribute, like this:

bq. @<txp:article limit=1 />@

or this:

bq. @<txp:article limit=10 />@

If no @limit@ is specified, the default is 5.

To link to the next and previous _pages_ from a _list_ page (i.e. on your front page, or a section page), use the "txp:older":http://textpattern.net/wiki/index.php?title=older and "txp:newer":http://textpattern.net/wiki/index.php?title=newer tags.

To link to the next and previous _article_ from an _article_ page, use the "txp:link_to_next":http://textpattern.net/wiki/index.php?title=link_to_next and "txp:link_to_prev":http://textpattern.net/wiki/index.php?title=link_to_prev tags.

You can do this with one chunk of code in your page template, as used in Textpattern's default template:

bq. @<txp:if_individual_article>@
@<txp:link_to_prev><txp:prev_title /></txp:link_to_prev>@
@<txp:link_to_next><txp:next_title /></txp:link_to_next>@
@</txp:if_individual_article>@
@<txp:if_article_list>@
@<txp:older>Previous</txp:older>@
@<txp:newer>Next</txp:newer>@
@</txp:if_article_list>@
