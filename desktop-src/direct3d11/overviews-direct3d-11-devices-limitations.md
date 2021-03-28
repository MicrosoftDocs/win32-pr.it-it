---
title: Limitazioni della creazione di dispositivi WARP e Reference
description: Esistono alcune limitazioni per la creazione di dispositivi WARP e Reference in Direct3D 10,1 e Direct3D 11,0. In questo argomento vengono illustrate tali limitazioni.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337558"
---
# <a name="limitations-creating-warp-and-reference-devices"></a><span data-ttu-id="bd031-104">Limitazioni della creazione di dispositivi WARP e Reference</span><span class="sxs-lookup"><span data-stu-id="bd031-104">Limitations Creating WARP and Reference Devices</span></span>

<span data-ttu-id="bd031-105">Esistono alcune limitazioni per la creazione di dispositivi WARP e Reference in Direct3D 10,1 e Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="bd031-105">Some limitations exist for creating WARP and Reference devices in Direct3D 10.1 and Direct3D 11.0.</span></span> <span data-ttu-id="bd031-106">In questo argomento vengono illustrate tali limitazioni.</span><span class="sxs-lookup"><span data-stu-id="bd031-106">This topic discusses those limitations.</span></span>

<span data-ttu-id="bd031-107">I tipi di driver di riferimento per il tipo di driver D3D10 e il driver \_ \_ \_ D3D10 \_ \_ \_ non sono supportati nei \_ \_ livelli di funzionalità di D3D10 da \_ 9 \_ a 2 \_ a D3D10 \_ \_ a livello di funzionalità 9 \_ 3 in Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="bd031-107">The D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE driver types are not supported on the D3D10\_FEATURE\_LEVEL\_9\_1 through D3D10\_FEATURE\_LEVEL\_9\_3 feature levels in Direct3D 10.1.</span></span> <span data-ttu-id="bd031-108">Inoltre, il tipo di driver D3D del \_ \_ tipo \_ di driver non è supportato \_ nel livello di funzionalità D3D \_ \_ 11 \_ 0 in Direct3D 11,0.</span><span class="sxs-lookup"><span data-stu-id="bd031-108">Additionally, the D3D\_DRIVER\_TYPE\_WARP driver type is not supported on D3D\_FEATURE\_LEVEL\_11\_0 in Direct3D 11.0.</span></span> <span data-ttu-id="bd031-109">Ovvero, quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10,1 o quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11,0, se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità nella chiamata, la chiamata non è valida.</span><span class="sxs-lookup"><span data-stu-id="bd031-109">That is, when you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device or when you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.0 device, if you specify a combination of one of these driver types with one of these feature levels in the call, the call is invalid.</span></span> <span data-ttu-id="bd031-110">Solo le combinazioni seguenti di livelli di funzionalità, Runtime e tipi di driver sono valide per i dispositivi WARP e Reference:</span><span class="sxs-lookup"><span data-stu-id="bd031-110">Only the following combinations of feature levels, runtimes, and driver types are valid for WARP and Reference devices:</span></span>

-   <span data-ttu-id="bd031-111">\_ \_ Distorsione del tipo di driver D3D \_ a tutti i livelli di funzionalità in Direct3D 11,1, incluso in Windows 8</span><span class="sxs-lookup"><span data-stu-id="bd031-111">D3D\_DRIVER\_TYPE\_WARP on all feature levels in Direct3D 11.1, which Windows 8 includes</span></span>

    <span data-ttu-id="bd031-112">Riferimento al tipo di driver D3D in \_ \_ \_ tutti i livelli di funzionalità in Direct3D 11,1</span><span class="sxs-lookup"><span data-stu-id="bd031-112">D3D\_DRIVER\_TYPE\_REFERENCE on all feature levels in Direct3D 11.1</span></span>

    <span data-ttu-id="bd031-113">Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11,1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bd031-113">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="bd031-114">\_ \_ \_ Distorsione del tipo di driver D3D sul \_ livello di funzionalità D3D \_ \_ 9 \_ 1 tramite i \_ \_ \_ \_ livelli di funzionalità di 10 1 a livello di funzionalità D3D in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bd031-114">D3D\_DRIVER\_TYPE\_WARP on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="bd031-115">Informazioni \_ \_ di riferimento sul tipo di driver D3D \_ sul livello di \_ funzionalità D3D \_ \_ 9 \_ 1 tramite i \_ \_ livelli di funzionalità di livello funzionalità \_ di D3D 11 \_ in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="bd031-115">D3D\_DRIVER\_TYPE\_REFERENCE on D3D\_FEATURE\_LEVEL\_9\_1 through D3D\_FEATURE\_LEVEL\_11\_0 feature levels in Direct3D 11</span></span>

    <span data-ttu-id="bd031-116">Quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) per creare un dispositivo Direct3D 11, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bd031-116">When you call [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) to create a Direct3D 11 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

-   <span data-ttu-id="bd031-117">\_Guida \_ \_ \_ di riferimento al tipo di driver D3D10 e \_ al tipo di driver D3D10 \_ sul livello di funzionalità D3D10 da \_ \_ \_ 10 \_ 0 \_ a D3D10 \_ \_ \_ livelli di funzionalità 10 1 in Direct3D 10,1</span><span class="sxs-lookup"><span data-stu-id="bd031-117">D3D10\_DRIVER\_TYPE\_WARP and D3D10\_DRIVER\_TYPE\_REFERENCE on D3D10\_FEATURE\_LEVEL\_10\_0 through D3D10\_FEATURE\_LEVEL\_10\_1 feature levels in Direct3D 10.1</span></span>

    <span data-ttu-id="bd031-118">Quando si chiama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) per creare un dispositivo Direct3D 10,1, la chiamata è valida se si specifica una combinazione di uno di questi tipi di driver con uno di questi livelli di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bd031-118">When you call [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) to create a Direct3D 10.1 device, the call is valid if you specify a combination of one of these driver types with one of these feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd031-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bd031-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd031-120">Dispositivi</span><span class="sxs-lookup"><span data-stu-id="bd031-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="bd031-121">Introduzione a Direct3D 11 su hardware di livello inferiore</span><span class="sxs-lookup"><span data-stu-id="bd031-121">Introduction to Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[<span data-ttu-id="bd031-122">Procedura: creare un dispositivo WARP</span><span class="sxs-lookup"><span data-stu-id="bd031-122">How To: Create a WARP Device</span></span>](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[<span data-ttu-id="bd031-123">Procedura: creare un dispositivo di riferimento</span><span class="sxs-lookup"><span data-stu-id="bd031-123">How To: Create a Reference Device</span></span>](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[<span data-ttu-id="bd031-124">**\_Tipo di driver D3D10 \_**</span><span class="sxs-lookup"><span data-stu-id="bd031-124">**D3D10\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[<span data-ttu-id="bd031-125">**\_Level1 funzionalità \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="bd031-125">**D3D10\_FEATURE\_LEVEL1**</span></span>](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[<span data-ttu-id="bd031-126">**\_Tipo di driver D3D \_**</span><span class="sxs-lookup"><span data-stu-id="bd031-126">**D3D\_DRIVER\_TYPE**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[<span data-ttu-id="bd031-127">**\_Livello di funzionalità D3D \_**</span><span class="sxs-lookup"><span data-stu-id="bd031-127">**D3D\_FEATURE\_LEVEL**</span></span>](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 