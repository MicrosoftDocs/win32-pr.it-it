---
title: Strutture DirectDraw
description: Questa sezione contiene informazioni sulle strutture seguenti usate con DirectDraw
ms.assetid: 36424B41-B179-414A-ACFF-E63DA7B27043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4aba62751b619982628575b380ea75eb57661db8737325fee1fb1b042e856ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504343"
---
# <a name="directdraw-structures"></a>Strutture DirectDraw

Questa sezione contiene informazioni sulle strutture seguenti usate con DirectDraw:

-   [**DDBLTBATCH**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltbatch)
-   [**DDBLTFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddbltfx)
-   [**DDCAPS**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)
-   [**DDCOLORCONTROL**](/windows/win32/api/ddraw/nn-ddraw-idirectdrawcolorcontrol)
-   [**DDCOLORKEY**](/windows/desktop/api/Ddraw/ns-ddraw-ddcolorkey)
-   [**DDDEVICEIDENTIFIER2**](/windows/win32/api/ddraw/ns-ddraw-dddeviceidentifier2)
-   [**DDGAMMARAMP**](/windows/desktop/api/Ddraw/ns-ddraw-ddgammaramp)
-   [**DDOVERLAYFX**](/windows/desktop/api/Ddraw/ns-ddraw-ddoverlayfx)
-   [**DDPIXELFORMAT**](/windows/desktop/api/Ddraw/ns-ddraw-ddpixelformat)
-   [**DDSCAPS**](/previous-versions/ms783271(v=vs.85))
-   [**DDSCAPS2**](/previous-versions/bb943980(v=vs.85))
-   [**DDSURFACEDESC**](/previous-versions/ms783272(v=vs.85))
-   [**DDSURFACEDESC2**](/previous-versions/bb943981(v=vs.85))

> [!Note]  
> È necessario inizializzare la memoria per ogni struttura DirectX su 0 prima di usare la struttura . Inoltre, per tutte le strutture che contengono un membro **dwSize,** è necessario impostare il membro sulla dimensione della struttura, in byte, prima che venga usata la struttura . Nell'esempio seguente vengono eseguite queste attività in una struttura comune, [**DDCAPS:**](/windows/desktop/api/Ddraw/ns-ddraw-ddcaps_dx3)

 


```
DDCAPS ddcaps; // You cannot use this yet.
 
ZeroMemory(&ddcaps, sizeof(DDCAPS));
ddcaps.dwSize = sizeof(DDCAPS);
 
// Now you can use the structure.
.
.
```



 

 




