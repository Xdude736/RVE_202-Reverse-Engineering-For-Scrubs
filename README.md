# RVE_202-Reverse-Engineering-For-Scrubs
**A fake college course designed to help programmers new to reverse engineering get started on the path. I am by no means an expert and I am learning this myself. If you reference this guide, please do so by linking to it. Feel free to use this for a real course if you are a professor and think the material/structure is worth it, just let me know how it went and how it can be improved for everyone**

Hello and welcome to (RVE 202 - Reverse Engineering for Scrubs)! I am, essentially, a Senior TA helping out with this class and I will be here to guide you through what I know. I'll make sure to keep the course work updated as myself and the Professor work through what sorts of work needs done. This course is the prerequisite to (RVE 236 - Networks, Operating Systems, and Bugs. Oh My!).

## Prerequisites:
(CIS 103 - Python for 9 to 5er's) and (CIS 136 - Linux for n00bs) are necessary to understand the basic coursework. (CIS 253 - Assembly for Code Monkeys) and (CIS 144 - C's get degrees, C gets jobs) would also be helpful, though they are not required.

## Learning Goals:
Throughout this course:
1. Students will read assembly and create a pseudo-code representation of the assembly
2. Students will demonstrate understanding of basic Stack/Heap protection implemented on modern operating systems
3. Students will learn the basic layout of a C program while it is being executed in Memory
4. Students will show understanding of, be able to recognize, and be able to exploit: Stack Overflows, Heap Overflows, 
   Formatting errors, and general errors in C binaries
5. Students will be able to create a clear write up for a vulnerable program: explaining what the exploit is, how they 
   found it, how to use it as a threat actor, and how to correct the issue
6. Students will be able to write an exploit program in C or Python that will run an exploit on a vulnerable program, 
   allowing for exploit automation

## Content and Sequencing
1. Introduce programming principles requisite to start reversing (C, Memory Layout, Assembly conventions, etc.)
2. Reversing (what it is/isn’t)
3. Stack Overflows
4. Stack Protections
5. Format Vulnerabilities
6. Heap Overflows
7. Basic Operating Systems (Setup for RVE 236)
8. Basic C Networking (Setup for RVE 236)

## Required Texts:
1. [Hacking: the Art of Exploitation 2nd Ed. by Jon Erikson](https://www.amazon.com/Hacking-Art-Exploitation-Jon-Erickson/dp/1593271441/ref=sr_1_2?ie=UTF8&qid=1545281046&sr=8-2&keywords=hacking+the+art+of+exploitation)

2. [Reversing: Secrets of Reverse Engineering by Eldad Eilam](https://www.amazon.com/Reversing-Secrets-Engineering-Eldad-Eilam/dp/0764574817/ref=sr_1_1?ie=UTF8&qid=1545281077&sr=8-1&keywords=reversing+secrets+of+reverse+engineering)

***THERE WILL BE REQUIRED READING FROM THE BOOKS. GET THE BOOKS. NO JOKE.***

## Academic Honesty:
Like all courses, we expect acedemic honesty from students. There is nothing wrong with getting help from fellow students or the internet when you are stuck or need something explained in a different way. There is something wrong when you are copying other people's writeups and exploits. Cheaters don't win. They may get degrees but they become *That Guy* or worse...Script Kiddi3s. Don't be those people.

## Assignments:
During this course you will be required to do readings, watch videos, and complete projects. All of these materials were selected based on previous student's recommendations on what worked for them and what did not. As such the course will be upated over time to provide the best content available to the public. While doing readings it is highly recommended that the student take notes, be they handwritted or highlighted. While watching the videos, it helps to write the code and follow along, as well as taking notes. ***FOR THE PROJECTS A WRITEUP IS REQUIRED IN ORDER TO GET ANY FORM OF POINTS. YOU CANNOT TURN IN AN IDIDATHINK.C FILE AND EXPECT CREDIT. DOCUMENT EVERYTHING!***

## Tips & Tricks:
1. Never take less than $20. You are worth more than that.
2. This course is designed to be self paced, so feel free to take your time and really dig into the material. The order of assignments listed below are in the recommended order. It is not required that you do them in that order.
3. For Microcorruption: the MSP430 is a real microprocessor from Texas Insturments. It has real documentation out there that may be useful. There is also a custom manual for the different locks available on the microcorruption site. Look for it, it's there.
4. While watching Live0verflow's videos: if at any point he starts walking you through a protostar challenge STOP WATCHING IMMEDIATELY! The point of these challenges are for you to learn and figure them out on your own. Watching a walkthrough should only happen AFTER you have completed the challenge and want to get a different perspective/deeper understanding of wtf you just did.
5. For anyone new to C: it can be a real pain. And that's an understatement. Take your time while trying to figure it out and always make sure you know what is going on with Null Terminators. Also, pointers. Pointers, pointers, pointers, pointers.
6. RTFM n00b. Seriously though, man pages will be your best friend. Learn how to read documentation sooner rather than later. You will be better for it.
7. On Protostar: try and solve the challenges only using the provided binary file. It can be very frustrating but it will help you better understand assembly and the sooner you can read assembly the sooner you can get into the real meat and potatoes. If you get really stuck on a challenge (10+hrs with no real progress) look at the source code mirror for the challenge on Live0verflow's website. If you still can't figure it out after (15+hrs) watch his video tutorial and fiugre out what it is that blocked you and make sure to include that in your writeup. The key here is to learn, both from the challenges and from your mistakes. It will make you a better programmer.

## Conventions:
  _LVF_ = Live0verflow,
  _MC_ = Microcorruption,
  _PST_ = Protstar,
  Books will be referenced by their main title, minus the sub title.

## Week 1:
This week will start out easy with a couple of chapters to read and videos to watch. Along with that there will be two writeups due.
- **Readings:** _Hacking_: 0x100, 0x250 thru 0x280. _Reversing_: Ch.1 (This week is a lot more required reading than normal, but we are trying to get everyone on the same page). 
- **Videos:** [Live0verflows Intro](https://liveoverflow.com/intro.html) and 0x00 through 0x05 of his [LVF: Binary Hacking Course](https://liveoverflow.com/binary_hacking/index.html)
- **Projects:** _MC_: Tutorial(No writeup necessary), New Oreleans, Sydney
- **Resources:** [Microcorruption](https://microcorruption.com/)

## Week 2
This week will ease you into the basics of reversing. Make sure to take notes and create cheat sheets for any concepts/commands you think you'll need.
- **Readings:** _Hacking_: 0x310 and 0x320. _Reversing_: Chapter 2 (Some of the material is repeated from last week, but reading it again reinforces the ideas/concepts)
- **Videos:** [LVF: Binary Hacking Course](https://liveoverflow.com/binary_hacking/index.html): 0x06, 0x09 - 0x0B (0x07-0x08 are bonus if you are interested)
- **Projects:** _MC_: Hanoi, Cusco ; _PST_: Stack0, Stack1
- **Resources:** Protostar can be found [here](https://exploit.education/protostar/). For now, ignore the warning that protostar is out of date.

## Week 3
This week will be relatively laid back, focusing more on understanding previous assignments and slowly working towards a more in depth understanding of stack overflows.
- ***Readings:*** _Hackng_: 0x330. _Reversing_: Chapters 3 and 4.
- ***Videos:*** _LVF_: 0x0C (don't watch if you have not completed last weeks protostars)
- ***Projects:*** _MC_: Johannesburg, Reykjavik. _PST_: Stack2, Stack3. If you need more to do; stack4 (can also be done next week).

***COURSE WILL BE UPDATED OVER TIME***
