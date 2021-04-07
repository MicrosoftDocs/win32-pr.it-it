---
title: Interfacce obbligatorie (Windows Media Player SDK)
description: Interfacce obbligatorie
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Plug-in di Windows Media Player, interfacce
- plug-in, interfacce
- plug-in di elaborazione dei segnali digitali, interfacce
- Plug-in DSP, interfacce
- interfacce, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873217"
---
# <a name="required-interfaces-windows-media-player-sdk"></a><span data-ttu-id="8d2ed-108">Interfacce obbligatorie (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="8d2ed-108">Required Interfaces (Windows Media Player SDK)</span></span>

<span data-ttu-id="8d2ed-109">Windows Media Player esegue il rendering di audio e video utilizzando una delle seguenti pipeline.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-109">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="8d2ed-110">DirectShow</span><span class="sxs-lookup"><span data-stu-id="8d2ed-110">DirectShow</span></span>
-   <span data-ttu-id="8d2ed-111">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8d2ed-111">Media Foundation</span></span>

<span data-ttu-id="8d2ed-112">In Microsoft Windows XP e versioni precedenti, il lettore utilizza DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-112">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="8d2ed-113">In Windows Vista, il lettore talvolta utilizza DirectShow e talvolta utilizza Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-113">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="8d2ed-114">Un plug-in DSP implementa alcune o tutte le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="8d2ed-114">A DSP plug-in implements some or all of the following interfaces:</span></span>

-   <span data-ttu-id="8d2ed-115">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-115">**IMediaObject**</span></span>
-   <span data-ttu-id="8d2ed-116">**IWMPPluginEnable**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-116">**IWMPPluginEnable**</span></span>
-   <span data-ttu-id="8d2ed-117">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-117">**IMFTransform**</span></span>
-   <span data-ttu-id="8d2ed-118">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-118">**IMFGetService**</span></span>
-   <span data-ttu-id="8d2ed-119">**ISpecifyPropertyPages**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-119">**ISpecifyPropertyPages**</span></span>

<span data-ttu-id="8d2ed-120">Un plug-in che implementa **IMediaObject** e **IWMPPluginEnable** può essere eseguito nella pipeline DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-120">A plug-in that implements **IMediaObject** and **IWMPPluginEnable** can run in the DirectShow pipeline.</span></span> <span data-ttu-id="8d2ed-121">Può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-121">It can also run in the Media Foundation Pipeline inside a wrapper provided by Media Foundation.</span></span> <span data-ttu-id="8d2ed-122">Un plug-in di questo tipo è denominato Microsoft DirectX Media Object (DMO).</span><span class="sxs-lookup"><span data-stu-id="8d2ed-122">A plug-in of this type is called a Microsoft DirectX Media Object (DMO).</span></span> <span data-ttu-id="8d2ed-123">È comune pensare a un DMO come analogo a un oggetto filtro in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-123">It is common to think of a DMO as being analogous to a filter object in DirectShow.</span></span> <span data-ttu-id="8d2ed-124">La documentazione DMO si trova nella sezione DirectShow del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-124">The DMO documentation is in the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="8d2ed-125">Un plug-in che implementa **IMFTransform** e **IMFGetService** può essere eseguito in modalità nativa (nessun wrapper necessario) nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-125">A plug-in that implements **IMFTransform** and **IMFGetService** can run natively (no wrapper required) in the Media Foundation pipeline.</span></span> <span data-ttu-id="8d2ed-126">Un plug-in di questo tipo è denominato trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="8d2ed-126">A plug-in of this type is called a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="8d2ed-127">La documentazione di MFT si trova nella sezione Media Foundation della Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-127">The MFT documentation is in the Media Foundation section of the Windows SDK.</span></span>

<span data-ttu-id="8d2ed-128">Un plug-in che implementa **IMediaObject**, **IWMPPluginEnable**, **IMFTransform** e **IMFGetService** può essere eseguito nella pipeline DirectShow e può anche essere eseguito in modalità nativa nella pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-128">A plug-in that implements **IMediaObject**, **IWMPPluginEnable**, **IMFTransform**, and **IMFGetService** can run in the DirectShow pipeline and can also run natively in the Media Foundation pipeline.</span></span> <span data-ttu-id="8d2ed-129">Questo tipo di plug-in, noto come *plug-in DSP Dual Mode*, può svolgere il ruolo di DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-129">This type of plug-in, which is called a *dual-mode DSP plug-in*, can play the role of a DMO or an MFT.</span></span>

<span data-ttu-id="8d2ed-130">Quando Windows Media Player usa un plug-in DSP in modalità duale nella pipeline Media Foundation, esegue prima una query per l'interfaccia **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="8d2ed-130">When Windows Media Player uses a dual-mode DSP plug-in in the Media Foundation pipeline, it first queries for the **IMFTransform** interface.</span></span> <span data-ttu-id="8d2ed-131">Se la query ha esito negativo, Windows Media Player query per l'interfaccia **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="8d2ed-131">If that query fails, Windows Media Player queries for the **IMediaObject** interface.</span></span> <span data-ttu-id="8d2ed-132">Se la query **IMediaObject** ha esito positivo, il plug-in viene incapsulato e aggiunto alla pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-132">If the **IMediaObject** query is successful, the plug-in is wrapped and added to the Media Foundation pipeline.</span></span>

<span data-ttu-id="8d2ed-133">Indipendentemente dalla pipeline, qualsiasi plug-in DSP che consente all'utente di impostare le proprietà deve implementare **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="8d2ed-133">Regardless of the pipeline, any DSP plug-in that allows the user to set properties must implement **ISpecifyPropertyPages**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d2ed-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d2ed-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d2ed-135">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="8d2ed-136">**Interfacce plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-136">**DSP Plug-in Interfaces**</span></span>](dsp-plug-in-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8d2ed-137">**Creazione del pacchetto di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="8d2ed-137">**DSP Plug-in Packaging**</span></span>](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




