---
title: Visualizzazione in anteprima di video (Windows Multimedia)
description: Anteprima del video
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- capPreview (macro)
- capPreviewRate (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79c8e24d30fd5141b5b1ac14de99d83e0b2bc620
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300782"
---
# <a name="previewing-video-windows-multimedia"></a><span data-ttu-id="71eb4-105">Visualizzazione in anteprima di video (Windows Multimedia)</span><span class="sxs-lookup"><span data-stu-id="71eb4-105">Previewing Video (Windows Multimedia)</span></span>

<span data-ttu-id="71eb4-106">Nell'esempio seguente viene usata la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) per impostare la frequenza di visualizzazione dei frame per la modalità di anteprima su 66 millisecondi per fotogramma, quindi viene usata la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) per inserire la finestra di acquisizione in modalità di anteprima.</span><span class="sxs-lookup"><span data-stu-id="71eb4-106">The following example uses the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro to set the frame display rate for preview mode to 66 milliseconds per frame and then uses the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro to place the capture window in preview mode.</span></span>


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a><span data-ttu-id="71eb4-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71eb4-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71eb4-108">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="71eb4-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




