**SASS**

```
(a)SASS(Stands for syntatically aweseme stylesheets)

(b)It is also known as a CSS preprocessor,language or extension and normally
helps us to go beyond the normal capabilities of css.

Its more like typescript in javascript.

(c)Lets you use features that do not exist in CSS.

We may have conditionals and logic in our css

(d)Sass(.scss) files are compiled to regular css.

```

**File extension type**

```
(a).SCSS file

we write sass like regular css way of styling with curly braces.

(b).sass

we write our sass in more of an indentation type manner.

convenient eg when you are using the pug templating engine.

```

**Features of SASS**

**(A) Variables in CSS.**

```

Prefixed with a dollar "$"

eg : $primary-color:blue

Easier to use than the css custom properties or the now variables in css.


$primary-color : #333;

body{

color:$primary-color;

}

```

**(B)Nesting**

```
(a)Helps us write cleaner code in that it allows nesting.

<div class="nav>

<ul> </ul>
<li></li>
<a></a>

</div>

SCSS

.nav{
ul{
    margin:0;
    padding:0;
    list-style:none;
  }

li{display:inline-block}
a{
    display:block;
    padding:6px 12px;
    text-decoration:none;
}

}

CSS

nav ul{
    margin:0;
    padding:0;
    list-style:none;
}

nav li{
display:inline-block
}

nav a{
    display:block;
    padding:6px 12px;
    text-decoration:none;
}

```

**Modules and Partials**

```
We can break up our sass into separate files and imports
to the main file without making mutiple http requests.

This is hugely advantageous since you can break up your
css instead of having one very large file.

You may prefix your modules with _about.scss and they will not be
compiled.

```

**Mixins and Functions**

```
Allows us to have functions and thus we can be able to reuse properties
from within our css.


Sass

@mixin transform($property){

--webkit-transform:$property;
--ms-transform:$property;
transform:$property

}

//calling the mixin
.box {@include transform(rotate(30deg));}


CSS

.box{
--webkit-transform:rotate(30deg);
--ms-transform:rotate(30deg);
transform:rotate(30deg)

}

```

**Inheritance**

```
We can create base styles and extend them into these other classes.

Example when making alerts and the only thing that changes in alerts is color.

%message-shared{
    border: 1px solid #ccc;
    padding:10px;
    color:#333;
}

.message{
    @extend %message-shared;
}

.success{
    @extend %message-shared;
    border-color: green;
}

.error{
    @extend %message-shared;
    border-color: red;
}

.warning{
    @extend %message-shared;
    border-color: yellow;
}

&(ampasard) refers to the parent class
```

**Operators**

```
We can do something like calculation of floats from within our css.

article[role="main"]{
    float:left;
    width:600px/960px *100%
}

Output
article[role="main"]{
    float:left;
    width:62.5%
}

```

**Conditionals**

```
@mixin triangle($size, $color, $direction){

  height:0;
  width:0;

  border-color:transparent;
  border-style:solid;
  border-width:$size/2;

@if $direction ==up{
    border-bottom-color:$color;
}@else if $direction ==right{
    border-left-color:$color;
}@else if $direction ==left{
    border-right-color:$color;
}@else if $direction ==down{
    border-top-color:$color;
}@else{
    @error "Unknown direction #{$direction}.";
}
}

//Calling it

.next{

    @include triangle(5px,black,right);

}

//Output

.next{
  height:0;
  width:0;
  border-color:transparent;
  border-style:solid;
  border-width:$size/2;
  border-left-color:black
}
```

**Compiling Sass**

```
(a) Via Npm

sudo npm i -g sass

sass --watch scss/style.scss css/style.css
sass --watch (main sass file) (output css.file)

Compling cannot happen if there is a mistake.

```
