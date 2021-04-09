---
title: Per usare un video interlacciato
description: Per usare un video interlacciato
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK, video interlacciato
- Windows Media Format SDK, codifica video interlacciata
- Windows Media Format SDK, codifica video interlacciato
- Windows Media Format SDK, decodifica video interlacciato
- Windows Media Format SDK, ordine dei campi
- ASF (Advanced Systems Format), video interlacciato
- ASF (Advanced Systems Format), video interlacciato
- ASF (Advanced Systems Format), codifica video interlacciata
- ASF (Advanced Systems Format), codifica video interlacciata
- ASF (Advanced Systems Format), codifica di video interlacciati
- ASF (Advanced Systems Format), codifica video interlacciato
- ASF (Advanced Systems Format), decodifica video interlacciato
- ASF (Advanced Systems Format), decodifica video interlacciato
- ASF (Advanced Systems Format), ordine dei campi
- ASF (formato avanzato dei sistemi), ordine dei campi
- video interlacciato, informazioni
- video interlacciato, codifica
- video interlacciato, decodifica
- video interlacciato, ordine dei campi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858014"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="ca95e-122">Per usare un video interlacciato</span><span class="sxs-lookup"><span data-stu-id="ca95e-122">To Use Interlaced Video</span></span>

<span data-ttu-id="ca95e-123">Sono disponibili due tipi di codifica video di base: progressivo e interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ca95e-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="ca95e-124">Nella codifica progressiva ogni frame è una rappresentazione codificata di un frame di video.</span><span class="sxs-lookup"><span data-stu-id="ca95e-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="ca95e-125">Nella codifica interlacciata ogni frame è una rappresentazione codificata di tutte le righe pari di pixel nel video o di tutte le righe dispari.</span><span class="sxs-lookup"><span data-stu-id="ca95e-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="ca95e-126">Ogni frame interlacciato è denominato *campo*, quindi sono presenti campi dispari e persino campi.</span><span class="sxs-lookup"><span data-stu-id="ca95e-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="ca95e-127">Una visualizzazione interlacciata (ad esempio un televisore) esegue il rendering dei campi uno alla volta, alternando i campi.</span><span class="sxs-lookup"><span data-stu-id="ca95e-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="ca95e-128">Una visualizzazione progressiva esegue il rendering di tutti i frame contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="ca95e-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="ca95e-129">Il codec del profilo avanzato Windows Media Video 9 fornisce supporto per la gestione dell'interlacciamento nei flussi compressi.</span><span class="sxs-lookup"><span data-stu-id="ca95e-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="ca95e-130">Quando usare un video interlacciato</span><span class="sxs-lookup"><span data-stu-id="ca95e-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="ca95e-131">Codifica video interlacciato è utile solo quando il contenuto viene visualizzato in un dispositivo interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ca95e-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="ca95e-132">Il contenuto che deve essere visualizzato in un televisore (tramite un set-top box o un altro dispositivo) potrebbe dover essere interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ca95e-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="ca95e-133">Il contenuto che deve essere visualizzato esclusivamente in uno schermo del computer non deve essere codificato come interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ca95e-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="ca95e-134">Per codificare video interlacciato come video progressivo, è necessario configurare le impostazioni di input.</span><span class="sxs-lookup"><span data-stu-id="ca95e-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="ca95e-135">Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="ca95e-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="ca95e-136">Ordine campi</span><span class="sxs-lookup"><span data-stu-id="ca95e-136">Field Order</span></span>

