# Pills

> A simple, responsive, and tiny CSS grid for humans who don't like memorising all those cryptic codes like col-*-6 or something.
> [View the Demo -->](http://arkpod.in/pills)

## Why?
You must be thinking there are like a thousand grid frameworks. So why another one?? What's so special about this one??

Well, there are three types of people who use css grids in their own way -

* First - The ones who just memorize the cryptic codes like col-md-6 or whatever from their favourite CSS Framework like Bootstrap or Foundation. And not long before, I too was in this category using Bootstrap's grid all the time.

* Second - The ones who simplify the grids into simple partitions of the page. Like half of the page or one-third or something like that and process ahead with that. One of the best grid frameworks that is present for this category is [Gridism](http://cobyism.com/gridism/) which  actually inspired me to create Pills in the first place.

* Third -  The ones who like to count number of rows and columns but in a simple, human-like language.


### My thoughts
Trust me, Gridism is awesome and it simplifies stuff like anything. But still sometimes I felt the one-third, two-fifths, golden-small n all are a bit of confusing (_For me at least_). And Gridism is just a 5 column grid which can sometimes be a bit limiting compared to 12-column grids. 

> What if I wanted a simple 12-column layout and I could say that I want this div to be of size of **four columns**  and another div in the same row with size of **eight columns**?? 
> What if I wanted to use offsets??

This made me think about a grid which will focus on both the Second and Third category of people. A grid which can be used like traditional row-column layout or the more contemporary thinking of dividing the page like half or one-third or something.

So, Pills has two parts (Not literally, I mean there is just one file that is pills.css) - 

* First - This will have a 12 columns for that granular control but still would be simple enough like English language.

* Second - Inspired by Gridism thinking and catering to people who think fractional division of page is simpler.


## Installation

### 1. Get the files

The easiest way to use Pills in your project is via the [Bower](http://twitter.github.com/bower) package manager.

```sh
bower install pills
```

Also, you can download it using npm.
```sh
npm install pills
```

Otherwise, [download the zip folder from here](https://github.com/rohitkrai03/pills), extract it, and copy `dist/pills.min.css` into your project’s folder. Boom. Done.

### 2. Link the stylesheet

Add the following stylesheet to your HTML’s `<head>` section:

```html
<link rel="stylesheet" href="bower_components/pills/dist/pills.min.css">
```

**Note:** If you didn’t install using Bower, you need to adjust the path of the CSS file to match your file structure.

### 3. Viewport scale

Add the following meta tag to your HTML’s `<head>` section:

```html
<meta name="viewport" content="width=device-width,initial-scale=1">
```

Without this meta tag, mobiles and tablets might load your page as a scaled-down version of the desktop size, instead of resizing the content to match the device’s actual viewport width.

## Build
Install npm dev dependencies.
```sh
npm install
```

For compiling scss files and watching the changes.
```sh
gulp
```

## Usage

### 1. First 

A part of Pills is to build using `columns` classes which are inside of a `row` class.

The `row` class encapsulates the `columns`. As Pills uses a twelve column grid, the `twelve columns` class will take up the whole of the row.
```html
		<div class="row">
			<div class="twelve columns">
			</div>
		</div>
```


You can mix it up however you like though.
```html
		<div class="row">
			<div class="four columns">
			</div>
			<div class="eight columns">
			</div>
		</div>
```


You can put a `row` class inside of a `column` class in order to nest `columns`.
```html
		<div class="row">
			<div class="four columns">
			</div>
			<div class="eight columns">
				<div class="row">
					<div class="six columns">
					</div>
					<div class="six columns">
					</div>
				</div>
			</div>
		</div>
```


You can also offset a column as per your wish.
```html
		<div class="row">
				<div class="eight columns offset by-four">
		</div>
```




### 2. Second 

The second part of Pills consists of a five column layout with division of page in mind. If you want to strech the column to the whole page, just use `whole` along with `column`

```html
		<div class="row">
			<div class="column whole">
			</div>
		</div>
```


Using two halves of the page
```html
		<div class="row">
			<div class="column half">
			</div>
			<div class="column half">
			</div>
		</div>
```


This can also be nested like above.
```html
		<div class="row">
			<div class="column one-fourth">
			</div>
			<div class="column three-fourths">
				<div class="row">
					<div class="column two-fifths">
					</div>
					<div class="column three-fifths">
					</div>
				</div>
			</div>
		</div>
```


You can also offset a column as per your wish.
```html
		<div class="row">
				<div class="column two-thirds offset by-one-third">
		</div>
```



## Contributing
I'd love to get contributions for this project. This is just my amateur attempt at doing something which came to my mind. I'm all up for criticism if i've done something wrong, but do help me correct those by contributing to this project. Fork at your will. 

## License

[LICENSE](https://github.com/rohitkrai03/pills/blob/gh-pages/LICENSE) (MIT).
 
