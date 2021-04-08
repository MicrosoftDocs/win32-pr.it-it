---
title: Apertura della finestra di riproduzione
description: Apertura della finestra di riproduzione
ms.assetid: 180f3fb9-cdcb-49ec-a708-84a597295b2f
keywords:
- Comando MCI_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6ea203c3a5d36ab747632b18b6550a3a0319159
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045325"
---
# <a name="opening-the-playback-window"></a>Apertura della finestra di riproduzione

Nell'esempio seguente viene illustrato come utilizzare il comando [**MCI \_ Open**](mci-open.md) per impostare una finestra padre e creare un elemento figlio di tale finestra.


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



 

 




