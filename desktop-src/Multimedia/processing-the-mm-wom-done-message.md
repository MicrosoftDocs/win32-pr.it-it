---
title: Elaborazione del MM_WOM_DONE messaggio
description: Elaborazione del messaggio \_ MM WOM \_ DONE
ms.assetid: 215167d0-3020-453d-b6b3-cee5803836c9
keywords:
- audio waveform, messaggi
- audio ausiliario, messaggi
- audio waveform, MM_WOM_DONE messaggio
- audio ausiliario, MM_WOM_DONE messaggio
- MM_WOM_DONE messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6aca93f23ed74a4a4974633d8345f2e897535e156ccc03f46eb0da92a2d2fdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037861"
---
# <a name="processing-the-mm_wom_done-message"></a>Elaborazione del messaggio \_ MM WOM \_ DONE

L'esempio seguente illustra come elaborare il [**messaggio MM \_ WOM \_ DONE.**](mm-wom-done.md) Questo esempio presuppone che l'applicazione non riproduci più blocchi di dati, quindi può chiudere il dispositivo di output dopo la riproduzione di un singolo blocco di dati.


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



 

 




