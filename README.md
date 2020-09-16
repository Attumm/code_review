# CODE REVIEW GUIDE

### Technical
##### Read the code like a compiler
Read each line of code line by line. Never assume, always check.

##### Trust but verify.
* When in doubt create comment to verify.
* Learn the list of [code smells](https://en.wikipedia.org/wiki/Code_smell) by heart.

##### Simple is better than complex.
* If something is too hard to understand, maybe it's too hard to justify supporting it in the future.
* Code it written once, read many times.

##### Follow checklist
This is a great checklist to follow [code review checklist](https://github.com/while1malloc0/code-review-checklist)

### Stay profesional
##### Use Egoless programming
Live by [the ten commandments of egoless programming](https://blog.codinghorror.com/the-ten-commandments-of-egoless-programming/). It will be great for yourself and the team.


### Communication
* English isn't the 1st language of many of us. Don't assume that what someone wrote expresses their thought exactly in 100%. Or maybe your English isn't perfect and you're reading it wrongly. Don't assume what someone else wrote is exactly what they meant.
* If the written thread gets too long (usually more than 4 posts is too long) then reach out on chat or voice/video call to discuss it.
* We're all human so we might forget about the review guide or for various psychological reasons might not adhere to it fully. Then please remind each other about it
* WIP(Work In Progress) in the title is the best way to eliminate unnecessary discussions.

### Code is made by and for humans.

* Please assume that the comment and code is written in good intention. if in doubt please ask.
* The thing we have to keep in mind is, we are all trying to achieve the same goal. Perfect code (it's existence is not the point right now).
* We are all humans. We have emotions. We have fears.
* Please ensure that everyone is feeling warm and welcome to reach out.
* As humans, we tend to get tunnel vision, please think outside of the box.


### Knowledge
* As reviewer it is not expected that you have *all* the answers.
* Don't assume you know more than writer of the code, It could be the [Dunning-Kruger effect](https://en.wikipedia.org/wiki/Dunning%E2%80%93Kruger_effect) (You think you are more knowledgable than you actually are)
* Don't assume you know less then the writer of the code. It could be [Imposter Syndrome](https://en.wikipedia.org/wiki/Impostor_syndrome) (You know more than you think you do)
* If something is unclear ask questions, maybe some comments in the code could help the next person reading the code.

Make sure your comments don't fall under [law of triviality](https://en.wikipedia.org/wiki/Law_of_triviality).
If the only thing you can suggest is change of variable name or something similarly small, maybe it's not important enough to change.

### Layout of great comment
A great comment has three parts.

1. Problem statement, include why it's a problem.
2. Possible Solution, why does this solve the problem, and how good is the suggestion?
3. Try to use sources to backup and or better explain for example Link to documentation / stackoverflow for more information.
For the reviewer having to find and read sources shows the commitment.



###### Example Comment
```
This project is a RESTful json api (at least it tries to be :)), other formats if needed.
Returning a string directly (like you did here with "bar") instead of a json object, will break with the rest of the app.

To quote [The zen of Python](https://www.python.org/dev/peps/pep-0020/):

> Special cases aren't special enough to break the rules.

Instead of returning a string, you should return an object like so:

   return jsonify({"foo": "bar"})

For more information about our RESTful app see the link to our documentation: http://mycompany.com/docs/restful-api.md
```
