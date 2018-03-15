
Dialog Designer v1.5

This readme echos the "Introduction" and "Installation and Activation" sections of the main documentaion found in "Dialog Designer v1-5.doc" (Word 2003 document).  That document will be your main resource when learning how to use this application.


Introduction
--------------------------------------------------------------

Welcome to the Dialog Designer.  This has been a pet project of mine about a year. With it you should be able to create the essential Magik source code for simple or complex GUIs in a matter of minutes, rather than hours.  This tool allows you to create and manipulate the key portions of a GUI without writing any Magik or XML.  The idea is to develop the GUI quickly to the stage where the GUI activates and the internal behavior can be developed – the really interesting part of GUI creation in my opinion.

The Dialog Designer can generate an entire module for the dialog design, complete with XML, message and Magik files.  Reverse engineering of existing dialogs so they can be manipulated is not supported.  You may, however, save a design you have created to XML and later reload it.  This allows the creation of standard dialog XML files that can be used as the basis for future development.

I have implemented the most common Magik GUI widgets, but there are many less common widgets that a developer may desire.  For these, I would suggest inserting a common widget into the dialog design for layout purposes and once the Magik GUI code is finalized, update the code with the desired widget.  In addition, I have added a few ‘custom’ widgets that address common programming tasks like opening a file-selection or directory-selection dialog, selecting styles, dates and inserting an action from another plugin.

This application was developed against SW4.1 (SWAF) and SW4.0 (SWAF) images and relies on some classes specific to SWAF images. 


Whether you use this tool to create GUIs or just to learn the syntax, I hope you find the tool useful and fun, as I do.

Cheers,

Graham Garlick
graham@ifactorconsulting.com

Jan 2008







Installation and Activation
--------------------------------------------------------------

The Dialog Designer is written entirely using Magik and XML.  You will need a SW4 or SW4.1 image based on the core 'swaf.msf' base image.

Put the dialog_designer module somewhere logical.  I have included a product.def file if you want to keep it separated from other code.  

You can start Dialog Designer directly from the Magik prompt once the module is loaded:

MagikSF> dialog_designer.open()

This will open a new, non-cached instance of the dialog designer. 


If you want to launch the Dialog Designer from a button within an existing application then add these lines to your application config.xml and gui.xml respectively.

<plugin name=”dialog_designer_plugin” class_name=”dialog_designer_plugin”/>

<action name=”dialog_designer_plugin.activate_dialog”/>



