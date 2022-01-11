Usage
=====

.. _installation:

Installation
------------

Pip
*****

To install Sportyfin with pip, follow the steps bellow:


.. code:: console

   pip install sportyfin --no-binary=sportyfin


Docker
*******

To install Sportyfin with Docker, follow the steps bellow:


.. code:: console

   git clone <repo>
   cd sportyfin
   docker build --tag sportyfin .
   docker run -v <Path Where You Want Output>:/sportyfin/output sportyfin 
   # For example: docker run -v ~/Desktop:/sportyfin/output sportyfin 


Or you may pull the container with the following:


.. code:: console

   docker pull sportyfin/sportyfin:latest 
   docker run -v <Path Where You Want Output>:/sportyfin/output sportyfin/sportyfin:latest


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

.. image:: https://i.ibb.co/7Vxvqkp/Screen-Shot-2022-01-11-at-10-47-26-AM.png
.. image:: https://i.ibb.co/VH6b0Hc/Screen-Shot-2022-01-11-at-10-47-42-AM.png

Additionally, make sure to change the "Refresh Guide" setting under:

``Dashboard > Scheduled Tasks > Live TV > Refresh Guide > Task Triggers``

.. image:: https://i.ibb.co/q7mhTMt/Screen-Shot-2022-01-11-at-10-58-57-AM.png
.. image:: https://i.ibb.co/JxcdXC3/Screen-Shot-2022-01-11-at-10-59-11-AM.png

Once the path has been defined, you can check out your streams under:

``Home > Live TV > Channels (at the top)``

.. image:: https://i.ibb.co/yS5ycS6/Screen-Shot-2022-01-11-at-11-08-08-AM.png

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
