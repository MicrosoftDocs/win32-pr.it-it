---
title: Creazione del pacchetto di plug-in DSP
description: Creazione del pacchetto di plug-in DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-in di Windows Media Player, pipeline Media Foundation
- plug-in, pipeline di Media Foundation
- plug-in per l'elaborazione di segnali digitali, pipeline di Media Foundation
- Plug-in DSP, pipeline di Media Foundation
- Pipeline Media Foundation
- Plug-in di Windows Media Player, pipeline DirectShow
- plug-in, pipeline DirectShow
- plug-in di elaborazione dei segnali digitali, pipeline DirectShow
- Plug-in DSP, pipeline DirectShow
- Pipeline DirectShow
- plug-in per l'elaborazione di segnali digitali, di base
- Plug-in DSP, di base
- Plug-in di Windows Media Player, DSP Basic
- plug-in, DSP di base
- plug-in DSP di base
- Plug-in di Windows Media Player, DSP Dual Mode
- plug-in, DSP Dual Mode
- plug-in di elaborazione dei segnali digitali, Dual Mode
- Plug-in DSP, modalità duale
- plug-in DSP a doppia modalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300002"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="d90a4-123">Creazione del pacchetto di plug-in DSP</span><span class="sxs-lookup"><span data-stu-id="d90a4-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="d90a4-124">Windows Media Player esegue il rendering di audio e video utilizzando una delle seguenti pipeline.</span><span class="sxs-lookup"><span data-stu-id="d90a4-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="d90a4-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="d90a4-125">DirectShow</span></span>
-   <span data-ttu-id="d90a4-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d90a4-126">Media Foundation</span></span>

<span data-ttu-id="d90a4-127">In Microsoft Windows XP e versioni precedenti, il lettore utilizza DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d90a4-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="d90a4-128">In Windows Vista, il lettore talvolta utilizza DirectShow e talvolta utilizza Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d90a4-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="d90a4-129">Un plug-in DSP progettato per essere eseguito nella pipeline DirectShow è denominato *plug-in DSP di base*.</span><span class="sxs-lookup"><span data-stu-id="d90a4-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="d90a4-130">Un plug-in DSP di base funge da oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="d90a4-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="d90a4-131">Un plug-in DSP di base può essere eseguito in modalità nativa nella pipeline DirectShow e può anche essere eseguito nella pipeline Media Foundation all'interno di un wrapper fornito da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d90a4-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="d90a4-132">Un plug-in DSP progettato per l'esecuzione a livello nativo (senza wrapper necessario) sia nella pipeline DirectShow che in quella Media Foundation viene definito *plug-in DSP a doppia modalità*.</span><span class="sxs-lookup"><span data-stu-id="d90a4-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="d90a4-133">Un plug-in DSP in modalità duale può fungere da DMO o come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d90a4-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="d90a4-134">Un plug-in DSP è un oggetto COM confezionato come file con estensione dll autoregistrato.</span><span class="sxs-lookup"><span data-stu-id="d90a4-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="d90a4-135">Le interfacce implementate dal plug-in variano a seconda che il plug-in sia stato progettato come plug-in DSP di base o come plug-in DSP a doppia modalità.</span><span class="sxs-lookup"><span data-stu-id="d90a4-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="d90a4-136">Per informazioni dettagliate sulle interfacce che devono essere implementate dai plug-in DSP, vedere [interfacce obbligatorie](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d90a4-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="d90a4-137">Un plug-in DSP eseguito nella pipeline Media Foundation (in modo nativo o di cui è stato eseguito il wrapper) deve registrare il modello di threading come "both".</span><span class="sxs-lookup"><span data-stu-id="d90a4-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="d90a4-138">Per informazioni dettagliate sulle sottochiavi del registro di sistema e le voci associate ai plug-in DSP, vedere [registrazione dei plug-in DSP](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="d90a4-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="d90a4-139">Un plug-in DSP che implementa interfacce personalizzate e viene eseguito nella pipeline Media Foundation (in modalità nativa o a capo) deve essere associato a un file con estensione dll dello stub proxy in grado di effettuare il marshalling delle interfacce personalizzate tra i limiti dei processi.</span><span class="sxs-lookup"><span data-stu-id="d90a4-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="d90a4-140">Per informazioni sul componente stub-proxy, vedere [aggiornamento dei plug-in DSP esistenti](updating-existing-dsp-plug-ins.md) e [aggiornamenti alla procedura guidata plug-in dsp per Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="d90a4-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="d90a4-141">Gli oggetti plug-in DSP non devono essere creati come singleton.</span><span class="sxs-lookup"><span data-stu-id="d90a4-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="d90a4-142">Windows Media Player deve essere in grado di creare più istanze separate di un plug-in DSP specifico.</span><span class="sxs-lookup"><span data-stu-id="d90a4-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="d90a4-143">I plug-in DSP eseguiti in Windows Vista Protected Media Path (PMP) devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="d90a4-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="d90a4-144">Per ulteriori informazioni, vedere [la pagina relativa alla firma del codice per i componenti multimediali protetti in Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="d90a4-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d90a4-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d90a4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d90a4-146">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="d90a4-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 