---
description: 'Un modello di tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il modello sullo sfondo.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Riempimento di una forma con un motivo di tratteggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987769"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Riempimento di una forma con un motivo di tratteggio

Un modello di tratteggio è costituito da due colori: uno per lo sfondo e uno per le linee che formano il modello sullo sfondo. Per riempire una forma chiusa con un motivo di tratteggio, usare un oggetto [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) . Nell'esempio seguente viene illustrato come riempire un'ellisse con un motivo di tratteggio:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



Nell'illustrazione seguente viene mostrata l'ellisse piena.

![illustrazione di un'ellisse riempita con lo schema tratteggiato delle linee orizzontali su uno sfondo a tinta unita](images/hatch1.png)

Il costruttore [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) accetta tre argomenti: lo stile di tratteggio, il colore della linea di tratteggio e il colore dello sfondo. L'argomento dello stile di tratteggio può essere qualsiasi elemento dell'enumerazione [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) . Sono presenti più di 50 elementi nell'enumerazione **HatchStyle** . alcuni di questi elementi sono illustrati nell'elenco seguente:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



