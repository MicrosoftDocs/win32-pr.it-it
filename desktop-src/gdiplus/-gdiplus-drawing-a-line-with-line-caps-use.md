---
description: È possibile creare l'inizio o la fine di una riga in una delle diverse forme denominate Caps di riga. Windows GDI+ supporta diversi limiti di riga, ad esempio round, Square, Diamond e Arrowhead.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Disegno di una linea con estremità di riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987674"
---
# <a name="drawing-a-line-with-line-caps"></a>Disegno di una linea con estremità di riga

È possibile creare l'inizio o la fine di una riga in una delle diverse forme denominate Caps di riga. Windows GDI+ supporta diversi limiti di riga, ad esempio round, Square, Diamond e Arrowhead.

È possibile specificare i limiti di riga per l'inizio di una riga (Cap iniziale), la fine di una riga (estremità finale) o i trattini di una linea tratteggiata (limite del trattino).

Nell'esempio seguente viene disegnata una linea con una freccia a un'estremità e un arrotondamento all'altra estremità:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



Nella figura seguente viene illustrata la riga risultante.

![illustrazione che mostra una linea orizzontale con una freccia a sinistra e un cerchio all'estremità destra](images/pens4.png)

**LineCapArrowAnchor** e **LineCapRoundAnchor** sono elementi dell'enumerazione [**estremità**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .

 

 



