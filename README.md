# Project-2-Transiting-Planetary-Systems

Project 2: Time-Series Imaging of a Transiting Planet with the McDonald 30"

In this project, you will remotely operate the 30” telescope at McDonald Observatory to obtain many images of a known transiting planet host star, spanning the full duration of a transit (and at least some time before and after). You will choose which planet host to observe, and on which night, so as to be sure to catch a transit given the known timing. The telescope will be equipped with the SDSS (Sloan Digital Sky Survey) filters ugri, plus a narrowband filter centered on the Halpha spectral line (Balmer series, n=3-2 transition). For the purposes of this assignment, one of the broadband filters is probably most important. Consider important drivers like sky brightness (including the Moon's contribution) as well as the brightness and color of your target. Your goal is to monitoring the brightness of the star over time, calibrated for any changes in atmospheric conditions by measuring differential magnitudes compared to other nearby stars, and to determine the observational parameters (duration and depth of transit) and the corresponding planetary parameters (radius, impact parameter of orbit).  Make sure to convert all of your fluxes to instrumental magnitudes (-2.5*log flux) before doing the analysis.

All coding should take place in a single Jupyter notebook, which you will submit via GitHub following instructions below. We will follow the same rubric for the final report as in Project 1, where there will not be an Introduction or Conclusions, but all other parts will be included. The report will be due at 5:00 PM on Tuesday 3/31. This document will walk you through the steps you will take to perform this project in the order in which you should perform them.

GitHub Link: https://classroom.github.com/a/lpiDwUf8

1)  Create an observing plan for the time at the telescope. Outline each task (including startup and shutdown), decide how many of each type of file you will need, and estimate how long it will require to obtain all of these observations. Choose an open block of time and schedule your team in the Google Doc, requesting the number of hours on the telescope that you think will be needed. Be sure to allow a suitable amount of time for focusing, getting on the star before the transit starts, and staying on it until after the transit ends. Also, consider if a subarray might help you overcome the very long readout times, which otherwise will totally dominate the amount of time you spend observing. A draft of this observing plan will be due (via email to both instructors and Jackie - one per group) by Thursday 3/12 at 5pm, which the instructors will comment on, and then they will synthesize the feedback into a set of common lessons in an announcement back to the class. This should be written in such a way as to become Section 2 (Observations) in the report.


2)  Remotely operate the telescope and obtain the observations you planned for in #1. Note for the purposes of this class, all remote observing should be done from the computer lab in PMA 15.201. Each observation should be described using a standard Observing Log template, including notes about relevant events that occurred during the observations (i.e., clouds, software crashes, a mountain lion just walked in front of the telescope and blocked the target). Afterward, briefly add notes to your draft observing plan that reflect on how the implementation differed from the plan, and what lessons were learned which you will apply to future observing runs. You must attend an observing run! For proof of this, while observing, take a selfie of your entire group together, and turn it in along with the Jupyter notebook. If you cannot attend with your group, you may attend with another group. If circumstances prevent you from attending, talk to the instructors well in advance of the due date.


3)  In the computer lab, process the images in Python. While you won't need to observe calibrations like in Project 0 (observatory staff will take those), you will still need to apply those calibrations to your science observations.


4)  Analyze the data in Python. This will involve figuring out how the pixel positions translate to on-sky positions (which can be done using the Astrometry.net website, as in Project 1), and then measuring aperture photometry for the transiting planet host and for several other stars of similar brightness and color. Note that for our purposes, we don't necessarily need to care about photometric calibration onto a standard system. You're measuring "differential photometry", or how the difference between your science target and the comparison stars varies over time. (For our purposes, don't worry so much about color or airmass terms, but it would be great if your comparison stars are similar in color to the planet host star.)


5)  Plot the brightness of the planet host star over time, normalized so that the flux (not necessarily magnitudes!) outside of transit is 1 and then the individual measurements reflect the fractional flux above/below that amount (i.e., 0.99, 0.97, or 1.01). Measure the depth and duration of the transit.


6)  Using the measurements, estimate the radius of the planet and the impact parameter (i.e., how far off the equator the planet is crossing the disk of the star).


7)  Submit the final version of your code via Github. The code should be well commented so that the instructors can understand your coding process.


8)  Submit your report via Canvas, uploading as a single PDF.


