# Technical Interviewing for JavaScript-React Engineers <!-- omit in toc -->

Questions are organized by category (technical versus behavioral) and type (whiteboarding challenges, knowledge checks, etc.) Each question is given with the relevant answers– for whiteboarding challenges, this includes Starter Code, Questions (for the interviewer), Pseudocode, Brute-Force Solutions, and finally, the Refactored Solutions, where possible; for knowledge checks, this includes Key Talking Points and Conversational Examples, where possible.

***

## Table of Contents <!-- omit in toc -->

- [Computer Science](#computer-science)
- [Core Concepts](#core-concepts)
- [HTML](#html)
- [CSS](#css)
- [JavaScript](#javascript)
- [React](#react)

***

## Computer Science



## Core Concepts

<details><summary>Name and discuss key design principles in software engineering.</summary>

</details>

<details><summary>Name and discuss key design patterns in software engineering.</summary>

</details>

<details><summary>What is an API? What is a RESTful API?</summary>

</details>

<details><summary>Name and discuss the 5 key constraints (and optional 6th) in RESTful architecture.</summary>

**Uniform Interface**

**Client-Server Independence**

**Stateless Interactions**

**Cacheable Data**

**Layered Architecture**

Optional: **Code On Demand**

</details>

## HTML

<details><summary>What is the box model?</summary>

</details>

<details><summary>What is the DOM?</summary>

</details>

## CSS

<details><summary>What is the CSS waterfall?</summary>

</details>

## JavaScript

<details><summary>Classes</summary>

<details><summary>Name Array iteration methods and describe their uses and differences.</summary>

`.forEach()`, `.map()`, `.filter()`, `.reduce()`, `.from()`, `.keys()`, `.entries()`

</details>

<details><summary>Name Array boolean methods and describe their uses and differences.</summary>

`.every()`, `.some()`, `.includes()`

</details>

<details><summary>Name Array search methods and describe their uses.</summary>

`.indexOf()`, `.lastIndexOf()`, `.find()`, `.findIndexOf()`

</details>

<details><summary>Name Array sort methods and describe their uses.</summary>

`.sort()`, `.reverse()`

</details>

<details><summary>How would one return the highest or lowest value in an Array?</summary>

Since there's no built-in method for returning the highest or lowest values of an array, you can either:

1. Sort the array and return the first or last value, ie: `Arr.sort((a, b) => a - b)[0]`
2. Use the `Math.min()` or `Math.max()` methods on the _spread_ Array, ie: `Math.min(...Arr)`, or
3. Use the `.apply()` method on the `Math` class' `min` or `max` methods, ie: `Math.min.apply(_, Arr)`

</details>

</details>

<details><summary>What is difference between a function declaration, function expression, and arrow function?</summary>

</details>

<details><summary>What is a callback function?</summary>

</details>

<details><summary>What is a function bind?</summary>

</details>

<details><summary>What is a function closure?</summary>

Because JavaScript variables can belong to either a local or global scope, global variables can be made local, and therefore, protected or private, via a _closure_, while still allowing for the global function interaction.

</details>

## React

<details><summary>Describe the React lifecycle.</summary>

</details>

<details><summary>Describe the difference between a class component and functional component.</summary>

</details>

<details><summary>What are React hooks? Name and describe some key, built-in hooks.</summary>

</details>

***

What is unique about the ES6 arrow function, and how do you leverage that uniqueness in a React project?

If you use a function with a arrow function, it allows you to use hoist, meaning functions can be moved to the top of their scope. Arrow expressions in general though are just regular functions, but it also changes how this is defined, so because of this, arrow functions basically find their this value in its enclosing scope

What is unique about the ES6 arrow function is that while it does not have its own “this” value, it has the “this” value of the context that it is enclosed in. Before the arrow function, we would have to use .bind in order to bind this to whatever function you were using it with, otherwise it would result in an undefined. We use this all the time in React. If we did not use the arrow function, every time we tried to set state in a function, or whatever it may be, you would first have to bind to the this, which would be lengthy and honestly pretty annoying.

Explain the React lifecycle

If you were asking for a general overview of the React lifestyle, it happens in three phases otherwise known as intervals. There is first the first interval of Mounting, the second which is Updating, and the last which is Unmounting. There are of course many methods that occur during each of these intervals which are called lifecycle hooks, but back to the general overview. The Mounting interval is basically the first time a component is created and introduced into the DOM tree. It is the initial state of the component. The next interval is the Updating aspect, which is key to React. As we know, React is awesome because it allows for immediate re-renders of only whatever component it is you wish to re-render. All of this takes place during the Updating interval. Whether it’s an update in state or change in props, this is the time when all of this happens. The final interval is the Unmounting, where simply put, the component is removed from the DOM tree. It is important to note that order matters in this lifecycle, and these MUST go in order.

What does MVC mean? And what’s its purpose in web development?

MVC stands for Model View Controller. The purpose of it in web development lies in the fact that it is basically the basis for all user interfaces. The Model is the data that is used in a given application, and what exactly that data can be can differ. The View is exactly as it sounds, and it is the visual aspect and literally what you are seeing in a window. The Controller is what controls and updates both the model and the view. So basically the View displays the model, and the controller takes user input and updates the model and view accordingly.

Explain the difference between a framework and a library?

A framework and library can be explained using an analogy right within their names. A framework, is the structure or foundation upon which entire applications can be built. A library however, is built within a framework. Just like in real life, a library has a frame which supports the building, but inside that building are the many different books or collections that you can use. The books, in the programming world, would be various helper methods/modules whatever it is that has a slightly more narrow scope, but are awesome to have and implement because it makes life much easier.

What does REST stand for? What does it mean?

REST stands for Representational State Transfer– each side of the request and response should be independent of each other, there should be a uniform way of requesting and sending information back.

What is scope? And explain all the scope levels in JS.

What is a Promise? Why do we use them?
 
A promise basically lets you hold off on performing an action, based on a previous action either being completed or failing. We use them because sometimes we don’t want functions to run right away. Javascript is run synchronously, meaning functions are run from top to bottom one after another, one at a time. So the best use of a promise is to aid in asynchronous functions, which means functions will not run until another process has completed.This is great because certain functions may need a response back from a database in order to run the next few lines of code, and if it had to wait it could cause performance issues.

What are the different types of functions in JS?

What’s the purpose of semantic markup?

What is the purpose of semantic HTML5 elements? What are some.

What is the “THIS” keyword?

The “this” keyword is used in programming languages to refer to the object, class, or whatever else that the currently running code is a part of. In certain languages like React and JavaScript, the “this” is mandatory and is the only way to access data and methods that are in the current object. It is known as an instance method, because of the way they refer to the current object they are working in. The current object, acts as the parent that indicates where the “this” is referring to.

What is a higher order function?

Explain the differences between == and ===
What does it mean to clone a repository?

1. What does it mean to fork a repository?
2. Diagram the box model on the whiteboard.
3. How does absolute positioning work?
4. What is `upstream` in your local copy of repository? Can it be `timon`?
5. What is Doctype and is it mandatory?
6. What is the difference between Git and GitHub?
7. What is a block level element?  Name one.
8. How do you make two block level elements appear inline in the browser?
9. What do you think would be the result of the following css rule? a { text-decoration:none;}?
10. What is `git status` used for?
11. What are the advantages of using GIT?
12. What is HTML Anchor element? Provide an example.
13. Give an example of inline element.
14. In an ordered list: can you start the counter not from 1.? If yes, explain how.
15. What is the purpose of .gitignore?

16. When do you use the command git pull upstream master? How about git push origin master?
17. Whiteboard a function that takes an array  of numbers as an argument and returns a new array with each value doubled.
18. How does absolute positioning work?
19. How do you access the value `Timon` in the object const Pumbaa={numberOfFriends: 1000, bestFriend: `Timon`}.
20. What is pair programming and what is the value of it?
21. Create an empty Array and push the String “Gold” into it.
22. Create an ES6 base class called Animal with the property `name` and method `eats`.
23. What is a good strategy to use when you are confronted by a tough programming challenge?
24. How do you make two block level elements appear inline in the browser?
25. Why is it important to write clean, readable code with a consistent code style?
26. What will this code log to the console?  
 let a = [1,2,3]
 let b = 3
 a[2] == b
12. What will this JavaScript express return?  const a = 0; a = 1;
13. What is the difference between the return statement and console.log?
14. What are the index values of `a` in this array.  [“a”, “b”, “c”, “a”]
15. What will be logged to the console?
 let a = "0";
 let b = 0;
 console.log(a === b)

1. What is callback? Give an example.
2. What is closure? Give an example. What are some of the advantages?
3. Create an ES6 base class called Unicorn with the property "name" and method "poopsRainbows"
4. What is a JavaScript class constructor method?
5. What is the DOM?
6. In your opinion, is the practice of writing tests important? Why?
7. What is jQuery?
8. Create a variable and set the value to a new Div in jQuery
9. What is "new" keyword? (what is it doing?)
10. Does the .map method return a new array?
11. Does the .forEach method return a new array?
12. What is the result of in-place array manipulation?
13. Why would you have a constructor NOT accept any arguments? Can you?
14. Why would you need a constructor function in your class object?
15. What is hoisting? Are function declarations being hoisted? What about class declarations?
16. What the heck is `super()` and what is it doing? Give an example.

1. What is React and what are its benefits?
2. What does the javascript arrow function solve?
3. How does React know to re-render?
4. What is a React Component?
5. What is state? Why would you need to set state in a Component
6. When is `ComponentWillMount` lifecycle method executed?
7. When is `ComponentDidMount` lifecycle method executed?
8. Let`s say, you fetched some initial data and need to set it to state.  Which lifecycle method would you use to do so?
9. What is stateless component and how is it different from a regular component?
10. How would you check if the props passed are valid(what the child component is expecting them to be)?
11. What is the difference between an XMLHttpRequest, Fetch and an jQuery AJAX request?
12. What are Props?

1. What is the require() and what`s the point of using it?
2. What is a Node package?
3. What is the require() and what`s the point of using it?
4. What is npm? Why do you need it? What about package.json?
5. Explain `LEFT JOIN`. How about `RIGHT JOIN`?
6. What is Object.prototype?
7. What is postgres?
8. What are Modules? How are they useful?
9. What is ERD?',
10. What do you know about Relational databases? What about NON-relational?',
11. Design a small database for ice-cream shop(hint hint: ERD)',
12. Why would you need `.config` file in your application? What about `.env`?'

3. What is a Promise? Why do we use them?
4. Write a SQL query to return all rows in the Goblins table where name equals 'Green Goblin'.
5. Why are we using Express?
6. Create a route that will get a user by id
7. Create a route that will create a post for a user
8. Create a route that will get all posts for a user
9. What is Agile Development?
10. What is ORM?
CURRENT CLASS QUESTIONS:

1. How are Ruby classes different from Javascript “classes"
2. What are ivars used for? How do expose them outside the class?
3. How do we create new instances of a class? What methods are called when we create them?
4. How are Ruby classes different from Javascript "classes"
5. What does super do with inheritance in ruby? In Javascript/React?

BEHAVIORAL INTERVIEW QUESTIONS

Questions taken from 30 Behavioral Interview Questions You Should Be Ready to Answer

TEAMWORK
Talk about a time when you had to work closely with someone whose personality was very different from yours.
Give me an example of a time you faced a conflict while working on a team. How did you handle that?
Recently I worked with two classmates to program an algorithm. We seemed to be on a good path at first, each person contributing a different piece of the puzzle, however one member of the group wanted to write the code a certain way which deviated from the instructions. This person was adamant about their idea despite us explaining that we had to complete the problem in a different way. They continued to contribute disjointed steps to solve the problem in their way, which precluded us from proceeding with solving the problem as directed.

I tried to resolve this through openness and communication; in the moment, I struggled to understand what my classmate was trying to say so I encouraged them to pseudocode their thoughts. They did but their pseudocode was equally as confusing so I asked questions to break the pseudocode down into smaller pieces. This became challenging because my classmate became defensive and spoke in a condescending tone. When we reached an impasse, I suggested they write the code they had in mind, in the hopes that would communicate their idea.

This was the most successful strategy; although their solution wasn’t quite what we were supposed to have, we were able to mostly adapt it to our instructions.

At the end of the exercise, I encouraged my classmate that they had clearly been on the right path but what made the work so challenging was communicating about the steps we needed to take.

Describe a time when you struggled to build a relationship with someone important. How did you eventually overcome that?
We all make mistakes we wish we could take back. Tell me about a time you wish you’d handled a situation differently with a colleague.
Tell me about a time you needed to get information from someone who wasn’t very responsive. What did you do?

ABILITY TO ADAPT
Tell me about a time you were under a lot of pressure. What was going on, and how did you get through it?
Describe a time when your team or company was undergoing some change. How did that impact you, and how did you adapt?
Tell me about the first job you’ve ever had. What did you do to learn the ropes?
Give me an example of a time when you had to think on your feet in order to delicately extricate yourself from a difficult or awkward situation.
Tell me about a time you failed. How did you deal with the situation?
TIME MANAGEMENT SKILLS

Tell me about a time you had to be very strategic in order to meet all your top priorities.

The first job that taught me to be strategic with my priorities was bartending. As a bartender I learned the importance of preparation, of using my time well and of automating any process I could.

When I started bartending, I would often run out of things mid-shift: fruit, liquor, receipt paper, pens. Generally customers expected the bartender to be fast and when I had to stop making drinks just to refill fruit or leave the bar to find receipt paper, this hampered my ability to do my job (and make more money). Soon I began my shifts by stocking everything I needed, in easily accessible spaces (fruit in the fridge closest to the garnishes, receipt paper behind the printer, extra pens in the drawer below the printer, etc.).

An extension of this preparation was the importance of using my time well. Any moment I spent not making a drink, I could use to re-stock or clean up. I was constantly setting my future self up for success by keeping myself busy.

One of the last steps to making myself the most efficient bartender I could be was familiarizing myself with my tools and systems, and training myself to do things in a somewhat automated way. This meant a variety of things: if a customer ordered a vodka/soda and gin/tonic, I always gave the vodka drink one straw and the gin drink two so I never had to remember which was which - add a tequila soda to that and the tequila drink would always get 2 limes while the others got 1; if I was managing two transactions at once - one cash and one credit card - I would always process cash first because I could make change for one transaction while the credit processed for the second transaction; I could even make a round of drinks for a separate customer while I processed a credit card transaction.

These basic lessons about how to prepare, use my time and build processes into my muscle memory in order to increase efficiency have been lessons I’ve carried into every job and responsibility I’ve taken on since then.

Describe a long-term project that you managed. How did you keep everything moving along in a timely manner?
Sometimes it’s just not possible to get everything on your to-do list done. Tell me about a time your responsibilities got a little overwhelming. What did you do?
At my previous job, I would delegate tasks when I got overwhelmed.

As a manager at the front desk of a hotel, I spent each shift in front of guests, responding immediately to each request and/or issue that arose, whether it was from a guest in front of me, on the phone, or via email. Amidst these requests, I also had daily responsibilities such as to assign rooms to arriving guests, ensure all guests scheduled to depart in fact left, resolve billing issues and log/track all guest issues and preferences. On top of that, it was my responsibility to regularly ensure all employees followed procedure, track inventory of employee uniforms and guest packages and write/revise standard operating procedures for the department as well as train the team on new procedures and systems. I would not describe myself as being overwhelmed often but being extremely busy was a daily occurrence; myself and my team usually left our shifts exhausted.

Although I shared certain tasks with team members - namely concierge requests - there were certain things only I could handle. In the times I was overwhelmed, it was usually because I had received several concierge requests but also had multiple guest and/or billing issues to resolve. On these occasions, I would order my tasks by what was the most time sensitive and delegate the highest priority one that I could hand off. Next I would tackle the highest priority task that only I could work on; often resolving guest issues involved multiple departments so if I needed the help of another department I would ask them to start working on it and complete other tasks while they did; ideally by the time they completed their part, I would have finished my other tasks, could loop back to that initial problem and resolve the issue.

Tell me about a time you set a goal for yourself. How did you go about ensuring that you would meet your objective?
Give me an example of a time you managed numerous responsibilities. How did you handle that?

COMMUNICATION SKILLS
Give me an example of a time when you were able to successfully persuade someone to see things your way at work.
Describe a time when you were the resident technical expert. What did you do to make sure everyone was able to understand you?
Tell me about a time when you had to rely on written communication to get your ideas across to your team.

 In my role at Adafruit Industries, I led meetings for my team of managers each week. After each meeting I sent notes on what we discussed. I was always acutely aware of sending notes that succinctly but fully communicated an idea - for example if we had discussed reviews the note might read “review feedback for John due next Thursday by 6pm” instead of “review feedback due next week”. My sense was that the notes should be a complete reference point in themselves so my team could build their own workflow without having to come to me with every last question. It also allowed me to evaluate their performance - to see how much they were paying attention and how resourceful they could be. 

Give me an example of a time when you had to explain something fairly complex to a frustrated client. How did you handle this delicate situation?
Tell me about a successful presentation you gave and why you think it was a hit.

MOTIVATION AND VALUES
Tell me about your proudest professional accomplishment.
My proudest professional accomplishment involved receiving recognition from a team member I managed. This employee was one I worked with for years; towards the end of our time together she noted that she preferred working with me because while she respected me as her manager and trusted me to give her the best direction when needed, she never felt like I treated her differently because we held different titles. She felt that I spoke to her the same way I spoke to other managers and superiors. I feel that treating all coworkers with the same respect regardless of their role is important to building and maintaining a team. I was proud to be recognized for this.
Describe a time when you saw some problem and took the initiative to correct it rather than waiting for someone else to do it.
Tell me about a time when you worked under close supervision or extremely loose supervision. How did you handle that?
Give me an example of a time you were able to be creative with your work. What was exciting or difficult about it?
Creating my portfolio was a great exercise in creativity. It was exciting to consider how I wanted to represent myself through the visuals and content of my own website and a bit intimidating to think of all the possibilities. I really enjoyed the freedom to explore what was out there and only wish I had more time to really research what effects and styles I could apply. The most difficult part of the project was the thing that is always most difficult for me: getting started. For me, getting started on the right foot is important to my process; it sets the tone for the rest of the project, it allows me to envision the path ahead (and bring that path to life). I typically spend a good amount of time sitting with ideas and weighing their truths - the heavier they are, the truer they are - because if I don’t start from an honest place I feel a bit lost.
Tell me about a time you were dissatisfied in your work. What could have been done to make it better?

5 year plan = mission-driven company
Solutions engineers - work with clients
Three top hard skills: JavaScript, Express, React
Three top soft skills: communication, patience, diligence
Weakness:
What skills and what impact did you make in previous roles that will transfer into SE?
Communicating solutions to clients -
*Questions for
What does day to day look like?
How do you support your employees while they’re struggling?
How do you encourage your employees to move forward when you see they’re succeeding?
**what are the top 2-3 skills you’ve taken from previous role?
Pitch should be short
Present-past-future
S.T.A.R.T. method - helps you craft behavioral interview questions
My range is $70,000 - $80,000 and I’m open to negotiation. I do take the culture and benefits into consideration and I’d have to see the offer in writing before making a final decision.
What are the typical hours for this role?
