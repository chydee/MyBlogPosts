## How to get your debug SHA-1 fingerprint certificate in Android Studio

Hello again,
I was working on a pet project over the weekend and was trying to connect the app to Firebase, so I got to a part where I needed to input my app's SHA-1 fingerprint certificate for debug mode. I found this easy way to do it and I'll be sharing that in this article.

### Let's get started already



- Open Android Studio and open your Project
- Click on Gradle (From Right Side Panel, you will see Gradle Bar)
- Click on Your Project (Your Project Name form List (root))

![sha1_your_project.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610314975396/0uKIDiluT.png)

- Click on Tasks and click on Android
Double Click on signingReport (You will get SHA1 and MD5 in Run Bar(Sometimes it will be in Gradle Console))
Select app module from module selection dropdown to run or debug your application

![Sha1_other_steps.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610314992294/5K6TXx5Xc.png)

Voila  👾 your app's SHA-1 fingerprint is sitting right there
![Sha1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610315001108/5F21PmEdJ.png)

if you have another easy way to do this kindly share in the comment section.
Happy coding  👨‍💻
