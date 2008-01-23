To import this stuff in your system with saplink, you should start importing the nuggett file NUGG_ZSE16_URB.nugg,
which contains everything, activate its content, and then the slinkee WDYA_ZSE16_URB.slnk.
The latter file only contains the webdynpro application: saplink dumps if you try to install both the webdynpro component and 
the application from the same nugget.
On my system I had some trouble importing the webdynpro application: it only works if I already have a ZSE16_URB application to overwrite.
I hope you won't have this problem, however creating the application is a trivial task, as you can see from my SDN weblog.

NOTE: saplink doesn't handle tetx symbols for classes; as a result you might experience short dumps when the application tries todisplay an error message.
To fix that you should add those texts manually (transaction se24, class ZCL_SE16_URB_ASSIST,goto/text symbols):

E01	Context mapping error
E02	Table decoding error
E03	Select-options generation error
E04	Data selection error


This package's home is at http://code.google.com/p/urbani-saplink/
You can find saplink, the required webdynpro plugins and their documentation at http://code.google.com/p/saplink/

Disclaimer:
This software is distributed WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

Marcello Urbani
