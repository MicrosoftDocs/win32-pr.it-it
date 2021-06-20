---
title: Uso di forme predefinite
description: Questo articolo descrive l'uso di forme predefinite in VML, una funzionalità deprecata a Internet Explorer Windows 9.
ms.assetid: 9a2e8b5a-b1d0-4a73-b058-24dac1f0b655
keywords:
- Web workshop, forme predefinite
- progettazione di pagine Web, forme predefinite
- Vector Markup Language (VML), forme predefinite
- VML (Vector Markup Language),forme predefinite
- grafica vettoriale, forme predefinite
- Forme VML, predefinite
- forme predefinite
- Vector Markup Language (VML),elemento rect
- VML (Vector Markup Language),elemento rect
- grafica vettoriale, elemento rect
- Elemento rect
- Elementi VML, rect
- Vector Markup Language (VML),elemento roundrect
- VML (Vector Markup Language),elemento roundrect
- grafica vettoriale, elemento roundrect
- roundrect - elemento
- elementi VML, roundrect
- Vector Markup Language (VML),elemento line
- VML (Vector Markup Language),elemento line
- grafica vettoriale, elemento line
- line - elemento
- Elementi VML, riga
- Vector Markup Language (VML),elemento polyline
- VML (Vector Markup Language),elemento polyline
- grafica vettoriale, elemento polilinea
- elemento polyline
- elementi VML, polilinea
- Vector Markup Language (VML),elemento curve
- VML (Vector Markup Language),elemento curve
- grafica vettoriale, elemento curve
- elemento curve
- elementi VML, curva
- Vector Markup Language (VML),elemento arc
- VML (Vector Markup Language),elemento arc
- grafica vettoriale, elemento arc
- elemento arc
- elementi VML, arco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b410cf288a3ba63e4c1d745fd962a445b0b220b8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407684"
---
# <a name="using-predefined-shapes"></a>Uso di forme predefinite

Questo argomento descrive VML, una funzionalità deprecata a Internet Explorer Windows 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Come si è appreso, è possibile usare `<oval>` l'elemento di VML per creare un semplice ovale. VML fornisce diversi altri elementi predefiniti. In questo argomento verrà illustrato come disegnare grafica usando questi elementi.

In questo argomento

