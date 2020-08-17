You now have styled your intire homepage with Bootstrap. You now need to make your page unique

First you add some containers to your sections so you can give it individuell styling
    alert-container for your sign in/ sign up button
    callout-container
    quote-container
    feature-container
    table-container

Then you start to style your homepage from top to toe, most of this will be done in the style.css but some changes will be done in the index.html
We started with the callout-container, guess this is the biggest feature here

style.css
    callout-container
        Changed the height so it uses the full page: height 100vh
        Adding the fullwidth background image, go to https://css-tricks.com/perfect-full-page-background-image/ and copy the snippet and added it to the style.css file
    !!!!To add an image to GitPod, just drag the picture from your computer to the directory of your choice...hopefully the image directory

        Remove the "html {} this is not needed, Why...do not know at this point
                html { 
            background: url(images/bg.jpg) no-repeat center center fixed; 
            -webkit-background-size: cover;
            -moz-background-size: cover;
            -o-background-size: cover;
            background-size: cover;
            }
        
        To center the content use the flex box use
            display
            align-items (if you would use text-align here nothing will happen)
            justify-content

        To get the your container transparent use   
            background-color: transparent (if you use the class jumbotron here then this will override the default set by Bootstrap)

        To get the background image a bit darker so it does not obscure the text infront, add a new class name (.opaque-overlay) and do the following
            position: absolut
            top: 0
            left: 0
            heigth: 100%
            width: 100 %
            background-color: rgba(0(red),0(green),0(blue),0.5(alpha is the transparency 1 is complete visible and 0 completly transparent))


index.html
    To strech the background image "whiskey-background.jpg" over the full width of the page add to the class "container-fluid"
        
