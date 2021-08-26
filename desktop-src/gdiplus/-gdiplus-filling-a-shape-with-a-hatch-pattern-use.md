---
description: 'Un motivo a tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il motivo sullo sfondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Riempimento di una forma con un modello di tratteggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b571ab09dc91c037e0cc89a2b107c2f8d253b832b593bb32a169bc970295d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015101"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Riempimento di una forma con un modello di tratteggio

Un motivo a tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il motivo sullo sfondo. Per riempire una forma chiusa con un motivo tratteggiato, usa un [**oggetto HatchBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) L'esempio seguente illustra come riempire un'ellisse con un motivo a tratteggio:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



La figura seguente mostra l'ellisse piena.

![illustrazione di un'ellisse riempita con motivo tratteggiato di linee orizzontali su uno sfondo a tinta unita](images/hatch1.png)

Il [**costruttore HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) accetta tre argomenti: lo stile del tratteggio, il colore della linea tratteggiata e il colore dello sfondo. L'argomento dello stile del tratteggio può essere qualsiasi elemento [**dell'enumerazione HatchStyle.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) Nell'enumerazione HatchStyle sono presenti più di **10 elementi;** Alcuni di questi elementi sono visualizzati nell'elenco seguente:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



