# Assignment 3 - Booking prototype

In this assignment you need to create a prototype for a (online shopping) site using HTML and CSS. The prototype consists of three HTML pages (front page `index.html`, product page `product.html`, and shopping cart/checkout `cart.html`) and a single stylesheet file (`style.css`).

Under the `samples/` folder you will find screenshots that serve as examples of what you need to create. You don't have to produce the exact same output that is shown on the samples, you can deviate from it in any way you want (especially in the content) as long as you follow the instructions given below.

Note that you *only create a mockup*. The content does not have to be dynamic. We will do that in a later lab.

Media and images which you use should be creative commons licensed. If you need to attribute the author put a comment in the html/css.
[Openverse](https://wordpress.org/openverse/) is a good resource.

### Fonts and colors

  *	Sans-serif font family.
  * All headings are typeset Montserrat, all other text is typeset Raleway.
    -	https://fonts.google.com/specimen/Montserrat
    -	https://fonts.google.com/specimen/Raleway
  *	Font sizes are controlled by the browser; all font sizes need to be set relative, using *em*.
  *	Background color is white.
  *	You need to select a color palette with maximum five colors, and use only those colors (plus white for page background).
    -	Provide in the `README.md` file a list the hex codes of the colors from that palette. Create a color palette yourself: (Paletton)[https://paletton.com/]


### Layout

  *	Use the `<header>`,` <main>`, and `<footer>` HTML5 tags for structuring the page.
  *	The elements below are the same on all pages.
  *	**Header**
    -	Height is 40px. The header is always visible, even when the page is scrolled down.
	-   It has a background color from the palette
    -	The logo area has a height of 60px. It is positioned 5% from the left of the containing element
        -	You can write the name of your site here and/or create a logo. [Openverse](https://wordpress.org/openverse/)
        -	The logo needs to overlay any content (i.e., needs to have the highest z-index).
    -	The main menu is part of the header and is horizontally aligned.
        -	It has to be an unordered list inside a `<nav>` element.
        -	It is right aligned and 5% from the right side of the page.
        -	It contains 3 links, pointing to index.html, product.html and cart.html.
        - Every link is represented by an icon.
  *	**Main**
    -	There has to be 100px vertical space (margin or padding) on top of the main area.
    -	The main area is 90% of the width of the page and is center-aligned. That means it resizes automatically when the window is resized, but has a maximum width of 1400px (see the screenshots under `samples/`).
    -	Main headers (h1) inside `<main>` have a background color, 1.2em font size, and 5px padding around (see Product Page).
    -	Framed boxes (class `.framed`) have a solid 1px border and 5px padding. The font-size is 0.8em.
  *	**Footer**
    -	The footer always stays at the bottom of the page. For extra points, the footer can be "sticky": See Optional 2.
    -	The height of the footer is 120px. It has a 5px wide top border.
    -	The footer contains contact information (tel, email). These are center-aligned both vertically and horizontally.


### Front page (`index.html`)

  * The front page contains a summary of the shopping cart in an `<aside>` element and the shop content.
  * The shopping cart summary:
    - Has a width of 300px.
    - Is placed to the right, inside the `<main>` element.
    - Contains a clickable `<h2>` heading that links to `cart.html`.
    - Contains a table with contents of the shopping cart (at least 3 rows).
    - Is highlighted with a different background color.
  * The shop content:
    - Contains an (background) image banner that spans the width (i.e. 100%) of the shop content and resizes with the page. It has 5px wide solid top and bottom borders. 
    - Contains (at least) 3 products.
      - Put each product inside an `<article>` element.
      - The products have a target width of 280px, but may grow or shrink to fit on a line.
      - Depending on screen size, 1 or more products are shown per line.
      - Products contain an image, product name and a short summary.
      - Image is inside a framed box and resizes with the `<article>`.
      - Product name is an `<h3>`, with no margins.
      - Price is displayed together with the product name, but is right aligned.
      - The product image `<img>` is a link to `product.html`.
    - Change the appearance of the product on mouseover, e.g. change background or borders)
    - Some of the products should contain a discount batch that is displayed on top of the image.
    - Discount batch should be located 30px from the top and right side of the frame around the image.
  *Hint: Images with the same dimension will make the design easier.*

### Product page (`product.html`)

  * Just like the front page, product page contains a summary of the shopping cart in an `<aside>` element
  *	Show the image, name, and short description of the product at the top of the page in a framed box `.framed`.
  * Show a form to select amount and size of the elements. (You can replace size with any other select that fits your store)
  * The form contains a field that shows the price that does not allow input.
  * Size should be a select containing at least 3 options.
  * Form labels are right aligned, and all form elements have the same size.
  * Display an "Add to Cart" button which is colored with a (background) color from your palette.
  * Depending on the page width, the product information and form is displayed to the right or below the image (hint flexbox).
  *	Display a "Details" header (h1).
  *	Display a long description in a framed box `.framed`.


### Shopping cart page (`cart.html`)

  *	Display a "Cart" header (h1).
  * Display the cart as a table in a framed box `.framed`.
  * The table contains the product name, size, count, price, discount, calculated price, and for every row a cancel button.
  *	Display a "Checkout header" header (h1).
  * Display the checkout form in a framed box.
  * Checkout form contains the fields with appropriate input types
    - First name
    - Last name
    - Email
    - Street
    - City
    - Postal code
  * Form also contains a checkbox for agreeing to terms of service and a submit button.
  * Form elements are structured into Billing details, Delivery address and Submit order, as shown in images.
  * Form elements are horizontally and vertically aligned.
  * Form fields have the same size and labels are right aligned. 

Commit and push the files you created (`index.html`, `product.html`, `cart.html`, `style.css`, plus optional images) to GitHub.

**Optional1** Use a media query to display the `<aside>` element on top rather then next to the main content on small screens, as shown in [here](samples/optional_index_small.png). Hint: use a media query to change the flex-direction as in [this example](https://www.w3schools.com/csS/tryit.asp?filename=trycss3_flexbox_website2).

**Optional2** The footer is "sticky" (i.e., when the page is long, you need to scroll down to see the footer)
  - Main idea is to set `height: 100%` on the `<html>` and `min-height: 100%` on the `<body>` element.
  - Then position the footer absolute, or use a flexbox.
  -	See, e.g.,: https://css-tricks.com/couple-takes-sticky-footer/


# Oppgave 3 - Webshop-prototype

I denne innleveringen skal du lage en prototype for en (online shopping) nettside ved bruk av HTML og CSS. Prototypen skal best?? av tre HTML sider (hovedsiden `index.html`, produktsiden `product.html` og handlekurv/utskjekk-siden `cart.html`) og en enkel css-fil (`style.css`).

Under `samples/` mappen finner du skjermbilder som skal fungere som eksempel av hva du skal lage. Du trenge ikke ?? lage en eksakt kopi av bildene, og s?? lenge du f??lger instruksjonene under kan du forandre p?? dem som du ??nsker (spesielt i innhold).

Merk at i du *bare lager en "mockup"*. Innholdet trenger ikke ?? v??re dynamisk. Vil vil gj??re de i en senere lab.


### Skrift og farge

  *	Sans-serif font familie.
  *	Alle headings er av typen Montserrat, all annen tekst av typen Raleway.
    -	https://fonts.google.com/specimen/Montserrat
    -	https://fonts.google.com/specimen/Raleway
  *	Fontst??rrelse er kontrollert av nettleser; ergo m?? de alle v??re relative, med bruk av *em*.
  *	Bakgrunnsfargen skal v??re hvit.
  *	Du m?? velge en color palette med max fem farger, og bruk kun disse fargene (pluss whit for sidebakgrunn).
    -	Oppgi i `README.md` heksekoder for fargene fra den paletten. Du kan lage en palette selv: (Paletton)[https://paletton.com/]


### Layout
  
  *	Bruk `<header>`, `<main>`, og `<footer>` HTML5 taggene for ?? strukturere siden.
  *	Elementene under er like p?? alle sider.
  *	**Header**
    -	H??yden er 40px. Headeren er alltid tilgjengelig, selv om vi blar nedover siden.
    -	Logoen skal ha en h??yde p?? 60px. Den er posisjonert 5% fra venstre kant av overordnete element. 
        -	Du kan skrive navnet p?? siden din her og/eller lage en logo [Openverse](https://wordpress.org/openverse/)
        -	Logoen m?? ligge over alle andre typer innhold (ergo den trenger ?? ha den h??yeste z-indexen).
    -	Hovedmenyen er en del av headeren og ligger p?? rekke horisontalt.
        -	Det skal v??re en uordnet liste inni et `<nav>` element.
        -	Den er justert mot h??yre og ligger 5% fra h??yre side av dokumentet.
        - Den inneholder 3 lenker, som peker til index.html, product.html og cart.html.
        - Hver lenke er representert med et ikon.
    
  *	**Main**
    -	Det skal v??re 100px vertikalt rom (margin eller padding) p?? toppen av mainomr??det.
    -	Skal v??re 90% i bredden og v??re sentrert. Det betyr at den skal automatisk tilpasse seg n??r sidest??rrelsen forandres, men den skal ha en maximum bredde p?? 1400px (se bildene under `samples/`).
    -	Hovedoverskrifter (h1) i `<main>` skal ha en bakgrunnsfarge, 1.2em font st??rrelse og 5px padding rundt (e.g. p?? produktsiden)
    -	Innrammede bokser (class `framed`) har en solid 1px border og 5px padding. Font st??rrelse 0.8em.

  *	**Footer**
    -	Footeren skal alltid v??re p?? bunnen av siden. Optional kan den v??re sticky (se optional 2).
    -	H??yden skal v??re p?? 120px. Den skal ha en 5px bred topp border.
    -	Footeren skal inneholde kontaktinformasjon (telefon, e-post). Disse er sentrert b??de vertikalt og horisontalt.


### Hovedsiden (`index.html`)
  
  * Hovedsiden inneholder et sammendrag av handlekurven i et  `<aside>` element og butikk-innholdet.
  * Sammendrag av handlekurven:
    - Har en bredde p?? 300px.
    - Plasseres til h??yre, inne i `<main>` elementet.
    - Inneholder en klikkbar `<h2>` overskrift som lenker til `cart.html`.
    - Inneholder en tabell med innholdet i handlekurven (minst 3 rader).
    - Blir fremhevet gjennom en annen bakgrunnsfarge.
  * Butikk-innholdet:
    - Inneholder et bildebanner som spenner over bredden (dvs. 100%) av butikk-innholdet og som tilpasses sidest??rrelsen automatisk. Den har 5px bred solid topp og bunn border.
    - Det skal listes (minst) 3 produkter.
      - Plasser hvert produkt i et eget `<article>` element.
      - Produktene har en m??lbredde p?? 280px, men kan vokse eller krympe for ?? passe p?? en linje.
      - Avhengig av skjermst??rrelse vises 1 eller flere produkter per linje.
      - Produktene inneholder et bilde, produktnavn, pris, og en kort oppsummering.
      - Bildet vises i en box med ramme (`.framed`) og forandrer st??rrelse sammen med `<article>`.
      - Produktnavnet er en `<h3>` uten marginer.
      - Pris vises sammen med produktnavnet, men justert til h??yre.
      - Produktbildet `<img>` er en lenke til `product.html`.
    - Endre utseendet til `<article>` elemented ved "mouseover", f.eks. endre bakgrunn eller border).
    - Noen av produktene skal inneholde en rabattmarker som vises opp p?? bildet.
    - Rabattmarkeren skal v??re plassert 30px fra oversiden og h??yre siden rammen rundt bildet.

### Produkt side (`product.html`)

   * Lik hovedsiden inneholder produktsiden et sammendrag av handlekurven i et `<aside >` element.
   * Vis bilde, navn og kort beskrivelse av et produkt ??verst p?? siden i en innrammet boks `.framed`.
   * Vis et skjema for ?? velge mengde og st??rrelse p?? elementene. (Du kan bytte ut st??rrelse med noe annet som passer for dine produkter.)
   * Skjemaet ogs?? inneholder et felt som viser prisen som ikke tillater input.
   * St??rrelse skal v??re et select element som tilbyr minst 3 alternativer.
   * Skjemaets labels er aligned mot h??yre, og skjemaelementene har samme st??rrelse.
   * Vis en "Legg i handlekurv" -knappen som er uthevet gjennom bakgrunnsfarge fra paletten.
   * Avhengig av sidebredden, vises informasjonen og skjemaet til h??yre eller under bildet (hint flexbox).
   * Vis en "Details" overskrift (h1).
   * Vis en lang beskrivelse i en innrammet boks `.framed`.

### Handlekurv side (`cart.html`)

  * Vis en "Cart" overskrift (h1).
  * Vis handlekurven som en tabell i en innrammet boks `.framed`.
  * Tabellen inneholder product name, size, count, item price, discount, calculated price, og for hver rad en cancel-knapp.
  * Vis en "Checkout" overskrift (h1).
  * Vis utsjekkingsskjema i en innrammet rute.
  * Skjemaet inneholder feltene med passende inndatatyper
    - Fornavn
    - Etternavn
    - E-post
    - Gate
    - By
    - Postnummer
  * Skjemaet inneholder ogs?? en avkrysningsrute (checkbox) for ?? godta tjenestevilk??r og en sende-knapp.
  * Skjemaelementer er strukturert i Billing details, Delivery address, og Submit order, som vist p?? bilder.
  * Formelementer er horisontalt og vertikalt p?? linje.
  * Formfelt har samme st??rrelse og etikettene er riktig justert.

**Optional1** Bruk en media query for ?? vise `<aside>` elementet overfor, heller en ved siden av hoved innholdet p?? skjermer mindre enn 1200px, som vist [her](samples/optional_index_small.png). Tip bruk en media query for ?? bytte ut flex-direction som i [dette eksempel](https://www.w3schools.com/csS/tryit.asp?filename=trycss3_flexbox_website2).

**Optional2** Footeren skal kunne "blas vekk" (dersom siden er for lang m?? brukeren bla ned for ?? kunne se den).
  - Hovedideen er ?? sette `height:100%` p?? `<html>` og `min-height: 100%` p?? `<body>` elementet.
  - Deretter bruk absolutt posisjonering p?? footeren, eller bruk en flexbox.
  -	Eller se, for et eksempel: https://css-tricks.com/snippets/css/sticky-footer/

Commit og push filene du laget (`index.html`, `product.html`, `cart.html`, `style.css`, plus valgfrie bilder) til GitHub.
