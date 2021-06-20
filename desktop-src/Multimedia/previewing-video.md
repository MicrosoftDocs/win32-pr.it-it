---
title: Anteprima di video (Windows Multimedia)
description: Questo esempio in Windows Multimedia usa capPreviewRate per impostare la frequenza di visualizzazione dei fotogrammi per la modalità di anteprima e capPreview per impostare la finestra di acquisizione in modalità di anteprima.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- macro capPreview
- macro capPreviewRate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc3aaeb9a8ff0f040218fca4822af93ab8bfe29
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405544"
---
# <a name="previewing-video-windows-multimedia"></a>Anteprima di video (Windows Multimedia)

L'esempio seguente usa la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) per impostare la frequenza di visualizzazione dei fotogrammi per la modalità di anteprima su 66 millisecondi per frame e quindi usa la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) per posizionare la finestra di acquisizione in modalità di anteprima.


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

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




