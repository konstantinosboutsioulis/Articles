![Boutsioulis_Konstantinos!](assets/image.png "Icon")

----
>  ## Title :  ... 
>  
>  Description :  ... 
----
<p>In today's article I will show you how ... </p>

<p>First we select ... </p>

![Boutsioulis_Konstantinos!](assets/1.png "Icon")


```
#Initialize Variables for the excecution
$Site = "https://mytenant.sharepoint.com/sites/Mysite"
$LevelName = "Blog Post"
#Open Connection with SharePoint Online
Connect-PnPOnline -Url $Site -UseWebLogin
 
#Delete Permission Level Using PnP 
Remove-PnPRoleDefinition -Identity $LevelName -Force
```


![Boutsioulis_Konstantinos!](assets/5.png "Icon")

<p></p>




