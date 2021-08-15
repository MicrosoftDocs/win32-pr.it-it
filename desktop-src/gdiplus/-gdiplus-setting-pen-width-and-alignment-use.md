---
description: Quando crei un oggetto Pen, puoi fornire la larghezza della penna come uno degli argomenti al costruttore. Puoi anche modificare la larghezza della penna usando il metodo Pen::SetWidth.
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Impostazione della larghezza e dell'allineamento della penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2a6bd5be00fde0f27657cef558365d857775a5b55f9f108074884906916b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885015"
---
# <a name="setting-pen-width-and-alignment"></a>Impostazione della larghezza e dell'allineamento della penna

Quando crei un [**oggetto Pen,**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) puoi fornire la larghezza della penna come uno degli argomenti al costruttore. Puoi anche modificare la larghezza della penna usando il [**metodo Pen::SetWidth.**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth)

Una linea teorica ha uno spessore pari a zero. Quando si disegna una linea, i pixel vengono centrati sulla linea teorica. L'esempio seguente disegna una linea specificata due volte: una con una penna nera di larghezza 1 e una con una penna verde di larghezza 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



La figura seguente mostra l'output del codice precedente. I pixel verdi e i pixel neri sono centrati sulla linea teorica.

![illustrazione che mostra una linea sottile, diagonale e nera racchiusa da una linea larga e verde ](images/pens1a.png)

L'esempio seguente disegna due volte un rettangolo specificato: una con una penna nera di larghezza 1 e una con una penna verde di larghezza 10. Il codice passa il valore **PenAlignmentCenter** (un elemento dell'enumerazione [**PenAlignment)**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) al metodo [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) per specificare che i pixel disegnati con la penna verde sono centrati sul limite del rettangolo.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



La figura seguente mostra l'output del codice precedente. I pixel verdi sono centrati sul rettangolo teorico, rappresentato dai pixel neri.

![illustrazione che mostra una linea nera sottile a forma di rettangolo, racchiusa da una linea verde più ampia](images/pens2.png)

È possibile modificare l'allineamento della penna verde modificando la terza istruzione nell'esempio precedente come indicato di seguito:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Ora i pixel nella linea verde ampia vengono visualizzati all'interno del rettangolo, come illustrato nella figura seguente.

![illustrazione che mostra una linea nera sottile a forma di rectange, che racchiude una linea verde ampia della stessa forma](images/pens3.png)

 

 



