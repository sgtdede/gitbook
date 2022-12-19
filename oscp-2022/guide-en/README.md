---
description: OSCP 2022
---

# 🇬🇧 Guide (EN)

Here is the approach I followed to pass the OSCP exam.

All the advices that worked for me might not work for you.&#x20;

Pick what you like, throw what you don't.

## Whoami & Cybersec background:

* [Twitter](https://twitter.com/sgtdede)
* [Github](https://github.com/sgtdede)
* [Linkedin](https://www.linkedin.com/in/andr%C3%A9-lenoir-9487a2152/)

I'm a french engineer in computer science (network and cybersecurity). I have 7 years of professional experience in cybersec on both defensive and offensive tasks, including a significant number of pentests (web, externals and internals).

I do have very limited background in CTFs and CTFs platforms (TryHackMe, HackTheLab, root-me, etc.)

## TLDR:&#x20;

* Spend most of your time on labs ! it's by far the most useful resource of the PEN-200. You can pass the exam ignoring the course, but you won't pass it ignoring the labs.\

* Privilege Escalation is globally worth half of the exam points (AD and standalones mixed).\
  Here is the best practical introduction to privesc:\
  [https://tryhackme.com/room/linuxprivesc](https://tryhackme.com/room/linuxprivesc)\
  [https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)\
  Do those rooms and take notes, they will earn you a lot of time and self confidence. Windows PE room is a bit less quality than Linux but still very good.\

* &#x20;Active Directory is worth 40 points on the exam, so almost 2/3 of the required points required to validate. Do all the AD exercices and labs of the PEN-200. And also work on the AD boxes of PG-play/Pg-Practice/TryHackMe/HackTheBox.\

* Armageddon cheat sheet: [https://github.com/sgtdede/oscp/blob/main/armageddon.txt](https://github.com/sgtdede/oscp/blob/main/armageddon.txt)



## OSCP Exam:

Like the PEN-200 labs, you will be required to find an entry point and take over several machines (recon + exploitation) and gain root/system access on those machines (privilege escalation)

There is total of 6 machines to pown during the exam. &#x20;

* **1 Active Directory set (1 DC + 2 machines)** = 40 points
* **3 standalone servers** = 20 points each **** (10 pwn + 10 privilege escalation)
* **Points Bonus** = 10 points
* **Maximum total** =  110 points (40 points AD + 60 points standalones (3x20) + 10 bonus points)
* **Required points to pass the exam** = 70 points



## Recommandations:

### 1) Available resources: labs first

Here are the 4 resources available to you and sorted from the most useful to the less useful (in my opinion):

* Labs (Pen-200)
* PG-Play/PG-Practice/TryHackMe/HackTheBox (External labs)
  * [NetSecFocus lists (PG-Play, PG-Practice, HTB)](https://docs.google.com/spreadsheets/u/1/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/htmlview)
* S1REN walkthroughts, IppSev walkthroughts, writeups, TCM courses, etc.
  * [S1REN walkthroughs](https://www.youtube.com/playlist?list=PLJrSyRNlZ2EeqkJa12Tu-Ezun9kXvHufN)
  * [IPPSec walkthroughs](https://www.youtube.com/watch?v=2DqdPcbYcy8\&list=PLidcsTyj9JXK-fnabFLVEvHinQ14Jy5tf\&ab\_channel=IppSec)
* Courses  + Exercices (Pen-200)

First three resources are far more useful than the PEN-200 course IMO. And I put walkthroughs at the same level as PG-PLAY/PG-PRACTICE labs on second position. Walkthroughs  are a very good complement to the labs and I highly recommend to work those two resources in paralel, during the same period of your training. Indeed,  walkthroughs will enhance your labs resolution skills, and the labs will make you way more proactive during your walkthroughs lectures.

Main challenges that you will meet during the labs and the OSCP Exam are:

* Finding attack vectors
* Identifying quickly rabbitholes
* Identifying attack vectors that deserve too be digged deeper

Only experience through labs resolution will improve those three skills. The more you do labs, the more you'll improve, specifically for rabbitholes identification.



### 2) How to do a lab properly

#### a- Avoid hints/discord/forums

You'll need to quickly lose the habbits to use hints and refers to forums and Discord. Keep in mind that anytime you use them during a lab, you won't improve (or very little) any of the 3 previous skills: **Finding attack vectors**, **Identifying quickly rabbitholes** and **Identifying attack vectors that deserve too be digged deeper** because hints/discord/forum will give you the information instead.

That being said, those are quite useful tools to refer to during the first steps of your learning journey, specifically if you're a begginer.

You'll just need to make rules at some point of your learning steps:

* &#x20;Don't refer to discord/forum if you didn't pass a significant ammount of time on the reconnaisance. Make sure you digged into all the possible attack vectors before falling for it.
* However, there is absolutely no problem to refer to discord/forum after you resolved a lab. If you need to check if there was an alternative way, or if you doesn't fell good about the exploitation path you choosed.

There is one exception: if you need to validate 30 labs in order to get the 10 bonus points and you are too short in time. Then is this case and only this one, just do the most efficient way and refers to them (you'll lose all the others benefits linked to the lab resolution process though).

Some labs are obsoletes or not well made, set some time limits to yoursef and don't lose multiple days on those kind of labs. If you estimate that you arleady did a full research on the lab and you're completely out of idea, than refer to discord/forum.&#x20;

#### b- Take notes

Take notes during all the exploitation process of a lab (screenshots + writed notes + proofs). Learn from S1REN methodology which is simple and efficient (cf. [S1REN walkthroughs](https://www.youtube.com/playlist?list=PLJrSyRNlZ2EeqkJa12Tu-Ezun9kXvHufN)).  This methodology and constant note taking will earn you a lot over time.

During the exploitation or at the end of a lab, feed a Cheat Sheet dedicated to this specific lab with all the key commands that helped you to take over the lab (recon, exploitation and privilege escalation)

Here is the CherryTree template that I use when running a lab : [https://github.com/sgtdede/oscp/blob/main/target.ctb](https://github.com/sgtdede/oscp/blob/main/target.ctb)

![](<../../.gitbook/assets/image (2).png>)

I write all the recon, exploitations and privesc steps on the **Report** section.

**Last advice:** don't force it too much, if you're in a bad mindset (too much time on labs for the day, impatient, don't want to take the time to find the vulns), then maybe it's better to do the lab another time, or clear your mind before (take some fresh air, sport, etc.). In this set of mind you probably won't solve any labs anyway and you'll be even more frustrated at the end.



### 3) How to do a walkthrough properly

Don't watch on autopilot ! Youtube walkthroughs and writeups are excellents marerials, but if you're not focused while lecturing them, they are useless and you'll forget them in a week.

* Feed your notes and cheatsheets during the walkthrough: write every command that you didn't know before or that seems interesting to add to your arsenal.
* Regularly pause the video, before the solving and put yourself in the place of the attacker: what would you do if you were S1ren/Ippsec ? what commands would you launch ? Which service would you scan ? Which attack vectors would you dig in ? How?\
  When you're ready, unpause the video and compare: if you found the right solution bravo: try to find the different tools and options used during the walkthrough to eventually add to your arsenal our discover a new exploitation method.\
  If you didn't find, then that means you missed something: take notes of it and prepare to work again on those points in the future.\
  Do this work during all exploitation steps: after the nmap scan, after discovering a vulnerable service, before the privilege escalation, etc.
* When running a lab, be aware or take note of your weaknesses. Then try to remember them when lecturing a walkthrough and find how do S1REN/IPPSec/etc. react against those same problems. That will make you discover new concepts and methods and improves on those weaknesses.

If you do all those steps you'll earn the maximum out of walkthroughs and writeups, which are an insane resource.



### 4) Active Directory

Active Directory is now inevitable on the PEN-200 exam. It's worth 2/3 of the required points. Exploitation of AD sets is not very varied and you won't have a lot of unexpected surprises if you know the concepts of AD exploitation. Only the initial foothold can be very different from set to set.

The real challenge to train for AD attacks is the lack of resources: the PEN-200 AD course is not good, exercices and labs are both very good though, but there is not a lot of them. So you'll need to do them all. Do not hesisate to do them multiple times each, in order to be comfortable on AD attacks. Try to master differents tools and methods (2 or 3) for each steps of the AD exploitation, lateral movements and pivoting.&#x20;

**Additional resources :**

* [https://tryhackme.com/room/wreath](https://tryhackme.com/room/wreath)
* [https://tryhackme.com/room/adenumeration](https://tryhackme.com/room/adenumeration)
* [https://tryhackme.com/room/vulnnetroasted](https://tryhackme.com/room/vulnnetroasted)
* [https://tryhackme.com/room/postexploit](https://tryhackme.com/room/postexploit)
* [https://tryhackme.com/jr/lateralmovementandpivoting](https://tryhackme.com/jr/lateralmovementandpivoting)
* [https://tryhackme.com/room/enterprise](https://tryhackme.com/room/enterprise) (harder than OSCP)



### 5) Privilege Escalation

Privilege Escalation is worth 1/2 of the total OSCP Exam points (AD set and standalones included):

Do the two following TryHackMe rooms, they are worth it!\
[https://tryhackme.com/room/linuxprivesc](https://tryhackme.com/room/linuxprivesc)\
[https://tryhackme.com/room/windows10privesc](https://tryhackme.com/room/windows10privesc)

#### a- Automatic privesc enumeration scripts

Privescs enumeration scripts/binaries are very effective and I recommend using them

**Windows:** winpeas, powerup, sharpup

**Linux:** LinEnum.sh, linpeas.sh

For Linux, I used both LinEnum and linpeas equally. For Windows, I mainly used WinPeas because I was used to it. Howerver I do think that powerup/sharpup are a better alternative for the first searchs beacause Winpeas often spit too many information and noise. I recommend you to have at least two scripts/binaries per OS anyway.

**Be careful:** like the autorecon tool (cf. [recon](./#6-recon)), those are double-edged tools: They can make you go auto-pilot, which you want to avoid at any cost. And they can output so many information that you might miss an obvious privilege escalation and follow a rabbithole. FInally, sometimes privesc are not found by those scripts.

That's why I highly recommend that during your training on labs, you learn and do some privilege escalation the manual way. In order to understand and get comfortables with privesc concepts and techniques on Windows and Linux. The two previous TryHackMe rooms will help a lot for that !

#### b- Manual enumerations

S1REN always do manual privesc enumerations. Besides the TryHackMe rooms and runnings labs, watch some of S1REN's walkthroughs to improve your manual privesc exploitation skills.

Here are some resources that you can use for manual privesc enumeration:

* [https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation](https://book.hacktricks.xyz/windows-hardening/windows-local-privilege-escalation)
* [https://sirensecurity.io/blog/linux-privilege-escalation-resources/](https://sirensecurity.io/blog/linux-privilege-escalation-resources/)
* [https://sirensecurity.io/blog/windows-privilege-escalation-resources/](https://sirensecurity.io/blog/windows-privilege-escalation-resources/)



### 6) Recon

* **Use** [**Autorecon** ](https://github.com/Tib3rius/AutoRecon)**(or equivalent) as a secondary scanner**
* **Always use your own manual scans first**

This is probably the most important step for the labs and the OSCP Exam. Spend some time on this step in order to find attack verctors and quickly identify rabbitholes. The more labs you'll do, the more you'll improve on the recon process.&#x20;

Take the habbit to use differents tools during the recon phase. Some tools wont be compatible or complete against specific OS, services, applications, versions. And sometimes you might miss the entry point if you're using only one tool.

However don't spread yourself either, you don't need to master perfectly different tools. I recommend to master/be comfortable with one tool for each reconnaissance category, and know how to use basically 1 or 2 alternatives for each. For exemple in my case, my references tools are: nmap for port scanning, ssh tunnels/chisel for pivoting, ffuf for web fuzzing, impacket for windows/AD post-exploitation, etc.

Autorecon is  a very powerful tool for recon as it scan each service with multiphe different tools. However it can be a double-edged tool that might turn against you:

* Don't go auto-pilot: autorecon can make you become very passive. While it's a powerful tool, it won't replace manual scan that you might perform on your own. Always do your manual scan first.
* Autorecon will return a lot of informations against a lab box, sometimes too many. That might lead you into rabbitholes taht you wouldn't even consider without autorecon.

Alway keep your intuition a make your own attack plans. I highly recommend to use autorecon, **but as a secondary scanner**. When you are running a lab, let autorecon run in background and use you manual scans first.

Refer to autorecon only to validate/go deeper/ with what you already found with your manuals scans, if you have strong suspicions about a service, or in the case that you don't have any other tracks or ideas.



### 7) Notes : CherryTree, OneNote, Obsidian, Joplin

* **Use a not taking tool which will be useful during all your PEN-200 training, labs, OSCP exam, and for your future pentests.**

Choose the tool that fit best for you. I tested a lot during my training and I choosed CherryTree at end. It's the worse looking one but it's simple to learn, fast, with good shortcuts and the best structure for me among all the tools that I tried.

Here is my template that I used for the labs and the exam: [https://github.com/sgtdede/oscp/blob/main/target.ctb](https://github.com/sgtdede/oscp/blob/main/target.ctb)

![](<../../.gitbook/assets/image (2).png>)

I write all the recon, exploitations and PE steps on the **Report** section. (structure is inspired from S1REN)

I recommend you to watch some walkthroughs from S1REN and learn from here for the note taking and methodology.



### 8) Cheat Sheet

* **Do your owns cheat sheets, and keep some externel cheat sheets as a reference**
* **At the end of your preparation, compile all your existing cheat sheets into an ultimate one dedicated to the exam, your own armageddon cheat sheet which will be light and efficient**&#x20;

During all your training, maintain one or multiple cheat sheets. Personnaly I maintained multiples cheat sheet, one per theme of the PEN-200. I filled them over time during courses, labs and walkthroughs. I writed every commands that seemed important or might be useful one day.

Finally, those cheat sheet were a bit too big compared to what commands I needed 80% of the time and it was too long for me too find the information I was looking for.

So I writed a new cheat sheet light and compact dedicated for the exam, which contained the command that I used 80% of the time. (I still had my other cheat sheet, more complete, as a backup for when I need the other 20%)

#### Armageddon Cheat Sheet

I highly recommend you to prepare your own armaggedon cheat sheet for the exam. Here you can delete everything that's not related to the OSCP and the exam. The goal is to focus on the exam specifically so, not everything that you learned, so:

* Reconnaissance/exploitation
* Active Directory
* Privilege Escalation
* Every commands that you like and use frequently during labs, all of your favorites commands

As an exemple, here is my armaggedon Cheat Sheet that I prepared for the exam: [https://github.com/sgtdede/oscp/blob/main/armageddon.txt](https://github.com/sgtdede/oscp/blob/main/armageddon.txt)

Again, it was effective for me because it was my own, she probably won't be as good for you.  Build your own armageddon cheat sheet, you won't regret it.

#### Cheat Sheet references:

* [https://github.com/swisskyrepo/PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings)
* [https://www.thehacker.recipes/](https://www.thehacker.recipes/)
* [https://book.hacktricks.xyz/welcome/readme](https://book.hacktricks.xyz/welcome/readme)
* [https://www.ired.team/](https://www.ired.team/)
* [https://www.hackingarticles.in/](https://www.hackingarticles.in/)



### 9) Bonus Points (10 points), worth?

It is possible to collect 10 bonus points on the final note by filling the following objectives:

* Complete all the exercices of the PEN-200
* Pwn 30 machines on the PEN-200 labs

If you follow my recommandations, you will already fill the second objective. Indeed I recommand you too do as many labs as you can, so at least 30.

For the first one: the exercices are very good materials in my opinion, however the problem is that in order to validate them all, you will need to go through the courses part of PEN-200 which is not good...

If you have a one year access to PEN-200, then there is no questions: do the courses and exercices. 10 points might be the difference between a success and a failure at the final exam.

If you have only a 1 month access, you probably won't have the time to correctly do 30 labs and all the exercices, so I recommend you to invest all your time on labs/walkthroughs

If you have a 3 month access, this is a tough decision: course/exercice might take you 1 month to complete and besides the 10 points it won't give you much else. I personnaly worked 2 months on PEN-200, I did first month to complete course and exercices and 2nd month on labs. Before and after the exam, I had the impression that I would have been prepared better with 2 months of labs and ignoring the courses/exercices.



### 10) Planning

* 1 month access to PEN-200
* 3 months access to PEN-200
* 12 months access to PEN-200

For the 1 and 3 months, do not hesitate to add to your planning and additionnal 1 (or more) month access to PG-PLAY/PG-PRACTICE if you do not feel comfortable at the end of your labs, to keep training before the exam.

However, I do believe that it's much better to strike while the iron is hot. Meaning that you'd rather take the exam after an intense training period on PEN-200 labs while you're still sharp, even if you do not feel completely ready, rather than adding an additional 1 month if you know that you won't have much time to work/prepare on this additional month.

Depending on your level/experience, it's possible to pass the OSCP exam with a 1 month access (even without any training on PEN-200)



### 11) Exam

Do schedule some time in advance to familiarize with the exam rules:

* [https://help.offensive-security.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide](https://help.offensive-security.com/hc/en-us/articles/360040165632-OSCP-Exam-Guide)
* [https://help.offensive-security.com/hc/en-us/articles/360050299352-Proctoring-Tool-Student-Manual](https://help.offensive-security.com/hc/en-us/articles/360050299352-Proctoring-Tool-Student-Manual)

During the exam, revert the target machine if you have any doubt

Try to arrive with a basic attack plan, but without bloking you in any kind: personnaly, I choosed to start with the AD set, which was the less stressful IMO, as I had to validate the 40 points of AD anyway. So in my mind I already accepted that I might spend multiples hours on the AD sets without starting to panic.

Prepare meals, drinks, coffees, etc. in advance, to gain time and release some pressure in case things goes wrong and everything come down to the last hours. In short: put all the odds on your side.

Breath and relax, dont change your habbits and use your classic methods. Like you would if you were running labs on PEN-200.

It's not too bad to spend a lot of time on a machine, you need 70 points. Even if you unlock the first machines very late, the exam is still playable.

If you fail at the exam, it's not the end of the world, you'll come back stronger next time.



### 12) (optionnal) Report

I used Word and the [offensive security template](https://www.offensive-security.com/pwk-online/OSCP-Exam-Report.docx). I did not want to spend time to learn a new tool that was not necessary for the OSCP exam and that would not earn me anything.

I recommend you to use the tool you already are the most confortable with. There is already so much to work and learn in order to prepare the OSCP correctly, that you shouldn't add any additional uneeded learning... You might aswell take that time to take some fresh air, do some sport, enjoy family times and rest :)



### 13) (optionnal) Text editor: vim, nano

Learning to master a solid text editor is another story ! In my point of vue, it's essential that you become comfortable with either vim or nano at some points. Both of theme are powerful editor and built-in in a lot of Linux/Unix systems that you'll compromise. I would personnaly recommend vim by a little margin because it's the one that you'll always find on any Linux/UNIX (during PEN-200 and during your whole pentester life).

It's a very powerful tool, way more than an text editor when mastered. You'll earn a lot of time during many hacking/dev/administration tasks by mastering vim.

{% embed url="https://danielmiessler.com/study/vim/" %}

### 14) (optionnal) Terminal multiplexer: tmux, screen, terminator

In the same spirit, I highly recommand you to familiarize with a terminal multiplexer. This is also a powerful tool to have in your arsenal, that will make your pentester/admin life easier and earn you a lot of time.

I do use terminator personnaly, because it's the one that I know the most. It's the most simple to learn but it's less powerful than screen and tmux. If you don't know any of them yet, I would recommend learning tmux, which is natively built-in on multiple Linux/Unix systems and suitable for pentest.

{% embed url="https://www.youtube.com/watch?v=Lqehvpe_djs&ab_channel=IppSec" %}

## My OSCP journey

[my journey](my-oscp-journey.md)

