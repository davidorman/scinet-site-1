This guides assumes you already have an active scinet account and a LincPass card.

SCINet provides a cafe machine at many locations that is directly connected to the scinet network to racilitate file transers and other activities that benefit from more direct interaction with the SCINet network.

Access to the cafe machines is controlled with your lincpass card.  

To prepare your account to be able to work with the cafe machiens you will need to  upload the certificate from your lincpass into scinet.

To do this first start to login to ssh or OOD as you usually would.

When you get to eAuth and select PIV/CAC instead of clicking the OK button click the "Certificate information button

Then in the Certificate winodw that comes up go to the details tab

Click on the "Copy to File" button near the OK button.

This will bring up the "Cerfiticate Export Wizard"  click Next

Choose Base-64 encoded X509 (.CER)
Choose a location for the  file somewhere you will be able to find it for the next steps. name it mycert.cer, click Save, then Next, then Finish.
You should get a box stating "The export was sucessful."

click ok to close the wizard.   Your login had surely timed out out by now so close your browser and restart your login.

Now use whatever your favorite method of files to ceres is to move the certificate file to ceres. We'll assume its called mycert.cer.
scp mycert.crt first.last@ceres.scinet.usda.gov:~ 
will work fine among many aother methods.

Now login to ceres or atlas via ssh or OOD terminal.

Save your cert as your username.crt in your home directory.
A system process will pickup the file and add it to your authentication profile.  This happens once an hour at 15 minutes past the hour.

The file will be deleted when the process is finished.  If you wish to keep a copy save another copy with a different name.

