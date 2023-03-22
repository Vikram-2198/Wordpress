https://wordpress.stackexchange.com/questions/47062/short-code-output-too-early

function multilayer_svg() {

	ob_start();
	$svg = include(locate_template('/assets/svg/deception.svg'));
	$svg = ob_get_clean();
	return $svg;
}

add_shortcode( 'layeredsvg-test', 'multilayer_svg' );
