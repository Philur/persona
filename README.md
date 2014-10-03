persona
=======

How to define a persona

By default, this plugin doesn't ship with any particular persona, so you need to define one before you use. To define a new persona, place your files in the following directory structure:

$JENKINS_HOME
+- persona
   +- BruceLee
   |  +- persona.xml
   |  +- success.jpg/.png/.gif
   |  +- failure.jpg/.png/.gif
   |  +- other.jpg/.png/.gif
   |  +- icon.jpg/.png/.gif
   +- AnotherPersona
      +- ... same set of files ...

The image files can be of any image type. The 'success' file is used as a background image for successful builds, the 'failure' file for failed builds, and the 'other' file is used for all the other kinds of builds (such as unstable, aborted, etc.) The icon file should be 48x48, and is used as a small icon placed in front of a quote.

These files can be placed anywhere under $JENKINS_HOME/persona, so long as they are side by side to each other.

The format of the persona.xml file is as follows:

<persona id='djb' displayName='Daniel J. Bernstein'>
  <quote>Just because it's automatic doesn't mean it works.</quote>
  <quote>Be careful what you wish for you just might get it.</quote>
  <quote>I do engineering, not religion.</quote>
  <quote type="success">This is only for stable builds.</quote>
  <quote type="failure">This is only for unstable builds.</quote>
  <quote type="other">This is only for failed builds.</quote>  ...
</persona>

"type" : build status such as 'success', 'failure', 'other' (case insensitive).
