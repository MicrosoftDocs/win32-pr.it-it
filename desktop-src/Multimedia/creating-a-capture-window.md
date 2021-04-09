---
title: Creazione di una finestra di acquisizione
description: Creazione di una finestra di acquisizione
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- capCreateCaptureWindow (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28375da063839d3120ca60bdabd5ca997fa31b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044581"
---
# <a name="creating-a-capture-window"></a><span data-ttu-id="ebc8d-104">Creazione di una finestra di acquisizione</span><span class="sxs-lookup"><span data-stu-id="ebc8d-104">Creating a Capture Window</span></span>

<span data-ttu-id="ebc8d-105">Nell'esempio seguente viene creata una finestra di acquisizione tramite la funzione [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .</span><span class="sxs-lookup"><span data-stu-id="ebc8d-105">The following example creates a capture window by using the [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) function.</span></span>


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a><span data-ttu-id="ebc8d-106">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ebc8d-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebc8d-107">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="ebc8d-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




