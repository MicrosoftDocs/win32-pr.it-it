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
# <a name="creating-a-capture-window"></a>Creazione di una finestra di acquisizione

Nell'esempio seguente viene creata una finestra di acquisizione tramite la funzione [**capCreateCaptureWindow**](/windows/desktop/api/Vfw/nf-vfw-capcreatecapturewindowa) .


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

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




