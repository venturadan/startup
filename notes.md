# Week 1 (this is out of order because Mark subbed)
1. Why are you here and why and I here
	- Rah rah stuff---web site that the world can see
3. Very applied, learning tons of new stuff---be ok with that
4. Jump to GITHUB repo and explain
	- Build Simon and "Startup company" in parallel
4. Spend lots of time, focus on mastery, stay up to date
5. Codepen?
	1. HTML is structure, CSS is style, JS is behavior
		- browser renders HTML code
			- it doesn't throw errors, it just does its best and you have to "think like the computer" to debug (but also printf/comment technique)---you have to fix stuff or it will come back to bite you
	2. not all browsers play the same (show rotating border gradient doesn't work in safari problem (what about FireFox?) Chrome has better development tools (according to Mark).  Standardize on Chrome.
	3. cW3schools.com tutorials
	4. JS is dangerous because browsers can capture all kinds of events
6. History
	1. IPv4 (32bit addressing), IPv6 (128bit addressing)
	2. Packet: address, IP, TCP, UDP, port (16bit addressing)
	3. browser
	4. routers
	5. DNS (.com, .edu, .gov, .org, etc.?) subdomain servers
		- "trick is getting other people to use your DNS"
		- weakness to attack---bottleneck
	6. AWS (or whatever: google, Facebook, etc.)
		- virtual machines
	7. what about firewall???
	8. Net neutrality
	9. network address translation (NAT)
		- needed because we haven't adopted IPv6
		- lets us squeeze more machines into IPv4 by multiplexing using ports?
	10. how to register a new machine/address onto the internet?
		- used to be just the address
		- but now more chaotic
	11. punchcards-->personal computer-->virtual servers (command line)
	![Whiteboard internet 1](images/board1.jpeg)
	![Whiteboard internet 2](images/board2.jpg)
7. Use google to find answers and don't pay
	1. how to weed out the bad stuff
8. AWS Console
	1. spin up new server whenever
	2. always save to GitHub!!!
	3. use cs260.pem for class stuff so I don't have to chase key files
	4. if you create a new key pair, make sure you download it and save it somewhere (local/safe)
	5. terminate/stop/start server, etc.
	6. launch
	7. paste address into browser (use http?)
	8. manage firewall on security tab
	9. don't be afraid to make mistakes---do several server setups so it's no big
	10. we didn't give it a name yet/DNS address?
		- Route53
		- how to connect to new server(s)? And disconnect from terminated ones?
			- edit Caddyfile
	11. HTTPS certificate
9. SSH and command line
	1. we ssh into this server we are creating
	2. check out index.html
 	3. what is Caddy?
		- edit Caddy file
	4. vi, emacs, nano, (s)ftp
	5. don't worry about firehose syndrome

# Week 2 (this is out of order because Mark subbed)

1. Lee explains hard things like ask yourself first really well
	1. I used to ask the smart guy down the hall, but then I started feeling bad...
	2. lifetime learning skill to say figure it out
2. Three levels of "server":
	1. We can use about:blank, open inspector and write html, css and js right in the browser (local, no server)
	2. you can also run a server on your local machine (local, server)
	3. then, nonlocal server
3. What is websocket? How is it peer-to-peer and how does this give us more power?
4. You CANNOT get behind--> goes from being an awesome class to NO!!!!!!
5. Caddy is a multi-reverse proxy/gateway that figures out which service to serve (we have two: Simon, Startup)
	1. what is the bit about certificates
	2. adding services (instruction)
		- daemon
6. Node.js is just javascript running outside the environment---pull the runtime engine out of the browser and use it from the command line
7. Talk about mental models and their importance
8. OS
	1. Mac/Linux are Posix compliant
	2. Windows isn't--powershell, so need to get gitbash or something else Posix compliant
	3. WSL is windows subsystem for Linux---be careful
9. Console
	1. historical pic
	2. console
		- file explorer (command line)
		- execute programs
	3. deployment script---pushes dev code to prod server
		- show doing it by hand first?
	4. if server changes make AWS (or whatever) fuss about an unknown host, go to .ssh directory (on local machine?) and delete knownhosts? file
10. Visual Studio Code to develop
	1. GitLens extension
	2. Live Server extension
	3. command shift P
	4. command P
11. Use AWS Secrets to store stuff like .pem file if you want to be able to get it from multiple machines, share it, etc.
12. Git
	1. use command line
	2. editor
	3. visualizing git
	4. what is the gitconfig slide for?
13. Github
	1. Don't nest repos

# Week 3
1. Elevator pitch
 	1. passion
	2. what is the problem?
 	3. what is the win?
	4. how you are going to do it?
2. dropped "changing root domain" from course?
3. lots of time to answer questions before we covered anything
4. we don't have the browser just read files directly from our HD (if we are just local, especially) because of permissions/security issues/complexity
5. `<!DOCTYPE html>` means we are using HTML 5
6. language attribute just lets google, etc. know what language this is (in case it wants to find that kind of thing or translate or whatever)
7. localhost `127.0.0.1` loopback (LiveServer uses this)
8. TBL is famous WebFather because he thought of anchor tags---anyone can change the world
9. HTML steals from SGML
10. DOM (doc object model) is a tree representation in memory
11. HTML has styling attributes (like width) that are now deprecated by CSS
12. HTML Slide (3.1) "Header" is overloaded and misleading
13. CodePen assumes <!DOCTYPE html><html></html> and doesn't include it
14. Make clean structure with as much semantics as possible (for readers, google, etc.)
15. `<forms>` are kind of deprecated by JS now, but still...
16. why does `controls=false` not get rid of controls in Media code?
17. where to find videos, etc that you can access in CodePen?
	1. look at webpage source and link there or just host it locally?
18. Is there cool SVG repos somewhere?
19. In HTML, you have to use multiple pages, one for each "view"
	1. later, we use one page and JS to modify the page content dynamically
20. make the whole simon.html app live coding?  Or is that a bad idea?
21. Show how to deploy
22. cover the whole thing again for startup
23. HTML structure doesn't even (any more) need to worry about placement/location, just the elements/pieces, which can just appear linearly for now
24. Talk about what markup is and what we are doing with it 

# Week 4
1. Don't be late---I can't penalize you enough to reflect how much you are penalizing yourself by getting behind (especially Spr/Su)
2. CSS is just a bunch of rules that select an HTML element and apply declarations to it
	1. Browser introduces some defaulty rules; some CSS devs immediately wipe all those (how?) for better control
	2. look at element/styles in browser dev tools
4. Three ways to style (cascading preference order, highest to lowest)
	1. inline style attribute in HTML (using CSS declaration)---kind of lame/old/coupled/clunky
	2. put the rule separately in HTML
	3. put rules in an external file---best/modular approach
5. That's all there is to it---simple to learn; lifetime to master---it's subtle
6. Bootstrap is a CSS framework we are using???
7. `command /` comments out a highlighted block in Code
8. Some styling notes
	1. `font-size 3em` means 3x the width of the m in the parent font (size)
	2. 3rem is relative to the document, instead of the parent font
	3. start/end instead of left/right for language agnostic placment
9. Box model---In HTML, everything is boxes:content, padding, border, margin---make sure you are on the right element, and look at elements/style box view
10. you can tweak everything in browser debugger
11. Get to know all the CSS stuff
12. HTML is content/semantic "structure", but not location/relation structure
13. learn more about fonts and animation (we went way too fast)
14. what is the `display` style thing that we skipped?
15. native app and responsive design are different
17. not my job to know all the HTML/CSS/etc.  My job is to give mental models, work flow, how to debug/problem solve, find answers, etc.
18. `<meta name="viewport"/>` tells device to not guess scaling
	1. Lots of stuff we do is because of legacy problems (like when pages weren't written well for a device) that still haven't gone away yet
19. Froggy?
20. bootstrap framework
21. CDN content delivery network


## Instruction question/notes
1. AWS
	- what is TLD (for click server)?
2. Console
	- is it tracert(which doesn't work on my Mac terminal) or traceroute (which does)?
3. GitHub
	- Use the Git functionality of VS Code to add conflictTest.md to Git --> should this say to startup directory or something like that?
	- Better explain "Please tell me who you are" bit
	- What does "Git commits *must* represent all work" mean exactly?
		- atomic commits
		- and none means no credit
4. Webservers
	- Is Go code running on port 80 as it the text says, or port 3000 like the code looks?
	- Not sure how to differentiate service, microservice and serverless function?
	- In slides 2.1, what this the point of the two-slide sequence on servers?
	- A few other 2.* slide questions, if we don't see them in class...
5. Domain Names
	- What is the * in the image subdomain.*secondary.top
6. AWS Route 53
	- Why can't we do HTTPS with just and IP address?
	- What contact info should I use for the DNS if I'm using FHTL account (and not my personal one)?
	- if we register a wildcard subdomain, why in the troubleshooting guide does it suggest that the www subdomain won't work?
7. HTML Structure
	- some of the assignment instructions are misleading or don't quite match the output shown
8. Simon CSS
	- Should this not appear here? It seems like maybe a copy/paste error from the startup CSS page?
		- "Update your startup repository notes.md to record, what you modified and added with this deliverable. The TAs will only grade things that have been clearly described as being completed. Review the voter app as an example. Also update your notes.md to record what you learned."
9. CSS framworks assignment seems way too simple?  Can we at least make them drop in more of the components and/or modify some of them?
	

## To Do
- [] play with html tags (from HTML instructoin) I'm not familiar with
- [] CSS assignments
	-[] startup
- [] Go back over instruction and edit typos
- [] Divide instruction/schedule into week chunks
- [] What to about the prodution deployment stuff in 1.7 slides we didn't cover and I don't understand?
	- ask Lee about the staging/production envs and how the automated/continuous integration works (and why is there still a manual link there?)
	- figure out how to make them aware that it is a thing without spending any realy time on it.
- [] create personal AWS account?

## Questions for me to figure out myself
1. Learn all the stuff about Codepen
	1. How do HTML, CSS and JS know about each other and interact? In Codepen? In general?
	2. know what all the HTML/CS/JS stuff is called/for
2. How can you accidentally pull a Wingate?
3. what all is an AMI?
	1. how to make my own
4. Make sure to know what all the EC2 setup stuff is/does
5. why do we already have an index.html file on the new server?
6. what is the 0.0.0.0/??? Last part of this mean?
7. What does all the stuff in Caddyfile mean?
8. What does all the stuff in index.html mean?
9. Can I make my own name for a security group?
10. What is in an AMI and how to build your own?  Will we do it?
11. What is a hosted zone and how does making a duplicate mess things and how do you fix it (the stuff Lee explained about in class)
12. How is Lee making the videos he shows in the slides?
13. should I get Warp?
14. what do * * * mean in traceroute and why does it take so long?
15. is .gitignore just there so you don't have to white list each file (so you can "git add .")?
	1. if I add . And then put ignore something, does that work? Do I have to do the other order?
		- what is -a flag? Vs. git add vs. git commit?
	2. What does this mean-->"...the point of the stage (add) step, is so that you can commit some files while still leaving other..."
16. GitHub
	1. how does it work generally?
	2. how should I be interacting with this as shared resource?
	3. I need to understand how the thing is organized
	4. how do slides relate to instruction links in GitHub?
	5. do I have to fork the repo to make a pull request for typo edits?  Or, can I just edit directly in the main branch?
17. How does PHP relate to html+css+js?
18. What is a CLI?
19. How do IP and domain name fields relate?
20. Why does CodePen seem to not incorporate changes I make?
21. what is the multi-buffer copy/paste thing for mac?
22. Run example password HTML code stuff and look at stuff (including Network stuff) in localhost browser?
	1. forms: instead of post/get (which goes away and returns), we now can just use JS right in the browser
	2. something related to JSON?
23. you can hover over stuff and it will link you to MDN reference page
25. learn about web scraping (and how it relates to JS and browsers)
26. rmdir -rf simon will delete files if not empty
27. why do all checkbox/radio buttens share the same name attribute value?
28. go back and play with the ribbons in CodePen again and actually make changes this time (save files and debug)

## Questions for Lee/Mark


## Lunch topics
1. How are we suppose to share/interact with course GitHub repo? 
	- Do I clone the GitHub repo for my class?
	- Are the slides a shared resource, or should we all be doing our own (approach)?
	- How do we share the resource?
2. Is working in class a good thing or no?  Should they all bring laptops for doing so?
3. Are Simon assigments just part of the 60% that is startup grade? Or should they be separate?
4. Should required readings be enforced?
5. How does late work policy and is it actually beneficial?  How often do people get hosed by getting behind compared to getting partial credit when due?  Since we are building on earlier stuff, is there even a way forward without late leniency?

## Pedogogical Blatherings
1. Is Menti.com a useful tool?
2. What about a high-level diagram that shows the big picture?
	1. there's one on GitHub about the class tech (mostly), and it should be in the slides?
	2. should we have one with underlying internet stuff at the level Mark had on the board as well?
	3. and how do those two relate?
3. Can my PhD students get paid enough to TA this course?
4. Does the course view/organization in GitHub/Canvas make sense?
5. What is the point of in-person class, if the slides and (more critically) all the talking for the slides (instruction) is online (is it, in fact)?
	1. should I use (some) different slides?
	2. should I be saying (some) other stuff for slides in class?
		- a little bit of inspiring rah rah (TBL is just one regular dude), some useful info (leave rest to be read), demo???
6. How to balance answering questions with moving along (especially when they are remedial, and we've already talke about it)?
7. Watch out for pacing (duh)
8. HTML isn't about structure; it's about content?
9. Should we have a "personal" server to demo stuff in class (so we don't have to show stuff on the main class server)?


## Assignment stuff
1. CONSOLE: xxyy
2. GITHUB: https://github.com/venturadan/startup
3. CODEPEN: 
4. STARTUP Spec: https://github.com/venturadan/startup
5. AWS EC2: http://44.211.87.91
6. HTTPS: https://wafflesandcheese.click
7. HTML Structure: https://codepen.io/venturadan/pen/QWZrMox
8. HTML Input: https://codepen.io/venturadan/pen/PoyeJoO
9. HTML Media: https://codepen.io/venturadan/pen/ZEqoXBg
10. HTML startup: https://startup.wafflesandcheese.click
11. CSS Practice: https://codepen.io/venturadan/pen/XWxPmLp
12. CSS Flex: https://codepen.io/venturadan/pen/jOevaLJ
13. CSS Frameworks: https://codepen.io/venturadan/pen/jOevzpo



