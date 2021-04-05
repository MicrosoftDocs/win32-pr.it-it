---
title: Visualizzazione di finestre di dialogo per impostare le caratteristiche dei video
description: Visualizzazione di finestre di dialogo per impostare le caratteristiche dei video
ms.assetid: 8074f7d1-e8ab-46c3-acc2-a18be0eb4cc7
keywords:
- Struttura CAPDRIVERCAPS
- capDriverGetCaps (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73eea12d69a3d23b0345bee3495d32cbb1ad0ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856817"
---
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a><span data-ttu-id="fd5f5-105">Visualizzazione di finestre di dialogo per impostare le caratteristiche dei video</span><span class="sxs-lookup"><span data-stu-id="fd5f5-105">Displaying Dialog Boxes to Set Video Characteristics</span></span>

<span data-ttu-id="fd5f5-106">Ogni driver di acquisizione può fornire fino a tre diverse finestre di dialogo usate per controllare gli aspetti del processo di acquisizione e digitalizzazione dei video.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-106">Each capture driver can provide up to three different dialog boxes used to control aspects of the video digitization and capture process.</span></span> <span data-ttu-id="fd5f5-107">Nell'esempio seguente viene illustrato come visualizzare queste finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-107">The following example demonstrates how to display these dialog boxes.</span></span> <span data-ttu-id="fd5f5-108">Prima di visualizzare ogni finestra di dialogo, nell'esempio viene chiamata la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) e viene verificata la struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) restituita per verificare se il driver di acquisizione è in grado di visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="fd5f5-108">Before displaying each dialog box, the example calls the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro and checks the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure returned to see if the capture driver can display it.</span></span>


```C++
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

CAPDRIVERCAPS CapDriverCaps = { }; 
CAPSTATUS     CapStatus = { };

capDriverGetCaps(hWndC, &CapDriverCaps, sizeof(CAPDRIVERCAPS)); 
 
// Video source dialog box. 
if (CapDriverCaps.fHasDlgVideoSource)
{
    capDlgVideoSource(hWndC); 
}
 
// Video format dialog box. 
if (CapDriverCaps.fHasDlgVideoFormat) 
{
    capDlgVideoFormat(hWndC); 

    // Are there new image dimensions?
    capGetStatus(hWndC, &CapStatus, sizeof (CAPSTATUS));

    // If so, notify the parent of a size change.
} 
 
// Video display dialog box. 
if (CapDriverCaps.fHasDlgVideoDisplay)
{
    capDlgVideoDisplay(hWndC); 
}
```



## <a name="related-topics"></a><span data-ttu-id="fd5f5-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fd5f5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd5f5-110">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="fd5f5-110">Using Video Capture</span></span>](using-video-capture.md)
</dt> <dt>

[<span data-ttu-id="fd5f5-111">**capDriverGetCaps**</span><span class="sxs-lookup"><span data-stu-id="fd5f5-111">**capDriverGetCaps**</span></span>](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




