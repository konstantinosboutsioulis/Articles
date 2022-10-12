----
>  ## Title :  Create Permission Level For SharePoint Online Via Front End And Delete It Using PowerShell 
>  
>  Description :  We will create a permission level in SharePoint Online and we will delete this permission level using PowerShell 
----

<p>In today's article I will show you how we can create custom permission level in sharepoint online and then using PowerShell to delete it</p>

<p>First we select the site collection we want to create our new permission level</p>

<p>From the site settings we select advanced permission settings and then permission level</p>

![Boutsioulis_Konstantinos!](/assets/1.png "Icon")

<p>Then select add a permission level</p>

![Boutsioulis_Konstantinos!](/assets/2.png "Icon")

<p>Enter name and select properties for my new permission level</p>


![Boutsioulis_Konstantinos!](/assets/3.png "Icon")


<p>and as you can see my new Permission level has been created</p>

<p>Now I can apply the permission level to the user or group of my choice</p>

<p>In case I wish to delete the permission level I can do it either from front end by selecting the Permission level and then clicking deleted selected permission level</p>
![Boutsioulis_Konstantinos!](/assets/4.png "Icon")
<p>or via PowerShell . I run the following PowerShell and from SharePoint Shell with admin rights and I have</p>
```
{
  #Αρχικοποίηση Παραμέτρων
$Site = "https://mytenant.sharepoint.com/sites/Mysite"
$LevelName = "Blog Post"

#Σύνδεση με SharePoint Online
Connect-PnPOnline -Url $Site -UseWebLogin
 
#Διαγραφή Permission Level 
Remove-PnPRoleDefinition -Identity $LevelName -Force
}
```


![Boutsioulis_Konstantinos!](/assets/5.png "Icon")

<p></p>



