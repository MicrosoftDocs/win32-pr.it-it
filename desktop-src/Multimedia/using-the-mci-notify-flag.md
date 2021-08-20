---
title: Uso del flag MCI_NOTIFY
description: Uso del flag NOTIFY MCI \_
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- MCI_NOTIFY flag
- MCI_PLAY comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b0e7269ee7d80dd47372d9210fbdbc1332b3a88a96e2a17d6719c9945ab30aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136139"
---
# <a name="using-the-mci_notify-flag"></a>Uso del flag NOTIFY MCI \_

L'esempio seguente illustra l'uso del flag MCI \_ NOTIFY con il comando [**MCI \_ PLAY.**](mci-play.md) L'handle per la routine della finestra che eelaborare il [**messaggio \_ MM MCINOTIFY**](mm-mcinotify.md) è specificato in *hwnd*.


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




