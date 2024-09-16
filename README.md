# Asp.Net 8 – Multilingual Application with single Resx file

A practical guide to building a multi-language Asp.Net 8 MVC application.

***Abstract: A practical guide to building a multi-language Asp.Net 8 MVC application where all language resource strings are kept in a single shared file, as opposed to having separate resource files for each controller/view.*** 

## 1 The need for a newer tutorial
There are a number of tutorials on how to build a multi-language application Asp.Net Core 8 MVC, but many are outdated for older versions of .NET or are vague on how to resolve the problem of having all language resources strings in a single file. So, the plan is to provide practical instructions on how that can be done, accompanied by code samples and a proof-of-concept example application. 
### 1.1 Articles in this series
Articles in this series are:  
**•	ASP.NET 8 – Multilingual Application with single Resx file**  
https://www.codeproject.com/Articles/5378651/ASP-NET-8-Multilingual-Application-with-single-Res  
**•	ASP.NET 8 – Multilingual Application with single Resx file – Part 2 – Alternative Approach**  
https://www.codeproject.com/Articles/5378997/Asp-Net-8-Multilingual-Application-with-single-Res   
**•	ASP.NET 8 – Multilingual Application with single Resx file – Part 3 – Form Validation Strings**  
https://www.codeproject.com/Articles/5379125/Asp-Net-8-Multilingual-Application-with-single-Res   
**•	ASP.NET 8 – Multilingual Application with single Resx file – Part 4 – Resource Manager**  
http://www.codeproject.com/Articles/5379436/Asp-Net-8-Multilingual-Application-with-single-Res   


## 2 Multilingual sites, Globalization and Localization
I am not going to explain here what are benefits of having a site in multiple languages, and what are Localization and Globalization. You can read it in many places on the internet (see [4]). I am going to focus on how to practically build such a site in Asp.Net Core 8 MVC. If you are not sure what .resx files are, this may not be an article for you. 

## 3 Shared Resources approach
By default, Asp.Net Core 8 MVC technology envisions separate resource file .resx for each controller and the view. But most people do not like it, since most multilanguage strings are the same in different places in the application, we would like it to be all in the same place. Literature [1] calls that approach the “Shared Resources” approach. In order to implement it, we will create a marker class SharedResoureces.cs to group all the resources. Then in our application, we will invoke Dependency Injection (DI) for that particular class/type instead of a specific controller/view. That is a little trick mentioned in Microsoft documentation [1] that has been a source of confusion in StackOverflow articles [6]. We plan to demystify it here. While everything is explained in [1], what is needed are some practical examples, like the one we provide here. 



## 6 References
[1] https://learn.microsoft.com/en-us/aspnet/core/fundamentals/localization/make-content-localizable?view=aspnetcore-8.0  
Make an ASP.NET Core app's content localizable



