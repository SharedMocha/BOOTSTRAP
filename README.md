# BOOTSTRAP
bootstrap


BootStrap- Layout,Utilities,Components
VVIMP Trick -> For a box inside a grid to take full space you need to define it as ROW and COLUMN div . (https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-4/grid-project/Labeled+Composition+II.png)
VVIMP - in abpve image link A &B  are consuming 100% space- because we put then in a row and then inside a column=each one of them--check github code at  (https://github.com/SharedMocha/BOOTSTRAP/blob/master/BS_Grid_Assignement)
IMP-Know about BS grids,utility classes(Ccolor,bg,text-align,fixed-top), components (navbar, buttons, a carousel/slideshow for images, )
1.) In BS the default is make your entire page or div a container and add rows to it. Now for each row we can add columns.
2.) Need to add 2 meta tags and import BS from CDN 
3.) BS works when we assing a botostrap class to our div. Some of the classes are container,row,column etc.....

Grid-  https://getbootstrap.com/docs/4.2/layout/overview/
Utilities-> https://getbootstrap.com/docs/4.2/utilities/borders/
Components - https://getbootstrap.com/docs/4.2/components/alerts/

Bootstrap Classes to use  
----------------------------------------------------------GRID----------------------------------------------------------------------
Step1 -Decide container and apply it
1.) <div class="container"></div> // becomes horizontally centered, and has a left and right margin.
2.) <div class="container-fluid"></div> // full width of screen

Step2 -Decide rows and apply it
<div class="container"">
  <div class="row">
  </div>
</div>

Step3 - Decide columns and apply them - Max is 12 columns -> by default column takes entire width of row. you can add more to compress them accordingly
https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-4/simple-12-grid.svg

<div class ="container">
 <div class="row>
  <div class="col">
  </div>
 </div>
</div>

step3.1 If you want to customize columns -you can tell how mnay columns u want like 'col-4'->take 4 columns
<div class="container">
			<div class="row">
        <div class="col-3">
          <p>Left Column</p>
        </div>
        <div class="col-6">
          <p>Middle Column</p>
        </div>
        <div class="col-3">
          <p>Right Column</p>
        </div>
      </div>
</div>

Step 3.2 If you want your content to detrmine  -width --you can say so like below-
<div class="col-auto">
  <p>This content determines the width of the parent column</p>
</div>


--------------------------------------------------------------------------------
Bootstrap breakpoints -> Bootstrap categorizes screen sizes into 5 categories or as breakpoints: extra small, small, medium, large, and extra large.  (use this for responsive design)
**if you dont specify size then default is xs.
https://s3.amazonaws.com/codecademy-content/courses/learn-bootstrap-4/Film-Festival-Responive-updated.gif
https://getbootstrap.com/docs/4.2/layout/grid/#grid-options
Extra Small -<576px -Portrait smartphone
Small >= 576px - landscape smartphones
Medium >=768px - tablets
Large >= 992px - desktops
Extra large >=1200px large desktop

Step1.) Setting this  -
Syntax - "col-{breakpoint}-{width}

Example-<div class="col-sm-8"> 
</div>

The column in the example will be as wide as 8 individual columns on small screen sizes and also any larger screens (medium, large, and extra large)
**{breakpoint} can be sm, md, lg, or xl. Notice that there is no extra small or xs breakpoint. If we omit {breakpoint}, it is by default for extra small screens.
**{width} can be set from 1 to 12 and assigns a width to the column.
**When we set a {breakpoint}-{width}, it means that we want our column to have that set width for screens that fit in the specified breakpoint range and other larger screens.


 Step2.) mix multiple col for various screen sizes
 <div class="col-12 col-md-8">
 </div>
 here we are telling for smaller screens take 12 columns whers as for biggers screens take only 8 columns
 
 ----------------------------------------------------------utilities and componenets----------------------------------------------------------------------
 
 ----utility classes,---------------->
1.) Changing text-color from default black to blue-
<p class="text-primary">This text is blue!</p>
Refer to this for other colors - https://getbootstrap.com/docs/4.2/utilities/colors/#color

2.) changing background color
<div class="bg-success">
  Green! This signifies success! 
</div>
Refer to this for other color - https://getbootstrap.com/docs/4.2/utilities/colors/#background-color
https://getbootstrap.com/docs/4.2/utilities/colors/

3.) combine both colors in one line
  <div class="bg-success text-white">
      Alright, we want to have a green background AND change the text color to white.
  </div>
  
4.) making our font bold
<p class="font-weight-bold">
  This rendered text is bold.
</p>

5.) making our text uppercase
<p class="font-weight-bold text-uppercase">
  This rendered text is both bold and uppercased. 
</p>

6.) font-weight -refer to below docs
https://getbootstrap.com/docs/4.2/utilities/text/#font-weight-and-italics


7.) align text left,center or more
https://getbootstrap.com/docs/4.2/utilities/text/

8.)position --same like realtive,fixed,absolute etc..
https://getbootstrap.com/docs/4.2/utilities/position/
<div class="position-static">...</div>
<div class="fixed-top">...</div>

---------------components ---------------------
1.) Nav -  The first component we’ll investigate is the navigation (nav) component which offers our users a collection of links. The nav component is slightly different from a navbar component. The nav component is often specific to one or a few webpages, whereas a navbar often appears on all the pages of a website.
https://getbootstrap.com/docs/4.2/components/navs/

example->
<ul class="nav">
  <li class="nav-item">
    <a class="nav-link" href="#">First Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Second Link</a>
  </li>
