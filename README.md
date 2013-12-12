# Fader_Block
===========
This is a customizable jQuery utility plugin to select at random elements via CSS selector and transition from one class to another. Currently the animation is handled by CSS3 (modern broswer support only). Any animation that can be declared in a CSS3 class definition should work fine.

## How to use
1. **Include the plugin** --- Right now, this plugin assumes you have jQuery included in your HTML document. Use a script tag to include this plugin somewhere **after** the script tag that include the base jQuery library.
```html
<script type="text/javascript" src="jQuery_fader_block.js"></script>
```

2. **Invoke the plugin with your settings** --- The current default settings are:
    + **initialAction:** 'light-cloud'
      - a CSS class definition name that contains the animation end state and CSS3 transition styles to animate from the current color to the newly declared color
    + **revertAction:** 'dark-cloud'
      - a CSS class definition name that contains the animation starting and looping state point. This class must contain CSS3 transition styles to animate from the current state to the newly applied class
    + **selector:** '#qualities_cloud li'
      - A CSS selector for the objects you want to animate
    + **selectionCount:** 4
      - The number of items from the selected elements that you wish ti effect on each animation loop
    + **interval:** 3000
      - The animation speed in milliseconds (1000 = 1 second)
    
    
    
    Each of this default values can be overriden by creating an object literal and passing into the plugin when you invoke it. You can override any number of options.  Anything not overriden will utilized the afore mentiond default values.

```html
<script type="text/javascript">
  myOptions = {
    initialAction: 'my-CSS-class',
    revertAction: 'my-other-CSS-class',
    selector: 'my-CS-selector-statement'
  }
  
  $(document).fader_block( myOptions )			
</script>
```

Make sure this code snippet is inserted into the HTML **after** the line where the base jQuery library is declared


## Demo
[This html file] (https://github.com/theInternauts/Konami_Code/blob/master/demo.html) includes a working setup


### Roadmap
(in no particular order)
+ ~~Add support for options to be passed in for custom configuration.~~
+ refactor to smooth out animations and improve performance for large collections of elements
+ re-tool to trigger a custom event(s) to allow for greater flexibility and unknown use cases. (this could be epic :) )
+ consider utilizing javascript for the animations instead of CSS3 transitions for wider broswer compatibiliy and modulatrity

Your suggestions, bug fixes, and feature requests are welcome. [email Cricket] (mailto:cricketw@WeAreTheInternauts.com) or submit pull requests whichever you prefer.


### In the Wild
Are you using this plugin?  Let me know and I'll list your site here.
