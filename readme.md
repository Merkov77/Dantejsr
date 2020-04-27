# Dantejsr

## npm

> npm i dantejsr

## cdn

> <script src='https://unpkg.com/dantejsr'></script>

Dantejsr is a bookstore developed in javascript, capable to read the code HTML and taking all the identifiers of component, be the id name, or class, creating with these one function for each one, which will be able to receive all the properties that you want to include; Although by default the orientation of the module has been addressed in fast styles, css stackable with bootstrap, and events. The motto that I want to ensure chases the functional and interactive design. 

Certainly, you will ask yourself What do I refer myself to?. As in HTML each tag is in herself an independent element, in the javascript also, but now with the ability to dynamically invoke components within others.

> Here the explanation of my vision:

Design - the graphic Part
Functional - the logical Part
Interactive - flexibility

So only we will have to think about something, to create, to lay plans, to encourage, and to add events interconnected between components HTML isolated, each one with your properties.

In order to lay plans you can use properties style, className, cheer up and events. For the logical part and additional functions to the design, the events in themselves are the required property. From here you are free to place the properties that you desire, for instance, if it is about an image, src, or of one to, href, etc. 

USE

If you unload and you install the intervening module npm, you owe enrutar his index.html to the code base of dantejsr. 

If you use cdn, you should simply place unpkg's script below the structure general web. You need to have a root like class compulsorily or go, there should be a main div where all your application is contained to be able to use this module, otherwise there will be conflict.

Example:


	<body>
		<div id="container">
			<div id="container">
			<div id="one"> Hi </div>
			<div id="two"> Bye </div>
			<div id="three"> Hello, I am Dante </div>
		</div>
		<script src='https://unpkg.com/dantejsr@latest'></script>

		<script type="text/javascript">
			//Use the module

			Dan.one({ click : () => three.innerHTML = "Thanks for visit me :)" })
			Dan.two({ click : () => three.innerHTML = "Bye friend" })

		</script>
	</body>


Just as you can see, Dan is enough writing the expression, once the component was followed of a method with the given name (be the one of tag or identifier), and indoors of the same an objecto with the properties. With Dantejsr you can invoke the names of other components within events of components already circumscribed, and assigning them properties, animations, functions and all that you desire. However in the example given only you have been able to  see as can invoke a component from another one and generating interactivity. But do not forget that you will be capable to make something like this:

<pre>
	Dan.box({
		className : "row bg-dark p-4",
		animate : {
			transition : [
				{
					transform : "scale(0.7)"
				},{
					transform : "scale(1)"
				}
			],
			config : { duration: 1000, iterations: 1}
		}
		click : () => alert("Hi world")
	})
</pre>

As in the previous case, I use css cared about but I do not place it here, however you can appreciate how properties pile.

You require to know some rules of use to avoid errors:

1.- Every element HTML can be invoked using the expression They Give
2.- Any property according to the standards right now known can be used except in the case of animations and events, at least like first property:


ANIMATIONS

In order to do animations it is obligatory to use this syntax inside the objecto, the only thing that can be personalized is the animation in herself, from to, and the configuration (duration of animation and number of repetitions or repetitions). In iterations you can use Infinity if you want animation to repeat itself infinitely, or circumscribing a number of times brand-name drug. Every property written in from, should be also written in to, otherwise there will be an error.

<pre>
	Dan.example({ //Format
		animate : {
			transition : [
				{/*from*/},{/*to*/}
			],
			config : { duration: time, iterations: n}
		}
	})

	Dan.example({
		animate : {
			transition : [
				{ color: "blue", background: "red" },
				{ color: "black", background: "white" }
			],
			config : { duration: time, iterations: n}
		}
	})
</pre>


EVENTS

For events

<pre>
	Dan.example({ //Format
		eventName : () => {
			//instructions
		}
	})

	Dan.example({
		eventName : () => {
			//instructions
		}
	})
</pre>

You can write the name of any event like key directly, and his value will be a function with the instructions. Within said function you can knock at other components, but you should take some details into account:

In order to call boxes, only while they are boxes like div, header, section, aside, footer, nav, article, etc.

<pre>
	Dan.component1({
		eventName : () => {
			component2.style.background = "blue"
		}
	})
</pre>

In order to call components like buttons or matches, however, you need to assign them one go, this only happens with these cases. Although it does not mean that you may call them using They Give, without no problem.


	<div class="box">Click here</div> 
	<button id="btn"> Click here </button>
	
<pre>
	Dan.box({
		click : () => btn.innerHTML = "Like"
	})

	Dan.btn({
		dblclick : ()=> alert("Hi world")
	})
</pre>

-----------------------------------------------

From a component you can also knock at the container for his name, after all it is a box.

There is another function that it enables working with names of class repeated, he is called Dan.common({}), where the keys of the object that he should contain, common the names of class will be, and your values the properties that will assign to all the elements HTML with the same name class, including logical functions, not only I style.

	<button class="btn1"> btn 1 </button>
	<button class="btn2"> btn 2 </button>
	<button class="btn1"> btn 1 </button>
	<button class="btn2"> btn 2 </button>
	
<pre>
	Dan.common({
		btn1 : {
			className:"btn btn-dark m-2",
			click : () => alert("Hi world")
		},
		btn2 : {
			className:"btn btn-primary m-2",
			click : () => alert("Bye world")
		}
	})
</pre>

In this example all the properties assigned to btn1 will devote themselves to each element HTML (in this case buttons) with the same high-class identifier. The same thing for btn2.


To use Dantejsr can be a great advantage in multiple senses,
It is easy, dynamic, interactive, flexible, and you have the possibility of extending They Give like object. You should not worry about the process of obtaining of elements in variables, neither suchlike nothing, only of creating like an artist of the frontend. The method common also proves to be very practical then, you can assign logical instructions to multiple elements with identifiers of class shared. 

Author: José Mavo, <jose.mavo.125@gmail.com>
