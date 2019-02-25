# CSS Tutorial

Check out the [slides](https://docs.google.com/presentation/d/1JNq8nGdHXat6GMdY6SzlzCN4mtup2vhZORiJ990PqwM/edit?usp=sharing) first before proceeding. 

![poster](https://scontent-kut2-2.xx.fbcdn.net/v/t1.0-9/30724226_2073600839334824_3108705559454114921_n.jpg?_nc_cat=103&_nc_ht=scontent-kut2-2.xx&oh=9792658d04eea90c5d4773fdda4fb163&oe=5D25BFB6)

## Part 1: Link to .CSS file

1. Open **accessories.html** and add following element in the **head** section.

	```html
	<link rel="stylesheet" type="text/css" href="style.css">
	```

2. Open **style.css**
3. Create a body selector. 
4. Add **background-color** property.

	```css
	body {
		background-color: black;
	}
	```

5. Check if website color changed. 
6. Use browser developer tools to find out the banner's hex color code.
7. Change the value of **background-color** to the Hex code.


## Part 2: Contain item in a border

1. Create a class named **container** above earring image element.

	```html
	<div class = "container">
		<img src = "earrings.jpg" alt = "Diamond Earings">
	```

2. Close the container below the **Order button** element.

	```html
			</button>
		</div>
	</div>
	```

3. Open **style.css** and add **container** class as a selector, create a 10px **border**.
4. Set the **width** to 285px and **padding** to 60px and see what happens.

	```css
	.container {
		border: 10px solid block;
		width: 285px;
		padding: 60px;
	}
	```


## Part 3: Centering the container

1. Remember, to center elements you only need to use **display** and **margin** properties.

	```css
	display: block;
	margin: auto;
	```

2. Add these two properties into **container** class.
3. Refresh the page and the find the container in the middle.
4. Next step is to center the items inside the container.
5. Create a selector that selects everything inside **container**.

	```css
	.container * {
		display: block;
		margin: auto;
	}
	```

6. Refresh the page and see the elements inside the container centered.
7. Notice that the 'Click here' link has became a block element.
8. To fix that, select '**a**' in **container** and set it to inline.

	```css
	.container a {
		display: inline;
	}
	```


## Part 4: Floating card with shadows

1. First step, open **accessories.html** file and locate the table element.
2. Set the table border to 0. 

	```html
	<table border = "0" style = "text-align: center;">
	```

3. Meanwhile, remove the colons ':' from the table labels.
4. Now go back to **style.css**.
5. Locate **container** class and set the **background-color** to white. 
7. Add **border-radius** property with a value of 20px to change the four corners of the card to rounded.

	```css
	.container {
		...
		background-color: white;
		border-radius: 20px;
	}
	```

8. Next, remove or comment the border property.
9. Add a box-shadow property with the following values.

	```css
	.container {
		...
		border: 1px solid white;
		box-shadow: 2px 6px 25px rgba(0,0,0,0.1);
	}
	```

10. In RGBA, RGB - Red, Green, Blue. A stands for Alpha. It is used for setting the opacity of the color.
11. Now we can add some extra **padding** to the **paragraph** and **image** elements to make it look cleaner.

	```css 
	.container p {
		padding: 30px 8px;
	}
	
	img {
		padding-bottom: 40px;
		display: block;
		margin: auto;
	}
	```


## Part 5: Task - Reuse card in order form

1. Open **orderForm.html** and link to **style.css**.
2. Copy the same banner(change to max-width:100% in both pages) from **accessories.html** to show consistency. 
3. Some tips: 
	* You don't need to touch the CSS file, just repeat steps 1 & 2 of **Part 2**. 
	* To fix the messy form elements, take a look at step 8 of **Part 3**.


## Part 6: Fixing the button

1. Let's go back to accessories page.
2. Take a look at the order button, there is an underline because it is a link.
3. Also notice that only the link can be clicked, where the rest of the button area is unclickable.
4. To fix this, go to **accessories.html** and scroll to the bottom to locate the button element.
5. The mistake is that the **button element** is containing the **link element**.
6. Change both the elements as below: 
	
	```html 
	<a href = "orderForm-done.html"><button type = "button">Order</button></a>
	```

7. To remove the underline, go to **style.css** and locate **.container a** that you created in step 8 of Part 3.
8. Add in a new property called **text-decoration** and set the value to **none**.

	```css
	.container a {
		...
		text-decoration: none;
	}
	```


## Part 7: Redesigning the button

1. Now that the button is fixed, we can start adding some colors to it.
2. First, add a **button** selector in **style.css**.
3. Add **padding** with the value of top/bottom: 15px, left/right: 30px.
4. Set the **border-radius** to 10px.

	```css
	button {
		padding: 15px 30px;
		border-radius: 10px;
	}
	```

5. Next, remove the **border** and set a **background-color**to the button
6. Add **shadows** to the button to make it pop out.

	```css
	button {
		...
		border: 0px;
		background-color: #FFB0BE;
		box-shadow: 1px 4px 6px rgba(0,0,0,0.1);
	}
	```

7. Change the font **color**, **weight** and **size**.

	```css 
	button {
		...
		color: white;
		font-weight: bold;
		font-size: 13px;
	}
	```

8. Now, let's add a mouse hover effect on the button.
9. Create a new **button**:hover selector.
10. Copy the **box-shadow** property from Step 6 and set it wider and darker.

	```css 
	button:hover {
			box-shadow: 1px 4px 16px rgba(0,0,0,0.2);
	}
	```


## Part 8: Create more items

1. Before duplicating the item, create a **items-container** div class that contains all the items.
2. To avoid any hassle, you should **fold your code** in Sublime Text.
3. First, locate the **container** class, it is under banner image.
4. Move your cursor to the line number, very left side of the editor.
5. An arrow will appear, click the one next to **container** class and it will collapse everything inside.
6. Now, you can add the **items-container** class without scrolling all the way to the bottom.

	```html
	<div class="items-container">
		<!-- container class starts here -->
		<div class="container"> 
		...
		<!-- container class ends here -->
		</div>
	</div>
	```

7. You can easily duplicate the items now, just highlight the container class, copy and paste.
8. After you're done, you will notice that the items sorts in only one column. 
9. To fix that, go to **style.css** and locate **container** class, change **display** value to **inline-block**.
10. Also, change the **margin** from **auto** to **10px**.

	```css
	.container {
		margin: 10px;
		display: inline-block; 
		/* allows the element to have height and width but still acts as inline */
		...
	}
	```

11. All the items will move to the left now, to center it, use the **items-container** class you've created.

	```css 
	.items-container {
		text-align: center;
	}
	```


## Part 9: Adding a footer

1. Go to **accessories.html** and scroll to the bottom, add a **footer** tag above the closing **body** tag.

	```html 
		...
		<footer><p> Copyright © Sunway Tech Club 2018 </p></footer>
	</body>
	```

2. Go back to **style.css** and create a **footer** selector. 
3. Add **background-color**, **height**, **color** and **text-align** properties.
4. Set it as a **block display** and add some **paddings** at the top.

	```css
	footer {
		background-color: #394258;
		height: 70px;
		color: lightgrey;
		text-align: center;

		display:block;
		padding-top: 90px;
	}
	```

4. Notice the footer did not fill to the edges of the page, to fix this, go to **style.css**.
5. Scroll to the top and add a **margin** property with a value of 0 in the **body** selector.

	```css 
	body {
		...
		margin: 0;
	}
	```

6. Now let's add social media icons to the footer. Open **accessories.html** and add this in the **head** section.

	```html 
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

	```

7. The link element above links to an external CSS file from an online source.
8. Now, scroll down to **footer** section and add these classes inside.

	```html
	<footer>
		<a class="fa fa-facebook"></a>
		<a class="fa fa-instagram"></a>
		<a class="fa fa-twitter"></a>
		<p>Copyright © Sunway Tech Club 2018</p>
	</footer>
	```

## Part 10: Changing the font

1. Always leave changing fonts to the last so you can have time to pick the font you prefer. 
2. Go to [fonts.google.com](http://fonts.google.com/) to look for fonts.
3. Some fonts don't look good in paragraph so make sure you select paragraph to check.
4. I have chosen Alegreya Sans for this demonstration, click the red 'plus' logo at the top right corner.
5. There will be a bar at the bottom, click to open it and select **@import**.
6. Copy the link and paste it at the top-most section of **style.css**.
7. Then, add **font-family** property in **body** selector to apply the font.

	```css
	@import url('https://fonts.googleapis.com/css?family=Alegreya+Sans');
	body {
		...
		font-family: 'Alegreya Sans', sans-serif;
	}
	```

8. Congratulations! You have completed all the parts. 
