---
title: Interfacce necessarie (Windows Media Player SDK)
description: Informazioni sulle interfacce necessarie che Windows Media Player implementano in DirectShow o Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player plug-in, interfacce
- plug-in, interfacce
- plug-in per l'elaborazione di segnali digitali, interfacce
- plug-in DSP, interfacce
- interfacce, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406094"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="4d83b-108">Interfacce necessarie (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="4d83b-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="4d83b-109">Windows Media Player esegue il rendering di audio e video usando una delle pipeline seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d83b-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="4d83b-110">Directshow</span><span class="sxs-lookup"><span data-stu-id="4d83b-110">DirectShow</span></span>
-   <span data-ttu-id="4d83b-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d83b-111">Media Foundation</span></span>

<span data-ttu-id="4d83b-112">In Microsoft Windows XP e versioni precedenti, Player usa DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4d83b-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="4d83b-113">In Windows Vista, Il lettore usa a volte DirectShow e talvolta usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4d83b-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="4d83b-114">Un plug-in DSP implementa alcune o tutte le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="4d83b-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="4d83b-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="4d83b-115">**IMediaObject**</span></span>
-   <span data-ttu-id="4d83b-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="4d83b-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="4d83b-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="4d83b-117">**IMFTransform**</span></span>
-   <span data-ttu-id="4d83b-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="4d83b-118">**IMFGetService**</span></span>
-   <span data-ttu-id="4d83b-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="4d83b-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="4d83b-120">Un plug-in che implementa **IMediaObject** e **IWMPPluginEnable** può essere eseguito nella pipeline DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4d83b-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="4d83b-121">Può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4d83b-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="4d83b-122">Un plug-in di questo tipo è denominato Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="4d83b-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="4d83b-123">È comune pensare che un DMO sia analogo a un oggetto filtro in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="4d83b-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="4d83b-124">La documentazione di DMO è disponibile nella sezione DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4d83b-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="4d83b-125">Un plug-in che implementa **IMFTransform** e **IMFGetService** può essere eseguito in modo nativo (non è necessario alcun wrapper) nella pipeline Media Foundation richiesta.</span><span class="sxs-lookup"><span data-stu-id="4d83b-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="4d83b-126">Un plug-in di questo tipo è denominato Media Foundation Transform (MFT).</span><span class="sxs-lookup"><span data-stu-id="4d83b-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="4d83b-127">La documentazione di MFT è disponibile nella Media Foundation del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4d83b-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="4d83b-128">Un plug-in che implementa **IMediaObject,** **IWMPPluginEnable,** **IMFTransform** e **IMFGetService** può essere eseguito nella pipeline DirectShow e può anche essere eseguito in modo nativo nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="4d83b-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="4d83b-129">Questo tipo di plug-in, denominato *plug-in DSP* in modalità doppia, può svolgere il ruolo di DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="4d83b-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="4d83b-130">Quando Windows Media Player un plug-in DSP a modalità doppia nella pipeline Media Foundation, esegue prima una query per **l'interfaccia IMFTransform.**</span><span class="sxs-lookup"><span data-stu-id="4d83b-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="4d83b-131">Se la query ha esito negativo, Windows Media Player query per **l'interfaccia IMediaObject.**</span><span class="sxs-lookup"><span data-stu-id="4d83b-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="4d83b-132">Se la query **IMediaObject** ha esito positivo, il plug-in viene incapsulato e aggiunto alla Media Foundation pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d83b-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="4d83b-133">Indipendentemente dalla pipeline, qualsiasi plug-in DSP che consente all'utente di impostare le proprietà deve implementare **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="4d83b-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d83b-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4d83b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d83b-135">**Panoramica degli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="4d83b-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="4d83b-136">**Interfacce plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="4d83b-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4d83b-137">**Creazione di pacchetti plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="4d83b-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




