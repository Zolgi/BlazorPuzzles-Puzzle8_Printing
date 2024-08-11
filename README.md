# Blazor Puzzle #8

## A Printing Puzzle

YouTube Video: https://youtu.be/M5sNRlq2R2s

BlazorPuzzle Home Page: https://blazorpuzzle.com

### The Challenge:

This is a silly story generator that puts together a little story from words provided by the user.

![image-20231008121154886](images/image-20231008121154886.png)

Now, we'd like to print the story with Strg+P, but we don't want the input UI to print. How can we achieve this?

Answer:<br>
 css: class="d-print-none" <br>
 ***or***
  ```css
    /*Nur für Print css*/
    @media print {
        html , body {
            background-color: green;
            color: white;
        }

      
    .nocontent {
        margin: 0;
        padding: 0;
        display: none;
    }

        p {
            font-size: 24pt;
            background-color: purple;
            color: green;
        }
   }
   ```
   ```razor
    <div class="nocontent"> @* Eigene CssClasse *@
    <h1>@Title</h1>
    </div>
   ```


 

