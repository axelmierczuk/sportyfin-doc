Requirements
============

Please review the requirements, especially when running Sportyfin with
Selenium scraping enabled.

-  ``python3``

   -  There are numerous guides online on how to set up ``python3`` with
      your machine.

-  ``pip``

   -  There are numerous guides online on how to set up ``pip`` with
      your machine.

-  ``Google Chrome version 97.x``

   -  Selenium needs to have an instance of Google Chrome version 97.x
      installed. This only applies if you chose to scrape with Selenium.

Selenium Usage with Sportyfin
-----------------------------

Using Selenium with Sportyfin *can* provide better stream results.
Selenium is used to look at network traffic on streaming sites in order
to find links that may have not been discovered otherwise. Bellow are
some things to note about using Selenium with Sportyfin:

Speed
~~~~~

Using Selenium will greatly reduce the speed at which Sportyfin is able
to find streaming links. This is because Sportyfin accesses the
streaming site for 1 second in order to gather network traffic.
Therefore, using Selenium can greatly reduce speeds if, for example,
Sportyfin finds 100 streaming sites.