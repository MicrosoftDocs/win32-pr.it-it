---
description: Una spline di tipo Cardinal è una sequenza di curve singole Unite per formare una curva più grande.
ms.assetid: 4fc62f00-7006-4ade-bfcc-091a3a97d889
title: Spline di tipo Cardinal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d85c0163e405a6f9346f521b4057eb936108cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227103"
---
# <a name="cardinal-splines"></a>Spline di tipo Cardinal

Una spline di tipo Cardinal è una sequenza di curve singole Unite per formare una curva più grande. La spline viene specificata da una matrice di punti e da un parametro di tensione. Una spline Cardinal passa senza problemi a ogni punto della matrice; non ci sono angoli acuti e nessuna modifica brusca della curva. Nella figura seguente viene illustrato un set di punti e una spline di un cardinale che passa attraverso ogni punto del set.

![illustrazione che mostra una spline di Cardinal che passa da sei punti definiti](images/aboutgdip02-art09.gif)

Una spline fisica è un sottile pezzo di legno o altro materiale flessibile. Prima dell'avvento delle spline matematiche, le finestre di progettazione usavano le spline fisiche per creare curve. In una finestra di progettazione la spline viene posizionata su una porzione di carta e ancorata a un set di punti specificato. La finestra di progettazione potrebbe quindi creare una curva disegnando lungo la spline con una matita. Un determinato set di punti può produrre una serie di curve, a seconda delle proprietà della spline fisica. Una spline con una resistenza elevata al piegamento, ad esempio, produrrebbe una curva diversa rispetto a una spline estremamente flessibile.

Le formule per le spline matematiche si basano sulle proprietà delle barre flessibili, quindi le curve prodotte dalle spline matematiche sono simili alle curve che sono state generate da spline fisiche. Così come le spline fisiche con tensioni diverse produrranno curve diverse tramite un determinato set di punti, le spline matematiche con valori diversi per il parametro di tensionamento produrranno curve diverse tramite un determinato set di punti. Nella figura seguente sono illustrate quattro spline cardinali che passano attraverso lo stesso set di punti. La tensione viene visualizzata per ogni spline. Si noti che una tensione pari a 0 corrisponde alla tensione fisica infinita, forzando la curva ad assumere il modo più breve (linee rette) tra i punti. Una tensione di 1 corrisponde a nessuna tensione fisica, consentendo alla spline di prendere il percorso della curva meno totale. Con i valori di tensionamento maggiori di 1, la curva si comporta come una molla compressa, per cui viene eseguito il push per ottenere un percorso più lungo.

![illustrazione che mostra quattro spline cardinali attraverso gli stessi tre punti](images/aboutgdip02-art10.gif)

Si noti che le quattro spline nella figura precedente condividono la stessa linea tangente al punto iniziale. La tangente è la linea disegnata dal punto iniziale al punto successivo lungo la curva. Analogamente, la tangente condivisa al punto finale è la linea disegnata dal punto finale al punto precedente della curva.

Per creare una spline di cardinalità, è necessario un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e una matrice di oggetti [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) . L'oggetto **Graphics** fornisce il metodo [DrawCurve](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawcurve(inconstpen_inconstpointf_inint_inreal)) , che disegna la spline e l'oggetto **Pen** archivia gli attributi della spline, ad esempio la lunghezza della linea e il colore. La matrice di oggetti **punto** archivia i punti che la curva passerà. Nell'esempio seguente viene disegnata una spline di Cardinal che passa attraverso i punti di *myPointArray*. Il terzo parametro è la tensione.


```
myGraphics.DrawCurve(&myPen, myPointArray, 3, 1.5f);
```



 

 



