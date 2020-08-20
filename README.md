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
        
        When implementing hovering use all 4 of the below and do not forget the dot infront and the comma in the end
            .btn--red:hover,
            .btn--red:active,
            .btn--red:focus,
            .btn--red:active:focus

        When the navbar and the callout section have the same color the navbar will disapear so you need to set the z-index for the container

        If you target classes within classes then target first the parent class and add the child class
            .navbar navbar-toggler

        Why do I have to target the child element to get rid of the radius??? Has the content of the container the radius????
            .alert-container .col-12
                    padding-left: 0;
                    padding-right: 0;

            .side-wide-alert 
                border-radius: 0;
        
 !!!    When using a divider use command <hr>


index.html
    To strech the background image "whiskey-background.jpg" over the full width of the page add to the class "container-fluid"
!!! &nbsp; A non-breaking space is a space that will not break into a new line. Two words separated by a non-breaking space will stick together (not break into a new line). This is handy when breaking the words might be disruptive.
!!! Do not forget to copy the entire class name!!!
    e.g. class btn btn-lg btn--cta btn--red    
    If you want to button up another button then use the full class
    e.g. class btn btn--cta btn--red
    DO NOT FORGET THE FIRST PART "btn"
