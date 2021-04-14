---
title: Creazione di una funzione di callback di frame
description: Creazione di una funzione di callback di frame
ms.assetid: 37002ee0-9907-4aab-93cc-50fe9cd21cff
keywords:
- capSetCallbackOnFrame (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b2a921bfae235c50387c41865c44bb69b5c05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329287"
---
# <a name="creating-a-frame-callback-function"></a><span data-ttu-id="16094-104">Creazione di una funzione di callback di frame</span><span class="sxs-lookup"><span data-stu-id="16094-104">Creating a Frame Callback Function</span></span>

<span data-ttu-id="16094-105">L'esempio seguente è una semplice funzione di callback di frame.</span><span class="sxs-lookup"><span data-stu-id="16094-105">The following example is a simple frame callback function.</span></span> <span data-ttu-id="16094-106">Registrare questo callback usando la macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="16094-106">Register this callback by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="16094-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16094-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16094-108">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="16094-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




