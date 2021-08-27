---
title: Anteprima di video (Windows Multimediali)
description: Questo esempio in Windows Multimediali usa capPreviewRate per impostare la frequenza di visualizzazione dei fotogrammi per la modalità di anteprima e capPreview per impostare la finestra di acquisizione in modalità di anteprima.
ms.assetid: 33ae7d07-5fea-47d7-b60d-4ee412e91dec
keywords:
- Macro capPreview
- Macro capPreviewRate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e70d0520af3bb71906c6b0ea4d1c0a61464559eedfd2385753b228841fa6af4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037911"
---
# <a name="previewing-video-windows-multimedia"></a>Anteprima di video (Windows Multimediali)

L'esempio seguente usa la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) per impostare la frequenza di visualizzazione dei fotogrammi per la modalità di anteprima su 66 millisecondi per fotogramma e quindi usa la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) per impostare la finestra di acquisizione in modalità di anteprima.


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

 

 




