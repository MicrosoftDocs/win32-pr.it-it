---
description: Windows GDI+ disegna linee, rettangoli e altre figure in un sistema di coordinate.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Panoramica della grafica vettoriale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e9bfe98585ef8e073cf1c563c237436b7c982bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558130"
---
# <a name="overview-of-vector-graphics"></a>Panoramica della grafica vettoriale

Windows GDI+ disegna linee, rettangoli e altre figure in un sistema di coordinate. È possibile scegliere da un'ampia gamma di sistemi di coordinate, ma il sistema di coordinate predefinito ha l'origine nell'angolo superiore sinistro con l'asse x che punta verso destra e l'asse y che punta verso il basso. L'unità di misura del sistema di coordinate predefinito è il pixel.

![illustrazione di un sistema di coordinate con l'asse x che si estende a destra e l'asse y che si estende verso il basso](images/aboutgdip02-art01.png)

Un monitor del computer crea la propria visualizzazione su una matrice rettangolare di punti detti elementi immagine o pixel. Il numero di pixel visualizzati sullo schermo varia da un monitoraggio a quello successivo e il numero di pixel visualizzati in un singolo monitoraggio può in genere essere configurato in un certo modo dall'utente.

![illustrazione di una griglia rettangolare con tre celle nella griglia contrassegnate con le relative coordinate](images/aboutgdip02-art02.png)

Quando si utilizza GDI+ per disegnare una linea, un rettangolo o una curva, si forniscono determinate informazioni chiave sull'elemento da disegnare. È ad esempio possibile specificare una riga fornendo due punti ed è possibile specificare un rettangolo fornendo un punto, un'altezza e una larghezza. GDI+ funziona in combinazione con il software del driver di visualizzazione per determinare quali pixel devono essere attivati per mostrare la linea, il rettangolo o la curva. Nella figura seguente vengono mostrati i pixel accesi per visualizzare una riga dal punto (4, 2) al punto (12, 8).

![illustrazione che mostra una griglia rettangolare con celle riempite per indicare una linea tra due endpoint](images/aboutgdip02-art03.png)

Nel tempo, alcuni blocchi predefiniti di base si sono dimostrati più utili per la creazione di immagini bidimensionali. Questi blocchi predefiniti, tutti supportati da GDI+, sono indicati nell'elenco seguente:

-   Linee
-   Rettangoli
-   Ellissi
-   Archi
-   Poligoni
-   Spline cardinali
-   Spline di Bézier

La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in GDI+ fornisce i metodi seguenti per disegnare gli elementi nell'elenco precedente: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (per le spline cardinalhe) e [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Ognuno di questi metodi è sovraccarico; in altre termini, ogni metodo è presente in diverse varianti con elenchi di parametri diversi. Una variante del metodo DrawLine, ad esempio, riceve l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e quattro Integer, mentre un'altra variante del metodo DrawLine riceve l'indirizzo di un oggetto **Pen** e di due riferimenti a oggetti [**punto**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .

I metodi per disegnare linee, rettangoli e spline di Bézier hanno metodi complementari plurali che disegnano più elementi in una singola chiamata: [DrawLines](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)), [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))e [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)). Inoltre, il metodo [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) dispone di un metodo complementare, [DrawClosedCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint)), che chiude una curva connettendo il punto finale della curva al punto iniziale.

Tutti i metodi di disegno della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) funzionano insieme a un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . Pertanto, per creare qualsiasi elemento, è necessario creare almeno due oggetti: un oggetto **Graphics** e un oggetto **Pen** . L'oggetto **Pen** archivia gli attributi dell'elemento da disegnare, ad esempio la lunghezza della linea e il colore. L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al Metodo Drawing. Ad esempio, una variante del metodo [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) riceve l'indirizzo di un oggetto **Pen** e quattro Integer, come illustrato nel codice seguente, che disegna un rettangolo con una larghezza di 100, un'altezza di 50 e un angolo superiore sinistro di (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



