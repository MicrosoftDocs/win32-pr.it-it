---
title: Creazione di una funzione di callback di errore
description: Creazione di una funzione di callback di errore
ms.assetid: a489ec94-c566-44b1-aa93-9b43f23de744
keywords:
- capSetCallbackOnError (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac37c0e12b8f92520c4445c4c5ba3361974d836
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710459"
---
# <a name="creating-an-error-callback-function"></a><span data-ttu-id="9471c-104">Creazione di una funzione di callback di errore</span><span class="sxs-lookup"><span data-stu-id="9471c-104">Creating an Error Callback Function</span></span>

<span data-ttu-id="9471c-105">L'esempio seguente è una semplice funzione di callback degli errori.</span><span class="sxs-lookup"><span data-stu-id="9471c-105">The following example is a simple error callback function.</span></span> <span data-ttu-id="9471c-106">Registrare questo callback usando la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="9471c-106">Register this callback by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```
TCHAR gachBuffer[100]; // Global buffer.

// ErrorCallbackProc: error callback function. 
// hWnd:              capture window handle. 
// nErrID:            error code for the encountered error. 
// lpErrorText:       error text string for the encountered error. 
// 
LRESULT PASCAL ErrorCallbackProc(HWND hWnd, int nErrID,
    LPTSTR lpErrorText) 
{ 
 
    if (!hWnd) 
        return FALSE; 
 
    if (nErrID == 0)            // Starting a new major function. 
        return TRUE;            // Clear out old errors. 
 
    // Show the error identifier and text. 
    _stprintf_s(gachBuffer, TEXT("Error# %d"), nErrID); 
 
    MessageBox(hWnd, lpErrorText, gachBuffer, 
        MB_OK | MB_ICONEXCLAMATION); 
 
    return (LRESULT) TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="9471c-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9471c-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9471c-108">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="9471c-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




