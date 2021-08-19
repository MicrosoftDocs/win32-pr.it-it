---
title: Creazione di una funzione di callback di frame
description: Creazione di una funzione di callback di frame
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- Macro capSetCallbackOnFrame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac102baf62cbfabc79a9a38eb81127a0c6ea36b6ad694139f882bbae0e1bce1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497931"
---
# <a name="creating-a-frame-callback-function"></a>Creazione di una funzione di callback di frame

L'esempio seguente è una semplice funzione di callback dei frame. Registrare questo callback usando la macro [**capSetCallbackOnFrame.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe)


```
TCHAR gachBuffer[100];  // Global buffer.
DWORD gdwFrameNum = 0;

// FrameCallbackProc: frame callback function. 
// hWnd:              capture window handle. 
// lpVHdr:            pointer to structure containing captured 
//                        frame information. 
// 
LRESULT PASCAL FrameCallbackProc(HWND hWnd, LPVIDEOHDR lpVHdr) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    _stprintf_s(gachBuffer, TEXT("Preview frame# %ld "), gdwFrameNum++); 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE ; 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




