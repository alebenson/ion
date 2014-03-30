ion css
=======
#### Responsive CSS framework based on Atomic Styling

[Atomic Design](http://bradfrostweb.com/blog/post/atomic-web-design/) is a methodology for creating design systems.<br>
[Atomic Styling](http://coding.smashingmagazine.com/2013/10/21/challenging-css-best-practices-atomic-approach/) is bassed on mapping classes to a single style.<br>
[Responsive Design](http://alistapart.com/article/responsive-web-design) is the approach that suggests that design and development should respond to the user’s behavior and environment based on screen size, platform and orientation.

Form more info:<br>
[What is Atomic Design](http://bradfrostweb.com/blog/post/atomic-web-design/) *by* Brad Frost.<br>
[Challenging CSS Best Practices](http://coding.smashingmagazine.com/2013/10/21/challenging-css-best-practices-atomic-approach/) *by* Thierry Koblentz.<br>
[Responsive Web Design](http://alistapart.com/article/responsive-web-design) *by* Ethan Marcotte


#### Benefits of Atomic Styling.

+ **Reusable, faster development** <br>
Styles are driven by classes that are not related to content, so we can copy and paste existing modules to get started.
+ **Very little maintenance (on the CSS side)** <br>
Only a small set of rules are meant to change over time.
+ **Scalable** <br>
If you need to add a class go to [Emmet CheatSheet](http://docs.emmet.io/cheat-sheet/) to look for the completion.
+ **Less bloat** <br>
We can build entire modules without adding a single line to the style sheets.
+ **Better caching** <br>
A huge chunk of CSS can be shared across products and properties.
+ **Predictable code, less abstraction** <br>
There is no need to look for rules in a style sheet to figure out the styling of a template. It’s all in the markup.
+ **Third-party development** <br>
A third party can hand us a template without having to attach a style sheet (or a style block) to it. No custom rules from third parties means no risk of breakage due to rules that have not been properly namespaced.


#### Class Naming
The classes are named by the abbreviation of the property name as in [Emmet Completions](http://docs.emmet.io/cheat-sheet/),<br> and an abbreviation of their value.

```CSS
/* For predefine values as in Emmet. */
.posa {position:absolute;}

/* Letters S M L are used to indicate different values for units (always relative to a defaul one). */
.mt  {margin-top:24px;} /* default */
.mtx {margin-top:48px;} /* x = default*2 */
.mts {margin-top:12px;} /* s = default/2 */

/* Basic page parts are used to indicate values for colors. */
.cbody {color:#FFFFFF;} .bgbody{background-color:#FFFFFF;}
.ctext {color:#BADA55;} .bgtext{background-color:#BADA55;}

/* Filenames are used to indicate values for url */
.bgibg {background-image:url(bg.png)}

/*Class prefixes are used to indicate a break by the Media Query.
Every class that doesn't have a prefix is applied on every state.*/
.dn{display:none;}    /*always applied*/
.x-dn{display:none;}  /*from 320 to infinity*/
.xx-dn{display:none;} /*from 650 to infinity*/

```


## Code Samples
#### Desktop - Static

###### Card Pattern
```html
<article class="g4 fll ml bdrs ovh bgtitle cbody">
	<figure>
		<img class="mw100p" src="image.jpg" alt="">
	</figure>
	<div class="p">
		<h1 class="fzls"><a class="cbody" href="">Article Title</a></h1>
		<p>A passage or segment taken from a longer work,
		such as a literary or musical composition, a document, or a film.</p>
	</div>
</article>
```


###### Media Pattern
```html
<article class="g8 fll bdrs ovh bgtitle cbody">
	<figure class="g4 fll">
		<img class="mw100p" src="image.jpg" alt="">
	</figure>
	<div class="g8 fll ml p">
		<h1 class="fzls"><a class="cbody" href="">Article Title</a></h1>
		<p>A passage or segment taken from a longer work,
		such as a literary or musical composition, a document, or a film.</p>
	</div>
</article>
```

#### Mobile First - Responsive

###### Card to Media
```html
<article class="bdrs ovh bgtitle cbody xx-g8 xx-fll xx-ml">
	<figure class="xx-g4 xx-fll">
		<img class="mw100p" src="image.jpg" alt="">
	</figure>
	<div class="p xx-g8 xx-fll xx-ml">
		<h1 class="fzls"><a class="cbody" href="">Article Title</a></h1>
		<p>A passage or segment taken from a longer work,
		such as a literary or musical composition, a document, or a film.</p>
	</div>
</article>
```
