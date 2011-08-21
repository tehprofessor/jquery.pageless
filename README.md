PageLess - endless page
=======================

Description
-----------

Pageless is a jQuery plugin.
As you scroll down you see more results coming back at you automatically.
It provides an automatic pagination in an accessible way : if javascript is disabled your standard pagination is supposed to work.

* This is identical to the original jquery.Pageless with the addition of a 'loadHidden' setting to prevent .pageless from being called on hidden elements

Parameters
----------

* `currentPage`: current page (params[:page])
* `distance`: distance to the end of page in px when ajax query is fired
* `loadHidden`: checks to see if element is visible before loading, default is false
* `loader`: selector of the loader div (ajax activity indicator)
* `loaderHtml`: html code of the div if loader not used
* `loaderImage`: image inside the loader
* `loaderMsg`: displayed ajax message
* `pagination`: selector of the paginator divs. (if javascript is disabled paginator is required)
* `params`: paramaters for the ajax query, you can pass auth_token here
* `totalPages`: total number of pages
* `url`: URL used to request more data
* `scrape`: A function to modify the incoming data. (Doesn't do anything by default)
* `complete`: A function to call when a new page has been loaded (optional)
* `end`: A function to call when the last page has been loaded (optional)

Requirements
------------

* [jQuery](http://download.jquery.com)

Demo
----

In the `example` directory you'll find a Rails app that just runs. It demonstrates the basic usage of pageless scrolling.

    $ script/server
    
Then just navigate to http://localhost:3000 and enjoy!

Usage
-----

    $('#results').pageless({ totalPages: 10
                           , url: '/articles/'
                           , loaderMsg: 'Loading more results'
                           });

Thanks to
---------

* http://codemonky.com/post/34940898
* http://www.unspace.ca/discover/pageless/
* http://famspam.com/facebox

Contributors
------------

* [Jean-Sébastien Ney](https://github.com/jney)
* [Alexander Lang](https://github.com/langalex)
* [Lukas Rieder](https://github.com/Overbryd)