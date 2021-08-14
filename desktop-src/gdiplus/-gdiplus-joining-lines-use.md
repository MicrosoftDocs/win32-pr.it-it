---
description: Un join di linee è l'area comune formata da due linee le cui estremità si incontrano o si sovrappongono.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unione di linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066975"
---
# <a name="joining-lines"></a>Unione di linee

Un join di linee è l'area comune formata da due linee le cui estremità si incontrano o si sovrappongono. Windows GDI+ offre quattro stili di join di linea: miter, smussato, arrotondato e troncato. Lo stile di join della linea è una proprietà della [**classe**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Pen. Quando si specifica uno stile di join di linea per una penna e quindi si usa tale penna per disegnare un tracciato, lo stile di join specificato viene applicato a tutte le linee connesse nel tracciato.

È possibile specificare lo stile di join della linea usando il [**metodo Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) della [**classe**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Pen. L'esempio seguente illustra un join di linee smussate tra una linea orizzontale e una linea verticale:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



La figura seguente mostra il join di linee smussate risultante.

![illustrazione che mostra due linee che si insedino ad angolo retto, con un join con smussatura](images/pens5.png)

Nell'esempio precedente il valore (**LineJoinBevel**) passato al metodo [**Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) è un elemento dell'enumerazione [**LineJoin.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)

 

 



