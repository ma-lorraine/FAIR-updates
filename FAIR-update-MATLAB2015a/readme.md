Minor updates to FAIR to make it work with MATLAB version 2015a
============================================================================

Files affected
--------------
* `2011-08-10-FAIR/viewer/FAIRfigure.m`
* `2011-08-10-FAIR/viewer/FAIRplots.m`
* `2011-08-10-FAIR/viewer/plotMLIterationHistory.m`

Why
---
* 2011-08-10-FAIR worked for MATLAB 2014a, but when my MATLAB was updated to 2015a, the codes listed above would run into errors because of graphics updates (not sure if updates have been in place since MATLAB 2014b).

<!--Do EITHER one of the following
------------------------------
* Copy and paste the 2 updated files here in the directory `updated-files` to FAIR's `viewer` directory, replacing your existing files, OR
* Apply the patches to the existing files in FAIR's `viewer` directory. Instructions below.-->


Patch instructions
------------------
* To patch (old to new):

        patch < FAIRfigure.patch
        patch < FAIRplots.patch
        patch < plotMLIterationHistory.patch

* To undo the patch (new to old):

        patch -R < FAIRfigure.patch
        patch -R < FAIRplots.patch
        patch -R < plotMLIterationHistory.m

--------------------------------------------------------------------------------
FYI.  The patches were generated with the commands below.
(FAIRfigure.m and FAIRplots.m below are the 2014a version)

        diff -u FAIRfigure.m FAIRfigure_2015a.m > FAIRfigure.patch
        diff -u FAIRplots.m FAIRplots_2015a.m > FAIRplots.patch
        diff -u plotMLIterationHistory.m plotMLIterationHistory_2015a.m > plotMLIterationHistory.patch


---
Lorraine Ma  
July 2016