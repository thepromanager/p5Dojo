# p5Dojo

[p5Dojo](https://christernilsson.github.io/p5Dojo) christernilsson.github.io/p5Dojo

## grundläggande programmering med processing och p5

### målsättning
* Den första bitmappen ritar du, genom att programmera
* Den andra bitmappen ska du efterlikna
* Den tredje bitmappen visar skillnaden
* De två bitmapparna är lika när den tredje är helt svart (dvs 0,0,0)

### färger
  - 0,0,1 blå
  - 0,1,0 grön
  - 0,1,1 cyan
  - 1,0,0 röd
  - 1,0,1 magenta
  - 1,1,0 gul
  - 0 svart
  - 0.5 grå
  - 1 vit
  
### bakgrundsfärg
  - **bg** 1   vit
  - **bg** 1,1,0 gul

### fyllningsfärg
  - **fc**  ingen
  - **fc** 1   vit
  - **fc** 1,1,0   gul
  - **fc** 1,0,0,0.5 röd, halvgenomskinlig

### streckfärg
  - **sc**    ingen
  - **sc** 1   vit
  - **sc** 1,1,0   gul
  - **sc** 1,0,0,0.5   röd, halvgenomskinlig
  
### skapa en färg
  - **co** 1   vit
  - **co** 1,1,0   gul
  - **co** 1,0,0,0.5   röd, halvgenomskinlig
  - **color** 255   vit
  - **color** 255,255,0   gul
  - **color** 255,0,0,128   röd, halvgenomskinlig

### strecktjocklek
  - **sw** pixlar

### ritkommandon
  - **point** x,y
  - **line** x1,y1, x2,y2
  - **ellipse** x,y, w,h
  - **circle** x,y,r
  - **rect** x,y, w,h
  - **triangle** x1,y1, x2,y2, x3,y3
  - **quad** x1,y1, x2,y2, x3,y3, x4,y4
  - **arc** x,y, w,h, start,stopp, PIE 
  
### lerp  
 - linjär interpolation och extrapolation
 - lerp(10,12,-1) == 8
 - lerp(10,12,0) == 10
 - lerp(10,12,0.5) == 11
 - lerp(10,12,1) == 12
 - lerp(10,12,2) == 14
  
### for loop
  - Glöm ej att indentera innehållet med ett tabsteg!
  - **loopa** i    => [0,1,2,3,4,5,6,7,8,9]
  - **loopa** i 5  => [0,1,2,3,4]
  - **loopa** i 1,11  => [1,2,3,4,5,6,7,8,9,10]
  - **loopa** i 0,10,2  => [0,2,4,6,8]
  - **loopa** i 10,0,-2  => [10,8,6,4,2]
  - **for** **var** i **of** [1,1,2,3,5,8,13,21] => [1,1,2,3,5,8,13,21]
  
### if
  - Pythonsyntax. Kolon används ej
```javascript
if i%3==0
  fc 0
elif i%3==1
  fc 1
else
  fc 2
```    

### koordinatsystemet
  - **translate** x,y   flytta origo      
  - **rd** degrees      rotera runt origo
  - **scale** n         skala upp eller ner
  
### modes
  - **rectMode** CORNER
    * CORNER (default)
    * CORNERS
    * CENTER
    * RADIUS
  - **ellipseMode** CENTER
    * CORNER
    * CORNERS
    * CENTER (default)
    * RADIUS

### text
  - **textAlign** LEFT,BASELINE  
    * LEFT (default)
    * CENTER
    * RIGHT
    * TOP
    * CENTER
    * BOTTOM
    * BASELINE (default)
  - **textSize** n
  - **text** "p5",x,y

### push & pop
Sparar och återställer följande kommandon:
 - translate rotate scale fc sc sw rectMode
 - tint strokeCap strokeJoin imageMode ellipseMode colorMode
 - textAlign textFont textMode textSize textLeading
 - [information](https://www.processing.org/tutorials/transform2d)

### förenklad javascript
 - Orsak: Programmering ska vara så enkelt som möjligt
 - Kodblock indenteras med tab (som Python) istf blockparenteser {}
  * Tabstorlek alltid två mellanslag
  * Python-kolon används ej
 - Semikolon används ej
 - Parenteser används ej för att anropa funktioner, på högsta nivån.
 - Pilfunktioner kan användas för att hantera asserts. Parenteser ska ej användas.
  * x => x*x
  * a,b => a+b
 - Stäng av förenklad Javascript med //ECMA på första raden
  
### exempel 1: förenklad Javascript
```javascript
bg 1,0.5,1
sw 2
sc 0.5
loopa i
  fc i%2
  rd 5
  rect 20*i + 5,5, 10,10
```    

### exempel 1: normal Javascript
```javascript
background(255,127,255)
strokeWeight(2)
stroke(127)
for (var i=0; i<10; i++) {
  fill((i%2)*255)
  rotate(radians(5))
  rectangle(20*i + 5,5, 10,10)
}
```    

### exempel 2: pilfunktion
```javascript
a,b => a+b
```    

### exempel 2: normal funktion
```javascript
function (a,b) {
  return a+b
}
```    

### mera information

 - [download](https://p5js.org)
 - [manual p5.js](https://p5js.org/reference)
 - [manual processing java](https://processing.org/reference)
 - [manual processing python](http://py.processing.org/reference)
 - [engelsk e-bok i färg (om fem minuter) av Lauren McCarthy, SEK 55](https://play.google.com/store/books/details?id=iP3GCgAAQBAJ&rdid=book-iP3GCgAAQBAJ&rdot=1&source=gbs_atb&pcampaignid=books_booksearch_atb)
 - [svartvit pappersbok (om fem dagar), 130 SEK](https://www.adlibris.com/se/bok/getting-started-with-p5js-making-interactive-graphics-in-javascript-and-processing-9781457186776)
 - [funprogramming](http://funprogramming.org)
 - [p5.js video tutorial](https://www.youtube.com/user/shiffman/playlists?sort=dd&view=50&shelf_id=14)

### kontakt, synpunkter, felrapportering, förslag till exempelkod mm

 - https://github.com/ChristerNilsson/p5Dojo/issues
 - janchrister.nilsson snabela gmail.com