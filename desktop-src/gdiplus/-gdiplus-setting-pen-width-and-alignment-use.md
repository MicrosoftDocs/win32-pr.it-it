---
description: 'Quando si crea un oggetto Pen, è possibile specificare la larghezza della penna come uno degli argomenti per il costruttore. È anche possibile modificare la larghezza della penna usando il metodo Pen:: sewidth.'
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Impostazione della larghezza e dell'allineamento della penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104559521"
---
# <a name="setting-pen-width-and-alignment"></a>Impostazione della larghezza e dell'allineamento della penna

Quando si crea un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) , è possibile specificare la larghezza della penna come uno degli argomenti per il costruttore. È anche possibile modificare la larghezza della penna usando il metodo [**Pen:: sewidth**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth) .

Una linea teorica ha una larghezza pari a zero. Quando si crea una linea, i pixel vengono centrati sulla linea teorica. Nell'esempio seguente la riga specificata viene disegnata due volte: una volta con una penna nera di larghezza 1 e una volta con una penna verde di larghezza 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



Nella figura seguente viene illustrato l'output del codice precedente. I pixel verdi e i pixel neri sono centrati sulla linea teorica.

![illustrazione che mostra una linea sottile, diagonale, nera circondata da una linea verde ampia ](images/pens1a.png)

Nell'esempio seguente viene disegnato un rettangolo specificato due volte: una volta con una penna nera di larghezza 1 e una volta con una penna verde di larghezza 10. Il codice passa il valore **PenAlignmentCenter** (un elemento dell'enumerazione [**PenAlignment**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) ) al metodo [**Pen:: sealignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) per specificare che i pixel disegnati con la penna verde sono centrati sul limite del rettangolo.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



Nella figura seguente viene illustrato l'output del codice precedente. I pixel verdi sono centrati sul rettangolo teorico, rappresentato dai pixel neri.

![illustrazione che mostra una linea nera sottile nella forma di un rettangolo, circondata da una linea verde più ampia](images/pens2.png)

È possibile modificare l'allineamento della penna verde modificando la terza istruzione nell'esempio precedente come indicato di seguito:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Ora i pixel nella linea verde ampia vengono visualizzati all'interno del rettangolo, come illustrato nella figura seguente.

![illustrazione che mostra una linea nera sottile nella forma di un rectange, che racchiude una linea verde ampia con la stessa forma](images/pens3.png)

 

 



