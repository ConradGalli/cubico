# cubico

$oca_package = $oca_packages[0]['GroupPackageCount'];		
	
 
	
		$oca_packageb = 0;
		$oca_weightb = 0;
		$oca_lenthb = 0;
		$oca_widthb = 0;
		$oca_heightb = 0;
		$oca_amountb = 0;
		foreach ($oca_packages as $key) {
			$oca_package = $key['GroupPackageCount'];
	 		$oca_weight = $key['Weight']['Value'] * $oca_package;
			$oca_lenth = $key['Dimensions']['Length'] ;
			if($oca_lenth != 1){$oca_lenth = $oca_lenth * 2.54;}
			$oca_width = $key['Dimensions']['Width'];		
		if($oca_width != 1){$oca_width = $oca_width * 2.54;}
			$oca_height = $key['Dimensions']['Height'] ;	
		if($oca_height != 1){$oca_height = $oca_height * 2.54;}
			$oca_amount = $key['InsuredValue']['Amount'];	
			$oca_packageb += $oca_package;
			$oca_weightb += $oca_weight;
			$oca_lenthb += $oca_lenth;
			$oca_widthb += $oca_width;
			$oca_heightb += $oca_height;
 			$oca_volume = $oca_lenth * $oca_width * $oca_height;
$oca_volume = round($oca_volume , 2);
			 
 			$oca_volumeb = $oca_volume;
 			$oca_volumec += $oca_volumeb ;			
		}
			
 		// OLD VERSION $oca_volume = $oca_weightb * $oca_lenthb * $oca_widthb * $oca_heightb;

//$oca_volumec = round($oca_volumec, 2);
$oca_volumesy = $oca_volumec * 0.000001;
$oca_volumesy = number_format($oca_volumesy, 7);
