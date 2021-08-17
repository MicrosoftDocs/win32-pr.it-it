---
description: 'Una spline B&233;zier è una curva specificata da quattro punti: due punti finali (p1 e p2) e due punti di \# controllo (c1 e c2).'
ms.assetid: 3ee279ea-20cc-4089-b1a5-13bf1c7c4942
title: Spline Bezier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bcc9c56baa9cd1b3e93187ef00f9d6a2c8c1d218262c946028ed70429de18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399571"
---
# <a name="bezier-splines"></a>Spline Bezier

Una spline di Bézier è una curva specificata da quattro punti: due punti finali (p1 e p2) e due punti di controllo (c1 e c2). La curva inizia da p1 e termina in corrispondenza di p2. La curva non passa attraverso i punti di controllo, ma i punti di controllo fungono da calamite, estraendo la curva in determinate direzioni e influenzando il modo in cui la curva si curva. La figura seguente mostra una curva di Bézier insieme ai relativi endpoint e punti di controllo.

![Figura che mostra una spline di Bézier con due punti finali e due punti di controllo](images/aboutgdip02-art11a.png)

Si noti che la curva inizia da p1 e si sposta verso il punto di controllo c1. La linea tangente alla curva in corrispondenza di p1 è la linea disegnata da p1 a c1. Si noti anche che la linea tangente all'endpoint p2 è la linea disegnata da c2 a p2.

Per disegnare una spline di Bézier, sono necessari un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un [**oggetto Pen.**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) **L'oggetto Graphics** fornisce il [metodo DrawBezier](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbezier(inconstpen_inint_inint_inint_inint_inint_inint_inint_inint)) e l'oggetto **Pen** archivia gli attributi della curva, ad esempio lo spessore e il colore della linea. L'indirizzo **dell'oggetto Pen** viene passato come uno degli argomenti al metodo DrawBezier. Gli argomenti rimanenti passati al metodo DrawBezier sono gli endpoint e i punti di controllo. Nell'esempio seguente viene disegnata una spline di Bézier con punto iniziale (0, 0), punti di controllo (40, 20) e (80, 150) e punto finale (100, 10).


```
myGraphics.DrawBezier(&myPen, 0, 0, 40, 20, 80, 150, 100, 10);
```



La figura seguente mostra la curva, i punti di controllo e due linee tangenti.

![Figura che mostra una spline di Bézier con due punti finali, due punti di controllo e due linee tangenti](images/aboutgdip02-art12.png)

Le spline di Bézier sono state originariamente sviluppate da Pierre Bézier per la progettazione nel settore automobilistico. Da allora si sono dimostrati molto utili in molti tipi di progettazione con supporto informatico e vengono usati anche per definire i contorni dei tipi di carattere. Le spline di Bézier possono produrre un'ampia gamma di forme, alcune delle quali sono illustrate nella figura seguente.

![Illustrazione che mostra tre spline di Bézier](images/aboutgdip02-art13.png)

 

 



