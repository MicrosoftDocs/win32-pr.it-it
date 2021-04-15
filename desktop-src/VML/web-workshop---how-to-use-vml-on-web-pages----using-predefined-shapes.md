---
title: Uso di forme predefinite
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web Workshop, forme predefinite
- progettazione di pagine Web, forme predefinite
- Vector Markup Language (la), forme predefinite
- LA (Vector Markup Language), forme predefinite
- grafica vettoriale, forme predefinite
- Forme la, predefinite
- forme predefinite
- Vector Markup Language (la), elemento Rect
- LA (Vector Markup Language), elemento Rect
- grafica vettoriale, elemento Rect
- elemento Rect
- Elementi la, Rect
- Vector Markup Language (la), elemento RoundRect
- LA (Vector Markup Language), elemento RoundRect
- grafica vettoriale, elemento RoundRect
- elemento RoundRect
- Elementi la, RoundRect
- Vector Markup Language (la), elemento linea
- LA (Vector Markup Language), elemento linea
- grafica vettoriale, elemento linea
- elemento Line
- Elementi la, riga
- Vector Markup Language (la), elemento polilinea
- LA (Vector Markup Language), elemento polilinea
- grafica vettoriale, elemento polilinea
- elemento polilinea
- Elementi la, polilinea
- Vector Markup Language (la), elemento curva
- LA (Vector Markup Language), elemento curva
- grafica vettoriale, elemento curva
- curva-elemento
- Elementi la, curva
- Vector Markup Language (la), elemento Arc
- LA (Vector Markup Language), elemento Arc
- grafica vettoriale, elemento Arc
- elemento Arc
- Elementi la, Arc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c1cafacf00f6f3f9129c29c56837f3f485aa3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516882"
---
# <a name="using-predefined-shapes"></a>Uso di forme predefinite

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

Come si è appreso, è possibile usare l' `<oval>` elemento di la per creare un semplice Oval. LA fornisce molti altri elementi predefiniti. In questo argomento verrà illustrato come creare grafica usando questi elementi.

In questo argomento

-   [Rect](#roundrect)
-   [RoundRect](#roundrect)
-   [linea](#polyline)
-   [polilinea](#polyline)
-   [curva](#curve)
-   [arco](#arc)
-   [Summary](#summary)

## <a name="rect"></a>rect

`<rect>`Per creare un rettangolo, è possibile usare l'elemento. È quindi possibile personalizzare il rettangolo specificando attributi di proprietà diversi.

Ad esempio, è possibile disegnare un rettangolo che viene riempito con blu specificando **FillColor**= "Blue" e assegnargli un contorno rosso a 3,5 punti specificando **StrokeColor**= "Red" **StrokeWeight**= "3.5 pt", come illustrato nella rappresentazione la seguente:

![rect1.gif (485 byte)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . Nota: la specifica la non dispone di un segnalibro per l' `<rect>` elemento.

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="roundrect"></a>RoundRect

È possibile utilizzare l' `<roundrect>` elemento per creare un rettangolo con angoli arrotondati. È quindi possibile personalizzare il rettangolo arrotondato specificando attributi di proprietà diversi.

È possibile, ad esempio, disegnare un rettangolo con angoli arrotondati del 30% della metà della dimensione più piccola del rettangolo specificando **arcsize**= "0,3", riempirlo con il giallo specificando **FillColor**= "Yellow" e assegnargli un contorno rosso a 2 punte specificando **StrokeColor**= "Red" **StrokeWeight**= "2PT", come illustrato nella rappresentazione la seguente:

![roundrect1.gif (622 byte)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="line"></a>line

È possibile usare l' `<line>` elemento per creare una linea retta. È quindi possibile personalizzare la riga specificando attributi di proprietà diversi.

Ad esempio, è possibile creare una linea orizzontale specificando **from**= "20pt, 20pt" **a**= "100PT, 20pt" e impostarla su 2-Point e Red specificando **StrokeColor**= "Red" **StrokeWeight**= "2PT", come illustrato nella rappresentazione la seguente:

![line1.gif (88 byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





È possibile creare una linea verticale o diagonale semplicemente specificando valori diversi per gli attributi di proprietà **from** e **to** , come illustrato nella rappresentazione la seguente:

![line2.gif (86 byte)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="polyline"></a>polilinea

È possibile utilizzare l' `<polyline>` elemento per definire forme create da segmenti di linea connessi. È quindi possibile personalizzare la forma specificando attributi di proprietà diversi.

Per disegnare la forma illustrata nell'immagine seguente, ad esempio, è possibile digitare la rappresentazione la seguente:

![polyline1.gif (957 byte)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="curve"></a>curva

È possibile usare l' `<curve>` elemento per creare una curva di Bézier cubica. È quindi possibile personalizzare la curva specificando attributi di proprietà diversi.

Ad esempio, per creare una curva come illustrato nell'immagine seguente, è possibile digitare la rappresentazione la seguente:

![curve1.gif (992 byte)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="arc"></a>arco

È possibile utilizzare l' `<arc>` elemento per creare un arco definito come segmento di un Oval. L'arco è definito dall'intersezione dell'ovale con i vettori RADIUS iniziale e finale specificati dagli angoli. Gli angoli vengono calcolati usando le proprietà di un cerchio (larghezza uguale a altezza), quindi ridimensionato in modo anisotropico fino alla larghezza e all'altezza desiderate.

Ad esempio, è possibile creare un arco che inizia con 0 gradi e termina con 90 gradi specificando **startAngle** **= "0",** ovvero "90", come illustrato nella rappresentazione la seguente:

![arc1.gif (410 byte)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





È possibile modificare l'arco specificando **valori diversi** per **startAngle** e indicizzazione, come illustrato nella rappresentazione la seguente:

![arc2.gif (608 byte)](images/arc2.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="180"
strokecolor="red" strokeweight="2pt"/>
```





![arc3.gif (807 byte)](images/arc3.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="270"
strokecolor="red" strokeweight="2pt"/>
```





Per ulteriori informazioni su questo elemento, vedere la [specifica la](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![Torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile utilizzare gli elementi predefiniti la, ad esempio `<oval>` ,, `<line>` `<polyline>` , `<curve>` , `<rect>` , `<roundrect>` e `<arc>` per creare facilmente la grafica in una pagina Web e quindi personalizzare tali immagini cambiando semplicemente gli attributi di proprietà.

 

 