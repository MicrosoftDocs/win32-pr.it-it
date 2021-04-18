---
description: Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinazione del supporto hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303926"
---
# <a name="determining-hardware-support-direct3d-9"></a><span data-ttu-id="1ea89-103">Determinazione del supporto hardware (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1ea89-103">Determining Hardware Support (Direct3D 9)</span></span>

<span data-ttu-id="1ea89-104">Direct3D fornisce le funzioni seguenti per determinare il supporto hardware.</span><span class="sxs-lookup"><span data-stu-id="1ea89-104">Direct3D provides the following functions to determine hardware support.</span></span>

-   [<span data-ttu-id="1ea89-105">**IDirect3D9:: CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="1ea89-105">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    <span data-ttu-id="1ea89-106">Usato per verificare se un formato di superficie può essere usato come trama, se un formato di superficie può essere usato come trama e una destinazione di rendering o se un formato di superficie può essere usato come buffer di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="1ea89-106">Used to verify whether a surface format can be used as a texture, whether a surface format can be used as a texture and a render target, or whether a surface format can be used as a depth-stencil buffer.</span></span> <span data-ttu-id="1ea89-107">Questo metodo viene inoltre usato per verificare il supporto del formato del buffer di profondità e il supporto del formato di buffer dello stencil Depth.</span><span class="sxs-lookup"><span data-stu-id="1ea89-107">In addition, this method is used to verify depth buffer format support and depth-stencil buffer format support.</span></span>

-   [<span data-ttu-id="1ea89-108">**IDirect3D9:: CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="1ea89-108">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    <span data-ttu-id="1ea89-109">Usato per verificare la capacità di un dispositivo di eseguire l'accelerazione hardware, la capacità di un dispositivo di creare una catena di scambio per la presentazione o la possibilità di eseguire il rendering del dispositivo nel formato di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="1ea89-109">Used to verify a device's ability to perform hardware acceleration, a device's ability to build a swap chain for presentation, or a device's ability to render to the current display format.</span></span>

-   [<span data-ttu-id="1ea89-110">**IDirect3D9:: CheckDepthStencilMatch**</span><span class="sxs-lookup"><span data-stu-id="1ea89-110">**IDirect3D9::CheckDepthStencilMatch**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    <span data-ttu-id="1ea89-111">Utilizzato per verificare se un formato di buffer di stencil Depth è compatibile con un formato di destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="1ea89-111">Used to verify whether a depth-stencil buffer format is compatible with a render-target format.</span></span> <span data-ttu-id="1ea89-112">Si noti che prima di chiamare questo metodo, l'applicazione deve chiamare [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) sia nei formati depth-stencil che di rendering-target.</span><span class="sxs-lookup"><span data-stu-id="1ea89-112">Note that before calling this method, the application should call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) on both the depth-stencil and render-target formats.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ea89-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ea89-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ea89-114">Dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="1ea89-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
