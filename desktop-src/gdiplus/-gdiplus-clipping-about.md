---
description: Il ritaglio comporta la limitazione del disegno a una determinata area. Nella figura seguente viene illustrata la stringa &\# 0034; Hello&\# 0034; ritagliato in un'area a forma di cuore.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Ritaglio (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 156ae2209a3b7135cde2804103531eaf7b519d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049867"
---
# <a name="clipping-gdi"></a>Ritaglio (GDI+)

Il ritaglio comporta la limitazione del disegno a una determinata area. La figura seguente mostra la stringa "Hello" ritagliata in un'area a forma di cuore.

![illustrazione che mostra parti della stringa "Hello" all'interno di un cuore rosso](images/aboutgdip02-art30.png)

Le aree possono essere costruite da percorsi e i percorsi possono contenere le strutture delle stringhe, quindi è possibile usare il testo delineato per il ritaglio. Nella figura seguente viene illustrato un set di ellissi concentrici ritagliati all'interno di una stringa di testo.

![illustrazione che mostra la stringa "Hello" compilata da un modello di cerchi concentrici](images/aboutgdip02-art31.png)

Per disegnare con il ritaglio, creare un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , chiamare il relativo metodo [seclip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) e quindi chiamare i metodi di disegno dello stesso oggetto **Graphics** . Nell'esempio seguente viene disegnata una riga che viene ritagliata in un'area rettangolare.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



Nell'illustrazione seguente viene mostrata l'area rettangolare insieme alla linea ritagliata.

![illustrazione che mostra un rettangolo con una linea diagonale dall'alto verso il basso](images/aboutgdip02-art31a.png)

 

 



