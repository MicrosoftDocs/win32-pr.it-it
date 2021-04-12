---
title: Modifica di un'impostazione di acquisizione video
description: Modifica di un'impostazione di acquisizione video
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- capCaptureGetSetup (macro)
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396791"
---
# <a name="changing-a-video-capture-setting"></a>Modifica di un'impostazione di acquisizione video

Nell'esempio seguente vengono usate le macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) e [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) per modificare la velocità di acquisizione dal valore predefinito (15 fotogrammi al secondo) a 10 fotogrammi al secondo.


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di acquisizione video](using-video-capture.md)
</dt> </dl>

 

 




