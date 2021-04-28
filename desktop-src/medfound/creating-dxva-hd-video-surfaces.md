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
# <a name="creating-dxva-hd-video-surfaces"></a><span data-ttu-id="f9595-103">Creazione di superfici video DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="f9595-103">Creating DXVA-HD Video Surfaces</span></span>

<span data-ttu-id="f9595-104">L'applicazione deve creare una o più superfici Direct3D da usare per i fotogrammi di input.</span><span class="sxs-lookup"><span data-stu-id="f9595-104">The application must create one or more Direct3D surfaces to use for the input frames.</span></span> <span data-ttu-id="f9595-105">Devono essere allocati nel pool di memoria specificato dal membro **InputPool** della struttura [**\_ VPDEVCAPS DXVAHD.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="f9595-105">These must be allocated in the memory pool specified by the **InputPool** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="f9595-106">È possibile usare i tipi di superficie seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9595-106">The following surface types can be used:</span></span>

-   <span data-ttu-id="f9595-107">Una superficie video creata chiamando [**IDXVAHD \_ Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) e specificando il tipo di superficie **DXVAHD \_ SURFACE TYPE VIDEO \_ \_ \_ INPUT** o **DXVAHD \_ SURFACE TYPE VIDEO INPUT \_ \_ \_ \_ PRIVATE.**</span><span class="sxs-lookup"><span data-stu-id="f9595-107">A video surface created by calling [**IDXVAHD\_Device::CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface) and specifying the **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT** or **DXVAHD\_SURFACE\_TYPE\_VIDEO\_INPUT\_PRIVATE** surface type.</span></span> <span data-ttu-id="f9595-108">Questo tipo di superficie equivale a una superficie normale esterna allo schermo.</span><span class="sxs-lookup"><span data-stu-id="f9595-108">This surface type is equivalent to an off-screen plain surface.</span></span>
-   <span data-ttu-id="f9595-109">Superficie di destinazione del rendering del decodificatore, creata chiamando [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) e specificando il tipo di superficie **DXVA2 \_ VideoDecoderRenderTarget.**</span><span class="sxs-lookup"><span data-stu-id="f9595-109">A decoder render-target surface, created by calling [**IDirectXVideoAccelerationService::CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) and specifying the **DXVA2\_VideoDecoderRenderTarget** surface type.</span></span> <span data-ttu-id="f9595-110">Questo tipo di superficie viene usato per la decodifica DXVA.</span><span class="sxs-lookup"><span data-stu-id="f9595-110">This surface type is used for DXVA decoding.</span></span>
-   <span data-ttu-id="f9595-111">Una superficie normale fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="f9595-111">An off-screen plain surface.</span></span>

<span data-ttu-id="f9595-112">Il codice seguente illustra come allocare una superficie video usando [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span><span class="sxs-lookup"><span data-stu-id="f9595-112">The following code shows how to allocate a video surface, using [**CreateVideoSurface**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface):</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f9595-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f9595-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9595-114">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="f9595-114">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



