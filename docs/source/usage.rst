Usage
=====

.. _installation:

Installation
------------

To install Sportyfin, you must have ``python3`` and ``pip`` installed on
your machine. Please see :doc:`requirements` for more details.

Installation is as follows:

.. code:: console

   pip install sportyfin --no-binary=sportyfin

More documentation will be added when Docker is supported.

Finding Streams
----------------

Run Sportyfin using ``python3 -m sportyfin``, followed by the arguments
(please see :ref:`arguments`).

Below are some example uses:

.. code:: console

   # Run Sportyfin on all leagues supported.
   python3 -m sportyfin -a

.. code:: console

   # Run Sportyfin on NBA and NFL
   python3 -m sportyfin -nba -nfl

.. code:: console

   # Run Sportyfin on all leagues supported and in silent mode.
   python3 -m sportyfin -a -vv

.. code:: console

   # Run Sportyfin on English football leagues, in verbose more, with the output to Desktop.
   python3 -m sportyfin -ef -v -o "~/Desktop"

.. code:: console

   # Run Sportyfin on all leagues supported, and refresh every 60 minutes.
   python3 -m sportyfin -a -t 60
   
Once you have run the program, make sure to link to the .m3u's in the Jellyfin dashboard:

``Dashboard > Live TV > Tuner Devices (+) > Tuner Type (M3U Tuner) > File or URL (enter path)``

Once the path has been defined, you can check out your streams under:

``Home > Live TV > Channels (at the top)``

Arguments
------------
-  ``-a`` - Find streams for all leagues supported by Sportyfin.
-  ``-nba`` - Find streams for NBA matches.
-  ``-nhl`` - Find streams for NHL matches.
-  ``-nfl`` - Find streams for NFL matches.
-  ``-ef`` - Find streams for English football matches (Premier League,
   EFL, FA Cup…).
-  ``-v`` - Enables verbose mode.
-  ``-vv`` - Enables silent mode (no output).
-  ``-s`` - Enables Sportyfin to scrape for streams using Selenium.
   Please see :doc:`requirements` associated with this.
-  ``-t`` - Specify how often to scrape in minutes (default 30 mins).
-  ``-o`` - Specify the output directory. Sportyfin will create an ``output`` folder there and store meta-data, m3u/xml files.
