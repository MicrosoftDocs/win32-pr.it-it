---
description: Il ritaglio comporta la limitazione del disegno a una determinata area. La figura seguente mostra la stringa &\# 0034; Hello&\# 0034; ritagliato in un'area a forma di memoria.
ms.assetid: 58cc052d-31af-4410-81b9-defbad08a1dc
title: Ritaglio (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a57534c5934270374af356956285ad13838630666795d9f06a2623cbd3b453ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067635"
---
# <a name="clipping-gdi"></a>Ritaglio (GDI+)

Il ritaglio comporta la limitazione del disegno a una determinata area. La figura seguente mostra la stringa "Hello" ritagliata in un'area a forma di cuore.

![illustrazione che mostra parti della stringa "hello" all'interno di un rosso](images/aboutgdip02-art30.png)

Le aree possono essere costruite da tracciati e i tracciati possono contenere i contorni delle stringhe, quindi è possibile usare il testo con contorni per il ritaglio. La figura seguente mostra un set di puntini di sospensione concentrici ritagliati all'interno di una stringa di testo.

![illustrazione che mostra la stringa "hello" riempita da un modello di cerchi concentrici](images/aboutgdip02-art31.png)

Per disegnare con il ritaglio, crea un [**oggetto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) chiama il relativo [metodo SetClip](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-setclip(inconstregion_incombinemode)) e quindi chiama i metodi di disegno dello stesso **oggetto Graphics.** Nell'esempio seguente viene disegnata una linea ritagliata in un'area rettangolare.


```
Region myRegion(Rect(20, 30, 100, 50));
myGraphics.DrawRectangle(&myPen, 20, 30, 100, 50);  
myGraphics.SetClip(&myRegion, CombineModeReplace);
myGraphics.DrawLine(&myPen, 0, 0, 200, 200);
```



La figura seguente mostra l'area rettangolare insieme alla linea ritagliata.

![figura che mostra un rettangolo con una linea diagonale dall'alto verso il basso](images/aboutgdip02-art31a.png)

 

 



