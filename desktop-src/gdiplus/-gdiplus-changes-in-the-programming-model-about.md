---
description: Le sezioni seguenti descrivono diversi modi in cui la programmazione con Windows GDI+ è diversa dalla programmazione con Windows Graphics Device Interface (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Modifiche al modello di programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90cd6f1c3a6ebab1e55562e67cb4926f0ffedf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049868"
---
# <a name="changes-in-the-programming-model"></a>Modifiche al modello di programmazione

Le sezioni seguenti descrivono diversi modi in cui la programmazione con Windows GDI+ è diversa dalla programmazione con Windows Graphics Device Interface (GDI).

-   [Contesti di dispositivo, handle e oggetti grafici](#device-contexts-handles-and-graphics-objects)
-   [Due modi per creare una linea](#two-ways-to-draw-a-line)
    -   [Disegno di una linea con GDI](#drawing-a-line-with-gdi)
    -   [Disegno di una linea con GDI+ e interfaccia della classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Penne, pennelli, percorsi, immagini e tipi di carattere come parametri](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Overload di metodi](#method-overloading)
-   [Non sono più presenti posizioni correnti](#no-more-current-position)
-   [Metodi distinti per l'estrazione e il riempimento](#separate-methods-for-draw-and-fill)
-   [Creazione di aree](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contesti di dispositivo, handle e oggetti grafici

Se sono stati scritti programmi che usano GDI (l'interfaccia grafica del dispositivo inclusa nelle versioni precedenti di Windows), si ha familiarità con l'idea di un contesto di dispositivo (DC). Un contesto di dispositivo è una struttura usata da Windows per archiviare informazioni sulle funzionalità di uno specifico dispositivo di visualizzazione e gli attributi che specificano la modalità di disegno degli elementi su tale dispositivo. Un contesto di dispositivo per una visualizzazione video è associato anche a una particolare finestra sullo schermo. Per prima cosa si ottiene un handle per un contesto di dispositivo (HDC), quindi si passa tale handle come argomento alle funzioni GDI che eseguono effettivamente il disegno. È anche possibile passare l'handle come argomento alle funzioni GDI che ottengono o impostano gli attributi del contesto di dispositivo.

Quando si utilizza GDI+, non è necessario preoccuparsi degli handle e dei contesti di dispositivo come si fa quando si utilizza GDI. È sufficiente creare un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e richiamarne i metodi nel familiare stile orientato a oggetti, ovvero MyGraphicsObject. DrawLine (*Parameters*). L'oggetto **Graphics** si trova all'interno di GDI+ esattamente come il contesto del dispositivo è alla base di GDI. Il contesto di dispositivo e l'oggetto **Graphics** svolgono ruoli simili, ma esistono alcune differenze fondamentali tra il modello di programmazione basato su handle usato con i contesti di dispositivo (GDI) e il modello orientato a oggetti usato con gli oggetti **grafici** (GDI+).

L'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , come il contesto di dispositivo, è associato a una particolare finestra sullo schermo e contiene attributi, ad esempio modalità di smussatura e hint per il rendering del testo, che specificano la modalità di disegno degli elementi. Tuttavia, l'oggetto **Graphics** non è associato a una penna, un pennello, un percorso, un'immagine o un tipo di carattere come contesto di dispositivo. Ad esempio, in GDI, prima di poter usare un contesto di dispositivo per creare una linea, è necessario chiamare [SelezionaOggetto](/windows/win32/api/wingdi/nf-wingdi-selectobject) per associare un oggetto Pen al contesto di dispositivo. Questa operazione viene definita selezione della penna nel contesto di dispositivo. Tutte le linee disegnate nel contesto di dispositivo useranno tale penna fino a quando non si seleziona una penna diversa. Con GDI+, viene passato un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) come argomento al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della classe **Graphics** . È possibile usare un oggetto **Pen** diverso in ognuna di una serie di chiamate DrawLine senza dover associare un oggetto **penna** specificato a un oggetto **Graphics** .

## <a name="two-ways-to-draw-a-line"></a>Due modi per creare una linea

I due esempi seguenti consentono di creare una linea rossa di larghezza 3 dalla posizione (20, 10) alla posizione (200.100). Nel primo esempio viene chiamato GDI e il secondo chiama GDI+ tramite l'interfaccia della classe C++.

-   [Disegno di una linea con GDI](#drawing-a-line-with-gdi)
-   [Disegno di una linea con GDI+ e interfaccia della classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Disegno di una linea con GDI

Per creare una linea con GDI, sono necessari due oggetti: un contesto di dispositivo e una penna. Si ottiene un handle per un contesto di dispositivo chiamando [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)e un handle a una penna chiamando [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Chiamare quindi [SelezionaOggetto](/windows/win32/api/wingdi/nf-wingdi-selectobject) per selezionare la penna nel contesto di dispositivo. Per impostare la posizione della penna su (20, 10), chiamare [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) , quindi creare una linea da tale posizione nella penna (200, 100) chiamando **LineTo**. Si noti che MoveToEx e [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) entrambi ricevono **HDC** come argomento.


```
HDC          hdc;
PAINTSTRUCT  ps;
HPEN         hPen;
HPEN         hPenOld;
hdc = BeginPaint(hWnd, &ps);
   hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
   hPenOld = (HPEN)SelectObject(hdc, hPen);
   MoveToEx(hdc, 20, 10, NULL);
   LineTo(hdc, 200, 100);
   SelectObject(hdc, hPenOld);
   DeleteObject(hPen);
EndPaint(hWnd, &ps);
```



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Disegno di una linea con GDI+ e interfaccia della classe C++

Per creare una linea con GDI+ e l'interfaccia della classe C++, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Si noti che gli handle di questi oggetti non vengono richiesti da Windows. Usare invece i costruttori per creare un'istanza della classe **grafica** (un oggetto **Graphics** ) e un'istanza della classe **Pen** (un oggetto **Pen** ). Il disegno di una linea richiede la chiamata del metodo [**Graphics::D rawline**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della classe **Graphics** . Il primo parametro del metodo **Graphics::D rawline** è un puntatore all'oggetto **Pen** . Si tratta di uno schema più semplice e flessibile rispetto alla selezione di una penna in un contesto di dispositivo, come illustrato nell'esempio GDI precedente.


```
HDC          hdc;
PAINTSTRUCT  ps;
Pen*         myPen;
Graphics*    myGraphics;
hdc = BeginPaint(hWnd, &ps);
   myPen = new Pen(Color(255, 255, 0, 0), 3);
   myGraphics = new Graphics(hdc);
   myGraphics->DrawLine(myPen, 20, 10, 200, 100);
   delete myGraphics;
   delete myPen;
EndPaint(hWnd, &ps);
```



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Penne, pennelli, percorsi, immagini e tipi di carattere come parametri

Gli esempi precedenti mostrano che gli oggetti [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) possono essere creati e gestiti separatamente dall'oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , che fornisce i metodi di disegno. Gli oggetti [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush), [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath), [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)e [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) possono anche essere creati e gestiti separatamente dall'oggetto **Graphics** . Molti dei metodi di disegno forniti dalla classe **Graphics** ricevono un oggetto **Brush**, **GraphicsPath**, **Image** o **font** come argomento. Ad esempio, l'indirizzo di un oggetto **Brush** viene passato come argomento al metodo [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e l'indirizzo di un oggetto **GraphicsPath** viene passato come argomento al metodo [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) . Analogamente, gli indirizzi degli oggetti **Image** e **font** vengono passati ai metodi [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) e [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) . Questo si differenzia da GDI in cui si seleziona un pennello, un percorso, un'immagine o un tipo di carattere nel contesto di dispositivo, quindi si passa un handle al contesto di dispositivo come argomento a una funzione di disegno.

## <a name="method-overloading"></a>Overload di metodi

Molti dei metodi GDI+ sono in overload. ovvero, diversi metodi condividono lo stesso nome ma hanno elenchi di parametri diversi. Ad esempio, il metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è costituito dai formati seguenti:


```
Status DrawLine(IN const Pen* pen,
                IN REAL x1,
                IN REAL y1,
                IN REAL x2,
                IN REAL y2);
Status DrawLine(IN const Pen* pen,
                IN const PointF& pt1,
                IN const PointF& pt2);
Status DrawLine(IN const Pen* pen,
                IN INT x1,
                IN INT y1,
                IN INT x2,
                IN INT y2);
    
Status DrawLine(IN const Pen* pen,
                IN const Point& pt1,
                IN const Point& pt2);
```



Tutte e quattro le varianti di [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) precedenti ricevono un puntatore a un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) , le coordinate del punto iniziale e le coordinate del punto finale. Le prime due varianti ricevono le coordinate come numeri a virgola mobile e le ultime due varianti ricevono le coordinate come numeri interi. La prima e la terza variante ricevono le coordinate come un elenco di quattro numeri distinti, mentre la seconda e la quarta variazione ricevono le coordinate come coppia di oggetti [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (o [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).

## <a name="no-more-current-position"></a>Non sono più presenti posizioni correnti

Si noti che nei metodi [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) illustrati in precedenza il punto iniziale e il punto finale della linea vengono ricevuti come argomenti. Si tratta di una partenza dallo schema GDI in cui si **chiama MoveToEx** per impostare la posizione corrente della penna seguita da **LineTo** per creare una riga che inizia con (**X1**, **Y1**) e termina in corrispondenza di (**X2**, **Y2**). GDI+ nel suo complesso ha abbandonato la nozione di posizione corrente.

## <a name="separate-methods-for-draw-and-fill"></a>Metodi distinti per l'estrazione e il riempimento

GDI+ è più flessibile di GDI quando si tratta di disegnare i profili e di riempire gli interni di forme come i rettangoli. GDI dispone di una funzione [Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) che disegna la struttura e riempie l'area interna di un rettangolo in un unico passaggio. Il contorno viene disegnato con la penna attualmente selezionata e la parte interna viene riempita con il pennello attualmente selezionato.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ dispone di metodi distinti per disegnare la struttura e riempire l'area interna di un rettangolo. Il metodo [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) come uno dei relativi parametri e il metodo [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) ha l'indirizzo di un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) come uno dei relativi parametri.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Si noti che i metodi [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) in GDI+ ricevono argomenti che specificano il bordo sinistro, superiore, larghezza e altezza del rettangolo. Si differenzia dalla funzione[Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) GDI, che accetta argomenti che specificano il bordo sinistro, il bordo destro, l'inizio e la fine del rettangolo. Si noti inoltre che il costruttore per la classe [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) in GDI+ dispone di quattro parametri. Gli ultimi tre parametri sono i normali valori rosso, verde e blu; il primo parametro è il valore alfa, che specifica la misura in cui il colore da disegnare viene mescolato con il colore di sfondo.

## <a name="constructing-regions"></a>Creazione di aree

GDI fornisce diverse funzioni per la creazione di aree: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn e CreatePolyPolygonRgn. Ci si potrebbe aspettare che la classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) in GDI+ abbia costruttori analoghi che accettano rettangoli, ellissi, rettangoli arrotondati e poligoni come argomenti, ma questo non è il caso. La classe **Region** in GDI+ fornisce un costruttore che riceve un riferimento a un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e un altro costruttore che riceve l'indirizzo di un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) . Per costruire un'area in base a un'ellisse, a un rettangolo arrotondato o a un poligono, è possibile creare facilmente un oggetto **GraphicsPath** (che contiene un'ellisse, ad esempio) e quindi passare l'indirizzo dell'oggetto **GraphicsPath** a un costruttore di **area** .

GDI+ consente di creare facilmente aree complesse combinando forme e percorsi. La classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) dispone di metodi [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) e [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) che è possibile usare per aumentare un'area esistente con un percorso o un'altra area. Una funzionalità interessante dello schema GDI+ è che un oggetto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) non viene eliminato definitivamente quando viene passato come argomento a un costruttore di **area** . In GDI è possibile convertire un percorso in un'area con la funzione [PathToRegion](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) , ma il percorso viene eliminato definitivamente nel processo. Inoltre, un oggetto **GraphicsPath** non viene eliminato definitivamente quando il relativo indirizzo viene passato come argomento a un metodo Union o Intersect, quindi è possibile utilizzare un percorso specificato come blocco predefinito per diverse aree separate. come illustrato nell'esempio seguente. Si supponga che **OnePath** sia un puntatore a un oggetto **GraphicsPath** (semplice o complesso) che è già stato inizializzato.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
