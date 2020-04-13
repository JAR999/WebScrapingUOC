# Pràctica 1 Web Scraping
## M2.951 - Tipologia i cicle de vida de les dades aula 1
## Autors: Oriol Calvo i Josep Adrian

### 1. Context. 
<!--Explicar en quin context s'ha recol·lectat la informació. Explicar per què el lloc web triat proporciona aquesta informació.-->
El lloc web escollit és [Resultats eleccions municipals 2019](https://www.naciodigital.cat/municipals2019). Aquest lloc presenta informació dels resultats electorals de les eleccions municipals espanyoles de 2019 en tots els municipis de Catalunya. La informació es recopila quasi un any després de la cita electoral en un dels diaris digitals que presentaven els resultats detallats de les votacions. El diari digital va construïr aquesta eina per tal que els seus lectors poguessin consultar aquests resultats en temps real, permetent filtrar la cerca per conèixer els regidors i vots obtinguts per cada partit municipi a municipi. Aquesta és només una de les pàgines webs que en aquest context publicaven dels resultats en temps real, aprofitant els mecanismes de transmissió d'informació que el Ministeri de l'Interior acostuma a habilitar durant els darrers anys en periode electoral.

En el fitxer [robots.txt](https://nucli.naciodigital.cat/robots.txt) de la pàgina web observem que es permet l'ús de web scraping per a tot el domini excepte un directori, per la qual cosa es tracta d'un origen de dades vàlid per a recol·lectar informació.

### 2. Definir un títol pel dataset. 
<!--Triar un títol que sigui descriptiu.-->
Denominem el dataset "Resultats eleccions municipals 2015 i 2019 a Catalunya".

### 3. Descripció del dataset. 
<!--Desenvolupar una descripció breu del conjunt de dades que s'ha extret (és necessari que aquesta descripció tingui sentit amb el títol triat).-->
El conjunt de dades presenta els resultats de les eleccions municipals de 2015 i 2019 en cada municipi de Catalunya. Primerament es persenten els resultats globals en cada municipi (total participació, vots en blanc, abstencions...) i posteriorment els resultats obtinguts per cada una de les candidatures, en vots i en regidors.

### 4. Representació gràfica. 
<!--Presentar una imatge o esquema que identifiqui el dataset visualment-->
S'adjunta la definició gràfica del dataset en el lloc web dbdiagram.io
https://dbdiagram.io/d/5e88b9a14495b02c3b894075

### 5. Contingut. 
<!--Explicar els camps que inclou el dataset, el període de temps de les dades i com s'ha recollit.-->
Els 2 datasets generats inclouen la següent informació:

Resultats Globals
* Id Municipi
* Nom Municipi
* Nom Comarca
* Nom Província
* URL Municipi
* Cens (2019)
* Valor escrutat (2019)
* Nombre abstencions (2019)
* Vots comptabilitzats (2019)
* Vots nuls (2019)
* Vots en blanc (2019)
* Cens (2015)
* Valor escrutat (2015)
* Nombre abstencions (2015)
* Vots comptabilitzats (2015)
* Vots nuls (2015)
* Vots en blanc (2015)

Resultats per Candidatura
* Id Candidatura
* Nom candidatura
* Acrònim candidatura
* Id Municipi
* Nom Municipi
* Vots obtinguts
* Regidors obtinguts
* Any dels resultats

Les dades van generar-se durant el 24 de maig de 2015 i durant el 26 de maig de 2019, jornades en que van celebrar-se les darreres eleccions municipals a Espanya. Els resultats s'han descarregat de la pàgina web durant el mes d'abril de 2020, un cop les eleccions ja s'havien dut a terme, mitjançant el codi presentat a l'apartat 9.

### 6. Agraïments. 
<!--Presentar el propietari del conjunt de dades. És necessari incloure cites de recerca o anàlisis anteriors (si n'hi ha).-->
Els autors volen agraïr la seva feina al l'editorial SCG Aquitània SL i al diari Naciódigital, propietari del lloc web on estan allotjades les dades. Aquest desenvolupament s'ha inspirat en el treball [FoodPriceScaper](https://github.com/rafoelhonrado/foodPriceScraper), de Rafael Reyna Camones.

### 7. Inspiració. 
<!--Explicar per què és interessant aquest conjunt de dades i quines preguntes es pretenen respondre.-->
El conjunt de dades és interessant perquè representa els resultats bruts de vot segregat per municipi i permet veure com aquest es distribueix segons diferents criteris: per partit, per tendència política, per municipi o àrea geogràfica, entre d'altres. 

Permet respondre gran quantitat de preguntes sobre comportaments electorals i distribució de vot en tot el territori, de forma agregada o detallada. Per citar-ne només alguns exemples podriem saber:

- Quina és la participació global en cada un dels municipis? Com es distribueix l'abstenció?
- Quins partits obtenen més regidors? I més vots?
- Com es distribueix el vot en els diferents partits i tendències polítiques?
- Quin és el partit més votat en cada una de les divisions territorials?
- Quants vots son necessaris per obtenir un regidor en cada divisió territorial?

### 8. Llicència. 
<!--Seleccionar una d'aquestes llicències pel dataset resultant i explicar
el motiu de la seva selecció:
○ Released Under CC0: Public Domain License
○ Released Under CC BY-NC-SA 4.0 License
○ Released Under CC BY-SA 4.0 License
○ Database released under Open Database License, individual contents
under Database Contents License
○ Other (specified above)
○ Unknown License-->
La llicència seleccionada és CC BY-NC-SA-ND, ja que és compatible amb el lloc web i el set de dades original. Aquesta llicència implica que els autors requereixen atribució de l'obra, que no permeten ús comercial de la mateixa, que requereixen que qui utilitzi les dades ho faci amb la mateixa llicència que l'original i que no en permeten obra derivada. 

Com que es tracta d'un treball acadèmic i que no es pretén distribuir comercialment, la llicència seleccionada és compatible amb la llicència original de les dades.

### 9. Codi. 
<!--Adjuntar el codi amb el qual s'ha generat el dataset, preferiblement en Python o, alternativament, en R.-->
Vegeu els fitxers adjunts a Githbub https://github.com/JAR999/WebScrapingUOC

### 10. Dataset. 
<!--Publicar el dataset en format CSV a Zenodo amb una xicoteta descripció.-->
El dataset es troba publicat a Zenodo amb el DOI 10.5281/zenodo.3750339  https://zenodo.org/record/3750339#.XpTY55ngrIU

### 11. Lliurar. 
<!--Presentar el treball amb el DOI del dataset a Github-->
El treball es troba publicat a Github a https://github.com/JAR999/WebScrapingUOC

| Contribucions             | Signa  |
|---------------------------|--------|
| Recerca prèvia            | OC, JA |
| Redacció de les respostes | OC, JA |
| Desenvolupament codi      | OC, JA |
