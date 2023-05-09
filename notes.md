# Week 1 (this is out of order because Mark subbed)

1. Why are you here and why and I here
	Rah rah stuff---web site that the world can see
2. Very applied, learning tons of new stuff---be ok with that
3. Jump to GITHUB repo and explain
	Build Simon and "Startup company" in parallel
4. Spend lots of time, focus on mastery, stay up to date
5. Codepen?
	a. HTML is structure, CSS is style, JS is behavior
		browser renders HTML code
			it doesn't throw errors, it just does its best and you have to "think like the computer" to debug (but also printf/comment technique)---you have to fix stuff or it will come back to bite you
	b. not all browsers play the same (show rotating border gradient doesn't work in safari problem (what about FireFox?) Chrome has better development tools (according to Mark).  Standardize on Chrome
	c. W3schools.com tutorials
	d. JS is dangerous because browsers can capture all kinds of events

6. History
![Whiteboard internet 1](board1).jpg
![Whiteboard internet 2](board2).jpg

	a. IPv4 (32bit addressing), IPv6 (128bit addressing)
	b. Packet: address, IP, TCP, UDP, port (16bit addressing)
	c. browser
	d. routers
	e. DNS (.com, .edu, .gov, .org, etc.?) subdomain servers
		"trick is getting other people to use your DNS"
		weakness to attack---bottleneck
	f. AWS (or whatever: google, Facebook, etc.)
			virtual machines
	g. what about firewall???
	h. Net neutrality
	i. network address translation (NAT)
		needed because we haven't adopted IPv6
		lets us squeeze more machines into IPv4 by multiplexing using ports?
	j. how to register a new machine/address onto the internet?
		used to be just the address
		but now more chaotic
	k. punchcards-->personal computer-->virtual servers (command line)



7. Use google to find answers and don't pay
	how to weed out the bad stuff

8. AWS Console
	How can you accidentally pull a Wingate?
	what all is an AMI?
		how to make my own
	spin up new server whenever
	always save to GitHub!!!
	use cs260.pem for class stuff so I don't have to chase key files
	if you create a new key pair, make sure you download it and save it somewhere (local/safe)
	terminate/stop/start server, etc.
	Make sure to know what all the EC2 setup stuff is/does
	launch
	paste address into browser (use http?)
	why do we already have an index.html file on the new server?
	manage firewall on security tab
	don't be afraid to make mistakes---do several server setups so it's no big
	we didn't give it a name yet/DNS address?
		Route53
		how to connect to new server(s)? And disconnect from terminated ones?
			edit Caddyfile
	HTTPS certificate
	why does it not add SSH when I tell it to on spinning up?
		using new security group (sg-0a21b82629c4eddeb - launch-wizard-2)
		works fine when selecting existing group (sg-0526f14f2820aebc4 - cs260-webserver)
			jk---it just sets up the source to be another hardcoded machine (not mine); change to mine, it works fine; change to 0.0.0.0/0 and it seems to still work? Nope---only for a minute until refreshed then no go.  Apparently something does like SSH being public/open
	And, why doesn't it apply the new SSH rule when I add it after spinning up?
		it worked when I used MyIP as source (instead of 0.0.0.0/0)???
		and it broke again (meaning the SSH rule just disappeared) when I edited the source from MyIP to 0.0.0.0/0...?
	what is the 0.0.0.0/??? Last part of this mean?
	What does all the stuff in Caddyfile mean?
	What does all the stuff in index.html mean?
	Can I make my own name for a security group?
	What is in an AMI and how to build your own?  Will we do it?
	What is a hosted zone and how does making a duplicate mess things and how do you fix it (the stuff Lee explained about in class)


SSH and command line
	we ssh into this server we are creating
	check out index.html
 	what is Caddy?
		edit Caddy file
	vi, emacs, nano, (s)ftp
	don't worry about firehose syndrome


# Week 2

Lee explains hard things like ask yourself first really well
	I used to ask the smart guy down the hall, but then I started feeling bad...
	lifetime learning skill to say figure it out

We can use about:blank, open inspector and write html, css and js right in the browser (local, no server)
	you can also run a server on your local machine (local, server)
	then, nonlocal server

What is websocket? How is it peer-to-peer and how does this give us more power?

CC something for my startup?

You CANNOT get behind--> goes from being an awesome class to NO!!!!!!

How is Lee making the videos he shows in the slides?

What does "Git commits *must* represent all work" mean exactly?
	atomic commits
	and none means no credit

Caddy is a multi-reverse proxy/gateway that figures out which service to serve (we have two: Simon, Startup)
	what is the bit about certificates
	adding services (instruction)
		daemon
Node.js it just javascript running outside the environment---pull the runtime engine out of the browser and use it from the command line
How is Atlas free?  Will it quit being?

Talk about mental models and their importance

Mac/Linux are Posix compliant
Windows isn't--powershell, so need to get gitbash or something else Posix compliant
WSL is windows subsystem for Linux---be careful

Console
	historical pic
	console
		file explorer (command line)
		execute programs
		should I get Warp?
	deployment script---pushes dev code to prod server
		show doing it by hand first?
	if server changes make AWS? fuss about an unknown host, go to .ssh directory (on local machine?) and delete knownhosts? file
	what do * * * mean in traceroute and why does it take so long?
Visual Studio Code to develop
	GitLens extension
	Live Server extension
	command shift P
	command P
How did Lee say to grab .pem file from AWS?
Use AWS Secrets to store stuff like .pem file if you want to be able to get it from multiple machines, share it, etc.
Should we have a "personal" server to demo stuff in class (so we don't have to show stuff on the main class server?
Git
	is .gitignore just there so you don't have to white list each file (so you can "git add .")?
		if I add . And then put ignore something, does that work? Do I have to do the other order?
	use command line
	editor
	what is -a flag? Vs. git add vs. git commit?
		What does this mean-->"...the point of the stage (add) step, is so that you can commit some files while still leaving other..."
	visualizing git!
	what is the gitconfig slide for?
Github
What about the stuff in 1.7 slides we didn't cover and I don't understand?
	ask Lee about the staging/production envs and how the automated/continuous integration works (and why is there still a manual link there?)
Where are the cheat sheet notes (for exams) supposed to go (in our repo)?
	Startup notes.md file?

Is Menti.com a useful tool?
Do I clone the GitHub repo for my class?
What about a high-level diagram that shows the big picture?
	there's one on GitHub about the class tech (mostly), and it should be in the slides?
	should we have one with underlying internet stuff at the level Mark had on the board as well?
	and how do those two relate?
Can my PhD students get paid enough to TA this course?
What is the deal with the two different AWS login screens?
Is working in class a good thing or no?  Should they all bring laptops for doing so?
Are the slides a shared resource, or should we all be doing our own (approach)?
GitHub
	how does it work generally?
	how should I be interacting with this as shared resource?
	I need to understand how the thing is organized
	how do slides relate to instruction links in GitHub?
	do I have to fork the repo to make a pull request for typo edits?  Or, can I just edit directly in the main branch?
Does the course view/organization in GitHub/Canvas make sense?
Slides say startup is 40%, but Lee said 60% in class...?
What certification is the Instruction page talking about (with the checkmarks)?
(How) Are required readings enforced?
How does late work policy and is it actually beneficial?  How often do people get hosed by getting behind compared to getting partial credit when due?  Since we are building on earlier stuff, is there even a way forward without late leniency?
Can we organize the GitHub stuff by day/week (like on my web schedule for other courses) in a semester-agnostic way?
-->What is the point of in-person class, if the slides and (more critically) all the talking for the slides (instruction) is online (is it, in fact)?<--
	should I use (some) different slides?
	should I be saying (some) other stuff for slides in class?
		a little bit of inspiring rah rah (TBL is just one regular dude), some useful info (leave rest to be read), demo???
What if, in my course, I don't like/wouldn't say/would say differently than Lee some of the stuff that is in the instruction?
	small example: I do office hours by appointment, not W9-11...
	I did not (have a Simon game)---I did!  Personal sounds fun and intimate, but it's personal...
Next/back navigation in GitHub?
What is a notes.md file?
How does PHP relate to html+css+js?
Is it useful in any way for me to submit all the assignments in Canvas?  If so, can I even?
Do we worry at all about students just using code from other students public repos?
Discord
	how to add a @#@#@@ avatar?
	is there a way to block posts before the current semester?  Is that a good idea?
	did Lee's "what to delete so I'm not charged later" post make it into the instructions somewhere?
What is a CLI?
How to IP and domain name fields relate?

# Week 3


## Instruction question/notes
1. AWS
	what is TLD (for click server)?
2. Console
	is it tracert(which doesn't work on my Mac terminal) or traceroute (which does)?
3. GitHub
	Use the Git functionality of VS Code to add conflictTest.md to Git --> should this say to startup directory or something like that?
	Better explain "Please tell me who you are" bit
4. Webservers
	Is Go code running on port 80 as it the text says, or port 3000 like the code looks?
	Not sure how to differentiate service, microservice and serverless function?
	In slides 2.1, what this the point of the two-slide sequence on servers?
	A few other 2.* slide questions, if we don't see them in class...
5. Domain Names
	What is the * in the image subdomain.*secondary.top
6. AWS Route 53
	Why can't we do HTTPS with just and IP address?
	What contact info should I use for the DNS if I'm using FHTL account (and not my personal one)?
	if we register a wildcard subdomain, why in the troubleshooting guide does it suggest that the www subdomain won't work?



## To Do

	1. create personal AWS account?
	6. Come up with startup idea and do spec assignment
		something super simple the first time, just to do it and understand it
		codenames (probably too hard)
		some simple CC thing?
	7. Go back over instruction and edit typos
	8. Next batch of questions to Lee(/Mark?)
	12. organize this file
	13. post The Stack article on Discord
	
## Questions for me to figure out myself
	1. Learn all the stuff about Codepen
		a. How do HTML, CSS and JS know about each other and interact? In Codepen? In general?
		b. know what all the HTML/CS/JS stuff is called/for

## Questions for Lee/Mark
	1. I remember Mark pushing at lunch for having this organized in week-sized chunks, and I think that is a good idea.  It will help the students know where they are in the course, what's coming when, etc.  Also, maybe the online folks require it?  If organized that way, it doesn't have to be tied to the calendare (so, for example, in Spring, for a T/TH class like what Lee is teaching now, a day is simply a week-sized chunk all at once.  It does impose more of a order than is currently there, which might make updating things a bit more of a pain; but, in theory, the main organization should be pretty stable soon? 
	2. Is looking at webpage code a good idea?  It seems like Mark gave some kind of caution about this the first day, but I can't now remember what that was...?

## Pedogogical Blatherings


