## __CycleConf 2017__
We are really excited to announce CycleConf 2017, a 3-day hackfest and conference, for JavaScript developers.
Get your ticket [here!](http://cycleconf.com/#tickets)

Learn about Cycle.js from some of the most talented JavaScript professionals and Cycle.js experts in the world. Join a team or hack freely during the conference in a unique 3-day experience. 

#### Location and dates
* Stockholm, Melt Bar
* 21st – 23rd of April

#### Also included in the ticket
* Lunch, Saturday - Sunday
* Dinner, Friday - Saturday
* Coffee, Fruit and a Saturday afternoon snack

#### Key benefits
* Deepen your knowledge in Cycle.js, regardless of if you are a beginner or an expert
* A truly international experience with attendees and speakers from all over the world
* Be part of a growing open source community

<<<<<<< HEAD
Join us on Gitter for CycleConf chatter.

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/cycleconf/cycleconf.github.io)
=======
Cycle's core abstraction is your application as a pure function `main()` where inputs are read effects (*sources*) from the external world and outputs (*sinks*) are write effects to affect the external world. These I/O effects in the external world are managed by *drivers*: plugins that handle DOM effects, HTTP effects, etc.

The internals of `main()` are built using Reactive Programming primitives, which maximizes separation of concerns and provides a fully declarative way of organizing your code. The *dataflow* is plainly visible in the code, making it readable and traceable.
>>>>>>> cyclejs/master

Follow us on Twitter for the latest CycleConf updates. Our official twitter hashtag is __#CycleConf__

<<<<<<< HEAD
<a href="https://twitter.com/cycleconf" class="twitter-follow-button" data-show-count="false">Follow @cycleconf</a> <script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+'://platform.twitter.com/widgets.js';fjs.parentNode.insertBefore(js,fjs);}}(document, 'script', 'twitter-wjs');</script>

We are organizing this conference to connect cyclists from around the world, for a time of tech talks and presentations, and making a space for focused contributions upon Cycle.js and its ecosystem.

## Sponsors

### Gold Sponsors

<img src="img/verizon.png" style="width:120px!important;min-width:0">

