---
description: 'A B&\# 233; Zier spline è una curva specificata da quattro punti: due punti finali (P1 e P2) e due punti di controllo (C1 e C2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Spline Bezier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd725e64f9ba0035849d2d1d6fbc03d5efa0b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131386"
---
# <a name="bezier-splines"></a>Spline Bezier

Una spline di Bézier è una curva specificata da quattro punti: due punti finali (P1 e P2) e due punti di controllo (C1 e C2). La curva inizia a P1 e termina in corrispondenza di P2. La curva non passa attraverso i punti di controllo, ma i punti di controllo fungono da magneti, spostando la curva in determinate direzioni e influenzando il modo in cui la curva curva. La figura seguente mostra una curva di Bézier insieme ai relativi endpoint e punti di controllo.

![illustrazione che mostra una spline di Bezier con due punti finali e due punti di controllo](images/aboutgdip02-art11a.png)

Si noti che la curva inizia da P1 e viene spostata verso il punto di controllo C1. La linea tangente alla curva in P1 è la linea disegnata da P1 a C1. Si noti inoltre che la linea tangente nell'endpoint P2 è la linea disegnata da C2 a P2.

Per creare una spline di Bézier, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L'oggetto **Graphics** fornisce il metodo [DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi della curva, ad esempio la lunghezza della linea e il colore. L'indirizzo dell'oggetto **Pen** viene passato come uno degli argomenti al metodo DrawBezier. Gli argomenti rimanenti passati al metodo DrawBezier sono gli endpoint e i punti di controllo. Nell'esempio seguente viene disegnata una spline Bézier con punto iniziale (0,0), punti di controllo (40, 20) e (80, 150) e punto finale (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



Nella figura seguente vengono illustrati la curva, i punti di controllo e due linee tangente.

![illustrazione che mostra una spline di Bezier con due punti finali, due punti di controllo e due linee tangente](images/aboutgdip02-art12.png)

Le spline di Bézier sono state originariamente sviluppate da Pierre Bézier per la progettazione nel settore automobilistico. Hanno dimostrato di essere molto utile in molti tipi di progettazione assistita da computer e vengono usati anche per definire le strutture dei tipi di carattere. Le spline di Bézier possono produrre un'ampia gamma di forme, alcune delle quali sono illustrate nella figura seguente.

![illustrazione che mostra tre spline di Bezier](images/aboutgdip02-art13.png)

 

 



