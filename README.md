App ID: 21rgjw5bzpsgwfy0eie8xpw21rgjw5g3

# School Of Code (pre joining tasks) #


## Task 2: ##
Common Variable Naming Conventions: - 
-	Pascal Case – When the first letter of a variable is uppercase, along with the first letter of every new word that is compounded together.
For example: ThisIsPascalCase
-	Camel Case – Sae rules as Pascal Case but it does not have the requirement to capitalise the first letter. The difference with Camel Case is that the first letter is not capitalised (Dromedary Camel Case). However, the first letter of the first word can be capitalised and this is known as (Upper Camel Case).
For example: thisIsDromedaryCamelCase
	          ThisIsUpperCamelCase
-	Snake Case – This is when words are separated using underscores; it is also called a “pothole case". When every letter is capitalised, it is known as a "screaming Snake Case".
For example: this_is_snake_case
             THIS_IS_SCREAMING_SNAKE_CASE
-   Kebab Case - This follows the same rules as the snake case but uses a dash instead of an underscore. When all words are capitalised it is known as a "Scream Kebab".
For example: this-is-kebab-case
             THIS-IS-A-SCREAM-KEBAB

### Task 3: ###
How The Internet Works:
Computer Networks: -
-   Latency: The time it takes for a message to transfer. 
-   Local area networks (LAN): Small networks of close-by computers.
-   Ethernet: In it's simplest form, a series of computers are connected to a single, common ethernet cable. When a computer wants to transmit data to another computer, it writes the data as an electric signal onto the cable. In order to determine which computer is to receive the data, each computer must have a unique Media Access Control Address (MAC Address). Every computer today comes with it's own unique MAC Address.
The general term for this approach is Carrier Sense Multiple Access (CSMA for short). The 'Carrier', in this case, is any shared transmission medium that carries data - copper wire in the case of ethernet and the air carryin radio waves for WIFI.
-   Bandwidth: The rate at which a carrier can transmit data.
-   Exponential Backoff: A 'backing off' behaviour by computers used to prevent collisions in transmitting data at the same time.
-   Collision Domain: A way to shrink the number of devices on any given shared carrier to prevent collisions and improve efficiency.
-   Circuit Switching: Switching wholecircuits to route traffic to the correct destination, however it is considered inflexible and expensive because there is often unused capacity.
-   Message Switching: A way to send data from one place to another. It 'hops' from one destination to another and is considered more reliable and fault-tolerant as if there is a routing problem, it will take another route to get to it's destination address, this is also known as the 'hop count'.

The Internet: - 
-   IP (Internet Protocol) Packets: Consist of IP header (destination) and data payload.
-   User Datagram Protocol (UDP): Consists of IP header, UDP header and data. UDP has extra information inside including a port number which is checked by the header to determine whether or not the data has been sent to the correct destination. UPD also contains a checksum which checks the sum of the data.
- IP gets the packet to the right computer, but UDP gets the packet to the right program running on that computer. UDP does not offer any mechanisms to fix the data or request a new copy - receiving programs are alerted to the corruption but typically just discard the packet. They also do not provide confirmation that a packet has actually reached its destination.
-   Transmission Control Protocol (TCP or TCP/IP): TCP is included within the data payload of an IP packet and contain sequence numbers which allow a recieving computer to put the packets into the correct order even if they arrive at different times on the network. Once the packet has reached its desination successfully, an acknoledgement ("ACK") is sent back to confirm, this allows for the next packet to then be sent.
-   Domain Name System (DNS): When you search for something, the computer asks the DNS server for the address, the DNS will look at its registry and then reply with the address of your search if one exists.
-   Domain Structure (Tree structure): Top level domains (.org, .gov, .net, .com, .edu, .uk), second level domains (google.com, dftba.com), sub-domain or parent (drive.google.com, images.google.com, store.dftba.com).

The World Wide Web: -
-   The World Wide Web runs on top of the internet meaning that they are not the same thing which is often confused.
-   Uniform Resource Locator (URL): In order for pages to link to one another, each hypertext page needs a URL.
-   Hypertext Transfer Protocol (HTTP): HTTP prettu much only has one command, "GET" which, when you search, you are asking the internet to "get" whatever it is that you are searching for. This command is sent as raw ASCII text to the web server which then replies back with the web page hypertext that we requested.
-   Hypertext Markup Language (HTML): HTML is the building blocks of a webpage.
-   Network Neutrality: This is the principle that all packets on the internet should be treated equally. It does not matter what the packets are, they shold all chug along at the same speed and priority.

