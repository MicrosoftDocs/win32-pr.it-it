---
description: Per disegnare linee e rettangoli, sono necessari un oggetto Graphics e un oggetto Pen. L'oggetto Graphics fornisce il metodo DrawLine e l'oggetto Pen archivia le caratteristiche della linea, ad esempio colore e larghezza.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso di una penna per disegnare linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da700d61a5c8c1ce605678ea09aa540706d569361cebba8f5a93110ccdc304bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884861"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Uso di una penna per disegnare linee e rettangoli

Per disegnare linee e rettangoli, sono necessari un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un [**oggetto**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) Pen. **L'oggetto Graphics** fornisce [il metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia le caratteristiche della linea, ad esempio colore e larghezza.

Nell'esempio seguente viene disegnata una linea da (20, 10) a (300, 100). Si **supponga che la** grafica sia un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



La prima istruzione del codice usa il [**costruttore della classe Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per creare una penna nera. L'unico argomento passato al **costruttore Pen** è un [**oggetto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) I valori usati per costruire l'oggetto **Color** ( 255, 0, 0, 0) corrispondono ai componenti alfa, rosso, verde e blu del colore. Questi valori definiscono una penna nera opaca.

L'esempio seguente disegna un rettangolo con l'angolo superiore sinistro in corrispondenza di (10, 10). La larghezza del rettangolo è 100 e l'altezza è 50. Il secondo argomento passato al costruttore [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica che la larghezza della penna è di 5 pixel.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Quando il rettangolo viene disegnato, la penna viene centrata sul limite del rettangolo. Poiché la larghezza della penna è 5, i lati del rettangolo vengono disegnati con una larghezza di 5 pixel, in modo che 1 pixel sia disegnato sul limite stesso, 2 pixel all'interno e 2 pixel all'esterno. Per altri dettagli sull'allineamento della penna, vedere [Impostazione della larghezza e dell'allineamento della penna.](-gdiplus-setting-pen-width-and-alignment-use.md)

La figura seguente mostra il rettangolo risultante. Le linee tratteggiate indicano dove sarebbe stato disegnato il rettangolo se la larghezza della penna fosse stata di un pixel. La visualizzazione ingrandita dell'angolo superiore sinistro del rettangolo indica che le linee nere spesso sono centrate su tali linee tratteggiate.

![illustrazione di un rettangolo disegnato con una linea nera spesso che circonda una linea sottile, grigia e tratteggiata](images/pens1.png)

 

 



