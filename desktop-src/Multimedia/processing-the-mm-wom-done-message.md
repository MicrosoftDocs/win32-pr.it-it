---
title: Elaborazione del messaggio di MM_WOM_DONE
description: Elaborazione del \_ messaggio mm WOM \_ done
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- audio Waveform, messaggi
- audio ausiliario, messaggi
- audio Waveform, messaggio MM_WOM_DONE
- audio ausiliario, messaggio MM_WOM_DONE
- Messaggio MM_WOM_DONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e909777c115b6b10500e081a08bde6cfe24b00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471251"
---
# <a name="processing-the-mm_wom_done-message"></a><span data-ttu-id="63ee9-108">Elaborazione del \_ messaggio mm WOM \_ done</span><span class="sxs-lookup"><span data-stu-id="63ee9-108">Processing the MM\_WOM\_DONE Message</span></span>

<span data-ttu-id="63ee9-109">Nell'esempio seguente viene illustrato come elaborare il messaggio [**mm \_ WOM \_ done**](mm-wom-done.md) .</span><span class="sxs-lookup"><span data-stu-id="63ee9-109">The following example shows how to process the [**MM\_WOM\_DONE**](mm-wom-done.md) message.</span></span> <span data-ttu-id="63ee9-110">In questo esempio si presuppone che l'applicazione non riproduca più blocchi di dati, quindi può chiudere il dispositivo di output dopo la riproduzione di un singolo blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="63ee9-110">This example assumes the application does not play multiple data blocks, so it can close the output device after playing a single data block.</span></span>


```C++
// WndProc--Main window procedure. 
LRESULT FAR PASCAL WndProc(HWND hWnd, UINT msg, WPARAM wParam, 
    LPARAM lParam) 
{ 
switch (msg) 
{ 
    case MM_WOM_DONE: 
 
    // A waveform-audio data block has been played and 
    // can now be freed. 
    waveOutUnprepareHeader((HWAVEOUT) wParam, 
        (LPWAVEHDR) lParam, sizeof(WAVEHDR) ); 
    
    // Free hData memory. 
    
    waveOutClose((HWAVEOUT) wParam); 
    break; 
    } 
    return DefWindowProc(hWnd, msg, wParam, lParam); 
} 
```



 

 




