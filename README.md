# react-netlify-deployment

## Getting Started 

Before we begin, lets go into our app's folder and touch a file called `_redirects`. Like our .env and .gitignore it doesn't get a standard name, it simply is called "_redirects". Don't forget the underscore!

In your _redirects folder, which is a sibling to your index.html file, add in this line of code:
```
/* /index.html 200
```

This will set a redirect to your index.html file and allow your routes to load correctly if you send over anything besides the landing page.

Once we have this set, lets get started. Run "npm run build" in your root directory to create a new folder called "dist", which will give us all of the tools necessary to deploy the page.

Once our files are complete and pushed to git, create your own Netlify account. Signing up with Github is recommended for easy deployment, and is the method this guide is following. 
![Screen Shot 2022-11-07 at 2 28 49 PM](https://user-images.githubusercontent.com/100215009/200397628-f129e2eb-687d-4c9e-ba84-ca246aa4eb10.png)

After creating an account, there will be a few user questions. Follow through the prompts until you get to this page:
![Screen Shot 2022-11-04 at 1 02 13 PM](https://user-images.githubusercontent.com/100215009/200397901-8c06e05b-c2b7-43c3-933d-fd11d3468278.png)
Select import from an existing project

Your screen will look like the image below.
![Screen Shot 2022-11-07 at 2 32 12 PM](https://user-images.githubusercontent.com/100215009/200398269-0d43a93d-0111-41ba-8f1d-12d07e7209cd.png)
Now we want to connect to the Git provider, select Github

The following page will allow you to select any repos in your Github account. Search and select the repo you wish to deploy. 
![Screen Shot 2022-11-07 at 2 35 03 PM](https://user-images.githubusercontent.com/100215009/200398694-351d342b-39f4-4d44-8b84-b2a39a6ce189.png)

Now we want to give Netlify a few instructions when deploying your site. In the base directory section add the name of your react app, NOT your root directory/GitHub repo name. In the build command section include 'npm run build', and for your publish directory 'build'. 
![Screen Shot 2022-11-07 at 2 36 26 PM](https://user-images.githubusercontent.com/100215009/200419058-db45d9b3-0130-4cdc-a3d1-1f10387aaa69.png)
Now you can select deploy site. This will bring you to the following page:

In "Build and Deploy", change your "Build" command to be "CI= npm run build"
![cli-fix](https://i.stack.imgur.com/239it.png)

Then change your Environment Values to have a Key of "CI" and a value of "False"

![env-fix](https://i.stack.imgur.com/EHSqn.png)


![Screen Shot 2022-11-07 at 2 42 29 PM](https://user-images.githubusercontent.com/100215009/200400035-072d323f-a0e7-448f-9ebf-771e4ed22e84.png)
It may take a few minutes to a few hours for your react site to fully deploy, so be patient. Once your site is deployed you can edit the domain name and send the URL to friends and family! 





