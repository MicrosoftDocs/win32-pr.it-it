---
description: Creazione di superfici video DXVA-HD
ms.assetid: a4508a1e-d68b-4c55-bce4-c8b462134fa1
title: Creazione di superfici video DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20dea8f34a275aab59b2d57f68ca76d46b1c1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102549"
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

 

 



