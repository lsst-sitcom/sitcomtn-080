:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

.. TODO: Delete the note below before merging new content to the main branch.

.. note::

   **This technote is a work-in-progress.**

Abstract
========

This technote is linked with the SITCOM-910 jira ticket

After inital balancing of the TMA we have noticed larger than expected torques, as well as unusual torqe profiles. This behaviour was likely caused by the asymetric distribution of magnets in the elevation drive. For slews lower than 3.5 degrees not all drives were able to fully function. Rebalancing excluding elevations below 5 deg resulted in more well behaved torque profiles. We also present torque profiles for purely azimuth slews.






Introduction
============

After installing the M1M3 cell we have noticed a few issues.
First, even after balancing we are seeing larger than expected torques reqired to move the telesope (we would expect this to be close to 0). (is this still true?)
Aditionally there is a hysteresis in the torque profiles (between upward and downward slews).
Finally, we are seeing elevation dependent behaviour in the torque profiles (amount required to slew, and a jump in torque at different elevations such as 3 deg) .

Behaviour post inital balancing
===============================

Inital balancing efforts left some interesting features in torque profiles during a slew.
Figure 1, below, shows an upward and downward 90 degree slew from June, 27, 2023.
Most notably, there is large jump in torque required at 3.5 deg, as well as a large hysteresis and change in required torque as function of elevation for all elevations, not just 3.5 deg.

.. image:: ./_static/elevation_slews_before_balancing_20230627.png

**Figure 1. :** Here we show the torque required as a function of elevation for 90 degree slews upward (downward) in green (purple). For each slew the shaded area shows the raw measurements from the efd, and the line shows a rolling mean. A jump in the torque required can be seen at 3.5 degrees, and the rest of the torque profile is not symetric around the torque = 0 Nm line.
.. chage name to before final balancing.

Investigation of possible casuses
=================================

A of possible causes for this behaviour were considered.
These included the elevation breaks, elevation axis hard points, TMA ballance, cooling cables, and finally the *elevation drives themsselves*.

Elevation Axis Motors
---------------------

After some investigation.

.. image:: ./_static/magnet_drive_zenith.png

.. image:: ./_static/magnet_drive_horizon.png

.. image:: ./_static/magnet_drive_horizon_2.png


Other possible causes
---------------------

Elevation breaks
^^^^^^^^^^^^^^^^

We checked for possible contact of the elevation brakes and the TMA during slews causing a dragging effect.
This was done in a few different ways.
First, by looking at the wear patterns between the break pads and the elvation axis a different elevations, there seemed to be some variance in the wear but nothing obvious.
Then, we took infrared images of the TMA during slews no hot points were detected.
Finally, we measured the distance betewwn the break pads and the TMA at multiple elvations while the breaks were released finding at no points did the breaks make contact with the axis duing a slew.

*Include photo of breaks, and wear patterns*

Elevation Axis Hard Stops
^^^^^^^^^^^^^^^^^^^^^^^^^^
We also slewed the telescope to elevations of 7,3 and 0 deg and visually checked wether the hard stops were engaged in a way that could possibly explain the behaviour at 3.5 deg.
It was found this was not possible and **notably** it looked like the hard stops would engage at a negative **after** the TMA would have encountered portions of the dome floor.

TMA Balance iterations
^^^^^^^^^^^^^^^^^^^^^^

Other systems on the TMA that could cause drag during slews
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- excell speasdsheet from doug --> transfer to python and fit? see ticker
- With startrackers we could test the effect of this, could also look at elevation velocities (looks ok, but maybe a quantitative statement is good)


Updated Torque profiles
=======================

Results for elevation
---------------------
.. image:: ./_static/elevation_slews_after_balancing_20230630.png


Comparison with previous profiles
---------------------------------
.. image:: ./_static/elevation_slews_comparison_20230630.png

Azimuth slews
-------------

.. image:: ./_static/azimuth_slews_20230630.png


.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
..
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
