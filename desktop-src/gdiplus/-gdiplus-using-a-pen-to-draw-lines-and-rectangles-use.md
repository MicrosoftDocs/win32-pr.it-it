---
description: Per creare linee e rettangoli, sono necessari un oggetto Graphics e un oggetto Pen. L'oggetto Graphics fornisce il metodo DrawLine e l'oggetto Pen archivia le funzionalità della riga, ad esempio il colore e la larghezza.
ms.assetid: f2e4144f-f2f1-49db-bfdf-ffce3023b4cb
title: Uso di una penna per disegnare linee e rettangoli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b335caf7e2ecbad6bc49965ff757809c3b1179c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967196"
---
# <a name="using-a-pen-to-draw-lines-and-rectangles"></a>Uso di una penna per disegnare linee e rettangoli

Per creare linee e rettangoli, sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) . L'oggetto **Graphics** fornisce il metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** archivia le funzionalità della riga, ad esempio il colore e la larghezza.

Nell'esempio seguente viene disegnata una riga da (20, 10) a (300, 100). Si supponga che **Graphics** sia un oggetto [**grafico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) esistente.


```
Pen pen(Color(255, 0, 0, 0));
graphics.DrawLine(&pen, 20, 10, 300, 100);
```



La prima istruzione di codice usa il costruttore della classe [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) per creare una penna nera. L'unico argomento passato al costruttore **Pen** è un oggetto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . I valori utilizzati per costruire l'oggetto **colore** , (255, 0, 0, 0), corrispondono ai componenti alfa, rosso, verde e blu del colore. Questi valori definiscono una penna nera opaca.

Nell'esempio seguente viene disegnato un rettangolo con l'angolo superiore sinistro in corrispondenza di (10, 10). Il rettangolo ha una larghezza di 100 e un'altezza di 50. Il secondo argomento passato al costruttore [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) indica che la lunghezza della penna è 5 pixel.


```
Pen blackPen(Color(255, 0, 0, 0), 5);
stat = graphics.DrawRectangle(&blackPen, 10, 10, 100, 50);
```



Quando il rettangolo viene disegnato, la penna viene centrata sul limite del rettangolo. Poiché la larghezza della penna è 5, i lati del rettangolo vengono disegnati a 5 pixel di larghezza, in modo che 1 pixel venga disegnato sul limite, 2 pixel siano disegnati all'interno e 2 pixel vengono disegnati all'esterno. Per altri dettagli sull'allineamento della penna, vedere [impostazione della larghezza e dell'allineamento della penna](-gdiplus-setting-pen-width-and-alignment-use.md).

Nella figura seguente viene illustrato il rettangolo risultante. Le linee tratteggiate indicano dove sarebbe stato disegnato il rettangolo se la lunghezza della penna era un pixel. La visualizzazione ingrandita dell'angolo superiore sinistro del rettangolo indica che le linee nere spesse sono centrate su tali linee tratteggiate.

![illustrazione di un rettangolo disegnato con una linea nera spessa che racchiude una linea sottile, grigia tratteggiata](images/pens1.png)

 

 



