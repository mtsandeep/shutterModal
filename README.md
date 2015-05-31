# shutterModal
Simple jQuery modal plugin which slides in from top

##Basic usage

```
// basic trigger for the shutterModal
$('#modal-content').shutterModal();
```

##With all available options

```
// These are the default values
$('#modal-content').shutterModal({
	background: 'rgba(0,0,0,0.8)', // background color for the cover
	zIndex:99, // z-index value if you need any higher value
	url: '', // url to fetch content, if you want to load content from another url via ajax
	easing: 'swing', // you can use easing plugin to add other easing effects for the shutter animation
	duration: 1000, // animation duration of shutter from top
	showAfter: 0, // delay for shutter to trigger, useful when you need shutter automatically triggered after x seconds
	hideAfter: 0, // close the shutter automatically after x seconds
	close: true, // If you need a close button added automatically
	escClose: true, // do you want to close shutter with escape key
	remove: false, // remove the shutter
	onLoad : function(){}, // function called after completely loading the shutter
	onClose : function(){} // function called after completely removing the shutter
});
```
##example

Include the shutterModal.css , jquery, shutterModal.js into your html page and trigger the shutterModal

```
<link rel="stylesheet" href="css/shutterModal.css" type="text/css">
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>

<script src="js/shutterModal.js"></script>

<script>
	$(function(){
		$('.show-shutter').on('click', function(e){
			e.preventDefault();
			$('#modal-content').shutterModal({easing:'jswing'});
		})
	});
</script>


<a class="show-shutter" href="#">show shutter</a> 

<!-- content in hidden div -->
<div id="modal-content" style="display:none">
	<p>Hello this is a demo text</p>
</div>
```
