---
description: La classe PathGradientBrush consente di personalizzare la modalità di riempimento di una forma con colori a modifica graduale.
ms.assetid: f6a8085c-3d6a-494f-a1ee-5fa96efb1aae
title: Creazione di una sfumatura del percorso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ef39793547b1485525f8cf1fd5b344773e7a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568247"
---
# <a name="creating-a-path-gradient"></a>Creazione di una sfumatura del percorso

La classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) consente di personalizzare la modalità di riempimento di una forma con colori a modifica graduale. Un oggetto **PathGradientBrush** ha un percorso limite e un punto centrale. È possibile specificare un colore per il punto centrale e un altro colore per il limite. È anche possibile specificare colori distinti per ognuno dei diversi punti lungo il limite.

> [!Note]  
> In GDI+ un percorso è una sequenza di linee e curve gestite da un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Per ulteriori informazioni sui percorsi GDI+, vedere [percorsi](-gdiplus-paths-about.md) e [costruzione e](-gdiplus-constructing-and-drawing-paths-use.md)creazione di percorsi.

 

Nell'esempio seguente viene riempita un'ellisse con un pennello sfumatura del percorso. Il colore centrale è impostato su blu e il colore limite è impostato su Aqua.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



Nell'illustrazione seguente viene mostrata l'ellisse piena.

