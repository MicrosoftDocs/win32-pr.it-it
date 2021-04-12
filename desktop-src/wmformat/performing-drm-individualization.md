---
title: Esecuzione dell'individualizzazione DRM
description: Esecuzione dell'individualizzazione DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, individualizzazione DRM
- Windows Media Format SDK, individualizzazione
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), individualizzazione
- DRM (Digital Rights Management), individualizzazione
- Digital Rights Management (DRM), individualizzazione DRM
- DRM (Digital Rights Management), individualizzazione DRM
- API estese del client DRM, individualizzazione
- API estese client, individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331711"
---
# <a name="performing-drm-individualization"></a><span data-ttu-id="0e224-122">Esecuzione dell'individualizzazione DRM</span><span class="sxs-lookup"><span data-stu-id="0e224-122">Performing DRM Individualization</span></span>

<span data-ttu-id="0e224-123">L'individualizzazione è il processo di aggiornamento del componente DRM nel computer client, della crittografia e della sua univocità.</span><span class="sxs-lookup"><span data-stu-id="0e224-123">Individualization is the process of updating the DRM component on the client computer, encrypting it, and making it unique.</span></span> <span data-ttu-id="0e224-124">Quando un computer è individualizzato, il componente DRM è collegato al computer e non sarà in grado di decodificare il contenuto in un altro computer.</span><span class="sxs-lookup"><span data-stu-id="0e224-124">When a computer is individualized, the DRM component is tied to the computer and will not be able to decode content on any other computer.</span></span> <span data-ttu-id="0e224-125">Le API estese del client Windows Media DRM forniscono supporto per individualizzazione il componente DRM nei computer client.</span><span class="sxs-lookup"><span data-stu-id="0e224-125">The Windows Media DRM Client Extended APIs provide support for individualizing the DRM component on client computers.</span></span>

<span data-ttu-id="0e224-126">L'individualizzazione viene eseguita chiamando il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) .</span><span class="sxs-lookup"><span data-stu-id="0e224-126">Individualization is performed by calling the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method.</span></span> <span data-ttu-id="0e224-127">È possibile chiamare **PerformSecurityUpdate** in modo che venga individuato solo se la versione sul server è più recente di quella installata nel computer client o se è possibile forzare l'individualizzazione senza considerare le versioni di sicurezza relative.</span><span class="sxs-lookup"><span data-stu-id="0e224-127">You can call **PerformSecurityUpdate** so that it will individualize only if the version on the server is newer than the one installed on the client computer, or you can force individualization without regard to the relative security versions.</span></span> <span data-ttu-id="0e224-128">Il flag per l'individualizzazione necessaria è WMDRM \_ Security \_ \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="0e224-128">The flag for as-needed individualization is WMDRM\_SECURITY\_PERFORM\_INDIV.</span></span> <span data-ttu-id="0e224-129">Il flag per l'individualizzazione forzata è WMDRM \_ Security \_ eseguire \_ Force \_ indiv.</span><span class="sxs-lookup"><span data-stu-id="0e224-129">The flag for forced individualization is WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV.</span></span>

<span data-ttu-id="0e224-130">**PerformSecurityUpdate** è una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="0e224-130">**PerformSecurityUpdate** is an asynchronous call.</span></span> <span data-ttu-id="0e224-131">Viene restituito rapidamente e quindi genera eventi per fornire informazioni sullo stato del processo di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e224-131">It will return quickly and then generate events to provide status information about the individualization process.</span></span> <span data-ttu-id="0e224-132">La maggior parte degli eventi generati sarà costituita da eventi **MEWMDRMIndividualizationProgress** , ognuno dei quali ha un'interfaccia [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associata.</span><span class="sxs-lookup"><span data-stu-id="0e224-132">The majority of the events generated will be **MEWMDRMIndividualizationProgress** events, and each has an associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span> <span data-ttu-id="0e224-133">Per ottenere l'interfaccia di stato, è necessario chiamare **IMFMediaEvent:: GetValue** per recuperare un puntatore **IUnknown** che si trova nello stesso oggetto, quindi eseguire una query per **IWMDRMIndividualizationStatus**.</span><span class="sxs-lookup"><span data-stu-id="0e224-133">To get the status interface, you must call **IMFMediaEvent::GetValue** to retrieve an **IUnknown** pointer that is on the same object and then query it for **IWMDRMIndividualizationStatus**.</span></span>

<span data-ttu-id="0e224-134">È possibile ottenere dati per una struttura di [**\_ \_ stato di personalizzazione WM**](drmwm-individualize-status.md) chiamando [**IWMDRMIndividualizeStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span><span class="sxs-lookup"><span data-stu-id="0e224-134">You can get data for a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure by calling [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md).</span></span> <span data-ttu-id="0e224-135">Ogni evento generato ha un proprio oggetto con lo stato, quindi è necessario eseguire ogni volta il processo di recupero del valore dell'evento ed esecuzione di query per l'interfaccia di stato.</span><span class="sxs-lookup"><span data-stu-id="0e224-135">Each event that is generated has its own object with status, so you must go through the process of getting the event value and querying for the status interface every time.</span></span>

<span data-ttu-id="0e224-136">A seconda delle dimensioni del download, potrebbero essere presenti dozzine o centinaia di eventi **MEWMDRMIndividualizationProgress** .</span><span class="sxs-lookup"><span data-stu-id="0e224-136">Depending on the size of the download, there may be dozens or hundreds of **MEWMDRMIndividualizationProgress** events.</span></span> <span data-ttu-id="0e224-137">Al termine del processo di individualizzazione, viene generato un evento **MEWMDRMIndividualizationCompleted** .</span><span class="sxs-lookup"><span data-stu-id="0e224-137">When the individualization process is finished, an **MEWMDRMIndividualizationCompleted** event is generated.</span></span>

<span data-ttu-id="0e224-138">Una volta completata l'individualizzazione, gli unici oggetti esistenti che riflettono il nuovo stato individualizzato saranno quelli che ereditano da [**IWMDRMSecurity**](iwmdrmsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="0e224-138">When individualization is completed, the only existing objects that will reflect the new individualized state are those that inherit from [**IWMDRMSecurity**](iwmdrmsecurity.md).</span></span> <span data-ttu-id="0e224-139">Tutti gli altri oggetti esistenti non verranno aggiornati.</span><span class="sxs-lookup"><span data-stu-id="0e224-139">All other existing objects will not be updated.</span></span> <span data-ttu-id="0e224-140">È necessario rilasciare e ricreare altri oggetti in modo che riflettano il nuovo stato individualizzato.</span><span class="sxs-lookup"><span data-stu-id="0e224-140">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e224-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e224-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e224-142">**Esempio di individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="0e224-142">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="0e224-143">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="0e224-143">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="0e224-144">**Uso del modello di eventi Media Foundation**</span><span class="sxs-lookup"><span data-stu-id="0e224-144">**Using the Media Foundation Event Model**</span></span>](using-the-media-foundation-model.md)
</dt> <dt>

<span data-ttu-id="0e224-145">[Procedure consigliate per l'individualizzazione DRM di Windows Media](/previous-versions/ms867216(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0e224-145">[Windows Media DRM Individualization Best Practices](/previous-versions/ms867216(v=msdn.10))</span></span>
</dt> </dl>

 

 




