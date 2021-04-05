---
title: Uso del flag di MCI_NOTIFY
description: Uso del flag di notifica di MCI \_
ms.assetid: 1d1803c8-f315-463e-ae0d-a258aa3af3c9
keywords:
- Flag di MCI_NOTIFY
- Comando MCI_PLAY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472613d2e6efcd6b30c88ed64dfa7875b4742527
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855686"
---
# <a name="using-the-mci_notify-flag"></a><span data-ttu-id="5249b-105">Uso del flag di notifica di MCI \_</span><span class="sxs-lookup"><span data-stu-id="5249b-105">Using the MCI\_NOTIFY Flag</span></span>

<span data-ttu-id="5249b-106">Nell'esempio seguente viene illustrato come \_ usare il flag di notifica MCI con il comando [**MCI \_ Play**](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="5249b-106">The following example shows how the MCI\_NOTIFY flag is used with the [**MCI\_PLAY**](mci-play.md) command.</span></span> <span data-ttu-id="5249b-107">L'handle alla routine della finestra che elaborerà il messaggio [**mm \_ MCINOTIFY**](mm-mcinotify.md) viene specificato in *HWND*.</span><span class="sxs-lookup"><span data-stu-id="5249b-107">The handle to the window procedure that will process the [**MM\_MCINOTIFY**](mm-mcinotify.md) message is specified in *hwnd*.</span></span>


```C++
MCI_DGV_PLAY_PARMS mciPlay; 
DWORD dwFlags; 
 
mciPlay.dwCallback = MAKELONG(hwnd, 0); 
dwFlags = MCI_NOTIFY; 
 
mciSendCommand(wMCIDeviceID, MCI_PLAY, dwFlags, (DWORD)(LPSTR)&mciPlay); 
```



 

 




