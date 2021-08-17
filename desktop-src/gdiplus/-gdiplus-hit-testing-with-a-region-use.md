---
description: Lo scopo dell'hit testing è determinare se il cursore si trova su un determinato oggetto, ad esempio un'icona o un pulsante.
ms.assetid: 9776b73e-191e-4a8e-9abe-e485ffed954c
title: Hit testing con un'area
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0673466bc368c9288765b1c7e6f460716d8d40674802a0977690a7ef79b58b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117885399"
---
# <a name="hit-testing-with-a-region"></a>Hit testing con un'area

Lo scopo dell'hit testing è determinare se il cursore si trova su un determinato oggetto, ad esempio un'icona o un pulsante. Nell'esempio seguente viene creata un'area a forma di segno più formando l'unione di due aree rettangolari. Si supponga che il punto **variabile** contiene la posizione del clic più recente. Il codice verifica se point **si** trova nell'area a forma di segno più. Se **il punto** si trova nell'area (un hit), l'area viene riempita con un pennello rosso opaco. In caso contrario, l'area viene riempita con un pennello rosso semitrasparente.


```
Point point(60, 10);
// Assume that the variable "point" contains the location
// of the most recent click.
// To simulate a hit, assign (60, 10) to point.
// To simulate a miss, assign (0, 0) to point.
SolidBrush solidBrush(Color());
Region region1(Rect(50, 0, 50, 150));
Region region2(Rect(0, 50, 150, 50));
// Create a plus-shaped region by forming the union of region1 and region2.
// The union replaces region1.
region1.Union(&region2);
if(region1.IsVisible(point, &graphics))
{
   // The point is in the region. Use an opaque brush.
   solidBrush.SetColor(Color(255, 255, 0, 0));
}
else
{
   // The point is not in the region. Use a semitransparent brush.
   solidBrush.SetColor(Color(64, 255, 0, 0));
}
graphics.FillRegion(&solidBrush, &region1);
```



 

 



