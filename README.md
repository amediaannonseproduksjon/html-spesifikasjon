# html-spesifikasjon
Spesifikasjoner til HTML-annonser


	Levering av digitale annonser																								
	Image:																								
		jpg, png eller gif 																							
		max 100 kb																							
		Url som annonsen skal linkes til må være vedlagt																							
		filnavnet må inneholdet formatet																							
		filnavnet må ikke innholde store bokstaver, mellomrom, tegn eller bokstavene æ, ø og å.																							

	Rich media: 																								
		html/iframe																							
		redirect tag/third part tag																							
		max 100 kb																							
		linken må åpnes i nytt vindu																							
		filnavnet må inneholdet formatet																							
		filnavnet må ikke innholde store bokstaver, mellomrom, tegn eller bokstavene æ, ø og å.																							

	Amedia specs:																								
		https://github.com/amedia/advertsspec/blob/master/specification.md																							

	Adtech specs: 																								
		https://github.com/fredrikborggren/ADTECH-creativespec																							

	Validator/for å teste annonsen:																								
		http://validator.gardr.org/																							

	Info til lokale produksjonsbyråer:																								
		Det er to måter å levere html-annonser på:																							
		• alle filene sendes publiserer. Merk: da må disse spesifikasjonene følges																							
			https://github.com/fredrikborggren/ADTECH-creativespec																						

		• alle filene ligger på egen server, og annonsen leveres som en iframe-kode. 																							
			Egen clickTag må legges inn, se tips under																						
			desktop:	<iframe src="LINK_TIL_ANNONSEN_SOM_LIGGER_PÅ_SERVEREN_EVT_MED_ADCLICK_VARIABEL" width="_bredde_px" height="_høyde_px" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" seamless></iframe>																					
			mobil 1:1	<style>/* flexible iFrame */ .k-flexible-container {position: relative;padding-bottom: 100%;height: 0;overflow: hidden;} .k -flexible-container iframe,k -flexible-container object,k-flexible-container embed {position: absolute; top: 0;left: 0; width: 100%;height: 100%;}</style><div class="k-flexible-container"><iframe src="LINK_TIL_ANNONSEN_SOM_LIGGER_PÅ_SERVEREN_EVT_MED_ADCLICK_VARIABEL" width="_bredde_px" height="_høyde_px" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" seamless></iframe> </div>																					
    mobil 2:1	<style>/* flexible iFrame */ .k-flexible-container {position: relative;padding-bottom: 50%;height: 0;overflow: hidden;} .k -flexible-container iframe,k -flexible-container object,k-flexible-container embed {position: absolute; top: 0;left: 0; width: 100%;height: 100%;}</style><div class="k-flexible-container"><iframe src="LINK_TIL_ANNONSEN_SOM_LIGGER_PÅ_SERVEREN_EVT_MED_ADCLICK_VARIABEL" width="_bredde_px" height="_høyde_px" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" seamless></iframe> </div>																					

	ClickTAG:																								
	Her er noen tips ang ClickTAG. Hvis dere ikke får det til å virke, anbefaler vi at de bruker google analytics e.l.																								
	Vi har dessverre liten mulighet for å ha support på dette.																								

	Klikk på annonsen kan registreres ved hjelp av variabelen _ADCLICK_ i Adtech IQ.																								
	Kort sagt så erstatter annonsesystemet denne variabelen med en lang url som inneholder en del informasjon om annonsen.																								
	Nettleseren tar en snartur innom denne adressen for å registrere klikket før den går til f.eks. landingssiden.																								
	Sluttbrukeren vil ikke merke denne svippturen.																								
	Innholdet i en ADCLICK-variabel ser f.eks slik ut:																								

	http://adserver.adtech.de/adlink|1361|4206997|0|554|AdId=9942423;BnId=10;itime=400147026;key=forsiden;nodecode=yes;link=																								
	Merk at linken avsluttes med link= og bak her settes det inn det annonsen faktisk skal linkes til.																								

	Det er flere måter å bruke denne variabelen på, f.eks JavaScript eller PHP.																								
	Googlesøketips: javascript get query string parameter.																								