</ul>

We created a navigation component using an <ul> that has a class of "nav".
The <ul> has nested <li> elements which each have a class of "nav-item".
Inside each <li> is an <a> which has a class of "nav-link".


2.) You can center links or change to tabs or anything possible-
for center nav-       

        <nav class="nav justify-content-center">
				  <a href="#" class="nav-link">About Us</a>
          <a href="#" class="nav-link">Contact Us</a>
          <a href="#" class="nav-link">Subscribe</a>
        </nav>


3.)buttons ->
https://getbootstrap.com/docs/4.2/components/buttons/#examples
<button type="button" class="btn btn-danger">Danger</button>

It has a type of "button".
It has two classes, "btn" and "btn-danger".
The "btn" class provides Bootstrap’s default button styling.
The "btn-danger" turns the button red and conveys the purpose of the button, i.e. clicking this button might not be safe!


4.)collpasing components - One way to include interactivity is to toggle the visibility of an element.
https://getbootstrap.com/docs/4.2/components/collapse/
To add such a feature, we need two elements and a few attributes — one element with content and another element that switches the visibility of the previous element. For example:

Code--
<button class="btn btn-primary" type="button" data-toggle="collapse" data-target="#collapseExample" aria-expanded="false" aria-controls="collapseExample">
  This button controls the following div's visibility. 
</button>

<div class="collapse" id="collapseExample">
  <p>This content's visibility gets toggled</p>
</div>


In the example above, we have a <button> element that toggles the visibility of the <div> element below it.
The button has an attribute data-toggle="collapse" which enables button’s toggle ability. Another attribute, data-target="#collapseExample", means that this button toggles the visibility of the element with the id of "collapseExample". The aria-expanded and aria-controls attributes are information for screen readers and other accessibility means.

Focusing our attention on the <div> below the button, notice that it has a class of "collapse", which hides the content when the webpage initially renders. Our <div> also has an id of "collapseExample" which corresponds to the value of the button’s data-target.

5.) Nav bar-> Let’s combine our knowledge of collapse, buttons, and the nav component to make a responsive navbar! We often find navbars at the top of websites and we can use a navbar to quickly navigate to useful/important pages on the website.
https://getbootstrap.com/docs/4.2/components/navbar/#supported-content

Example- >
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">Brand Goes Here</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="#">Current Page Link <span class="sr-only">(current)</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Another Page Link</a>
      </li>
    </ul>
  </div>
</nav>


Explanation->
There’s a lot going on, so let’s break it down before we use it in our own code:

We have a <nav> element with multiple classes:
"navbar" makes this <nav> a Bootstrap navbar.
"navbar-expand-lg" renders the <div class="collapse navbar-collapse"> element on large (and extra large screens). The "lg" portion is called a breakpoint and refers to screen size widths. We can append one of any breakpoint value at the end, i.e. "sm", "md", "lg", or "xl".
"navbar-light" assigns a color scheme to the navbar.
"bg-light" assigns a background color to the navbar.
Inside the <nav> is an <a> with a class of "navbar-brand" which can be an image or text that represents the brand/logo of the website.
There is a <button> that renders when a user’s screen size is smaller than the breakpoint value in "navbar-expand-{breakpoint}" and toggles the visibility of the navbar menu to save space.
If the user’s screen size matches the breakpoint (or is bigger), then the <div>, with the nav component and its links, renders instead of the button.
The <ul> and the nested <li> make up a nav component.
The first <li> has a class of "active" which highlights the user’s current page.


6.)Jumbotran component--
https://getbootstrap.com/docs/4.2/components/jumbotron/
In arenas and stadiums, there are giant screens called jumbotrons which display the main event for everyone in the crowd to see. Bootstrap also offers a jumbotron component that serves a similar function and makes content stand out.

<div class="jumbotron">
  <h1>Wow this stands out!</h1>
</div>


7.)card component -> (one isntagram  feed is a card)
https://getbootstrap.com/docs/4.2/components/card/#example
Bootstrap also has a card component that serves as a container for smaller customized content. Card components are often grouped together to display a collection of similar content in manageable chunks. We can draw a comparison of the card component to playing cards in deck — in both cases, there are cards grouped together and each one contains something different.


Example->
<div class="card">
  <img class="card-img-top" src="placeholder.jpg" alt="card example image">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">Card description goes here.</p>
    <a href="#" class="card-link">Link to somewhere.</a>
  </div>
</div>

explanation-
Let’s highlight a few key points from the example:

To make a card component we need to assign a class of "card" to an element.
Inside the card component, there are two children, an <img> and a <div> element.
The <img> has a class of "card-img-top" which adds styling and formatting to the image.
The <div> has a class of "card-body" which adds a section with default padding.
The content inside the card body all have classes with "card-{value}" which adds styling to these elements specific for Bootstrap cards.
By default, this card will take up the entire width of its parent element.


8.)The Carousel Component
There are times that we want to showcase a group of images but not want to have our users scroll through one picture on top of another. Instead, we could fit our images into a slideshow using Bootstrap’s carousel component.
https://getbootstrap.com/docs/4.2/components/carousel/
https://getbootstrap.com/docs/4.2/components/carousel/#slides-only


code-
<div id="carouselExampleSlidesOnly" class="carousel slide" data-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img class="d-block w-100" src="example_slide_1.png" alt="First slide">
    </div>
    <div class="carousel-item">
      <img class="d-block w-100" src="example_slide_2.png" alt="Second slide">
    </div>
  </div>
</div>


