# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?

Fully responsive websites continuously render a single layout for a given page, that 'responds' in real-time to whatever the current browser size is - regardless of what device you're on. Responsive design continuously 'responds' to the browser size and re-renders the page fluidly - essentially having a sensible layout answer for any possible browser size. Adaptive sites typically have several discreet views of the page that are pre-defined, and targeted at different devices. Each view is rendered 'discreetly' when that device is detected. Adaptive websites will "snap" their view into place when a specific environment is detected, while responsive sites will fluidly transition / re-render between environments without any visible snapping.

2. Describe what it means to be mobile first vs desktop first.

Mobile first vs desktop first refers to which platform the developer/designer thinks of, and builds around as the "starting point" of the user experience. Recently there's a trend towards mobile-first due to the huge growth in mobile web usage. A mobile-first experience typically implements "progressive enhancement" meaning that you first (as the developer) build and optimize the mobile experience - and then as your platform becomes larger (mobile -> tablet -> desktop) gradually add in features that "enhance" the experience, 'progressively'. Conversely, the desktop first approach starts with the desktop experience - aka you build it first - and you assume that this is the default/most-important experience to build. Then as your platform becomes smaller (desktop -> tablet -> mobile) you strip away features .. this is referred to as "graceful degradation" and is often argued to provide a less good overall experience for all platforms.

3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

The initial impetus for implementing a % for default font-size is to accommodate for the default font-size preferences the user has set on their browser. In other words you can't assume that every browser's default font-size is 16px and then build a pixel-driven layout around that assumption. That said, given that the standard default browser font-size is 16px, setting font-size: 62.5% on the html tag is a great median-case heuristic, and will mean that 1 rem unit = 62.5% of 16px which is 10px. This makes using rem units really easy going forward, and means that in the median case we're working with multiples of 10px. EG 1.5rem = 15px.

4. How would you describe preprocessing to someone new to CSS?

CSS was built a long time ago. More recently some smart programmers have thought up ways that CSS could be better. A lot of these ways borrow concepts from 'scripting' languages - concepts like variables and functions. So there are now some CSS-like languages that have these improvements in them. The problem is that browsers can't read and render these languages by default. So these same smart programmers invented programs that will 'translate' their improved CSS languages into vanilla CSS that the browser knows how to deal with. Think of it sort of like Google Translate where you're going from something that looks basically like CSS, with some new features, over to vanilla CSS.

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

In preprocessing as a concept (ie not an implementation like LESS or SASS specifically) - my favorite idea you can design enhancements into a language (eg variables, mixins) that then are available instantly to all web users because preprocessor compiles these enhancements into vanilla CSS. It's the idea of making the dev experience better today, without having to wait for the underlying standards/protocols to evolve.

My least favorite facet is the ever-bloating complexity of modern dev environments (ie having to run a preprocessor in the background) as "just one more thing you have to worry about".

In LESS , specifically, my favorite concept is nesting. It's easier for the human eye to read and understand which makes development faster and is beneficial for collaboration. It also maps more closely to the HTML that it's styling, as HTML is also a nested structure. Additionally, you can reduce the number of classes / ids that clutter up your HTML because nesting allows you to implicitly target elements without them.

The thing I am having the most trouble dealing with is with the compiler at all times. One semicolon out of place and it breaks. This of course has its upside - you can't make mistakes and not realize you've made them. But it feels like a harsher environment than vanilla CSS.


You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Follow these steps to set up your project:

### Git Set up

- [ ] Create a forked copy of this project.
- [ ] Add your project manager as collaborator on Github.
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [ ] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [ ] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [ ] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [ ] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [ ] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [ ] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [ ] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [ ] Add a viewport meta tag to the head of your index.html page

* [ ] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [ ] Navigation Styles: Use the `navigation.less` file for styling.

* [ ] Main Content Styles: Use the `home-page.less` file for styling

* [ ] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [ ] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [ ]  Use at least 2 parameters to create your button

* [ ] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription