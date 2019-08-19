# shebang-framework
This is a foundational framework combining bash shell and Unix capabilities to create a fast static site generation, as well as a dynamic web application used to fetch data from API endpoints with no delays.
The application combines the power of heredocuments and the versality of regular expressions in bash shell to create script templates
for you to start out with. 

Upon clonning the application from the repository, navigate to the source directory and install it by running the following commands:

$ sudo apt-get install shebang_1.01-1_amd64.deb

Once it is installed, you should see an output like this:

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

Next,navigate to the area of your projects, say desktop,  create a directory you would like to use for your projects say you want
to call it "shebang", you will then do this:

$ mkdir shebang
$ cd shebang

Open your favorite teminal application and run the following command:

$ shebang

The project dialog will begin immediately, and you will just need to follow the directions on our dedicated command line interface (CLI)

$ Enter project name (shebang ?): #Enter the project folder you wish to create - (if you are lazy press enter with no input) the default is the preceeding directory#
$ Enter application entry point (default 'app.sh'?): #Enter the application name, the default one is 'app.sh' if you don't enter anything#
The following text will follow if all goes well

================ start ============  
===== wait as we prepare your bang project =========
Cloning into './my-project/public/shared/img'...
remote: Counting objects: 37, done.
remote: Compressing objects: 100% (37/37), done.
remote: Total 37 (delta 11), reused 0 (delta 0)
Unpacking objects: 100% (37/37), done.
===== ... writing application directories ===========
all set! cd to (your project) and see if it worked
Ensure all dependencies are installed.
Run the command *npm run install* for the dependencies.
Initiate the project by running *npm run rot*
================== end ==============  
As the application says, navigate to the project directory you just created. Install the dependencies by doing the following

$ (sudo) npm install
.  
.  
.  
.  
done  
$ npm run rot #This is the magig command, it creates the routes, template scripts, and even create our own first page to direct you to
our documentation and guides#
$ npm run dev #This is your usual command used to trigger the server. By default, She-Bang uses port 8080#

*/ After this you are ready to carry on the development. Familiarize yourself with the project directories created and where necessary 
consult our guide /*