Verizon Labs is changing the way we communicate by building innovative products and solutions to fuel the telecommunications industry.
[Twittter](https://twitter.com/VerizonLabs)



#### Become a Sponsor

To make CycleConf 2017 possible we need help from some generous sponsors, learn more about how you can be part of the effort <a href="./sponsor.pdf">here</a>

## Speakers

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/jan.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Jan van Brügge</h4>

<p style="margin-top:0">Self-taught programmer, I make everything from Cycle.js web apps to satellite control software.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: Property based testing in Cycle.js</p>
<p style="margin-top:0">How to explore mathematical properties in pieces of your code and how to use them to generate unit tests.</p>

<p style="text-align:right">
<a href="https://github.com/jvanbruegge">Github</a>
<a href="https://twitter.com/SuperManitu">Twitter</a>
</p>
</div>
<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/nick.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Nick Johnstone</h4>

<p style="margin-top:0">I am passionate about building tools to enable people to build better software and a better world.
 When not doing that, I enjoy skateboarding and music.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: The Hitchhiker's Guide to Cycle.js</p>
<p style="margin-top:0">A story about my journey so far working in the Cycle.js community.</p>

<p style="text-align:right">
<a href="http://github.com/Widdershin/">Github</a>
<a href="https://twitter.com/widdnz">Twitter</a>
</p>
=======
{% highlight text %}
npm install xstream @cycle/xstream-run @cycle/dom
{% endhighlight %}

{% highlight js %}
import {run} from '@cycle/xstream-run';
import {div, label, input, hr, h1, makeDOMDriver} from '@cycle/dom';

function main(sources) {
  const sinks = {
    DOM: sources.DOM.select('.field').events('input')
      .map(ev => ev.target.value)
      .startWith('')
      .map(name =>
        div([
          label('Name:'),
          input('.field', {attrs: {type: 'text'}}),
          hr(),
          h1('Hello ' + name),
        ])
      )
  };
  return sinks;
}

run(main, { DOM: makeDOMDriver('#app-container') });
{% endhighlight %}

<div class="example-hello-world-container"></div>

<div class="homepage-features" markdown="1">
## Functional and Reactive

Functional enables "predictable" code, and Reactive enables "separated" code. Cycle.js apps are made of pure functions, which means you know they only take inputs and generate predictable outputs, without performing any I/O effects. The building blocks are reactive streams from libraries like [xstream](http://staltz.com/xstream), [RxJS](http://reactivex.io/rxjs) or [Most.js](https://github.com/cujojs/most/), which greatly simplify code related to events, asynchrony, and errors. Structuring the application with streams also separates concerns, because all [dynamic updates to a piece of data are co-located](/observables.html#reactive-programming) and impossible to change from outside. As a result, apps in Cycle are entirely `this`-less and have nothing comparable to imperative calls such as `setState()` or `update()`.
>>>>>>> cyclejs/master
</div>

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/justin.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Justin Woo</h4>

<<<<<<< HEAD
<p style="margin-top:0">Justin is a failed material scientist who now spends his time writing JavaScript for work and Purescript/Haskell for fun. He now lives in Finland as a result of being Twitter friends with André.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: Simpler Cycling with Megadrivers:</p>
<p style="margin-top:0">Writing cyclejs apps can be weird when you have to work with separate streams fed into drivers. This talk proposes one way to get both stronger typing and a simpler model for your cycle projects by combining them into a 'megadriver'.</p>

<p style="text-align:right">
<a href="http://github.com/justinwoo/">Github</a>
<a href="https://twitter.com/jusrin00">Twitter</a>
</p>
=======
Cycle.js is a framework with very few concepts to learn. The core API has just one function: `run(app, drivers)`. Besides that, there are **streams**, **functions**, **drivers** (plugins for different types of I/O effects), and a helper function to isolate scoped components. This is a framework with very little "magic". Most of the building blocks are just JavaScript functions. Usually the lack of "magic" leads to very verbose code, but since functional reactive streams are able to build complex dataflows with a few operations, you will come to see how apps in Cycle.js are small and readable.
>>>>>>> cyclejs/master
</div>

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/aron.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Aron Nyborg Allen</h4>

<<<<<<< HEAD
<p style="margin-top:0">Aron is passionate about building digital interfaces. With an eye for aesthetics in design and engineering he has found a new home with Cycle.js </p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: Multi-threading in Cycle.js.</p>
<p style="margin-top:0">The architecture of Cycle.js opens up for new utilizations of Web Workers. Aron will walk through his journey of running UI components in a Web Worker.</p>

<p style="text-align:right">
<a href="http://github.com/aronallen/">Github</a>
<a href="https://twitter.com/newfoort">Twitter</a>
</p>
=======
Drivers are plugin-like simple functions that take messages from sinks and call imperative functions. All I/O effects are contained in drivers. This means your application is just a pure function, and it becomes easy to swap drivers around. The community has built drivers for [React Native](https://github.com/cyclejs/cycle-react-native), [HTML5 Notification](https://github.com/cyclejs/cycle-notification-driver), [Socket.io](https://github.com/cgeorg/cycle-socket.io), etc. Sources and sinks can be easily used as [Adapters and Ports](https://iancooper.github.io/Paramore/ControlBus.html). This also means testing is mostly a matter of feeding inputs and inspecting the output. No deep mocking needed. Your application is just a pure transformation of data.
>>>>>>> cyclejs/master
</div>

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/raquel.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Raquel Moss</h4>

<<<<<<< HEAD
<p style="margin-top:0">Code, cats, feminism, and functional programming.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: Organising your code in Cycle.js - An ex-librarian tries to put things in order.</p>
<p style="margin-top:0">In my quest to create a neatly-organised Cycle.js component, I tried several different ways of arranging my code. Let's look at each, discuss what I've learned, the benefits and the drawbacks, and how we might innovate in the future.</p>
=======
In every Cycle.js app, each of the stream declarations is a node in a dataflow graph, and the dependencies between declarations are arrows. This means there is a one-to-one correspondence between your code and *minimap*-like graph of the dataflow between external inputs and external outputs.
>>>>>>> cyclejs/master

<p style="text-align:right">
<a href="http://github.com/raquelxmoss/">Github</a>
<a href="https://twitter.com/raquelxmoss">Twitter</a>

</p>
</div>
<<<<<<< HEAD

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/gleb.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Gleb Bahmutov</h4>

<p style="margin-top:0">JavaScript ninja, image processing expert, software quality fanatic.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: Web application quality beyond testing.</p>
<p style="margin-top:0">A successful web application should work. How do you deliver a single component or a complete application that never breaks; that is simple to understand and reuse? Let us discuss what the modern quality tools can do, and where they will go next.</p>

<p style="text-align:right">
<a href="http://github.com/bahmutov/">Github</a>
<a href="https://twitter.com/bahmutov">Twitter</a>
</p>
=======
<div class="dataflow-minimap-code" markdown="1">
{% highlight js %}
function main(sources) {
  const decrement$ = sources.DOM
    .select('.decrement').events('click').mapTo(-1);

  const increment$ = sources.DOM
    .select('.increment').events('click').mapTo(+1);

  const action$ = xs.merge(decrement$, increment$);
  const count$ = action$.fold((x, y) => x + y, 0);

  const vtree$ = count$.map(count =>
    div([
      button('.decrement', 'Decrement'),
      button('.increment', 'Increment'),
      p('Counter: ' + count)
    ])
  );
  return { DOM: vtree$ };
}
{% endhighlight %}
</div>
>>>>>>> cyclejs/master
</div>

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/thomas.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Thomas Belin</h4>

<p style="margin-top:0">I am a pure function of Time</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: UI as Pure Functions of Time.</p>
<p style="margin-top:0">What if we considered Time as a fundamental input of our applications?</p>

<p style="text-align:right">
<a href="http://github.com/atomrc/">Github</a>
<a href="https://twitter.com/atomrc">Twitter</a>
</p>
</div>

<div style="margin-bottom:2em;padding:1em;background:#f8f8f8;border-radius:90px 0 0 0">
<img src="/img/andre.jpg" class="speaker" style="border-radius:100%;float:left;width:128px;margin-right:1em;" />
<h4 style="margin-top:0;margin-bottom:0.5em;font-weight:bold">Andre Staltz</h4>

<p style="margin-top:0">I worked at Futurice and authored Cycle.js, and now open source is my main occupation.</p>
<br>
<p style="margin:0;font-weight:bold;clear:left">Speaks on: The Past, Present, and Future of Cycle.js</p>
<p style="margin-top:0">Let's take a look at how Cycle.js was born, and how suggestions from the community were crucial to shape it and become what it is today. Then, let's see what possibilities we have for the next significant updates to the framework, and beyond.</p>

<p style="text-align:right">
<a href="http://github.com/staltz/">Github</a>
<a href="https://twitter.com/andrestaltz">Twitter</a>
</p>
</div>

## Hackathon

Like last year CycleConf won't just be a place to learn from our amazing speakers. It will also be a place to build upon the ecosystem.
After an open pitching session teams can form around ideas to build technologies over the weekend. Every team will have an opportunity to present their work Sunday.
It might sound a bit intimidating, but it was a great success last year, even beginners had a great time in a learning and explorative atmosphere.

## Lightning talks

During CycleConf every participant will have an opportunity to share something in a 5-minute format.
You will be able to register your lightning talk during the conference.

## Tickets

<a name="tickets"></a>
<tito-widget event="futurice/cycleconf-2017"></tito-widget>

Our aim is to keep CycleConf to accessible and affordable. So we are happy to announce 1000  SEK ticket price for students and 2000 SEK ticket price for the rest of us! We also offer day passes at 700 SEK each. We will cover most conference expenses through sponsorships, if you are interested in sponsoring CycleConf please contact emma.sjostrom@futurice.com for details.

_1000 SEK is ~100 EUR_

## Schedule

| **Friday, 21/4** | |
|---|---|
| 13:00 | Registration |
| 14:00 | Opening Keynote |
| 15:00 | Talks - Jan van Brügge & Nick Johnstone |
| 17:00 | Idea pitching, team forming and hacking |
| 19:30 | Dinner at venue |
| 21:00 | Socializing and/or hacking |
| 00:00 | Venue closing |
| **Saturday, 22/4** | |
| 8:00 | Doors opening - Morning hacking |
| 10:00 | One day pass - registration |
| 11:00 | Talk - Thomas Belin |
| 12:00 | Lunch at venue |
| 13:00 | Talks - Raquel Moss, Justin Woo, Gleb Bahmutov |
| 16:00 | Hacking (bar opens at 17:00) |
| 19:00 | Evening lightning talks |
| 20:00 | Common dinner and socializing outside of venue |
| **Sunday, 23/4** | |
| 8:00 | Morning hacking |
| 10:00 | One day pass - registration |
| 11:00 | Talk - Aron Nyborg Allen |
| 12:00 | Lunch at venue |
| 13:00 | Talk - André Staltz |
| 14:00 | Demo code from hacking |
| 15:00 | Thank you and goodbye! |

## Venue
<<<<<<< Updated upstream
Our venue for the conference is [Melt Bar](http://www.meltbar.se/story). This 1920's style cocktail bar is located near the city center, which offers a wide variety of restaurants, bars and other services near by. For CycleConf, Melt Bar will offer a unique surrounding for a close community feeling. You can get there by metro taking any of the lines 17, 18, or 19 to Hötorget station.
=======
We are happy to announce [Skofabriken]( http://summit.se/en/meeting-facilities/skofabriken/), "The shoe factory" as our CycleConf venue this year! In this hundred-year-old factory building, hacking and learning will take place in rooms named after some of the greatest minds known to human kind. Located in Hornstull, a trendy area on the south-bank of Stockholm, it is not only easy to get to, but also surrounded by a great variety of bars and restaurants.

## Sponsorships


To make CycleConf 2017 possible we need help from some generous sponsors, learn more about how you can be part of the effort <a href="./sponsor.pdf">here</a>
>>>>>>> Stashed changes

## CycleConf 2016
CycleConf 2016 was a great success and acted as the launch pad for the next major version of Cycle.js, <a href="/2016">click here to see the talks, and to read more about CycleConf 2016</a>.

<<<<<<< HEAD
## Code of Conduct

We want CycleConf to be a fun and fruitful event for everyone, regardless of their gender, sexual orientation, disability, physical appearance, body size, race, or religion.
Harassment will not be tolerated at the conference.
If you witness intolerable behavior during the conference, please get in touch with the organizers. We care.
Be nice, welcoming, and respectful.
=======
## Learn it in 1h 37min

<p>
  {% include /img/egghead.svg %}
</p>

Got 1 hour and 37 minutes? That is all it takes to learn the essentials of Cycle.js. Watch [**this free Egghead.io video course**](https://egghead.io/series/cycle-js-fundamentals) given by the creator of Cycle.js. Understand Cycle.js from within by following how it is built from scratch, then learn how to transform your ideas into applications.

<script src="https://opencollective.com/cyclejs/banner.js"></script>

## Supports...

- [**Virtual DOM rendering**](https://github.com/cyclejs/cyclejs/tree/master/dom)
- [**Server-side rendering**](https://github.com/cyclejs/cyclejs/tree/master/examples/isomorphic)
- [**JSX**](http://cycle.js.org/getting-started.html)
- [**TypeScript**](https://github.com/cyclejs/cyclejs/tree/master/examples/bmi-typescript)
- [**React Native**](https://github.com/cyclejs/cycle-react-native)
- [**Time traveling**](https://github.com/cyclejs/cycle-time-travel)
- [**Routing with the History API**](https://github.com/cyclejs/history)
- [**And more...**](https://github.com/cyclejs-community/awesome-cyclejs)
>>>>>>> cyclejs/master
