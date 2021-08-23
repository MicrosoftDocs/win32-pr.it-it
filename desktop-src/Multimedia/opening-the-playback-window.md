---
title: Apertura della finestra di riproduzione
description: Apertura della finestra di riproduzione
ms.assetid: 180f3fb9-cdcb-49ec-a708-84a597295b2f
keywords:
- MCI_OPEN comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11aed7802a3536beb069c1fd7048b66be217d21f0dd3e47fa21caaad80d854e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806171"
---
# <a name="opening-the-playback-window"></a>Apertura della finestra di riproduzione

L'esempio seguente illustra come usare il [**comando MCI \_ OPEN**](mci-open.md) per impostare una finestra padre e creare un elemento figlio di tale finestra.


```C++
MCI_DGV_OPEN_PARMS    mciOpen; 
 
mciOpen.lpstrElementName = lpstrFile;  // Set the filename.
mciOpen.dwStyle = WS_CHILD;            // Set the style. 
mciOpen.hWndParent = hWnd;             // Give a window handle. 
 
if (mciSendCommand(0, MCI_OPEN, 
   (DWORD)(MCI_OPEN_ELEMENT|MCI_DGV_OPEN_PARENT|MCI_DGV_OPEN), 
   (DWORD)(LPSTR)&mciOpen) == 0)
{ 
    // Open operation is successful. Continue. 
} 
```



 

 




