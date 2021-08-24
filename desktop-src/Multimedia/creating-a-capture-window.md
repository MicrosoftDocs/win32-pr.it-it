---
title: Creazione di una finestra di acquisizione
description: Creazione di una finestra di acquisizione
ms.assetid: a727ce14-9b12-4f21-bab4-fa2eb245dce7
keywords:
- Funzione capCreateCaptureWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d44e7701900d090a8d73b226039d468e2da817e9c0f9746fc10eaa13578d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144774"
---
# <a name="creating-a-capture-window"></a>Creazione di una finestra di acquisizione

L'esempio seguente crea una finestra di acquisizione usando la [**funzione capCreateCaptureWindow.**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa)


```C++
hWndC = capCreateCaptureWindow (
    TEXT("My Capture Window"),   // window name if pop-up 
    WS_CHILD | WS_VISIBLE,       // window style 
    0, 0, 160, 120,              // window position and dimensions
    (HWND) hwndParent, 
    (int) nID /* child ID */); 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




