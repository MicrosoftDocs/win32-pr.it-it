---
description: È possibile disegnare l'inizio o la fine di una linea in una delle diverse forme denominate estremità. Windows GDI+ supporta più estremità di linea, ad esempio arrotondato, quadrato, rombo e punta a freccia.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Disegno di una linea con estremità riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e72e4e1c9c36a7233688378852dfda73196cd7e7131cf7def587ad29a70e82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696163"
---
# <a name="drawing-a-line-with-line-caps"></a>Disegno di una linea con estremità riga

È possibile disegnare l'inizio o la fine di una linea in una delle diverse forme denominate estremità. Windows GDI+ supporta più estremità di linea, ad esempio arrotondato, quadrato, rombo e punta a freccia.

È possibile specificare estremità di linea per l'inizio di una linea (estremità iniziale), la fine di una linea (estremità finale) o i trattini di una linea tratteggiata (estremità tratteggiata).

Nell'esempio seguente viene disegnata una linea con una freccia a un'estremità e un estremità rotonda all'altra estremità:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



La figura seguente mostra la riga risultante.

![illustrazione che mostra una linea orizzontale con una freccia all'estremità sinistra e un cerchio all'estremità destra](images/pens4.png)

**LineCapArrowAnchor** e **LineCapRoundAnchor** sono elementi dell'enumerazione [**LineCap.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap)

 

 