-   [Rect](#roundrect)
-   [roundrect](#roundrect)
-   [Linea](#polyline)
-   [Polilinea](#polyline)
-   [curva](#curve)
-   [Arco](#arc)
-   [Summary](#summary)

## <a name="rect"></a>rect

È possibile usare `<rect>` l'elemento per disegnare un rettangolo. È quindi possibile personalizzare il rettangolo specificando attributi di proprietà diversi.

Ad esempio, è possibile disegnare un rettangolo riempito di blu specificando **fillcolor**="blue" e assegnargli un contorno rosso di 3,5 punti specificando **strokecolor**="red" **strokeweight**="3.5pt", come illustrato nella rappresentazione VML seguente:

![rect1.gif (485 byte)](images/rect1.gif)


```HTML
<v:rect style='width:100pt;height:75pt' fillcolor="blue"
strokecolor="red" strokeweight="3.5pt"/>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) . Nota: la specifica VML non ha un segnalibro per `<rect>` l'elemento .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="roundrect"></a>roundrect

È possibile usare `<roundrect>` l'elemento per disegnare un rettangolo con angoli arrotondati. È quindi possibile personalizzare il rettangolo arrotondato specificando attributi di proprietà diversi.

Ad esempio, è possibile disegnare un rettangolo con angoli arrotondati pari al 30% della metà della dimensione più piccola del rettangolo specificando **arcsize**="0.3", riempirlo di giallo specificando **fillcolor**="yellow" e assegnargli un contorno rosso a 2 punti specificando **strokecolor**="red" **strokeweight**="2pt", come illustrato nella rappresentazione VML seguente:

![roundrect1.gif (622 byte)](images/roundrect1.gif)


```HTML
<v:roundrect style='width:100pt;height:75pt"
arcsize="0.3" fillcolor="yellow"
strokecolor="red" strokeweight="2pt"/>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858405) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="line"></a>line

È possibile usare `<line>` l'elemento per creare una linea retta. È quindi possibile personalizzare la riga specificando attributi di proprietà diversi.

Ad esempio, è possibile disegnare una linea orizzontale specificando da ="20pt,20pt" a ="100pt,20pt" e impostarla su 2 punti e sul rosso specificando **strokecolor**="red" **strokeweight**="2pt", come illustrato nella rappresentazione VML seguente:

![line1.gif (88 byte)](images/line1.gif)


```HTML
<v:line from="20pt,20pt" to="100pt,20pt" '
strokecolor="red" strokeweight="2pt">
```





È possibile disegnare una linea verticale o diagonale specificando semplicemente valori diversi per gli attributi delle proprietà **from** e **to,** come illustrato nella rappresentazione VML seguente:

![line2.gif (86 byte)](images/line2.gif)


```HTML
<v:line from="20pt,20pt" to="20pt,100pt"
strokecolor="red" strokeweight="2pt">
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858402) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="polyline"></a>Polilinea

È possibile usare `<polyline>` l'elemento per definire le forme create da segmenti di linea connessi. È quindi possibile personalizzare la forma specificando attributi di proprietà diversi.

Ad esempio, per disegnare la forma illustrata nell'immagine seguente, è possibile digitare la rappresentazione VML seguente:

![polyline1.gif (957 byte)](images/polyline1.gif)


```HTML
<v:polyline points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt"
strokecolor="red" strokeweight="2pt"/>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858403) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="curve"></a>curva

È possibile usare `<curve>` l'elemento per disegnare una curva di Bézier cubica. È quindi possibile personalizzare la curva specificando attributi di proprietà diversi.

Ad esempio, per disegnare una curva come illustrato nell'immagine seguente, è possibile digitare la rappresentazione VML seguente:

![curve1.gif (992 byte)](images/curve1.gif)


```HTML
<v:curve style='position:relative'
from="0,0" control1="100pt,100pt" control2="200pt,100pt"
to="300pt,0" strokecolor="red" strokeweight="3pt"/>
```





Per altre informazioni su questo elemento, vedere la [specifica VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858404) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="arc"></a>arco

È possibile usare `<arc>` l'elemento per disegnare un arco definito come segmento di un ovale. L'arco è definito dall'intersezione dell'ovale con i vettori di raggio iniziale e finale specificati dagli angoli. Gli angoli vengono calcolati usando le proprietà di un cerchio (larghezza uguale all'altezza), quindi ridimensionati in modo orizzontale in base alla larghezza e all'altezza desiderate.

Ad esempio, è possibile disegnare un arco che inizia da 0 gradi e termina a 90 gradi specificando **startangle**="0" **endangle**="90", come illustrato nella rappresentazione VML seguente:

![arc1.gif (410 byte)](images/arc1.gif)


```HTML
<v:arc style='width:100pt;height:100pt'
startangle="0" endangle="90"
strokecolor="red" strokeweight="2pt"/>
```





È possibile modificare l'arco specificando valori **startangle** ed **endangle** diversi, come illustrato nella rappresentazione VML seguente:

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





Per altre informazioni su questo elemento, vedere la specifica [VML](https://WWW.w3.org/TR/NOTE-VML#-toc416858407) .

[![torna all'inizio ](images/top.gif) Torna all'inizio](#top)

## <a name="summary"></a>Riepilogo

È possibile usare elementi predefiniti vml, ad esempio , , , , , e per disegnare facilmente grafica in una pagina Web e quindi personalizzare tali elementi grafici modificando semplicemente gli attributi `<oval>` `<line>` delle `<polyline>` `<curve>` `<rect>` `<roundrect>` `<arc>` proprietà.

 

 