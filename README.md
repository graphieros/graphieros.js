# graphieros_react.js
a JS library ready for use in React.


# graphieros0.2.js
a JS library to edit linear, fractal and molecular graphieros in your HTML

What you need to make it work:

1. stick graphieros0.2.js in the head of your html, as a module. Don't forget to import the 'graphieros_dictionnary.js' and save it on your side too.
2. format your HTML as follows
    
# linear graphieros

<p>Linear Graphieros needs 2 DIVS in the HTML, the first will host the SVG (let's call it "linear HOST"), the other the glyph phonology inputs from which the parsing will be computed (let's call this one the "linear CODE")</p>

<ul>
    <li><b>Linear HOST :</b> give it an ID, and leave it empty</li>
    <li><b>Linear CODE :</b> give it a className. The graphieros phonology must be written as follows: all glyphs of a same word must be separated with a dash; words are separated with a space, punctuation must be separated with spaces. Example: ka-fy-go ma nmo-ka tae .<br><b>There can be as many CODE divs as you please, but they must bear the same className.</b>
    </li>
</ul>

Then the linear function must be called, either in a script tag of your HTML or on a separate JS file:

<code>
    <script type = "module">
        
        import { linear } from './graphieros0.2.js';
        
        let myLinearParagraph = { 
            section: '', // mandatory string: ID of the host div
            container: '', // mandatory string: className of your code divs
            size: '', // optional integer: size of individual glyphs
            background: [], // optional array: RGB background color
            color: [], // optional array: RGB color for your glyphs
            padding: '', // optional integer
            cartouche: '', // optional boolean (true: round border radius; false: no border radius)
            border: '' // optional string, standard CSS syntax, example: "1px solid rgb(0,0,0)"
        }
        
    </script>
</code>

# fractal graphieros

<p>Fractal graphieros only requires a HOST div, with an ID, which will be left empty</p>

Then the fractal function must be called, either in a script tag of your HTML or on a separate JS file:

<code>
    <script type = "module">
        
        import { fractal } from './graphieros0.2.js';
        
        let myFractalWord = { 
            section: '', // mandatory string: ID of the host div
            sequence: '', // mandatory string: the sequence of letters to form tehe glyphs (example: 'qzedxwq qzedxwq' will output two fractal hexagons)
            size: '', // optional integer to set the size of your SVG
            colors: [], // optional array to set RGB colors of the glyphs
            light: '', // optional boolean to set gradient towards black or white
            intensity: '', // optional integer to set the gradient intensity (1.2 to 3 ideally)
        }
        
    </script>
</code>

# molecular graphieros

<p>Molecular graphieros only requires a HOST div, with an ID, which will be left empty</p>

Then the molecular function must be called, either in a script tag of your HTML or on a separate JS file:

<code>
    <script type = "module">
        
        import { molecular } from './graphieros0.2.js';
        
        let myMolecularWord = { 
            section: '', // mandatory string: ID of the host div
            sequence: '', // mandatory string: the sequence of graphieros phonology, 7 max, separated with spaces (example: 'sro kfa du srei ktu foi ksi')
            size: '', // optional integer, to set the size of your SVG
            colors: [], // optional array to set the RGB colors of the glyphs
            strokeWidth: '', // optional integer to set the stroke width
            background: [], // optional array to set te RGB background color
            border: '' // optional string, standard CSS syntax
            borderRadius: ''// optional string, standard CSS syntax
        }
        
    </script>
</code>

# callifracal graphieros

<p>Callifractal graphieros only requires a HOST div, with an ID, which will be left empty</p>

Then the callifractal function must be called, either in a script tag of your HTML or on a separate JS file:

<code>
    <script type = "module">
        
        import { callifractal } from './graphieros0.2.js';
        
        let myCallifractal = { 
            section: '', // mandatory string: ID of the host div
            sequence: '', // mandatory string: the sequence of strokes, using the 'qzedxws' letters. One stroke is a two letter sequence, a dash must link all strokes of a same glyph. Example: 'qz-ze-ed-dx-xw-wq' will output a hexagon 
            svgSize: '', // optional integer, to set the size of your SVG
            size: '', // optional integer, to set the stroke width, it's called size, you'll see why
            colors: [], // optional array, to set the RGB colors of the glyphs
            radius: '', // optional integer, to set the size of the apex circles
            background: [], // optional array, to set the RGB background color
            light: '', // optional boolean to set gradient towards black or white
            intensity: '', // optional integer to set the gradient intensity (1.2 to 3 ideally)
            fit: '',// optional boolean, false by default. If set to true, will make the second glyph stick to the bottom of the first one.
        }
        
    </script>
</code>
