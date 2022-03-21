
# Using $\LaTeX$ In Jupyter Notebooks



## What is $\LaTeX$?

>_LaTeX, which is pronounced «Lah-tech» or «Lay-tech» (to rhyme with «blech» or «Bertolt Brecht»), is a document preparation system for high-quality typesetting. It is most often used for medium-to-large technical or scientific documents but it can be used for almost any form of publishing.\
    $~~~~$ - https://www.latex-project.org/about/_


This git is designed to be a primer in using $\LaTeX$ in Jupyter notebooks with the intention of improving presentation.

$\LaTeX$ is a powerful tool in making your markdowns cells look more professional and stand out. One can introduce $\LaTeX$ into the Jupyter Notebooks markdown cells using imported libraries, however, Jupyter Notebook natively leverages JavaScripts library MathJax to allow rendering of special characters and formatting. Its intended to allow for displaying mathematical functions and text in a more legible format and is widely used in academia.

This notebook aims to act like a cheat sheet for commonly used formatting. As we get progress along in the notebook, explanations will be limited to expounding on usage idiosyncrasies of the function in question. In other words, sections later in the book rely on knowledge of previous sections.

---

## Jupyter Workbook

Please refer to the Jupyter Workbook for detailed examples. 

### Table of Contents

-   $\LaTeX$
    - Getting-Started
    - Spacing
    - Justification
        - Centering
        - Multiline-formatting-for-math
    - The-Greeks
    - Mathematical Symbols
        - Superscript and Subscript
        - Grouping
        - Sets & Probability
        - Mathematical comparators
        - Mathematical operators
        - Fractions
    - A few examples of using $\LaTeX$
        - Einstein's mass energy equivalence
        - Equations of motion
        - Quadratic Equation
        - Some calculus for good measure
    - Using in visualizations


<h1>Table of Contents<span class="tocSkip"></span></h1>
<div class="toc"><ul class="toc-item"><li><span><a href="#$\LaTeX$" data-toc-modified-id="$\LaTeX$-1"><span class="toc-item-num">1&nbsp;&nbsp;</span>$\LaTeX$</a></span><ul class="toc-item"><li><span><a href="#Getting-Started" data-toc-modified-id="Getting-Started-1.1"><span class="toc-item-num">1.1&nbsp;&nbsp;</span>Getting Started</a></span><ul class="toc-item"><li><span><a href="#Spacing" data-toc-modified-id="Spacing-1.1.1"><span class="toc-item-num">1.1.1&nbsp;&nbsp;</span>Spacing</a></span></li><li><span><a href="#Justification" data-toc-modified-id="Justification-1.1.2"><span class="toc-item-num">1.1.2&nbsp;&nbsp;</span>Justification</a></span><ul class="toc-item"><li><span><a href="#Centering" data-toc-modified-id="Centering-1.1.2.1"><span class="toc-item-num">1.1.2.1&nbsp;&nbsp;</span>Centering</a></span></li><li><span><a href="#Multiline-formatting-for-math" data-toc-modified-id="Multiline-formatting-for-math-1.1.2.2"><span class="toc-item-num">1.1.2.2&nbsp;&nbsp;</span>Multiline formatting for math</a></span></li></ul></li></ul></li><li><span><a href="#The-Greeks" data-toc-modified-id="The-Greeks-1.2"><span class="toc-item-num">1.2&nbsp;&nbsp;</span>The Greeks</a></span></li><li><span><a href="#Mathematical-Symbols" data-toc-modified-id="Mathematical-Symbols-1.3"><span class="toc-item-num">1.3&nbsp;&nbsp;</span>Mathematical Symbols</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#Superscript-and-Subscript" data-toc-modified-id="Superscript-and-Subscript-1.3.0.1"><span class="toc-item-num">1.3.0.1&nbsp;&nbsp;</span>Superscript and Subscript</a></span></li><li><span><a href="#Grouping" data-toc-modified-id="Grouping-1.3.0.2"><span class="toc-item-num">1.3.0.2&nbsp;&nbsp;</span>Grouping</a></span></li></ul></li><li><span><a href="#Sets-&amp;-Probability" data-toc-modified-id="Sets-&amp;-Probability-1.3.1"><span class="toc-item-num">1.3.1&nbsp;&nbsp;</span>Sets &amp; Probability</a></span><ul class="toc-item"><li><span><a href="#Mathematical-comparators" data-toc-modified-id="Mathematical-comparators-1.3.1.1"><span class="toc-item-num">1.3.1.1&nbsp;&nbsp;</span>Mathematical comparators</a></span></li><li><span><a href="#Mathematical-operators" data-toc-modified-id="Mathematical-operators-1.3.1.2"><span class="toc-item-num">1.3.1.2&nbsp;&nbsp;</span>Mathematical operators</a></span></li><li><span><a href="#Fractions" data-toc-modified-id="Fractions-1.3.1.3"><span class="toc-item-num">1.3.1.3&nbsp;&nbsp;</span>Fractions</a></span></li></ul></li></ul></li><li><span><a href="#A-few-examples-of-using-$\LaTeX$" data-toc-modified-id="A-few-examples-of-using-$\LaTeX$-1.4"><span class="toc-item-num">1.4&nbsp;&nbsp;</span>A few examples of using $\LaTeX$</a></span><ul class="toc-item"><li><ul class="toc-item"><li><span><a href="#Einstein's-mass-energy-equivalence" data-toc-modified-id="Einstein's-mass-energy-equivalence-1.4.0.1"><span class="toc-item-num">1.4.0.1&nbsp;&nbsp;</span>Einstein's mass-energy equivalence</a></span></li><li><span><a href="#Equations-of-motion" data-toc-modified-id="Equations-of-motion-1.4.0.2"><span class="toc-item-num">1.4.0.2&nbsp;&nbsp;</span>Equations of motion</a></span></li><li><span><a href="#Quadratic-Equation" data-toc-modified-id="Quadratic-Equation-1.4.0.3"><span class="toc-item-num">1.4.0.3&nbsp;&nbsp;</span>Quadratic Equation</a></span></li><li><span><a href="#Some-calculus-for-good-measure" data-toc-modified-id="Some-calculus-for-good-measure-1.4.0.4"><span class="toc-item-num">1.4.0.4&nbsp;&nbsp;</span>Some calculus for good measure</a></span></li></ul></li><li><span><a href="#Using-in-visualizations" data-toc-modified-id="Using-in-visualizations-1.4.1"><span class="toc-item-num">1.4.1&nbsp;&nbsp;</span>Using in visualizations</a></span></li></ul></li></ul></li></ul></div>

---

## Citations
https://www.latex-project.org/

https://www.mathjax.org/