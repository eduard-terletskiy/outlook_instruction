https://portal.azure.com/#view/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/~/RegisteredApps

Click New registration

![plot](./img/1.png)

Fill fields

![plot](./img/2.png)

Click Register

![plot](./img/3.png)

Click Add a certificate or secret

![plot](./img/4.png)

New client secret

![plot](./img/5.png)

Fill fields

![plot](./img/6.png)

Click Add

![plot](./img/7.png)

Copy value

![plot](./img/8.png)

Select api permission

![plot](./img/9.png)

Add permissions->APIs my organization uses->Office 365 Exchange Online-> Application
permissions

![plot](./img/10.png)
![plot](./img/11.png)

Add permissions

![plot](./img/12.png)

Add permissions->Microsoft Graph->Delegated permissions

![plot](./img/13.png)

Create email account.
Enable:
https://admin.exchange.microsoft.com/#/mailboxes
Click on email - > Manage email apps settings


![plot](./img/14.png)

![plot](./img/15.png)

Register service principal
https://learn.microsoft.com/en-us/exchange/client-developer/legacy-protocols/how-to-authenticate-an-imap-pop-smtp-application-by-using-oauth#register-service-principals-in-exchange


Use

New-AzADServicePrincipal -ApplicationId <APPLICATION_ID>

instead


New-ServicePrincipal -AppId <APPLICATION_ID> -ServiceId <OBJECT_ID> [-Organization <ORGANIZATION_ID>]

Don't forget add Add-MailboxPermission for new email


New emails into existing app.


Enable https://admin.exchange.microsoft.com/#/mailboxes
Click on email - > Manage email apps settings
