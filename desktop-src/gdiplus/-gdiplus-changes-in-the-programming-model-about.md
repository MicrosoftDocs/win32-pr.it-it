---
description: Le sezioni seguenti descrivono diversi modi in cui la programmazione con Windows GDI+ è diversa dalla programmazione con Windows Graphics Device Interface (GDI).
ms.assetid: 89a154c1-6a49-45d6-a73c-94b0b1567408
title: Modifiche al modello di programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05dd8b74662d0141405b9d11b9b4446ffb19dd4ef3bfdec788afe7a51a8c681a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249888"
---
# <a name="changes-in-the-programming-model"></a>Modifiche al modello di programmazione

Le sezioni seguenti descrivono diversi modi in cui la programmazione con Windows GDI+ è diversa dalla programmazione con Windows Graphics Device Interface (GDI).

-   [Contesti di dispositivo, handle e oggetti grafici](#device-contexts-handles-and-graphics-objects)
-   [Due modi per disegnare una linea](#two-ways-to-draw-a-line)
    -   [Disegno di una linea con GDI](#drawing-a-line-with-gdi)
    -   [Disegno di una linea con GDI+ e l'interfaccia della classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)
-   [Penna, pennelli, tracciati, immagini e tipi di carattere come parametri](#pens-brushes-paths-images-and-fonts-as-parameters)
-   [Overload del metodo](#method-overloading)
-   [No More Current Position](#no-more-current-position)
-   [Metodi separati per il disegno e il riempimento](#separate-methods-for-draw-and-fill)
-   [Costruzione di aree](#constructing-regions)

## <a name="device-contexts-handles-and-graphics-objects"></a>Contesti di dispositivo, handle e oggetti grafici

Se sono stati scritti programmi con GDI (l'interfaccia del dispositivo grafico inclusa nelle versioni precedenti di Windows), si ha familiarità con l'idea di un contesto di dispositivo (DC). Un contesto di dispositivo è una struttura usata da Windows per archiviare informazioni sulle funzionalità di un particolare dispositivo di visualizzazione e attributi che specificano come verranno disegnati gli elementi in tale dispositivo. Un contesto di dispositivo per una visualizzazione video è associato anche a una determinata finestra sullo schermo. Prima di tutto si ottiene un handle per un contesto di dispositivo (HDC) e quindi si passa tale handle come argomento alle funzioni GDI che esere effettivamente il disegno. L'handle viene passato anche come argomento alle funzioni GDI che ottengono o impostano gli attributi del contesto di dispositivo.

Quando si usa GDI+, non è necessario preoccuparsi degli handle e dei contesti di dispositivo come quando si usa GDI. È sufficiente creare un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e quindi richiamarne i metodi nello stile orientato agli oggetti familiare, myGraphicsObject.DrawLine(*parameters*). **L'oggetto Graphics** è alla base dell'GDI+ proprio come il contesto di dispositivo è alla base di GDI. Il contesto di dispositivo e l'oggetto **Graphics** svolgono ruoli simili, ma esistono alcune differenze fondamentali tra il modello di  programmazione basato su handle usato con i contesti di dispositivo (GDI) e il modello orientato a oggetti usato con gli oggetti Graphics (GDI+).

L'oggetto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) come il contesto di dispositivo, è associato a una determinata finestra sullo schermo e contiene attributi ,ad esempio la modalità smoothing e l'hint per il rendering del testo, che specificano la modalità di disegno degli elementi. Tuttavia, **l'oggetto Graphics** non è associato a una penna, un pennello, un percorso, un'immagine o un tipo di carattere come un contesto di dispositivo. Ad esempio, in GDI, prima di poter usare un contesto di dispositivo per disegnare una linea, è necessario chiamare [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) per associare un oggetto penna al contesto di dispositivo. Questa operazione viene definita selezione della penna nel contesto di dispositivo. Tutte le linee disegnate nel contesto di dispositivo useranno tale penna fino a quando non si seleziona una penna diversa. Con GDI+, si passa un [**oggetto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) come argomento al [metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della **classe** Graphics. È possibile usare un **oggetto Pen** diverso in ogni serie di chiamate DrawLine senza dover associare un determinato **oggetto Pen** a un **oggetto** Graphics.

## <a name="two-ways-to-draw-a-line"></a>Due modi per disegnare una linea

I due esempi seguenti disegnano ognuno una linea rossa di larghezza 3 dalla posizione (20, 10) alla posizione (200,100). Il primo esempio chiama GDI e il secondo chiama GDI+ tramite l'interfaccia della classe C++.

-   [Disegno di una linea con GDI](#drawing-a-line-with-gdi)
-   [Disegno di una linea con GDI+ e l'interfaccia della classe C++](#drawing-a-line-with-gdi-and-the-c-class-interface)

### <a name="drawing-a-line-with-gdi"></a>Disegno di una linea con GDI

Per disegnare una linea con GDI, sono necessari due oggetti: un contesto di dispositivo e una penna. Per ottenere un handle per un contesto di dispositivo, chiamare [**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)e un handle per una penna chiamando [CreatePen](/windows/win32/api/wingdi/nf-wingdi-createpen). Chiamare quindi [SelectObject](/windows/win32/api/wingdi/nf-wingdi-selectobject) per selezionare la penna nel contesto di dispositivo. Impostare la posizione della penna su (20, 10) chiamando [MoveToEx](/windows/win32/api/wingdi/nf-wingdi-movetoex) e quindi disegnare una linea dalla posizione della penna a (200, 100) chiamando **LineTo**. Si noti che MoveToEx e [LineTo](/windows/win32/api/wingdi/nf-wingdi-lineto) ricevono **entrambi hdc** come argomento.


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



### <a name="drawing-a-line-with-gdi-and-the-c-class-interface"></a>Disegno di una linea con GDI+ e l'interfaccia della classe C++

Per disegnare una linea con GDI+ e l'interfaccia della classe C++, sono necessari un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un [**oggetto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Si noti che non è necessario Windows handle per questi oggetti. Usare invece i costruttori per creare un'istanza della classe **Graphics** (un **oggetto Graphics)** e un'istanza della **classe Pen** **(un oggetto Pen).** Il disegno di una linea comporta la chiamata del metodo [**Graphics::D rawLine**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della **classe Graphics.** Il primo parametro del **metodo Graphics::D rawLine** è un puntatore all'oggetto Pen.  Si tratta di uno schema più semplice e flessibile rispetto alla selezione di una penna in un contesto di dispositivo, come illustrato nell'esempio GDI precedente.


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



## <a name="pens-brushes-paths-images-and-fonts-as-parameters"></a>Penna, pennelli, tracciati, immagini e tipi di carattere come parametri

Gli esempi precedenti mostrano che [**gli oggetti Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) possono essere creati e gestiti separatamente dall'oggetto [**Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) che fornisce i metodi di disegno. [**Gli oggetti Brush,**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) [**GraphicsPath,**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image)e [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) possono anche essere creati e gestiti separatamente **dall'oggetto** Graphics. Molti dei metodi di disegno forniti dalla **classe Graphics** ricevono un oggetto **Brush**, **GraphicsPath**, **Image** o **Font** come argomento. Ad esempio, l'indirizzo di un oggetto **Brush** viene passato come argomento al metodo [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e l'indirizzo di un **oggetto GraphicsPath** viene passato come argomento al metodo [**Graphics::D rawPath.**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) Analogamente, gli indirizzi **degli oggetti Image** e **Font** vengono passati ai [metodi DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_)) e [DrawString.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) A differenza di GDI, in cui si seleziona un pennello, un percorso, un'immagine o un tipo di carattere nel contesto di dispositivo e quindi si passa un handle al contesto di dispositivo come argomento a una funzione di disegno.

## <a name="method-overloading"></a>Overload del metodo

Molti dei metodi GDI+ sono sottoposti a overload. in altre informazioni, diversi metodi condividono lo stesso nome, ma hanno elenchi di parametri diversi. Ad esempio, il [metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) della [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) è disponibile nei formati seguenti:


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



Tutte e quattro le variazioni [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) precedenti ricevono un puntatore a un oggetto [**Pen,**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) le coordinate del punto iniziale e le coordinate del punto finale. Le prime due varianti ricevono le coordinate come numeri a virgola mobile e le ultime due le ricevono come numeri interi. La prima e la terza variante ricevono le coordinate come elenco di quattro numeri separati, mentre la seconda e la quarta variante ricevono le coordinate come coppia di oggetti [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) [**(o PointF).**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)

## <a name="no-more-current-position"></a>No More Current Position

Si noti che nei [metodi DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inreal_inreal_inreal_inreal)) mostrati in precedenza sia il punto iniziale che il punto finale della linea vengono ricevuti come argomenti. Si tratta di una deviazione dallo schema GDI in cui si chiama **MoveToEx** per impostare la posizione corrente della penna seguita da **LineTo** per disegnare una linea che inizia da (**x1**, **y1**) e termina in corrispondenza di (**x2**, **y2**). GDI+ nel suo complesso ha abbandonato la nozione di posizione corrente.

## <a name="separate-methods-for-draw-and-fill"></a>Metodi separati per il disegno e il riempimento

GDI+ è più flessibile di GDI quando si tratta di disegnare i contorni e riempire gli interni di forme come rettangoli. GDI ha una [funzione Rectangle](/windows/win32/api/wingdi/nf-wingdi-rectangle) che disegna il contorno e riempie l'interno di un rettangolo tutto in un unico passaggio. Il contorno viene disegnato con la penna attualmente selezionata e l'interno viene riempito con il pennello attualmente selezionato.


```
hBrush = CreateHatchBrush(HS_CROSS, RGB(0, 0, 255));
hPen = CreatePen(PS_SOLID, 3, RGB(255, 0, 0));
SelectObject(hdc, hBrush);
SelectObject(hdc, hPen);
Rectangle(hdc, 100, 50, 200, 80);
```



GDI+ metodi separati per disegnare il contorno e riempire l'interno di un rettangolo. Il [metodo DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) ha l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) come uno dei relativi parametri e il metodo [FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) ha l'indirizzo di un oggetto [**Brush**](/windows/win32/api/gdiplusbrush/nl-gdiplusbrush-brush) come uno dei relativi parametri.


```
HatchBrush* myHatchBrush = new HatchBrush(
   HatchStyleCross,
   Color(255, 0, 255, 0),
   Color(255, 0, 0, 255));
Pen* myPen = new Pen(Color(255, 255, 0, 0), 3);
myGraphics.FillRectangle(myHatchBrush, 100, 50, 100, 30);
myGraphics.DrawRectangle(myPen, 100, 50, 100, 30);
```



Si noti che [i metodi FillRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fillrectangle(inconstbrush_inreal_inreal_inreal_inreal)) e [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inreal_inreal_inreal_inreal)) in GDI+ ricevere argomenti che specificano il bordo sinistro, la parte superiore, la larghezza e l'altezza del rettangolo. A differenza della funzione Rectangle[GDI,](/windows/win32/api/wingdi/nf-wingdi-rectangle) che accetta argomenti che specificano il bordo sinistro, il bordo destro, la parte superiore e inferiore del rettangolo. Si noti anche che il costruttore per la [**classe Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) in GDI+ ha quattro parametri. Gli ultimi tre parametri sono i soliti valori rosso, verde e blu. Il primo parametro è il valore alfa, che specifica la misura in cui il colore disegnato viene sfusato con il colore di sfondo.

## <a name="constructing-regions"></a>Costruzione di aree

GDI offre diverse funzioni per la creazione di aree: CreateRectRgn, CreateEllpticRgn, CreateRoundRectRgn, CreatePolygonRgn e CreatePolyPolygonRgn. Si potrebbe prevedere che la classe [**Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) in GDI+ abbia costruttori analoghi che accettano rettangoli, ellissi, rettangoli arrotondati e poligoni come argomenti, ma questo non è il caso. La **classe Region** in GDI+ un costruttore che riceve un riferimento a un oggetto [**Rect**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-rect) e un altro costruttore che riceve l'indirizzo di un [**oggetto GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) Se si vuole costruire un'area basata su un'ellisse, un rettangolo arrotondato o un poligono, è possibile farlo facilmente creando un **oggetto GraphicsPath** (che contiene un'ellisse, ad esempio) e quindi passando l'indirizzo di tale **oggetto GraphicsPath** a un costruttore **Region.**

GDI+ semplifica la forma di aree complesse combinando forme e percorsi. La [**classe Region**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-region) include metodi [Union](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-union(inconstrectf_)) e [Intersect](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-region-intersect(inconstgraphicspath)) che è possibile usare per aumentare un'area esistente con un percorso o un'altra area. Una funzionalità utile dello schema GDI+ è che un [**oggetto GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) non viene eliminato automaticamente quando viene passato come argomento a un **costruttore Region.** In GDI è possibile convertire un percorso in un'area con la [funzione PathToRegion,](/windows/win32/api/wingdi/nf-wingdi-pathtoregion) ma il percorso viene eliminato nel processo. Inoltre, un **oggetto GraphicsPath** non viene eliminato automaticamente quando il relativo indirizzo viene passato come argomento a un metodo Union o Intersect, pertanto è possibile usare un determinato percorso come blocco predefinito per diverse aree separate. come illustrato nell'esempio seguente. Si supponga **che onePath** sia un puntatore a **un oggetto GraphicsPath** (semplice o complesso) già inizializzato.


```
Region  region1(rect1);
Region  region2(rect2);
region1.Union(onePath);
region2.Intersect(onePath);
```



 

 
