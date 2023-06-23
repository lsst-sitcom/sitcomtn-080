:tocdepth: 1

.. sectnum::

.. Metadata such as the title, authors, and description are set in metadata.yaml

.. TODO: Delete the note below before merging new content to the main branch.

.. note::

   **This technote is a work-in-progress.**

Abstract
========

We have noticed larger than expected torques on the tma after balancing, as well as unusual torqe profiles. and are using this technote to capture the details of our investigation



This is connected with SITCOM-910


Introduction
============

After installing the M1M3 cell we have noticed a few issues.
First, even after balancing we are seeing larger than expected torques reqired to move the telesope (we would expect this to be close to 0).
Aditionally there is a hysteresis in the torque profiles (between upward and downward slews).
Finally, we are seeing elevation dependent behaviour in the torque profiles (amount required to slew, and a jump in torque at different elevations such as 3 deg) .



Noticed issues
--------------
- We calculated the elevation axis torque hysteresis
- constan


Tests
-----

- wiggle tests

   - offset plot torque proflies to see the step vs elevation
   -
- swagger test

   - Miranda is looking at fitting the profiles and getting slope/zeropoint as a funciton of elevation.

- excell speasdsheet from doug --> transfer to python and fit? see ticker
- With startrackers we could test the effect of this, could also look at elevation velocities (looks ok, but maybe a quantitative statement is good)


possible explantions
--------------------


- Elevation Brakes

   - Photos of wear on the elevation axis
   - Infrared Photos: what was the result
   - Today we are checking if the breaks are free (looks like one side drags)

- Hard point activation angle

   - We performed the hard stop investigation at low elevation at the start of the night. We found that there was no contact with the hardstops at 7, 3, and 0 degrees elevation.


- TMA Balance

   - Freddy says it is ballanced

- Cables in Elevation Wrap?

   -Freddy mentioned we will look more
- (anything else?)





Add content here
================

Add content here.
See the `reStructuredText Style Guide <https://developer.lsst.io/restructuredtext/style.html>`__ to learn how to create sections, links, images, tables, equations, and more.

.. Make in-text citations with: :cite:`bibkey`.
.. Uncomment to use citations
.. .. rubric:: References
..
.. .. bibliography:: local.bib lsstbib/books.bib lsstbib/lsst.bib lsstbib/lsst-dm.bib lsstbib/refs.bib lsstbib/refs_ads.bib
..    :style: lsst_aa
