# SimpleSlider
Simple responsive slider created in pure javascript.

## Version
v1.3.0

## Usage

###### Include files
```html
<link rel="stylesheet" href="css/simpleSlider.min.css"> 
<script src="js/simpleSlider.min.js"></script>  
```

###### Create HTML layout
```html
<div class="simple-slider simple-slider-first">
	<div class="slider-wrapper">
		<!-- First slide -->
		<div class="slider-slide" style="background-image: url('path/to/image')">
			<!-- Any HTML content -->
		</div>

		<!-- Second slide -->
		<div class="slider-slide" style="background-image: url('path/to/image')">
			<!-- Any HTML content -->
		</div>

		<!-- Third slide -->
		<div class="slider-slide" style="background-image: url('path/to/image')">
			<!-- Any HTML content -->
		</div>
	</div>

	<!-- Buttons (Not required) -->
	<div class="slider-btn slider-btn-prev"></div>
    <div class="slider-btn slider-btn-next"></div> 
</div>
```

###### Initialize the module
```
<script>
    var slider = new simpleSlider('.simple-slider-first');
</script>
```

## API

###### Example

new simpleSlider(container, options)

	- container - string (required), selector of slider container
    - options - object (optional), slider options

You can initialize more than one slider per page.

```
<script>
	// Default options
	var slider = new simpleSlider('.simple-slider-first');	

	// User options
    var slider = new simpleSlider('.simple-slider-second', {
    	speed: 2000, //default
    	autoplay: true, //default
    	classes: {
			wrapper: 'slider-wrapper' //default
		}
    });
</script>
```

###### Options

| Option  | Type | Default value | Description |
| ----- | ----- | ----- | ----- |
| speed | number | 2000 | Transition duration in ms |
| delay | number | 6000 | Delay between transitions in ms |
| autoplay | boolean | true | slider autoplay |
| classes: wrapper | string | 'slider-wrapper' | Wrapper class |
| classes: slide | string | 'slider-slide' | Slide class |
| classes: buttons | string | 'slider-btn' | Buttons class |
