jekyll-gravatar-filter
======================

Octopress and Jekyll Gravatar Filter

 Place this file in your plugins directory

Usage:
======
	{{ email@domain.com | gravatar }}

You may want to set up those settings in _config.yml:

    gravatar:
      default_image: mm
      size: 20
      rating: g
      secure: true
      force: y

Look at https://en.gravatar.com/site/implement/images/ to get know what values you can use

If you are in a need of having different settings for different contexts like pages or posts then you can add context:

    gravatar:
	    some_context:
		    size: 20
	        force: y
    	some_other_context:
        	size: 80
	        size: 40
        default_image: mm

And use it like that:
	{{ email | gravatar:'some_context' }}

Any argument missing in context are taken from default settings or, if none provided, are set to nil

Credits
========
Michał Ostrowski, <ostrowski.michal@gmail.com>

repo@github: https://github.com/espresse/jekyll_gravatar_filter

blog: http://espresse.net

License
=======

See LICENSE file