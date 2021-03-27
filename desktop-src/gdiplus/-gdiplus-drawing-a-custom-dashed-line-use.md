---
description: In Windows GDI+ sono disponibili diversi stili di trattini elencati nell'enumerazione DashStyle. Se gli stili Dash standard non soddisfano le proprie esigenze, è possibile creare un modello Dash personalizzato.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Disegno di una linea tratteggiata personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988087"
---
# <a name="drawing-a-custom-dashed-line"></a>Disegno di una linea tratteggiata personalizzata

In Windows GDI+ sono disponibili diversi stili di trattini elencati nell'enumerazione [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) . Se gli stili Dash standard non soddisfano le proprie esigenze, è possibile creare un modello Dash personalizzato.

Per creare una linea tratteggiata personalizzata, inserire le lunghezze dei trattini e degli spazi in una matrice e passare l'indirizzo della matrice come argomento al metodo [**Pen:: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) di un oggetto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Nell'esempio seguente viene disegnata una linea tratteggiata personalizzata in base alla matrice {5, 2, 15, 4}. Se si moltiplicano gli elementi della matrice in base alla larghezza della penna di 5, si ottengono {25, 10, 75, 20}. I trattini visualizzati si alternano con una lunghezza compresa tra 25 e 75 e gli spazi si alternano con una lunghezza compresa tra 10 e 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



Nella figura seguente viene illustrata la linea tratteggiata risultante. Si noti che il trattino finale deve essere più breve di 25 unità in modo che la riga possa terminare in corrispondenza di (405, 5).

![illustrazione che mostra una linea tratteggiata; ogni segmento è una linea breve seguita da un lungo](images/pens6.png)

 

 



