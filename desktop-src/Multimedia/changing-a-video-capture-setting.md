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
# <a name="changing-a-video-capture-setting"></a><span data-ttu-id="21907-105">Modifica di un'impostazione di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="21907-105">Changing a Video Capture Setting</span></span>

<span data-ttu-id="21907-106">Nell'esempio seguente vengono usate le macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) e [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) per modificare la velocità di acquisizione dal valore predefinito (15 fotogrammi al secondo) a 10 fotogrammi al secondo.</span><span class="sxs-lookup"><span data-stu-id="21907-106">The following example uses the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) and [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macros to change the capture rate from the default value (15 frames per second) to 10 frames per second.</span></span>


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="21907-107">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21907-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21907-108">Uso di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="21907-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




