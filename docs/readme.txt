Link al corso: https://app.pluralsight.com/library/courses/bootstrap-4-developer/table-of-contents

Intro
	CSS3 ha aggiunto flexboxes
		consentono creare i layout web senza specificare una larghezza fissa delle colonne
		bootstrap4 ha iniziato a supportare flexbox, oltre il layout colonnare
		questo corso presenta in che modo possiamo creare il layout usando bootstrap4 flexboxes
Creazione layout usando flexboxes
	Cosa dobbiamo sapere
		HTML e CSS
		Basi di bootstrap4
		Javascript
	Problemi noti con il layout colonnare di bootstrap
		intro: usiamo row, che puo' essere divisa in 12 colonne
			   possiamo ragruppare le colonne 
			   e' semplice se abbiamo un layout che puo' essere diviso in 12 colonne
		- layout che non si addatta bene con le 12 colonne 
	Basi di un layout flexbox
		introdotto in CSS3 
		supportato in bootstrap4
		non e' legato ad numero predifinito di colonne con larghezza fissa
		dettagli
			- abbiamo un flex container
				possiamo sempre avere 12 item all'interno di questo container
				possiamo avere N item all'interno del container
			- all'interno del container definiamo delle sezioni dove ogni sezione puo' occupare piu' o meno spazio
			- molta piu' flessibilita'
	Preparazione app di esempio
		vedi repo git, sono due progetti, un sito e un gioco
	Disegnare layout usando flex containers
		Flex containers
			- css d-flex (allineato orizzontalmente)
				container si addatta al contenuto interno
			- tutto lo spazio orizzontale e' diviso x N sezioni, in base a N sezioni aggiunte al container
		Flexbox row e columns
			di default abbiamo impostazione di una row (quando usiamo d-flex), esiste cmq la classe flex-row
			la versione colonnare si applica quando vogliamo posizione i nostri elementi in verticale
			classe flex-column x impostare il layout colonnare
	Impostazione della Direzione all'interno di container
		flex-row-reverse, per invertire la direzione in orizzontale
		flex-column-reverse, per invertire la direzione in verticale
	Combinare piu' container, flex wrap
		vedi demo
	Utilizzo delle dimensioni previste da bootstrap
		classi w-75, w-25 etc...
		vedi demo
Allineamenti, margini, ordine di visualizzazione
	Flex axes
		Main axis and Cross Axis
		Flex-flow x una riga, allineamenti orizzontale (asse principale)
			Cross e' verticale
		Flex-flow x una riga, allineamenti verticale (asse principale)
			Cross e' orizzontale
		vedi slide
	Allineare il contenuto sulla asse principale
		vedi doc. di bootstrap su https://getbootstrap.com/docs/4.4/utilities/flex/#justify-content
		classi
			justify-content-center, justify-content-start, justify-content-end, justify-content-between (spazio tra elementi), 
				justify-content-around (spazio intorno ad ogni item presente nel container)
	Allineare il contenuto sull'asse secondario (cross)
		align-items-center, align-items-start, align-items-end, align-items-stretch (x occupare intera area)
	Allineare flexbox specifici
		align-self-start (vedi demo) applicato solo su un item specifico
		align-self-end, align-self-center
	Aggiunta di padding e margins
		ci sono classi dedicati in bootstrap4
		classi m-*, p-*, pr-* (pb, pt, pl), idem x margini
			es. m-2, p-5 
		numeri da 1 a 5 (min m-1, max m-5), idem per padding
			es. my-* (per applicare un margine al top e bottom), mx-* (per left e right)
		classe text-center
	Utilizzo di Fill, Grow e Shrink
		classi flex-fill (per occupare tutta area)
		flex-grow-1 (il numero indica true/false = 1/0), flex-grow-0 (area non viene ridimensionata, default)
		flex-shrink-1 (il contenuto va a capo, si ristringe, default), flex-grow-0 (contenuto non si ristringe)
			vedi demo
	Auto margins
		allineamento del contenuto
		es. classi mr-auto (tutto quello che e' a dx, viene spostato a dx)
			mx-auto, (x - sta per asse X), margine auto a sx e dx
	Addattamento in base alle dimensione della finestra di browser
		flex-wrap
		bootstrap4 ha le classi che si applicano in base alle dimensioni della finestra
			flex-sm, flex-lg, flex-xl, flex-md
			es. flex-sm-row, px-sm-5
Altri utility di bootstrap4
	classi di posizione
		fixed-bottom
	allineamento di testo
		stili da applicare a livello di container sono d-flex justify-content-center align-items-center
		es. flex-md-nowrap, x disabilitare wrap quando e' md (medium size)
	modali custom
		classi per img rounded, rounded-circle
	classe shadow x un ombra del container
	cambiare la visibilita' in base alle dimensioni
		d-none, x nascondere elemento
		d-sm-block, x mostrare elemento ad una certa dimensione
Aggiunta di altre funzionalita'
	aggiunta di js utile a completare la logica del gioco
	vedi repo git, niente di nuovo x quanto riguarda il css
	finalizzazione del progetto
		- ottimizzare le immagini (vedi https://tinypng.com/)
		- ottimizzare il codice (vedi https://beautifier.io/)
			sublime ha un plugin per minificare il JS (idem per altri editor, IDE)
		- minificare CSS
		
		
		