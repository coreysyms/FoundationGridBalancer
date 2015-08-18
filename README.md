# FoundationGridBalancer
Balances (centers) odd numbered remaining blocks for Foundations Block Grid - EX. 4 up grid with 5 blocks leaves last block centered on next line

# To Use
Apply "data-balancer" attribute to any ```<ul>``` block-grid.
Balancer will respect all media query layouts for the grid and "center" any remaining blocks that don't add up to the grid.

```
<div class="row">
	<div class="column">
    	<ul class="small-block-grid-2 medium-block-grid-3 large-block-grid-4" data-balancer>
        	<li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
        </ul>
    </div>
</div>
```

#Settings
Balancer only has one setting at this time. respectSiblingWidth.
Setting respectSiblingWidth to false will span the remaining ```<li>``` across the width of the parent ```<ul>```
View disrespect.html for an example.

To set respectSiblingWidth to false, do so at initalization.
```
$(document).foundation({
  balancer: {
	  respectSiblingWidth:false
  }
});
```

#Demos
You can view examples here: http://tangerineindustries.com/download/foundation-balancer/respect.html and http://tangerineindustries.com/download/foundation-balancer/disrespect.html
