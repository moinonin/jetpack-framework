# ![](http://imgur.com/kqwYh3Pl.png) __GETTING STARTED__ ![](http://imgur.com/rRGC6N8l.png)
## __Why She-Bang?__
She-Bang is a foundational framework leveraging all bash shell and Unix capabilities to give you a state-of-the-art static site generator, and API endpoint fetcher. Here we are referring to portability of bash, richness in regular expression (regex) libraries, accessibility to the filing systems, and the light-weightness of bash shell. The application uses heredocuments to create script templates for you to start out with. All these enables She-Bang to come up with two main purposes that most modern developers are intrigued about:
### __Static Site Generation__  
Sometimes you just want to create a site with no serverside embedded data. For instance documentation website, landing pages, portoflios, and what have you. These are the kind of tasks that shouldn't waste any of your money, as we know time = money :). She-Bang will harness its magic to create a site for you, literally within seconds.  
### __API data fetcher__
The second utility She-Bang comes with is the ability to fetch data from API endpoints. Our tool comes with a DEMO page named "apifetch-demo", which enables getting of data from any API url, or locally available *.json file. It's real-time capability is enable by an infinite loop that is used to read the information from the server, write them to an html file, and discard after a set loop (sleep) time. Upon expiry of the sleep time, the file is deleted and a fresh one is created with newer information. Users should be aware of the rate at which information is fetched from the server, set sleep time with a variable "delay" under the scripts directory 1-5 seconds was used for the trials and worked best for that specific API endpoint provided by the European Central Bank (ECB). In you case however, check with the server administrator to agree on the delay time. This is IMPORTANT! as when delay is set too short, the application will force the server to throttle the rate in which data is distributed to your local machine.
## __Requirements__  
She-bang framework is currently available only for 64 bit linux users. Depending on the interest, the team behind it will soon role out other versions. In addition, the package uses node package management, and thus you need nodejs installed (and thererefore npm).  
## __Installation__
Upon clonning the application from our [github repository](https://github.com/moinonin/shebang-framework) and open your favorite terminal application, navigate to the source directory (where it is downloaded to) and install it by running the following commands:
```
$ sudo apt-get install ./shebang_1.01-1_amd64.deb
```
Don't worry about the location of installed files, it is automatically set to go to usr/bin where all other applications are installed. While installing and once it is installed, you should see an output like this:  
==== start ===================  
Reading package lists... Done
Building dependency tree       
Reading state information... Done
Note, selecting 'shebang' instead of './shebang_1.01-1_amd64.deb'
The following NEW packages will be installed:
  shebang
0 upgraded, 1 newly installed, 0 to remove and 1 not upgraded.
After this operation, 272 kB of additional disk space will be used.
Get:1 /home/rotich/Desktop/portfolio/projects/shell/bash/packaged/she-bang/shebang_1.01-1_amd64.deb shebang amd64 1.01-1 [30.8 kB]
Selecting previously unselected package shebang.
(Reading database ... 269205 files and directories currently installed.)
Preparing to unpack .../shebang_1.01-1_amd64.deb ...
Unpacking shebang (1.01-1) ...
Processing triggers for menu (2.1.47+b1) ...
Setting up shebang (1.01-1) ...
Processing triggers for menu (2.1.47+b1) ...  
================== end =========  
## __She-bang Usage__  
Navigate to the area of your projects, say desktop,  create a directory you would like to use for your projects say you want to call it "my-project", you will then do this:
```
$ mkdir my-project
```
Change directory to the project as follows:
```
$ cd my-project
```
Next, run the following command:
```
$ shebang
```
Our dedicated command line interface (CLI) will begin a dialog immediately, and you will just need to follow the directions on the  CLI.
```
$ Enter project name (shebang ?): 
```
Enter the project folder you wish to create - (if you are lazy like me, press enter with no input) the default is the preceeding directory -- in that case "my-project". However, let's keep things in order and call the actual application "my-website":
```
$ Enter application entry point (default 'app.sh'?): 
```
Enter the application name, the default one is "app.sh" if you don't enter anything. However, I choose to call my main application script "index.sh", the following text will follow if all goes well.  
#=================== start ====================================#  
===== wait as we prepare your bang project =========  
Cloning into './my-website/public/shared/img'...  
remote: Counting objects: 37, done.  
remote: Compressing objects: 100% (37/37), done.  
remote: Total 37 (delta 11), reused 0 (delta 0)  
Unpacking objects: 100% (37/37), done.  
===== ... writing application directories ===========  
all set! cd to (my-website) and see if it worked  
Ensure all dependencies are installed.  
Run the command *npm run install* for the dependencies.  
Initiate the project by running *npm run rot*.  
#===================end ======================================#  
Do as the application says: navigate to the project directory you just created. Install the dependencies by doing the following:
```
$ cd my-website
```
```
$ sudo npm install  
``` 
```
$ npm run rot 
```
This is the magic command, it creates the routes, template scripts, and even create our own first page (index.html) to direct you to our documentation and guides. On running above command, you will be prompted to enter navigation bar items:
```
$ Enter navbar items (#word.html separated by spaces):
```
For the purposes of this example, to create two routes, I will enter "quick brown-fox.html". Note, you can choose to add file extensions to the words or live them the way they are as you can see, I left "quick" without extension, but added .html to "brown-fox". The next step is to spin the development server by running:
```
$ npm run dev 
```
This is your usual command used to trigger the localhost server. By default, She-Bang uses port 8080. If you get a server error, make sure to install "http-server" by typing.   
```
$ npm install -g http-server
```
You should see the following output.  
#=================== start ====================================#  
> she-bang@1.0.0 dev /home/rotich/Desktop/shebang/my-website
> npm run serve & npm run app

> she-bang@1.0.0 serve /home/rotich/Desktop/shebang/my-website
> http-server

> she-bang@1.0.0 app /home/rotich/Desktop/shebang/my-website
> ./index.sh

Starting up http-server, serving ./public
Available on:
  http://127.0.0.1:8080
  http://192.168.1.101:8080
Hit CTRL-C to stop the server  
#===================end ======================================#  
Navigate to your favorite browser and type:
``` http://localhost:8080 ```
or:
``` http://127.0.0.1:8080 ```
After this you are ready to carry on the development. You should see She-Bang home page below: ![](http://imgur.com/XFaIAc4l.png)
Familiarize yourself with the project directories created and where necessary consult this guide.
## __She-Bang files & directories__
In the next sections we will explain more about the files and directories She-Bang needs in order to run flawlessly. There are a total of seven directories (including the top one hosting the website -- named here "my-project"), and 18 files created by She-Bang. See the following file and directories tree:
```
├── index.sh
├── package.json
├── public
│   ├── apifetch-demo.html
│   ├── brown-fox.html
│   ├── index.html
│   ├── quick.html
│   └── shared
│       ├── bootstrap.css
│       ├── img
│       │   ├── inzpiro.png
│       │   └── logo.png
│       ├── index.css
│       └── main.css
├── scripts
│   ├── gen.sh
│   ├── home.sh
│   └── navgen.sh
├── templates
│   ├── footer.sh
│   ├── headtags.sh
│   └── nav.sh
└── variables
    └── global.sh
6 directories, 18 files
```
## __Directories__
### __public__
This is the directory hosting html files, or routes and assets such as cascaded style sheets (css) and image files. 
### __shared__
This directory contains the assets, images and css, and the folder is itself hosted under the public directory.
### __img__
The folder contains our logo, and those of our official sponsor [inzpiro gaming](https://inzpirogaming.com/). You will be able to leverage and utilize this directory to your liking, provided that your route files will be able to get access to the assets referenced.  
### __scripts__
As the directory name suggests, it contains unix shell scripts that are run through node package manager for She-Bang to work efficiently. The use of bash in itself is the novelty behind she-bang, as they are fast in execution, and are portable, meaning they can be run on either linux or windows, or mac OS platforms. Windows 10 particularly these days support linux-like environment where She-Bang can be executed. We have not tested this service though, but we hope to get it going soon. In summary, "navgen.sh" generates the navigation bar items and converts them into a variable "nav0", which is then rendered in the html files where the navigation bar list items should appear. The homepage aka index.html is actually created and rendered by the script "home.sh", and through looping, the script "gen.sh" writes all the rest of the routes that are presented here as plain templates where you can add your page title and page contents.
### __templates__
There are certain repetitive tasks that shouldn't bother you as a developer. These are things like the head components of an html file, the footer including the copyright information, and the navigation bar itemes. All these are writen by our scripts stored in the templates directory. Accordingly, this folder contains three files, nav.sh -- for the navigation bar items, footer.sh as the name suggests, and headtags.sh. 
### __Other important files__
#### __index.sh__ 
This is the main application file that creates the API DEMO fetch, it is basically an infinite loop that continuously creates and destroys the data imported from the server, and renders the new results each time to the client or the front-end. 
#### __package.json__
Is the node package management file containing all the project details, scripts, dependencies, etc. You can read more on this under the node package management official site. 
#### __global.sh__ 
This is a file that stores global variables that can be called in any file when required. In this case for instance, one such variable was "APIPath", which as you might have guessed, represents the url in which the API is hosted. The second variable was the "delay", which is time set in seconds at which the application should read the server. This is important as if many hits are sent to the server, it will sense possible hacking, and will immediately throttle the data streaming behavior. It is therefore IMPORTANT! to set the time delay appropriately. If necessary, contact the server administrator.
## __Conclusion__
If you have read this guide upto this point, you should be ready to hit the road with She-Bang static site generator and API fetcher. It is my sincere hope that you will find as much joy in utilizing this tool, as I did writing its code.

![](http://imgur.com/pD3Qr5Cl.png)  
__Software Author__: Nicolus K. Rotich  
__Contact__: [Linkedin](https://linkedin.com/in/rotichtheengineer/)
