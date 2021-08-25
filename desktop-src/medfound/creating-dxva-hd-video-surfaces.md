---
description: Creazione di superfici video DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Creazione di superfici video DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d40058a02c179a8f9f0690eea9cce777bdd0563d5d27b36ddcb3d34f8fff8a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829051"
---
# <a name="creating-dxva-hd-video-surfaces"></a>Creazione di superfici video DXVA-HD

L'applicazione deve creare una o più superfici Direct3D da usare per i fotogrammi di input. Devono essere allocati nel pool di memoria specificato dal membro **InputPool** della struttura [**\_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) È possibile usare i tipi di superficie seguenti:

-   Una superficie video creata chiamando [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e specificando il tipo di superficie **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT** o **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE.** Questo tipo di superficie equivale a una superficie normale esterna allo schermo.
-   Superficie di destinazione del rendering del decodificatore, creata chiamando [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e specificando il tipo di superficie **DXVA2 \_ VideoDecoderRenderTarget.** Questo tipo di superficie viene usato per la decodifica DXVA.
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

 

 