![illustrazione che mostra un'ellisse con riempimento sfumato](images/pathgradient1.png)

Per impostazione predefinita, un pennello sfumatura del percorso non si estende al di fuori del limite del percorso. Se si utilizza il pennello sfumatura percorso per riempire una forma che si estende oltre il limite del tracciato, l'area della schermata all'esterno del percorso non verrà compilata. La figura seguente mostra cosa accade se si modifica la chiamata [**Graphics:: FillEllipse**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillellipse(inconstbrush_inreal_inreal_inreal_inreal)) nel codice precedente a `graphics.FillRectangle(&pthGrBrush, 0, 10, 200, 40)` .

![illustrazione che mostra una sezione orizzontale dell'ellisse precedente](images/pathgradient2.png)

## <a name="specifying-points-on-the-boundary"></a>Specifica di punti sul limite

Nell'esempio seguente viene creato un pennello sfumatura tracciato da un percorso a forma di stella. Il codice chiama il metodo [**PathGradientBrush:: SetCenterColor**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor) per impostare il colore al centro della stella su rosso. Il codice chiama quindi il metodo [**PathGradientBrush:: SetSurroundColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setsurroundcolors) per specificare vari colori (archiviati nella matrice [**Colors**](/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color) ) nei singoli punti della matrice [**Points**](/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point) . L'istruzione del codice finale riempie il tracciato a forma di stella con il pennello sfumatura del percorso.


```
// Put the points of a polygon in an array.
Point points[] = {Point(75, 0),    Point(100, 50), 
                  Point(150, 50),  Point(112, 75),
                  Point(150, 150), Point(75, 100), 
                  Point(0, 150),   Point(37, 75), 
                  Point(0, 50),    Point(50, 50)};

// Use the array of points to construct a path.
GraphicsPath path;
path.AddLines(points, 10);

// Use the path to construct a path gradient brush.
PathGradientBrush pthGrBrush(&path);

// Set the color at the center of the path to red.
pthGrBrush.SetCenterColor(Color(255, 255, 0, 0));

// Set the colors of the points in the array.
Color colors[] = {Color(255, 0, 0, 0),   Color(255, 0, 255, 0),
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255), 
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0), 
                  Color(255, 0, 0, 255), Color(255, 255, 255, 255),
                  Color(255, 0, 0, 0),   Color(255, 0, 255, 0)};

int count = 10;
pthGrBrush.SetSurroundColors(colors, &count);

// Fill the path with the path gradient brush.
graphics.FillPath(&pthGrBrush, &path);
```



La figura seguente mostra la stella piena.

![illustrazione che mostra una stella a cinque punte che si riempie dal rosso al centro fino a vari colori in ogni punto della stella](images/pathgradient3.png)

Nell'esempio seguente viene costruito un pennello sfumatura del percorso basato su una matrice di punti. Un colore viene assegnato a ognuno dei cinque punti della matrice. Se fosse necessario connettere i cinque punti per linee rette, si otterrebbe un poligono a cinque lati. Un colore viene assegnato anche al centro (baricentro) del poligono, in questo esempio il centro (80, 75) è impostato su bianco. L'istruzione final code nell'esempio riempie un rettangolo con il pennello sfumatura del percorso.

Il colore utilizzato per riempire il rettangolo è bianco in corrispondenza di (80, 75) e viene modificato gradualmente man mano che si allontana (80, 75) verso i punti nella matrice. Ad esempio, quando si passa da (80, 75) a (0, 0), il colore cambia gradualmente da bianco a rosso e quando si passa da (80, 75) a (160, 0), il colore cambia gradualmente dal bianco al verde.


```
// Construct a path gradient brush based on an array of points.
PointF ptsF[] = {PointF(0.0f, 0.0f), 
                 PointF(160.0f, 0.0f), 
                 PointF(160.0f, 200.0f),
                 PointF(80.0f, 150.0f),
                 PointF(0.0f, 200.0f)};

PathGradientBrush pBrush(ptsF, 5);

// An array of five points was used to construct the path gradient
// brush. Set the color of each point in that array.
Color colors[] = {Color(255, 255, 0, 0),  // (0, 0) red
                  Color(255, 0, 255, 0),  // (160, 0) green
                  Color(255, 0, 255, 0),  // (160, 200) green
                  Color(255, 0, 0, 255),  // (80, 150) blue
                  Color(255, 255, 0, 0)}; // (0, 200) red

int count = 5;
pBrush.SetSurroundColors(colors, &count);

// Set the center color to white.
pBrush.SetCenterColor(Color(255, 255, 255, 255));

// Use the path gradient brush to fill a rectangle.
graphics.FillRectangle(&pBrush, Rect(0, 0, 180, 220));
```



Si noti che nel codice precedente non è presente alcun oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Il costruttore [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) particolare nell'esempio riceve un puntatore a una matrice di punti, ma non richiede un oggetto **GraphicsPath** . Si noti inoltre che il pennello sfumatura del percorso viene utilizzato per riempire un rettangolo, non un percorso. Il rettangolo è più grande del percorso utilizzato per definire il pennello, quindi parte del rettangolo non viene disegnata dal pennello. Nella figura seguente viene illustrato il rettangolo (linea tratteggiata) e la parte del rettangolo disegnata dal pennello sfumatura del percorso.

![illustrazione che mostra un rettangolo delimitato da una linea tratteggiata, parzialmente disegnata da una sfumatura multicolore](images/gradient4.png)

## <a name="customizing-a-path-gradient"></a>Personalizzazione di una sfumatura di tracciato

Un modo per personalizzare un pennello sfumatura del tracciato consiste nell'impostare le scale dello stato attivo. Le scale dello stato attivo specificano un percorso interno che si trova all'interno del percorso principale. Il colore centrale viene visualizzato ovunque all'interno del percorso interno anziché solo al punto centrale. Per impostare le scale dello stato attivo di un pennello sfumatura del tracciato, chiamare il metodo [**PathGradientBrush:: SetFocusScales**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setfocusscales) .

Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un percorso ellittico. Il codice imposta il colore limite su blu, imposta il colore centrale su Aqua, quindi usa il pennello sfumatura tracciato per riempire il percorso ellittico.

Il codice imposta quindi le scale dello stato attivo del pennello sfumatura del percorso. La scala dello stato attivo x è impostata su 0,3 e la scala dello stato attivo y è impostata su 0,8. Il codice chiama il metodo [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) di un oggetto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in modo che la chiamata successiva a [**Graphics:: FillPath**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-fillpath) riempia un'ellisse che si trova a destra della prima ellisse.

Per visualizzare l'effetto delle scale di messa a fuoco, Immaginate una piccola ellisse che condivide il centro con l'ellisse principale. L'ellisse (interna) di piccole dimensioni è l'ellisse principale ridimensionata orizzontalmente (attorno al centro) per un fattore di 0,3 e verticalmente in base a un fattore di 0,8. Quando si passa dal limite dell'ellisse esterna al limite dell'ellisse interna, il colore passa gradualmente da blu a Aqua. Quando si passa dal limite dell'ellisse interna al centro condiviso, il colore rimane Aqua.


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 200, 100);

// Create a path gradient brush based on the elliptical path.
PathGradientBrush pthGrBrush(&path);
pthGrBrush.SetGammaCorrection(TRUE);

// Set the color along the entire boundary to blue.
Color color(Color(255, 0, 0, 255));
INT num = 1;
pthGrBrush.SetSurroundColors(&color, &num);

// Set the center color to aqua.
pthGrBrush.SetCenterColor(Color(255, 0, 255, 255));
 
// Use the path gradient brush to fill the ellipse. 
graphics.FillPath(&pthGrBrush, &path);

// Set the focus scales for the path gradient brush.
pthGrBrush.SetFocusScales(0.3f, 0.8f);

// Use the path gradient brush to fill the ellipse again.
// Show this filled ellipse to the right of the first filled ellipse.
graphics.TranslateTransform(220.0f, 0.0f);
graphics.FillPath(&pthGrBrush, &path);
```



Nella figura seguente viene illustrato l'output del codice precedente. L'ellisse a sinistra è Aqua solo al punto centrale. L'ellisse a destra è Aqua ovunque all'interno del percorso interno.

![illustrazione che mostra due ellissi che ombreggiano da Aqua a blu: la prima è molto piccola. il secondo è molto più](images/focusscales1.png)

Un altro modo per personalizzare un pennello sfumatura del tracciato consiste nel specificare una matrice di colori preimpostati e una matrice di posizioni di interpolazione.

Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un triangolo. Il codice chiama il metodo [**PathGradientBrush:: SetInterpolationColors**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-pathgradientbrush-setinterpolationcolors) del pennello sfumatura del percorso per specificare una matrice di colori di interpolazione (verde scuro, Aqua, blu) e una matrice di posizioni di interpolazione (0, 0,25, 1). Quando si passa dal limite del triangolo al punto centrale, il colore cambia gradualmente da verde scuro a Aqua e quindi da Aqua a blu. Il passaggio da verde scuro a Aqua avviene nel 25% della distanza dal verde scuro al blu.


```
// Vertices of the triangle
Point points[] = {Point(100, 0), 
                  Point(200, 200), 
                  Point(0, 200)};

// No GraphicsPath object is created. The PathGradient
// brush is constructed directly from the array of points.
PathGradientBrush pthGrBrush(points, 3);

Color presetColors[] = {
   Color(255, 0, 128, 0),    // Dark green
   Color(255, 0, 255, 255),  // Aqua
   Color(255, 0, 0, 255)};   // Blue

REAL interpPositions[] = {
   0.0f,   // Dark green is at the boundary of the triangle.
   0.25f,  // Aqua is 25 percent of the way from the boundary
           // to the center point.
   1.0f};  // Blue is at the center point.
                  
pthGrBrush.SetInterpolationColors(presetColors, interpPositions, 3);

// Fill a rectangle that is larger than the triangle
// specified in the Point array. The portion of the
// rectangle outside the triangle will not be painted.
graphics.FillRectangle(&pthGrBrush, 0, 0, 200, 200);
```



Nella figura seguente viene illustrato l'output del codice precedente.

![illustrazione che mostra un triangolo che sfuma da blu al centro, a Aqua, in verde ai bordi](images/pathgradient4.png)

## <a name="setting-the-center-point"></a>Impostazione del punto centrale

Per impostazione predefinita, il punto centrale di un pennello sfumatura del tracciato si trova al centro del tracciato usato per costruire il pennello. È possibile modificare la posizione del punto centrale chiamando il metodo [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) della classe [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) .

Nell'esempio seguente viene creato un pennello sfumatura del percorso basato su un'ellisse. Il centro dell'ellisse si trova in (70, 35), ma il punto centrale del pennello sfumatura del tracciato è impostato su (120, 40).


```
// Create a path that consists of a single ellipse.
GraphicsPath path;
path.AddEllipse(0, 0, 140, 70);

// Use the path to construct a brush.
PathGradientBrush pthGrBrush(&path);

// Set the center point to a location that is not the centroid of the path.
pthGrBrush.SetCenterPoint(Point(120, 40));

// Set the color at the center point to blue.
pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

// Set the color along the entire boundary of the path to aqua.
Color colors[] = {Color(255, 0, 255, 255)};
int count = 1;
pthGrBrush.SetSurroundColors(colors, &count);

graphics.FillEllipse(&pthGrBrush, 0, 0, 140, 70);
```



Nella figura seguente vengono illustrati l'ellisse piena e il punto centrale del pennello sfumatura del percorso.

![illustrazione che mostra un'ellisse che riempie da blu a Aqua da un punto centrale vicino a un'estremità](images/pathgradient5.png)

È possibile impostare il punto centrale di un pennello sfumatura tracciato su una posizione esterna al percorso utilizzato per costruire il pennello. Nel codice precedente, se si sostituisce la chiamata a [**PathGradientBrush:: SetCenterPoint**](/windows/win32/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)) con `pthGrBrush.SetCenterPoint(Point(145, 35))` , si otterrà il risultato seguente.

![illustrazione che mostra un'ellisse riempita da rosso a giallo da un punto centrale esterno al bordo dell'ellisse](images/pathgradient6.png)

Nell'illustrazione precedente, i punti all'estrema destra dell'ellisse non sono puri blu (anche se sono molto vicini). I colori della sfumatura sono posizionati come se il riempimento avesse avuto la possibilità di raggiungere il punto (145, 35), il colore avrebbe raggiunto il blu puro (0, 0, 255). Tuttavia, il riempimento non raggiunge mai (145, 35) perché un pennello sfumatura del percorso disegna solo all'interno del percorso.

 

 
