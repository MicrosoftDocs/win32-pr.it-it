---
description: Windows GDI+ traccia linee, rettangoli e altre figure in un sistema di coordinate.
ms.assetid: a43bcb27-473b-4ca2-a937-2b54384ab86b
title: Panoramica della grafica vettoriale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33566b5d1d683c87ea1f6858abcc6ae375ce09b71e0ac74711118e92bca656c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695659"
---
# <a name="overview-of-vector-graphics"></a>Panoramica della grafica vettoriale

Windows GDI+ traccia linee, rettangoli e altre figure in un sistema di coordinate. È possibile scegliere tra diversi sistemi di coordinate, ma il sistema di coordinate predefinito ha l'origine nell'angolo superiore sinistro con l'asse x che punta a destra e l'asse y verso il basso. L'unità di misura nel sistema di coordinate predefinito è il pixel.

![illustrazione di un sistema di coordinate con l'asse x che si estende a destra e l'asse y che si estende verso il basso](images/aboutgdip02-art01.png)

Un monitor del computer crea la propria visualizzazione su una matrice rettangolare di punti denominata elementi immagine o pixel. Il numero di pixel visualizzati sullo schermo varia da un monitor a quello successivo e il numero di pixel visualizzati su un singolo monitor può in genere essere configurato in una certa misura dall'utente.

![illustrazione di una griglia rettangolare, con tre celle nella griglia etichettate in base alle relative coordinate](images/aboutgdip02-art02.png)

Quando si usa GDI+ per disegnare una linea, un rettangolo o una curva, si forniscono determinate informazioni chiave sull'elemento da disegnare. Ad esempio, è possibile specificare una linea specificando due punti ed è possibile specificare un rettangolo specificando un punto, un'altezza e una larghezza. GDI+ funziona in combinazione con il software del driver di visualizzazione per determinare quali pixel devono essere attivati per visualizzare la linea, il rettangolo o la curva. La figura seguente mostra i pixel attivati per visualizzare una linea dal punto (4, 2) al punto (12, 8).

![illustrazione che mostra una griglia rettangolare con celle riempite per indicare una linea tra due endpoint](images/aboutgdip02-art03.png)

Nel corso del tempo, alcuni blocchi predefiniti di base si sono rivelati i più utili per la creazione di immagini bidimensionali. Questi blocchi predefiniti, che sono tutti supportati da GDI+, sono disponibili nell'elenco seguente:

-   Linee
-   Rettangoli
-   Ellissi
-   Archi
-   Poligoni
-   Spline di tipo cardinal
-   Spline di Bézier

La classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) in GDI+ fornisce i metodi seguenti per disegnare gli elementi nell'elenco precedente: [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)), [DrawEllipse](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawellipse(inconstpen_inconstrectf_)), [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpointf_inint)), [DrawArc](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawarc(inconstpen_inconstrectf__inreal_inreal)), [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) (per spline cardinali) e [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inconstpoint__inconstpoint__inconstpoint__inconstpoint_)). Ognuno di questi metodi è sottoposto a overload. in altre parole, ogni metodo presenta diverse varianti con elenchi di parametri diversi. Ad esempio, una variante del metodo DrawLine riceve l'indirizzo di un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e quattro numeri interi, mentre un'altra variante del metodo DrawLine riceve l'indirizzo di un oggetto **Pen** e di due riferimenti all'oggetto [**Point.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)

I metodi per disegnare linee, rettangoli e spline di Bézier hanno metodi complementari plurali che disegnano diversi elementi in una singola chiamata: [DrawLines,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawlines(inconstpen_inconstpointf_inint)) [DrawRectangles](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangles(inconstpen_inconstrect_inint))e [DrawBeziers.](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) Inoltre, il [metodo DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpoint_inint)) ha un metodo complementare, [DrawClosedCurve,](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawclosedcurve(inconstpen_inconstpoint_inint))che chiude una curva collegando il punto finale della curva al punto iniziale.

Tutti i metodi di disegno della [**classe Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) funzionano in combinazione con un [**oggetto**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Pen. Pertanto, per disegnare qualsiasi elemento, è necessario creare almeno due oggetti: un **oggetto Graphics** e un **oggetto** Pen. **L'oggetto Pen** archivia gli attributi dell'elemento da disegnare, ad esempio lo spessore e il colore della linea. L'indirizzo **dell'oggetto Pen** viene passato come uno degli argomenti al metodo di disegno. Ad esempio, una variante del metodo [DrawRectangle](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawrectangle(inconstpen_inint_inint_inint_inint)) riceve l'indirizzo di un oggetto **Pen** e quattro numeri interi, come illustrato nel codice seguente, che disegna un rettangolo con una larghezza di 100, un'altezza di 50 e un angolo superiore sinistro di (20, 10).


```
myGraphics.DrawRectangle(&myPen, 20, 10, 100, 50);
```



 

 



