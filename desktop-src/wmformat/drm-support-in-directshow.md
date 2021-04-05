---
title: Supporto DRM in DirectShow
description: Supporto DRM in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, supporto DRM in DirectShow
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Digital Rights Management (DRM)
- ASF (Advanced Systems Format), supporto DRM in DirectShow
- ASF (Advanced Systems Format), supporto DRM in DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- ASF (formato avanzato dei sistemi), Digital Rights Management (DRM)
- DirectShow, supporto DRM
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956177"
---
# <a name="drm-support-in-directshow"></a><span data-ttu-id="5f812-115">Supporto DRM in DirectShow</span><span class="sxs-lookup"><span data-stu-id="5f812-115">DRM Support in DirectShow</span></span>

<span data-ttu-id="5f812-116">La lettura e la scrittura di file protetti da DRM in DirectShow viene eseguita in modo sostanzialmente analogo a quando si utilizza direttamente Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5f812-116">Reading and writing DRM-protected files in DirectShow is done in basically the same way as when you use the Windows Media Format SDK directly.</span></span> <span data-ttu-id="5f812-117">Per iniziare, è necessaria la libreria statica WMStubDRM, ottenuta separatamente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5f812-117">To begin with, you need the wmstubdrm static library, which is obtained separately from Microsoft.</span></span> <span data-ttu-id="5f812-118">Inoltre, è necessario implementare l'interfaccia **IKeyProvider** per consentire all'applicazione di accedere agli oggetti runtime di Windows Media Format SDK quando è abilitato DRM.</span><span class="sxs-lookup"><span data-stu-id="5f812-118">In addition, you must implement the **IKeyProvider** interface to enable your application to access the Windows Media Format SDK run-time objects when DRM is enabled.</span></span>

<span data-ttu-id="5f812-119">Quando si applica la protezione DRM versione 1, usare l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , ottenuta come descritto nella pagina relativa alla [lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="5f812-119">When applying DRM version 1 protection, use the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which is obtained as described in [Reading ASF Files in DirectShow](reading-asf-files-in-directshow.md).</span></span> <span data-ttu-id="5f812-120">Quando si applica la protezione DRM versione 7, ottenere l'interfaccia [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) chiamando **QueryService** sul filtro del [writer ASF WM](wm-asf-writer-filter.md) , come illustrato nel frammento di codice più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5f812-120">When applying DRM version 7 protection, obtain the [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface by calling **QueryService** on the [WM ASF Writer](wm-asf-writer-filter.md) filter, as shown in the code snippet later in this topic.</span></span>

<span data-ttu-id="5f812-121">Tutte le altre configurazioni specifiche di DRM sono identiche a quelle descritte in [Abilitazione del supporto DRM](enabling-drm-support.md).</span><span class="sxs-lookup"><span data-stu-id="5f812-121">All other DRM-specific configuration is exactly the same as described in [Enabling DRM Support](enabling-drm-support.md).</span></span> <span data-ttu-id="5f812-122">Usare **QueryService** per ottenere l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) dal filtro del [lettore WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5f812-122">Use **QueryService** to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface from the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>

<span data-ttu-id="5f812-123">DirectX 9,0 contiene un esempio, PlayWndASF, un'applicazione DirectShow Player abilitata per DRM che illustra l'acquisizione di licenze DRM versione 1 e 7.</span><span class="sxs-lookup"><span data-stu-id="5f812-123">DirectX 9.0 contains a sample, PlayWndASF, a DRM-enabled DirectShow player application that demonstrates DRM version 1 and version 7 license acquisition.</span></span> <span data-ttu-id="5f812-124">Questo esempio include anche un'implementazione della classe **CKeyProvider** , che supporta l'interfaccia **IKeyProvider** .</span><span class="sxs-lookup"><span data-stu-id="5f812-124">This sample also includes an implementation of the **CKeyProvider** class, which supports the **IKeyProvider** interface.</span></span>

 

 