<span data-ttu-id="ca95e-137">La maggior parte delle origini di video interlacciati, ad esempio schede di acquisizione video, fornisce esempi video che includono entrambi i campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="ca95e-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="ca95e-138">Il risultato è simile a un frame completo di video, ad eccezione del fatto che le linee dispari e pari vengono spostate leggermente nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="ca95e-139">Non è disponibile alcun standard universale per il campo nell'esempio video interleaved che si verifica prima nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="ca95e-140">È necessario consentire agli utenti di specificare l'ordine dei campi quando si passano esempi interlacciati all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ca95e-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="ca95e-141">Codifica video interlacciato</span><span class="sxs-lookup"><span data-stu-id="ca95e-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="ca95e-142">Per usare la codifica interlacciata, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="ca95e-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="ca95e-143">Configurare il flusso video nel profilo in modo che usi l'estensione dell'unità dati del tipo di contenuto chiamando il metodo [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="ca95e-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="ca95e-144">Il GUID dell'estensione di esempio per l'estensione del tipo di contenuto è WM \_ SampleExtensionsGUID \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="ca95e-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="ca95e-145">Impostare il flusso nel profilo e configurare il writer con il profilo come normale.</span><span class="sxs-lookup"><span data-stu-id="ca95e-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="ca95e-146">Prima di passare gli esempi interlacciati al writer, chiamare il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per impostare l' \_ impostazione di input g wszInterlacedCoding su **true**.</span><span class="sxs-lookup"><span data-stu-id="ca95e-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="ca95e-147">Per ogni campione interlacciato passato al writer, chiamare il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare il tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="ca95e-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="ca95e-148">I valori del tipo di contenuto sono combinazioni dei flag nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ca95e-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="ca95e-149">Flag</span><span class="sxs-lookup"><span data-stu-id="ca95e-149">Flag</span></span>                         | <span data-ttu-id="ca95e-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca95e-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca95e-151">\_INTERlacciato WM CT \_</span><span class="sxs-lookup"><span data-stu-id="ca95e-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="ca95e-152">Impostare sempre questo flag quando si codifica il contenuto interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ca95e-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="ca95e-153">Se si usa questo flag senza impostare un flag per l'ordine dei campi (primo campo di WM \_ CT in \_ basso \_ o primo \_ \_ campo WM CT \_ Top \_ \_ ), il codec presuppone che il campo superiore sia primo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="ca95e-154">Se il codec usa l'ordine dei campi errato, non dovrebbe avere alcun impatto sulla qualità dell'immagine, ma l'efficienza della codifica sarà interessata.</span><span class="sxs-lookup"><span data-stu-id="ca95e-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="ca95e-155">\_primo campo WM CT in \_ basso \_ \_</span><span class="sxs-lookup"><span data-stu-id="ca95e-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="ca95e-156">In combinazione con il \_ \_ flag interlacciato WM CT, questo flag indica che il campo inferiore (il campo che inizia con la seconda riga nell'esempio) si verifica prima nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="ca95e-157">\_ \_ \_ primo campo WM CT \_ Top</span><span class="sxs-lookup"><span data-stu-id="ca95e-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="ca95e-158">In combinazione con il \_ \_ flag interlacciato WM CT, questo flag indica che il campo superiore (il campo che inizia con la prima riga dell'esempio) si verifica prima nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="ca95e-159">\_ \_ \_ primo \_ campo per la ripetizione del CT WM</span><span class="sxs-lookup"><span data-stu-id="ca95e-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="ca95e-160">Indica che il primo campo dell'esempio deve essere ripetuto durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="ca95e-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="ca95e-161">Questo flag viene usato per i video creati da film dal processo di telecine. Se non viene impostato alcun flag di ordine dei campi insieme a questo flag, si presuppone che il campo superiore si verifichi prima nel tempo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="ca95e-162">Se il \_ \_ flag di WM CT interlacciato non è impostato, si presuppone che l'esempio contenga un frame video progressivo.</span><span class="sxs-lookup"><span data-stu-id="ca95e-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="ca95e-163">Decodifica video interlacciato</span><span class="sxs-lookup"><span data-stu-id="ca95e-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="ca95e-164">Quando si decodifica il video interlacciato, è necessario impostare l' \_ impostazione g wszAllowInterlacedOutput su **true** usando il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="ca95e-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="ca95e-165">In caso contrario, il codec fornirà frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="ca95e-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="ca95e-166">L'estensione dell'unità dati del tipo di contenuto viene mantenuta negli esempi di output.</span><span class="sxs-lookup"><span data-stu-id="ca95e-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="ca95e-167">È necessario passare l'orientamento del campo al dispositivo di rendering per garantire la riproduzione corretta.</span><span class="sxs-lookup"><span data-stu-id="ca95e-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca95e-168">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ca95e-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca95e-169">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="ca95e-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





