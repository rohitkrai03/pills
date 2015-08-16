#Pills

> A simple, responsive, and tiny CSS grid for humans who don't like memorising all those cryptic codes like col-*-6 or something.

## Why?
You must be thinking there are like a thousand grid frameworks. So why another one?? What's so special about this one??

Well, there are three types of people who use css grids in there own way -

* First - The ones who just memorize the cryptic codes like col-md-6 or whatever from their favourite CSS Framework like Bootstrap or Foundation. And not long before, i too was in this category using Bootstrap's grid all the time.

* Second - The ones who simplify the grids into simple partitions of the page. Like half of the page or one-third or something like that and process ahead with that. One of the best grid frameworks that is present for this category is [Gridism →](http://cobyism.com/gridism/) which  actually inspired me to create Pills in the first place.

* Third -  The ones who like to count number of rows and columns but in a simple human like language.


### My thoughts
Trust me, Gridism is awesome and it simplifies stuff like anything. But still sometimes i felt the one-third, two-fifths, golden-small n all are a bit of confusing (_For me atleast_). And Gridism is just a 5 column grid which can be sometimes a bit limiting compared to 12-column grids. 

> What if i wanted a simple 12-column layout and i could say that i want this div to be of size of **four columns**  and another div in the same row with size of **eight columns**?? 
> What if i wanted to use offsets??

This made me think about a grid which will focus on both the Second and Third category of people. A grid which can be used like traditional row column layout or the more contemporary thinking of diving the page like half or one-third or something.

So, Pills has two parts - 

* First - This will have a 12 columns for that granular control but still would be simple enough like english language.

* Second - Inspired by Gridism thinking and catering to people who think fractional division on page is simpler.


## Installation

### 1. Get the files

The easiest way to use Pills in your project is via the [Bower](http://twitter.github.com/bower) package manager.

```sh
bower install pills
```

Elsewise, [download the zip folder](https://github.com/rohitkrai03/pills), extract it, and copy `css/pills.min.css` into your project’s folder. Boom. Done.

### 2. Link the stylesheet

Add the following stylesheet to your HTML’s `<head>` section:

```html
<link rel="stylesheet" href="bower_components/pills/pills.min.css">
```

**Note:** If you didn’t install using Bower, you need to adjust the path of CSS file to match your file structure.

### 3. Viewport scale

Add the following meta tag to your HTML’s `<head>` section:

```html
<meta name="viewport" content="width=device-width,initial-scale=1">
```

Without this meta tag, mobiles and tablets might load your page as a scaled-down version of the desktop size, instead of resizing the content to match the device’s actual viewport width.

## Usage

A part of Pills is build using `columns` classes which are inside of a `row` class.

The `row` class encapsulates the `columns`. As Pills uses a twelve column grid, the `twelve columns` class will take up the whole of the row.
```html
    <div class='row'>
      <div class='twelve columns'>
      </div>
    </div>
```

You can mix it up however you like though.
```html
    <div class='row'>
      <div class='four columns'>
      </div>
      <div class='eight columns'>
      </div>
    </div>
```

You can put a `row` class inside of a `column` class in order to nest `columns`.
```html
    <div class='row'>
      <div class='four columns'>
      </div>
      <div class='eight columns'>
        <div class='row'>
          <div class='six columns'>
          </div>
          <div class='six columns'>
          </div>
        </div>
      </div>
    </div>
```

You can also offset a column as per your wish.
```html
    <div class='row'>
        <div class="eight columns offset by-four">
    </div>
```


The second part of Pills consist of five column layout with division of page in mind. If you want to strech the column to whole page, just use `whole` along with `column`
```html
    <div class='row'>
      <div class='column whole'>
      </div>
    </div>
```

Using two halves or the page
```html
    <div class='row'>
      <div class='column half'>
      </div>
      <div class='column half'>
      </div>
    </div>
```

This can also be nested like above.
```html
    <div class='row'>
      <div class='column one-fourth'>
      </div>
      <div class='column three-fourths'>
        <div class='row'>
          <div class='column two-fifths'>
          </div>
          <div class='column three-fifths'>
          </div>
        </div>
      </div>
    </div>
```

You can also offset a column as per your wish.
```html
    <div class='row'>
        <div class="column two-thirds offset by-one-third">
    </div>
```



## Contributing
I'd love to get contributions for this project. This is just my amateur attempt at doing something which came to my mind. I'm all up for criticism if i've done something wrong, but do help me correct those by contributing to this project. Fork at your will. 

## License

MIT [LICENSE](https://github.com/rohitkrai03/pills/blob/master/LICENSE) (MIT).
 