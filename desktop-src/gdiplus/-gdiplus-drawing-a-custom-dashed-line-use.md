---
description: Windows GDI+ fornisce diversi stili di trattino elencati nell'enumerazione DashStyle. Se questi stili di tratteggio standard non soddisfano le proprie esigenze, è possibile creare un motivo a trattini personalizzato.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Disegno di una linea tratteggiata personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad7bb415ff4f7b1cbde4637ab184c9ab05e4a707e0bce8328500d39ee2b840d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115081"
---
# <a name="drawing-a-custom-dashed-line"></a>Disegno di una linea tratteggiata personalizzata

Windows GDI+ fornisce diversi stili di trattino elencati [**nell'enumerazione DashStyle.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) Se questi stili di tratteggio standard non soddisfano le proprie esigenze, è possibile creare un motivo a trattini personalizzato.

Per disegnare una linea tratteggiata personalizzata, inserisci le lunghezze dei trattini e degli spazi in una matrice e passa l'indirizzo della matrice come argomento al metodo [**Pen::SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) di un oggetto [**Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) L'esempio seguente disegna una linea tratteggiata personalizzata basata sulla matrice {5, 2, 15, 4}. Se si moltiplicano gli elementi della matrice per la larghezza della penna di 5, si ottiene {25, 10, 75, 20}. I trattini visualizzati hanno una lunghezza alternativa compresa tra 25 e 75 e gli spazi hanno una lunghezza alternativa compresa tra 10 e 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



La figura seguente mostra la linea tratteggiata risultante. Si noti che il trattino finale deve essere più breve di 25 unità in modo che la linea possa terminare con (405, 5).

![illustrazione che mostra una linea tratteggiata; ogni segmento è una linea breve seguita da una lunga](images/pens6.png)

 

 



