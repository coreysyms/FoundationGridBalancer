# FoundationGridBalancer
Balances (centers) odd numbered remaining blocks for Foundation 6 Block Grid - EX. 4 up grid with 5 blocks leaves last block centered on next line

# To Use
Call ```<script src="js/vendor/foundation.balancer.js"></script>``` after your foundation.js call
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

#Settings
Balancer only has one setting at this time. data-respect-sibling-width.
Setting data-respect-sibling-width to false (default is true) will span the remaining ```<div>'s``` across the width of the parent, filling the remaing space. ```<ul>```
View disrespect.html for an example.

To set respectSiblingWidth to false:
```
<div class="row medium-up-3" data-balancer data-respect-sibling-width="false">
```

#Demos
Download and view index.html, or go <a href="http://tangerineindustries.com/Foundation/grid-balancer/" target="_blank">here.</a>
