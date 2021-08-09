---
title: Embedding Adaptive Forms/HTML5 forms in web page
description: Configuration steps needed to embed Adaptive Forms or HTML5 forms in a non AEM web page.
feature: Adaptive Forms
feature-set: Adaptive Forms
topics: development
audience: developer
doc-type: Tutorial
activity: implement
version: 6.4,6.5
topic: Administration
role: Admin
level: Beginner
kt: 8390
---

# Embedding Adaptive Form or HTML5 form in web page

The embedded adaptive form is fully functional and users can fill and submit the form without leaving the page. It helps the user remain in the context of other elements on the web page and simultaneously interact with the form.

The following video explains the steps needed to embed an Adaptive or HTML5 form in web page.
Please refer to the [documentation](https://experienceleague.adobe.com/docs/experience-manager-64/forms/adaptive-forms-basic-authoring/embed-adaptive-form-external-web-page.html?lang=en) for best prerequisites, best practices etc.
>[!VIDEO](https://video.tv.adobe.com/v/335893?quality=9&learn=on)

You can download the sample files used in the video [from here](assets/embedding-af-web-page.zip)

The following is the code used to fetch the adaptive form and embed the form in the container identified by the class name **right**

``` javascript
$(document).ready(function(){
  
	var formName = $( "#xfaform" ).val();
    $.get("http://localhost/content/dam/formsanddocuments/newslettersubscription/jcr:content?wcmmode=disabled", function(data, status){
	console.log(formName);
	$(".right").append(data);
      
    });
  
});


```













