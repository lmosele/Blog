---
layout: post
title:  "Web Typography For Dummies"
date:   2015-11-1 20:30:00
categories: design tutorial
---

Let's face it, not many people care about web typography, and for the 1% of geeks who do and want to learn more, it's very hard to find a community that is *open* to questions and beginners trying to find their footing. For that reason, I wanted to consolidate some of the more basic starting points of web typography in CSS for my own sake, if not for the sake of the people I learn alongside. 

*Please note that there is no "right" answer for typography, it's mostly subjective or based off of years of industry experience from people older than I, but nevertheless, it doesn't mean these rules are hard and fast.*

## The Markup

Let's start with our html, we want to cover a wide range of type here, so let's not limit ourselves to just a simple paragraph tag:

{% highlight html %}

<body>
	<div class="content">
		<h1>This Is My Title</h1>
		<p>Lorem ipsum Laboris <b>dolore ex anim Duis</b> nisi Ut dolor aliquip dolor enim aliqua occaecat consequat eiusmod occaecat in.</p>
		<p>Lorem <i>ipsum Laboris dolore</i> ex anim Duis nisi Ut dolor aliquip dolor enim aliqua occaecat consequat eiusmod occaecat in.</p>
		<ul>
			<li>List One</li>
			<li>List Two</li>
			<li>List Three</li>
		</ul>
		<a href="#">Lorem ipsum Irure dolore ad dolor magna.</a>
	</div>
</body>

{% endhighlight %}

Result:

<p data-height="268" data-theme-id="0" data-slug-hash="vNaYGq" data-default-tab="result" data-user="lmosele" class='codepen'>See the Pen <a href='http://codepen.io/lmosele/pen/vNaYGq/'>vNaYGq</a> by Lucas Mosele (<a href='http://codepen.io/lmosele'>@lmosele</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

---

## Basic Styling

### Font-Size
The biggest improvements you can make to a site can be made almost exclusively on a universal level. [Butterick's Practical Typography](http://practicaltypography.com/typography-in-ten-minutes.html) (a must read) states that the best type for screen sizes is 16px (1em in relative measurements). This is a common sight throughout the web, so it's a safe bet when choosing a standard, it's also worth noting that unless you choose otherwise, 1em is equivalent to 16px by default:

{% highlight css %}
div.content {
	font-size: 1em /* or 16px */
}
{% endhighlight %}

As I said before however, hard and fast rules may not *always* be the solution. Take phones for example, certain displays may render your 16px/1em text as smaller than you'd like, so boosting your font size to 18px/1.125em or 19px/1.2em may sometimes be a good option. 

{% highlight css %}
div.content {
	font-size: 1em /* or 16px */
}
@media (max-width: 480px) {
	div.content {
		font-size: 1.125em /* or 18px */
	}
}
{% endhighlight %}

Also, if you haven't noticed, I like to use *em* (relative measurements) rather than pixels. This keeps me from being inconsistent in my code since I'd rather keep with the 1em, 1.5em, 2em *font-size* pattern than memorizing 16px, 24px, 32px. There are many other benefits to *em* as well, but we'll get to that some other time. 

### Line-Height

If you haven't already read Jason Pamental's [*A More Modern Scale For Web Typography*](http://typecast.com/blog/a-more-modern-scale-for-web-typography) then I recommend you stop reading and go check it out now. 

Read it? Good. It's a great starting point for understanding the importance of responsive web typography and how it affects our readability and design. 

With that said, we can take some cues from the article and give our body text some breathing room by giving our 1em (16px) font a line height of 1.375em (22px) on desktop:

{% highlight css %}
div.content {
	font-size: 1em /* or 16px */
	line-height: 1.375em /* or 22px */
	color: #333;
}
@media (max-width: 480px) {
	div.content {
		font-size: 1.125em /* or 18px */
	}
}
{% endhighlight %}

Wonderful. Now it's time to style our headers, but first, let's talk about fonts. 

### Font Selection

The world of typography is surprisingly massive and in-depth, so without going too in depth, it's important to understand the basics of what makes a good font. For now

Serif & Sans-Serif

Besides script fonts and special fonts, the majority of fonts come in the form of either Serif or Sans-Serif fonts. Serif and San-Serif are just french for "little thingies" and "no little thingies" respectively.  

*Serif fonts* are sometimes referred to as "Roman" and tend to lean towards more old school styles and are commonly used in text and body copy due to its readability. The fonts you may be familiar with in this family are Times New Roman & Georgia. 

{% include images.html img="https://upload.wikimedia.org/wikipedia/commons/2/26/Serif_and_sans-serif_03.svg" caption="Serif Font, courtesy of Wikipedia" %}

*San-Serif* fonts (meaning "without serif") are sometimes referred to as Grotesque/Gothic typefaces. Sans-serif fonts are usually modern, and commonly used for headlines and user interfaces. Familar fonts in this family are Helvetica & Arial. 

{% include images.html img="https://upload.wikimedia.org/wikipedia/commons/9/99/Serif_and_sans-serif_01.svg" caption="Sans-Serif Font, courtesy of Wikipedia" %}

Obviously these are just generalizations, fonts like Open Sans and Helvetica work great for all sorts of roles, including long bodies of text, and with the right amount of styling some serif fonts can be used effectively for user interfaces. 

For our use however, 


