## Hi there 👋

This is the README file for the entire Satco project codebase.  
Useful cross-project information can be shown here.

## Firebase
Saturn Web uses Firebase to trigger push notifications to alert users of certain actions:  
-Informs user that the work order that they have opened, has been changed by somebody else.

It takes some setup and configuration to get it running.  
1 - The project must be created in Google Firebase  
2 - A ".json" file must be generated with a private key (https://console.firebase.google.com/project/[**saturnsatcodevtest**]/settings/serviceaccounts/adminsdk) this file must then be added to our [Info Service](https://github.com/satco/info-service/blob/main/src/main/resources/firebase-service-account.json).  
3 - An "App" must be created (https://console.firebase.google.com/project/[**saturnsatcodevtest**]/settings/general) and the "firebaseConfig" must be added to Saturn Web in the [service worker (dev)](https://github.com/satco/saturn-frontend-angular/blob/master/src/assets-dev/firebase-messaging-sw.js) and the [project's globals file (dev)](https://github.com/satco/saturn-frontend-angular/blob/master/projects/saturn-lib/src/lib/global-dev.ts).  
4 - Lastly a Web Push certificate must also be generated (https://console.firebase.google.com/project/[**saturnsatcodevtest**]/settings/cloudmessaging) and added to the [firebaseVapidKey property of the project's globals file (dev)](https://github.com/satco/saturn-frontend-angular/blob/master/projects/saturn-lib/src/lib/global-dev.ts).  

## Postman
This project contains snapshots of Postman 'Data Dumps'.  
These can be exported/imported to be able to share Postman configurations with all the requests collections and environment/global variables.

## Deploying Java Projects
As of December 2023, all the Java projects run as a Service.  
To compile any project:  
1 - Inside the projects folder run './mvnw install -Dspring.profiles.active=*environment*', where environment will be *development*, *test*, or *production*.  
2 - This will generate a .jar file, that should be named appropriately and moved to the correct location. Example: *mv -f /home/jquintela/auth-service/target/auth-service-1.0.0.jar /var/www/auth-service.jar*  
3 - '/var/www' will have the '*project-name*.jar' and the 'run-*project-name*'.  
4 - After moving the file, we can restart the Service. Example: *sudo systemctl stop auth.service*, followed by *sudo systemctl start auth.service*.

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
