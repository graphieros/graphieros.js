# graphieros.js
a JS library to edit linear and fractal graphieros in your HTML

What you need to make it work:

1. stick graphieros.js in the head of your html
2. format your graphieros as follows:
    
    # linear graphieros
    <code><section id="myLinearSVG"></section> where the SVG will appear. Leave it empty.
    <div class="myGlyphs">...</div> where you write graphieros phonotypes
    <script> linear("myLinearSVG", "myGlyphs", size, R, G, B) </script></code>
    
    The linear() function takes the following parameters:
    
      . section ID where the SVG will be displayed (I recommend a css grid for linear graphieros)
      . div CLASS where your graphieros is written. Words are formatted using a dash between the phonotypes that constitute them. Example: ka-fy-go ma ka-tae = 3 words, 6 glyphs. Why CLASS and not ID? Because the script will loop over all your divs, if you have many lines to write, so all the divs of a given paragraph should bear an identical className.
      . glyphs size. 30px to 40px is nice and readable for a normal text
      . red color from 0 to 255
      . green color from 0 to 255
      . blue color from 0 to 255
      
      
    # fractal graphieros
    <code><section id="myFractalSVG"></section> where the SVG will appear. Leave it empty.
    <div id="myFractalSequence">...</div> where you write the graphical sequence
    <script> fractal("myFractalSVG", "myFractalSequence", size, R, G, B) </script></code>
    
    The fractal() function takes the following parameters:
    
      . section ID where the SVG will be displayed
      . div ID where the sequence is written. Sequence is based on the "ze qsd wx" keys that form a hexagon shape on the AZERTY keyboard. You can remap the keys in the js file if you want to adapt sequencing to your keyboard type. Sequencing works as follows:
              > one glyph is represented by a sequence separated with dashes, for example <b>qzedxwq-ss</b> will render a hexagon with a central dot. Writing a second sequence will display a half-sized second glyph. A sequence to display two hexagons would therefore be like "qzedxwq-ss qzedxwq-ss".
      . size of the first glyph (max size)
      . red color from 0 to 255
      . green color from 0 to 255
      . blue color from 0 to 255
      
     
