---
title: Creazione di una funzione di callback di stato
description: Creazione di una funzione di callback di stato
ms.assetid: 9aa98340-a5a0-4084-9670-b3c27a1351ed
keywords:
- Macro capSetCallbackOnStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d7c7d8ed6adc409eef338213c8c4e1febf2ca0825e13d41735710938e733b97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497921"
---
# <a name="creating-a-status-callback-function"></a>Creazione di una funzione di callback di stato

L'esempio seguente è una semplice funzione di callback dello stato. Registrare questo callback usando la macro [**capSetCallbackOnStatus.**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus)


```C++
TCHAR gachAppName[] = TEXT("Application Name");  // Application name.
TCHAR gachBuffer[100];  // Global buffer.

// StatusCallbackProc: status callback function. 
// hWnd:               capture window handle. 
// nID:                status code for the current status. 
// lpStatusText:       status text string for the current status. 
// 
LRESULT PASCAL StatusCallbackProc(HWND hWnd, int nID, 
    LPTSTR lpStatusText) 
{ 
    if (!hWnd) 
        return FALSE; 
 
    if (nID == 0) {
        // Clear old status messages.
        SetWindowText(hWnd, gachAppName); 
        return (LRESULT) TRUE; 
    } 
    // Show the status ID and status text. 
    _stprintf_s(gachBuffer, TEXT("Status# %d: %s"), nID, lpStatusText); 
 
    SetWindowText(hWnd, gachBuffer); 
    return (LRESULT) TRUE; 
} 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