#### Task 5: ####
Line commander: -
-   pwd: Pre Working Directory (prints the path of the current folder that you are in).
-   cat: Concatenate (reads in the contents of a file you want).
-   ls: Lists the contents of your current directory.
-   cd: Changes directory (folder) followed by a path that takes us there.
-   ls -a: Lists all files including any hidden files that start with a dot.
-   cd ..: Changes directory up a folder.
-   ls -l: Lists the contents of the current directory with useful information about each item.
-   ls -lh: Lists the contents of the current directory and makes them more readable.
-   ls -lS: Lists the contents of the current directory and orders the largest file first.
-   ls -ltr: Lists the contents of the current directory and lists the age from newest up.
-   mv (mv folder-name ../folder-name): will move the folder-name up a folder. Can also change the name of the file at the same time. (mv folder-name ../new-folder-name) will move the folder-name up a directory ad change its name to 'new-folder-name'.
-   mkdir: Makes a folder in the current working directory.
-   nano: Command line text editor, enables us to add text into a file.
-   ls logs: Prints out the contents of logs.
-   '>' (Redirect Operator): Redirects the output to a file (ls > file-name.txt - This will write the output of ls to a file called 'file-name.txt').
-   | (Pipe to a command): These work very similarly except pipe will not write to a file and is used to hand the output to another command.
-   rev: This will reverse the lines of text.
-   grep (grep option "pattern" file): This command is used to search documents. Combined with the '-c' option wil count on how many lines the pattern occurs.

# Task 6: #
Git, Github And Version Control:
Version Control: -
Git: Git is version control, it's a database of the sort of history of our files. Everyone has their own local copy of what they are working on.
-   Starts with a folder that may have a file with our notes in, for example, 'notes.txt'. 
-   Firstly, what we want to do is set up Git so that Git will track that file/folder for changes. When we initialise Git in a project, we are setting up a mini database which is going to track all of the changes that we make. The command 'git init' is going to initialise the Git project. 
-   The next step will be to add the changes to what is known as a 'staging area'. The command 'git add notes.txt' will prepare the file to be saved as we are making Git aware that we have changes that we would like to be saved. 
-   Next, what we are going to do is to use the command 'git commit -m'. This command will save a version of our project that we can come back to, we can also add a comment as to why we have committed this version such as changes etc.
-   If we make another new file we will have to add this version to the staging area also, for example 'git add story.txt'. This tells Git that we are not changing anything in the file but only adding to the staging area the 'story.txt' file. The next stage for this new file would be 'git commit -m' followed by a comment of what we have done and why we have committed the file.

Summary of Git: -
-   'git init': This command is used to initialise a git repo.
-   'git add 'file-name': This command is used to stage our changes.
-   'git commit -m "message": This command is used to take a git snapshot of a version of the file we are working on.

Github: -
-   Github is basically a Dropbox for Git. It gives us the ability to post a repository to the cloud for other people to collaborate on.
-   'git push': This command is used for when you have made all the changes to the file that you want to and you are ready to push it up to Github.
-   'git pull': This command is used when you would like to get the most recent/updated version of your file from Github, you pull it from Github to your computer.
-   Branches: A branch in Git is simply a lightweight movable pointer to one of these commits. For example, if ypu want to add a new page to your website you can create a new branch just fir that page without affecting the main part of the project. Once you are done with the page, you can 'merge' your changes from your branch into the primary branch. 
-   When you create a new branch, Git keeps track of which commit your branch 'branched' off of so it knows the history behind all the files.
-   'git checkout -b 'my branch name': This command will automatically create a new branch and then 'check you out' on it, meaning Git will move you to that branch off of the primary branch.
-   After running the above command, you can use the 'git branch' command to confirm that your branch was created.
How To Push An Existing Repository From The Command Line:
-   git remote add origin git@github.com:OwenB-HamD/newrepo.git
-   git branch -M main
-   git push -u origin main
-   'git push' origin 'your-branch-name': This command will push changes onto a new branch on Github. Github will automatically create the branch for you on the remote repository.
-   In order to get the most recent changes that you or others have merged on Github, use the 'git pull origin master' command (when working on the primary branch). In most cases, this can be shortened to 'git pull'. This shows you all of the files that have changed and how they've changed.
-   'git log': This command is used to see all the new commits (You may need to switch branches back to the primary branch. You can do that using the 'git checkout master' command).
