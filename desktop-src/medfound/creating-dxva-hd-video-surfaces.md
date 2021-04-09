---
description: .
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Creazione di superfici video DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 459504a312ec0d59cf3642f528f433ffce8ba094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878462"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Creazione di superfici video DXVA-HD

L'applicazione deve creare una o più superfici Direct3D da usare per i frame di input. Questi devono essere allocati nel pool di memoria specificato dal membro **InputPool** della struttura [**DXVAHD \_ VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . È possibile utilizzare i tipi di superficie seguenti:

-   Una superficie video creata chiamando [**IDXVAHD \_ Device:: CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e specificando il tipo di superficie **DXVAHD \_ \_ \_ \_ input video input** o **DXVAHD Surface Type tipo di superficie \_ \_ \_ \_ \_ privata input** . Questo tipo di superficie è equivalente a una superficie normale fuori schermo.
-   Superficie di destinazione di rendering del decodificatore, creata chiamando [**IDirectXVideoAccelerationService:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e specificando il tipo di superficie **\_ VideoDecoderRenderTarget DXVA2** . Questo tipo di superficie viene usato per la decodifica DXVA.
-   Una superficie normale fuori schermo.

Il codice seguente illustra come allocare una superficie video usando [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):


```C++
    // Create the video surface for the primary video stream.
    hr = pDXVAHD->CreateVideoSurface(
        VIDEO_WIDTH,
        VIDEO_HEIGHT,
        VIDEO_FORMAT,
        caps.InputPool,
        0,  // Usage
        DXVAHD_SURFACE_TYPE_VIDEO_INPUT,
        1,      // Number of surfaces to create
        &pSurf, // Array of surface pointers
        NULL
        );
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



