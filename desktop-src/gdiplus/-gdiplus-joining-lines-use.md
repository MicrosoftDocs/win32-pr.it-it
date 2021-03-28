---
description: Un join a linee è l'area comune costituita da due righe le cui estremità soddisfano o si sovrappongono.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unione di linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567012"
---
# <a name="joining-lines"></a>Unione di linee

Un join a linee è l'area comune costituita da due righe le cui estremità soddisfano o si sovrappongono. In Windows GDI+ sono disponibili quattro stili di join a linee: Miter, smussato, arrotondato e Miter troncato. Lo stile di join a linee è una proprietà della classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Quando si specifica uno stile di join di riga per una penna e quindi si utilizza tale penna per tracciare un tracciato, lo stile di join specificato viene applicato a tutte le linee connesse del percorso.

È possibile specificare lo stile di join a linee usando il metodo [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) della classe [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Nell'esempio seguente viene illustrato un join a linee smussate tra una linea orizzontale e una linea verticale:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



Nell'illustrazione seguente viene mostrato il join di linea smussato risultante.

![illustrazione che mostra due linee che si riuniscono a un angolo retto, con un join smussato](images/pens5.png)

Nell'esempio precedente, il valore (**LineJoinBevel**) passato al metodo [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) è un elemento dell'enumerazione [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .

 

 



