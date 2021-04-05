---
title: Utilizzo dei livelli di protezione dell'output
description: Utilizzo dei livelli di protezione dell'output
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- Windows Media Format SDK, livelli di protezione dell'output (OPL)
- Windows Media Format SDK, livelli di protezione
- ASF (Advanced Systems Format), livelli di protezione dell'output (OPL)
- ASF (formato avanzato dei sistemi), livelli di protezione dell'output (OPL)
- ASF (Advanced Systems Format), livelli di protezione
- ASF (formato avanzato dei sistemi), livelli di protezione
- ASF (Advanced Systems Format), più licenze
- ASF (Advanced Systems Format), più licenze
- Digital Rights Management (DRM), livelli di protezione dell'output (OPL)
- DRM (Digital Rights Management), livelli di protezione dell'output (OPL)
- Digital Rights Management (DRM), livelli di protezione
- DRM (Digital Rights Management), livelli di protezione
- Digital Rights Management (DRM), valutazione del livello di protezione dell'output (OPL)
- DRM (Digital Rights Management), valutazione del livello di protezione dell'output (OPL)
- Digital Rights Management (DRM), più licenze
- DRM (Digital Rights Management), più licenze
- livelli di protezione dell'output (OPL)
- OPL (livelli di protezione dell'output)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab7023cc8285e5f3993aac69c57deca9675d9dd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336257"
---
# <a name="working-with-output-protection-levels"></a><span data-ttu-id="d7744-121">Utilizzo dei livelli di protezione dell'output</span><span class="sxs-lookup"><span data-stu-id="d7744-121">Working with Output Protection Levels</span></span>

<span data-ttu-id="d7744-122">Le licenze create mediante Windows Media Rights Manager 10 SDK possono specificare restrizioni di azione mediante i livelli di protezione dell'output (OPLs).</span><span class="sxs-lookup"><span data-stu-id="d7744-122">Licenses created by using the Windows Media Rights Manager 10 SDK can specify action restrictions using output protection levels (OPLs).</span></span> <span data-ttu-id="d7744-123">OPLs consente a un creatore di licenze di consentire alcune azioni solo sui dispositivi con tecnologie specifiche.</span><span class="sxs-lookup"><span data-stu-id="d7744-123">OPLs enable a license creator to allow some actions only on devices with specific technologies.</span></span> <span data-ttu-id="d7744-124">I vantaggi dell'uso di OPLs sono la maggiore flessibilità nella creazione di restrizioni di licenza rispetto alle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d7744-124">The benefits of using OPLs is that you get more flexibility in creating license restrictions than previous versions.</span></span> <span data-ttu-id="d7744-125">Inoltre, OPLs sono espandibili per supportare le tecnologie future.</span><span class="sxs-lookup"><span data-stu-id="d7744-125">In addition, OPLs are expandable to accommodate future technologies.</span></span> <span data-ttu-id="d7744-126">È possibile supportare tali licenze nelle applicazioni usando i metodi dell'interfaccia [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) .</span><span class="sxs-lookup"><span data-stu-id="d7744-126">You can support such licenses in your applications by using the methods of the [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) interface.</span></span>

<span data-ttu-id="d7744-127">Per leggere i file protetti da una licenza che specifica OPLs, è necessario controllare il OPL per l'azione desiderata.</span><span class="sxs-lookup"><span data-stu-id="d7744-127">To read files that are protected by a license that specifies OPLs, you must check the OPL for the desired action.</span></span> <span data-ttu-id="d7744-128">La tecnologia di output usata dall'applicazione deve essere consentita da OPL nella licenza.</span><span class="sxs-lookup"><span data-stu-id="d7744-128">The output technology your application is using must be allowed by the OPL in the license.</span></span> <span data-ttu-id="d7744-129">Ad esempio, alcune licenze per l'audio protetto potrebbero richiedere l'uso di un percorso audio sicuro per riprodurlo.</span><span class="sxs-lookup"><span data-stu-id="d7744-129">For example, some licenses for protected audio may require that you use secure audio path to play it.</span></span>

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a><span data-ttu-id="d7744-130">Configurazione del lettore per valutare i livelli di protezione dell'output</span><span class="sxs-lookup"><span data-stu-id="d7744-130">Configuring the Reader to Evaluate Output Protection Levels</span></span>

<span data-ttu-id="d7744-131">Prima di poter controllare OPLs per i file caricati nel lettore, è necessario chiamare il metodo [**IWMDRMReader2:: SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) , passando **true** per il parametro *fEvaluate* .</span><span class="sxs-lookup"><span data-stu-id="d7744-131">Before you can check OPLs for files loaded in the reader, you must call the [**IWMDRMReader2::SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) method, passing **TRUE** for the *fEvaluate* parameter.</span></span> <span data-ttu-id="d7744-132">Se non si chiama questo metodo, le licenze che richiedono OPLs non sono visibili per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d7744-132">If you do not call this method, licenses that require OPLs are not visible to your application.</span></span>

## <a name="evaluating-copy-output-protection-levels"></a><span data-ttu-id="d7744-133">Valutazione del livello di protezione dell'output di copia</span><span class="sxs-lookup"><span data-stu-id="d7744-133">Evaluating Copy Output Protection Levels</span></span>

<span data-ttu-id="d7744-134">Per ottenere i livelli di protezione dell'output per l'azione di copia, chiamare il metodo [**IWMDRMReader2:: GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="d7744-134">To get output protection levels for the copy action, call the [**IWMDRMReader2::GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) method.</span></span> <span data-ttu-id="d7744-135">I dati ricevuti dalla chiamata vengono archiviati in una struttura di [**\_ Copia \_ OPL di DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) .</span><span class="sxs-lookup"><span data-stu-id="d7744-135">The data you receive from the call is stored in a [**DRM\_COPY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) structure.</span></span> <span data-ttu-id="d7744-136">La struttura contiene un livello di protezione dell'output di base che specifica il livello di output minimo per l'azione di copia nella licenza.</span><span class="sxs-lookup"><span data-stu-id="d7744-136">The structure contains a base output protection level, which specifies the minimum output level for the copy action in the license.</span></span> <span data-ttu-id="d7744-137">Tuttavia, la \_ \_ struttura OPL copia DRM contiene anche due elenchi di identificatori di tecnologia: uno per le tecnologie consentite classificate a una OPL inferiore rispetto alla base e uno per le tecnologie classificate come uguale o superiore rispetto al OPL di base ma che sono limitate dalla licenza.</span><span class="sxs-lookup"><span data-stu-id="d7744-137">However, the DRM\_COPY\_OPL structure also contains two lists of technology identifiers: one for allowed technologies that are rated at a lower OPL than the base, and one for technologies that are rated equal to or higher than the base OPL but that are restricted by the license.</span></span> <span data-ttu-id="d7744-138">È necessario controllare le inclusioni e le esclusioni per assicurarsi che la tecnologia usata dall'applicazione sia consentita dalla licenza.</span><span class="sxs-lookup"><span data-stu-id="d7744-138">You must check the inclusions and exclusions to ensure that the technology your application is using is allowed by the license.</span></span>

## <a name="evaluating-play-output-protection-levels"></a><span data-ttu-id="d7744-139">Valutazione del livello di protezione dell'output di riproduzione</span><span class="sxs-lookup"><span data-stu-id="d7744-139">Evaluating Play Output Protection Levels</span></span>

<span data-ttu-id="d7744-140">Per ottenere i livelli di protezione dell'output per l'azione Play, chiamare il metodo [**IWMDRMReader2:: GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) .</span><span class="sxs-lookup"><span data-stu-id="d7744-140">To get output protection levels for the play action, call the [**IWMDRMReader2::GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) method.</span></span> <span data-ttu-id="d7744-141">I dati ricevuti dalla chiamata vengono archiviati in una struttura [**OPL di \_ riproduzione \_ DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) .</span><span class="sxs-lookup"><span data-stu-id="d7744-141">The data you receive from the call is stored in a [**DRM\_PLAY\_OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) structure.</span></span> <span data-ttu-id="d7744-142">La struttura contiene diverse altre strutture.</span><span class="sxs-lookup"><span data-stu-id="d7744-142">The structure contains several other structures.</span></span> <span data-ttu-id="d7744-143">I livelli di protezione dell'output di base per l'azione di riproduzione vengono archiviati in una struttura di livello di  [**\_ \_ \_ protezione \_ dell'output minimo DRM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) (il membro minOPL di **DRM \_ Play \_ OPL**), che definisce il OPL minimo necessario per riprodurre il contenuto in una varietà di formati.</span><span class="sxs-lookup"><span data-stu-id="d7744-143">The base output protection levels for the play action are stored in a [**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) structure (the **minOPL** member of **DRM\_PLAY\_OPL**), which defines the minimum OPL required to play content in a variety of formats.</span></span> <span data-ttu-id="d7744-144">È necessario controllare il membro per il tipo di formati di output che l'applicazione recapita.</span><span class="sxs-lookup"><span data-stu-id="d7744-144">You must check the member for the type of output formats that your application delivers.</span></span>

<span data-ttu-id="d7744-145">La **struttura \_ \_ OPL di riproduzione DRM** definisce due tipi di restrizioni: il campionamento inattivo richiesto e gli identificatori di protezione dell'output video consentiti.</span><span class="sxs-lookup"><span data-stu-id="d7744-145">The **DRM\_PLAY\_OPL** structure defines two kinds of restrictions: required down-sampling and allowed video output protection identifiers.</span></span>

<span data-ttu-id="d7744-146">Il sottocampionamento richiesto è definito come un elenco di identificatori di tecnologia di output (il membro **oplIdDownsample** di **DRM \_ Play \_ OPL**) che, se usato, può ricevere il contenuto per la riproduzione solo se il contenuto viene prima sottoposto a campionamento a una velocità in bit inferiore.</span><span class="sxs-lookup"><span data-stu-id="d7744-146">Required down-sampling is defined as a list of output technology identifiers (the **oplIdDownsample** member of **DRM\_PLAY\_OPL**) that, if used, can receive the content for playback only if the content is first down-sampled to a lower bit rate.</span></span>

<span data-ttu-id="d7744-147">Gli identificatori di protezione dell'output video consentiti sono definiti come un elenco di tecnologie di output video con le informazioni di configurazione per ognuna.</span><span class="sxs-lookup"><span data-stu-id="d7744-147">Allowed video output protection identifiers are defined as a list of video output technologies with configuration information for each.</span></span>

## <a name="handling-multiple-licenses"></a><span data-ttu-id="d7744-148">Gestione di più licenze</span><span class="sxs-lookup"><span data-stu-id="d7744-148">Handling Multiple Licenses</span></span>

<span data-ttu-id="d7744-149">Alcuni file possono avere più licenze associate nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="d7744-149">Some files may have multiple licenses associated with them in the local license store.</span></span> <span data-ttu-id="d7744-150">Quando si valuta OPLs per un file che si sta leggendo, è possibile verificare la presenza di licenze aggiuntive chiamando il metodo [**IWMDRMReader2:: TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) .</span><span class="sxs-lookup"><span data-stu-id="d7744-150">When you evaluate OPLs for a file that you are reading, you can check for additional licenses by calling the [**IWMDRMReader2::TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) method.</span></span> <span data-ttu-id="d7744-151">È necessario continuare a provare le licenze fino a quando non ne viene individuato uno che consente l'azione da eseguire o fino a quando TryNextLicense non restituisce DRM \_ S \_ false, che indica che non sono presenti altre licenze.</span><span class="sxs-lookup"><span data-stu-id="d7744-151">You should continue trying licenses until you find one that allows the action you want to perform or until TryNextLicense returns DRM\_S\_FALSE, which indicates that there are no more licenses.</span></span>

<span data-ttu-id="d7744-152">In alcuni casi, è possibile che un file disponga di una licenza associata che richiede un OPL che l'applicazione non può supportare.</span><span class="sxs-lookup"><span data-stu-id="d7744-152">In some cases, a file might have an associated license that requires an OPL that your application cannot support.</span></span> <span data-ttu-id="d7744-153">In tal caso è importante verificare la presenza di licenze aggiuntive perché potrebbe esistere una licenza che non specifica OPLs.</span><span class="sxs-lookup"><span data-stu-id="d7744-153">In such a case it is important to check for additional licenses because a license may exist that does not specify OPLs.</span></span>

<span data-ttu-id="d7744-154">**Nota** Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="d7744-154">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7744-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7744-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7744-156">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="d7744-156">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="d7744-157">**Interfaccia IWMDRMReader2**</span><span class="sxs-lookup"><span data-stu-id="d7744-157">**IWMDRMReader2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




