---
title: Scrittura di flussi con pixel non quadrati
description: Scrittura di flussi con pixel non quadrati
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, scrittura di flussi video
- Windows Media Format SDK, flussi video
- Windows Media Format SDK, pixel non quadrati
- Windows Media Format SDK, pixel (non quadrato)
- Formato di sistemi avanzati (ASF), scrittura di flussi video
- ASF (Advanced Systems Format), scrittura di flussi video
- Formati di sistemi avanzati (ASF), flussi video
- ASF (Advanced Systems Format), flussi video
- Formato di sistemi avanzati (ASF), pixel non quadrati
- ASF (formato avanzato dei sistemi), pixel non quadrati
- Formato di sistemi avanzati (ASF), pixel (non quadrato)
- ASF (formato avanzato dei sistemi), pixel (non quadrato)
- scrittura di flussi video
- flussi video, scrittura
- flussi video, pixel non quadrati
- pixel non quadrati
- pixel (non quadrato)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046301"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="218a4-120">Scrittura di flussi con pixel non quadrati</span><span class="sxs-lookup"><span data-stu-id="218a4-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="218a4-121">Esistono due modi per creare flussi video con pixel non quadrati che verranno visualizzati correttamente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="218a4-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="218a4-122">La prima tecnica consiste nell'impostare gli attributi a livello di flusso nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="218a4-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="218a4-123">La seconda tecnica prevede l'aggiunta di un'estensione di unità dati a un flusso nel profilo e quindi l'impostazione di un valore per esso in ogni esempio scritto.</span><span class="sxs-lookup"><span data-stu-id="218a4-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="218a4-124">Per usare gli attributi di intestazione a livello di flusso per impostare le proporzioni in pixel</span><span class="sxs-lookup"><span data-stu-id="218a4-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="218a4-125">Configurare l'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="218a4-125">Set up the writer object.</span></span> <span data-ttu-id="218a4-126">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="218a4-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="218a4-127">Creare o caricare un profilo con uno o più flussi video.</span><span class="sxs-lookup"><span data-stu-id="218a4-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="218a4-128">Per ulteriori informazioni, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="218a4-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="218a4-129">Chiamare [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="218a4-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="218a4-130">Chiamare sempre questo metodo prima di impostare gli attributi di intestazione.</span><span class="sxs-lookup"><span data-stu-id="218a4-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="218a4-131">Chiamare **QueryInterface** per ottenere l'interfaccia [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) e chiamare [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) due volte per aggiungere [**AspectRatioX**](aspectratiox.md) e [**AspectRatioY**](aspectratioy.md) come attributi a livello di flusso del flusso video.</span><span class="sxs-lookup"><span data-stu-id="218a4-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="218a4-132">Questi attributi sono valori **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="218a4-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="218a4-133">Scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="218a4-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="218a4-134">Per utilizzare le estensioni dell'unità dati per impostare le proporzioni in pixel</span><span class="sxs-lookup"><span data-stu-id="218a4-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="218a4-135">**Prima della scrittura:**</span><span class="sxs-lookup"><span data-stu-id="218a4-135">**Before writing:**</span></span>

1.  <span data-ttu-id="218a4-136">Configurare l'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="218a4-136">Set up the writer object.</span></span> <span data-ttu-id="218a4-137">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="218a4-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="218a4-138">Creare o caricare un profilo con uno o più flussi video.</span><span class="sxs-lookup"><span data-stu-id="218a4-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="218a4-139">Per ulteriori informazioni, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="218a4-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="218a4-140">Per ogni flusso (di qualsiasi tipo di supporto) nel profilo, chiamare [**IWMStreamConfig:: Sestreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) per specificare un nome univoco a scelta.</span><span class="sxs-lookup"><span data-stu-id="218a4-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="218a4-141">Non assegnare a due flussi lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="218a4-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="218a4-142">Usare [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) nel flusso video per aggiungere un'estensione dell'unità dati per le proporzioni in pixel.</span><span class="sxs-lookup"><span data-stu-id="218a4-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="218a4-143">Chiamare [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="218a4-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="218a4-144">Scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="218a4-144">Write the file.</span></span>

<span data-ttu-id="218a4-145">**Durante la scrittura:**</span><span class="sxs-lookup"><span data-stu-id="218a4-145">**While writing:**</span></span>

-   <span data-ttu-id="218a4-146">Per ogni esempio, chiamare [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) e specificare la proprietà WM \_ SampleExtensionGUID \_ PixelAspectRatio insieme al valore corretto.</span><span class="sxs-lookup"><span data-stu-id="218a4-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="218a4-147">I valori delle proporzioni vengono scritti come due valori concatenati a due cifre.</span><span class="sxs-lookup"><span data-stu-id="218a4-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="218a4-148">16:9, ad esempio, viene scritto come 1609 o 0x0649.</span><span class="sxs-lookup"><span data-stu-id="218a4-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="218a4-149">Si tratta sempre di un valore a 2 byte.</span><span class="sxs-lookup"><span data-stu-id="218a4-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="218a4-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="218a4-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="218a4-151">**Per leggere e scrivere flussi video con pixel non quadrati**</span><span class="sxs-lookup"><span data-stu-id="218a4-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




