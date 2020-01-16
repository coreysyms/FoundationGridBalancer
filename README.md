# FoundationGridBalancer
Note: This should only be used for legacy as flexbox is more flexable and less obstructive than JS. But to each his own!

Balances (centers) odd numbered remaining blocks for Foundation 6 Block Grid - EX. 4 up grid with 5 blocks leaves last block centered on next line

# To Use
Call Balancer after your Foundation call.
_Note: If you are only using certain plugins, ```foundation.util.mediaQuery``` is required._

```
<script src="js/vendor/jquery.js"></script>
<script src="js/vendor/what-input.js"></script>
<script src="js/vendor/foundation.js"></script>
<script src="js/vendor/foundation.balancer.js"></script>
<script src="js/app.js"></script>
```

Apply "data-balancer" attribute to any ```<div class=row">``` block-grid.
Balancer will respect all media query layouts for the grid and "center" any remaining blocks that don't add up to the grid.
Use any or all of the small, medium or large up grid layouts.

```
<div class="row medium-up-3" data-balancer>
	<div class="column">
    	<p>Hello World</p>
    </div>
	<div class="column">
    	<p>Hello World</p>
    </div>
	<div class="column">
    	<p>Hello World</p>
    </div>
	<div class="column">
    	<p>Hello World</p>
    </div>
	<div class="column">
    	<p>Hello World</p>
    </div>
</div>
```

# Settings
Balancer only has one setting at this time. ```data-respect-sibling-width```.
Setting data-respect-sibling-width to false (default is true) will span the remaining ```<div>'s``` across the width of the parent, filling the remaing space. ```<ul>```

To set respectSiblingWidth to false:
```
<div class="row medium-up-3" data-balancer data-respect-sibling-width="false">
```

# Q AND A
Q: It doesn't work with equalizer.

A: While Foundation will **NOT** allow you to apply multiple plugins to a single element
```
<div class="row medium-up-3" data-equalizer data-balancer> <!--- will not work --->
```
You can apply equalizer in a different manor since balancer needs to be on the "row". You can wrap your grid in a div and equalize any elements you need within. Nesting balancer inside a div with equalizer still allows both plugins to play nicely.
```
<div data-equalizer>
   <div class="row medium-up-3" data-balancer>
      <div class="column" data-equalizer-watch">
         ...etc...
      </div>
         ...etc...
   </div>
</div>
```
