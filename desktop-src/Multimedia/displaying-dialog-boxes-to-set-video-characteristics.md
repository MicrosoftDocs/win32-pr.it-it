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
# <a name="displaying-dialog-boxes-to-set-video-characteristics"></a>Visualizzazione di finestre di dialogo per impostare le caratteristiche dei video

Ogni driver di acquisizione può fornire fino a tre diverse finestre di dialogo usate per controllare gli aspetti del processo di acquisizione e digitalizzazione dei video. Nell'esempio seguente viene illustrato come visualizzare queste finestre di dialogo. Prima di visualizzare ogni finestra di dialogo, nell'esempio viene chiamata la macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) e viene verificata la struttura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) restituita per verificare se il driver di acquisizione è in grado di visualizzarlo.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> <dt>

[**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps)
</dt> </dl>

 

 




