### Lesson 01 
## Vanilla JavaScript Form validation

#### Why

So we have a form that looks like this 

```html
<html>
    <head>
    </head>
    <body>
        <form>
            <input name="email" type="email" value="" placeholder="Please enter your Email Address"/>
            <input name="name" type="text" value="" placeholder="Please enter your name"/>
            <input name="submit" type="submit" value="Register"/>
        </form>
    </body>
</html>
```

When we fill out this form and submit it, it doesn't go anywhere or do anything. The person submitting the form has no idea what's going on and what the form is doing. Nor if the values they entered were accepted or correct.

So in this lesson we want to achieve the following

- Show error messages to user when name and email are incorrect
- Show the user the value they entered in another section away from the form (this is just to prove we can get the values for when we want to use the form to register the data with a server, we'll cover this later).

But the achieve the above, we need to cover some basics in JavaScript. We need to 

- Wait for the DOM to load (otherwise all elements can't be found)
- Add an event listener to the form when it is submitted
- Prevent the form from doing the default action (submitting itself to another page)
- Find the form values, check if they are accepted
- If the values are not ok, add error messages to show the user
- If all the values are ok, then we want to display these values in a box under the form

#### Add your script tag

First step (which we didn't mention) is to add the script tag to the `head` part of your document.

```html
<script>
</script>
```

#### Loading the DOM (document.on('ready'))

So! The DOM. Basically it's all your elements, this is the dom `<body>...</body>`. But not quite. The DOM is all of your elements but loaded into javascript which can take a while to load when you load the page! So if you want to use JavaScript and interact with the DOM, it's best to wait for it to load which we can do with an event listener; this listens to when the document is loaded and ready for us to play with.

```html
<script>
document.addEventListener('', function() {
    // Now the DOM is loaded and ready for us to manipulte!
    console.log('Hello Beth, I have finished loading!');
});
</script>
```

#### Form event listener

So now we're going to add our event listener to the form so when it's submitted our code will run. 

Firstly we need to add an id attribute to our form so we can reference it in our code. `<form id="register-form">` <-- adding this we can now reference our form with it's `id`. It's very important! We can reference it in CSS like we've done before `#register-form` and in JavaScript `document.getElementById('register-form')`. 

> Important part is we're referencing our form so we can use it in our script.

> the `id=""` is an attribute

```javascript 
document.addEventListener('', function() {
    // Now the DOM is loaded and ready for us to manipulte!
    console.log('Hello Beth, I have finished loading!');
    const form = document.getElementById('register-form');
    console.log('form', form);
});
```

> `const form` is declaring a variable called form. Variables are like storage. Here we are storing the element to the variable `form`.

#### Event Listeners



