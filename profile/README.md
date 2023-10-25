## Hi there 👋

This is the README file for the entire Satco project codebase.  
Useful cross-project information can be shown here.

# Firebase
Saturn Web uses Firebase to trigger push notifications to alert users of certain actions:
-Informs user that the work order that they have opened, has been changed by somebody else.

It takes some setup and configuration to get it running.  
1 - The project must be created in Google Firebase  
2 - A ".json" file with must be generated with a private key (https://console.firebase.google.com/project/[**saturnsatcodevtest**]/settings/serviceaccounts/adminsdk) this file must then be added to our [Info Service](https://github.com/satco/info-service/blob/main/src/main/resources/firebase-service-account.json).  
3 - An "App" [must be created](https://console.firebase.google.com/project/saturnsatcodevtest/settings/general) and the "firebaseConfig" must be added to Saturn Web [here (dev)](https://github.com/satco/saturn-frontend-angular/blob/master/src/assets-dev/firebase-messaging-sw.js) and [here (dev)](https://github.com/satco/saturn-frontend-angular/blob/staging/projects/saturn-lib/src/lib/global-dev.ts).  


<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
