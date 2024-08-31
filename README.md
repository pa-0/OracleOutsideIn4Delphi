# Oracle Outside In Technology
  
http://www.oracle.com/technetwork/middleware/content-management/overview/index.html
http://www.oracle.com/technetwork/middleware/content-management/viewer-096532.html

## Overview

### The archive contains

* header files from the SDK ported to Delphi (from the vw-8-3-5-win-x86-32.zip archive)
* a wrapper component for viewing files in Delphi programs.

### Support sites:

  http://innenashev.narod.ru/
  http://www.sql.ru/forum/actualthread.aspx?tid=826134

### Terms of use:

Just let me know what you tried to use and what came out of it, regardless of whether it was successful or not. I also look forward to constructive criticism and pieces of code written by you that should be included in the component. For now - I think it would be appropriate for me to wait for feedback via the sql.ru forum

### Features of use:

* The project settings indicate that DCU files should be placed in the `C:\Output\DCU` folder this is more convenient for me, I think you will also like this idea, so as not to clutter the source folder beyond what is necessary.
* The stream from which the viewer loads the file must remain available during the entire viewing time. Because the viewer loads pages from there gradually, in several stages, according to a timer. Especially if the file is large. To do this, you may have to copy your data to `TMemoryStream`.
* demo.exe from the demo example is compiled into `C:\output`, and expects to find a folder `Plugins\OracleOutsideInTechnology\` next to it, which will contain the contents of the redist folder from the archive vw-8-3-5-win-x86-32.zip, downloaded from the Oracle site from the Viewer Technology 8.3.5 section from the page:
  http://www.oracle.com/technetwork/middleware/content-management/downloads/oit-dl-otn-097435.html
* It seems that Oracle's only requirement for using the library is to include the following lines in the help, documentation, or "About" window of its programs:
    ```
    Outside In Viewer © 1991, 2010 Oracle.
    The software is based in part on the work of the Independent JPEG Group.
    ```
    
### What else needs to be done:

1. #### Basically, I don't need anything else for now - this component already shows files from the stream quite well. However, it would be nice to do the rest, and I will do it in my free time from my main work. The more people want to receive updates - the more interesting it will be for me to switch to this.

2. #### By the way, I will be happy to integrate your additions and developments into this component, if you are too lazy to wait and you make them yourself and send them to me.

3. #### And it seems to me that the following would be good to finish:

    * Wrap methods and virtual procedures all messages that can be sent to the viewer and received from it.
    * Wrap all parameters (options) of settings that the viewer allows to configure in properties.
    * Make it possible to refuse to save files to disk, which, when viewing archives by double-clicking, are currently unpacked into a temporary folder and offered for viewing. So that no trace of the viewed information gets to the disk, for its greater protection.
    * By the way, figure out why, although they are saved to the folder, they are not shown in the new viewer window.
    * Make it possible to open such a file on the same component panel,
    with the display of the "back" button to return to viewing the archive.
    * Translate the viewer interface into Russian and switch to it.

    #### Or get a ready-made library of Russian string resources with the name sccloru.dll, fortunately, Google says that such a thing exists somewhere.

## History of package versions:

### 08.02.2011
* Improved to a working viewer.
* Slightly rethought the archive structure.
* Started this readme.txt

### 04.02.2011
* Ported headers using
  h2pas Free Pascal utility
  h2pas wisard dialog in the Lsarus project
* Published a draft version of the component
on the site http://innenashev.narod.ru/
and on the forum sql.ru

This is remembering how great it was to find modules for working with OpenOffice in the topic http://www.sql.ru/forum/actualthread.aspx?tid=405083
