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
# <a name="previewing-video-windows-multimedia"></a>Visualizzazione in anteprima di video (Windows Multimedia)

Nell'esempio seguente viene usata la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) per impostare la frequenza di visualizzazione dei frame per la modalità di anteprima su 66 millisecondi per fotogramma, quindi viene usata la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) per inserire la finestra di acquisizione in modalità di anteprima.


```C++
// Create the capture window.
HWND hWndC = capCreateCaptureWindow(TEXT("My Capture Window"),
    WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, hwndParent, nID);

capPreviewRate(hWndC, 66);     // rate, in milliseconds
capPreview(hWndC, TRUE);       // starts preview 

// Preview

capPreview(hWndC, FALSE);        // disables preview 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




