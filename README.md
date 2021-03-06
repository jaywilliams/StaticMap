Static Map
==========

_A super simple PHP class for the Google Static Maps API_

(c) 2011 Jay Williams  
<https://github.com/d3designs/StaticMap>  
License: MIT


Example
-------

	<?php

	include 'staticmap.class.php';

	$options = array('size'=>'300x300');
	$map = new StaticMap($options);

	$map->add_marker('1600 Pennsylvania Ave NW, Washington D.C., DC 20500');

	$styles = array('color'=>'blue');
	$map->add_marker('Lincoln Memorial Circle, Washington D.C., DC 20037', $styles);

	$styles = array('label'=>'C');
	$map->add_marker('38.891300,-77.03000', $styles);

	// Display Static Map (using magic methods)
	echo "<img src=\"$map\" alt=\"Google Map\" $map->dimensions>";

	?>
	
Result
------

<img src="http://maps.google.com/maps/api/staticmap?size=300x300&amp;sensor=false&amp;markers=%7C1600+Pennsylvania+Ave+NW%2C+Washington+D.C.%2C+DC+20500&amp;markers=color%3Ablue%7CLincoln+Memorial+Circle%2C+Washington+D.C.%2C+DC+20037&amp;markers=label%3AC%7C38.891300%2C-77.03000" alt="Google Map" width="300" height="300">

Google Static Maps API Documentation
------------------------------------

<http://code.google.com/apis/maps/documentation/staticmaps/>