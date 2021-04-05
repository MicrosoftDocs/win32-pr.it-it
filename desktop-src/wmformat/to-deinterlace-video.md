---
title: Per deinterlacciare il video
description: Per deinterlacciare il video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media Format SDK, Video deinterlacciato
- Windows Media Format SDK, telecine inversa
- Windows Media Format SDK, telecine
- ASF (Advanced Systems Format), Video deinterlacciato
- ASF (Advanced Systems Format), Video deinterlacciato
- ASF (Advanced Systems Format), telecine inversa
- ASF (formato avanzato dei sistemi), telecine inversa
- Formato di sistemi avanzati (ASF), telecine
- ASF (formato avanzato dei sistemi), telecine
- Video deinterlacciato
- Telecine inversa, informazioni
- telecine, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046322"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="f85b8-115">Per deinterlacciare il video</span><span class="sxs-lookup"><span data-stu-id="f85b8-115">To Deinterlace Video</span></span>

<span data-ttu-id="f85b8-116">Alcune origini di video, ad esempio schede di acquisizione video, forniscono dati video per la visualizzazione interlacciata.</span><span class="sxs-lookup"><span data-stu-id="f85b8-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="f85b8-117">Ogni frame di video interlacciato è costituito da due campi.</span><span class="sxs-lookup"><span data-stu-id="f85b8-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="f85b8-118">Il campo superiore contiene la prima riga di video e ogni altra riga successiva.</span><span class="sxs-lookup"><span data-stu-id="f85b8-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="f85b8-119">Il campo inferiore contiene la seconda riga di video e ogni altra riga successiva.</span><span class="sxs-lookup"><span data-stu-id="f85b8-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="f85b8-120">Un campo contiene quindi tutte le righe numerate pari e l'altra contiene tutte le righe numerate dispari.</span><span class="sxs-lookup"><span data-stu-id="f85b8-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="f85b8-121">I campi che costituiscono un frame rappresentano tempi di presentazione leggermente diversi, in modo che, in caso di interfoliazione, non formino un'immagine statica.</span><span class="sxs-lookup"><span data-stu-id="f85b8-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="f85b8-122">Quando si desidera visualizzare il video in un monitor del computer, ogni frame del video deve essere visualizzato come un'immagine (questo metodo di visualizzazione di un intero frame alla volta è denominato video *progressivo* ). Se si visualizza progressivamente il video interlacciato, i frame potrebbero non essere corretti, a causa della differenza di tempo tra i due campi.</span><span class="sxs-lookup"><span data-stu-id="f85b8-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="f85b8-123">Il codec Windows Media Video e il codec del profilo avanzato Windows Media Video supportano entrambe una funzionalità di pre-elaborazione che converte il contenuto interlacciato in frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="f85b8-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="f85b8-124">Per avere il video di input deinterlacciamento codec, chiamare il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) .</span><span class="sxs-lookup"><span data-stu-id="f85b8-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="f85b8-125">L'impostazione da usare è g \_ wszDeinterlaceMode.</span><span class="sxs-lookup"><span data-stu-id="f85b8-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="f85b8-126">Impostare la modalità di deinterlacciamento su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f85b8-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f85b8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="f85b8-127">Value</span></span></th>
<th><span data-ttu-id="f85b8-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f85b8-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f85b8-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="f85b8-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="f85b8-130">L'input è progressivo.</span><span class="sxs-lookup"><span data-stu-id="f85b8-130">Input is progressive.</span></span> <span data-ttu-id="f85b8-131">Usare questa impostazione per arrestare il deinterlacciamento se in precedenza è stata impostata la modalità di deinterlacciamento su un altro valore.</span><span class="sxs-lookup"><span data-stu-id="f85b8-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85b8-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="f85b8-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="f85b8-133">Selezionare questa modalità per combinare i campi pari e dispari di un frame interlacciato (usando un meccanismo di compensazione movimento). Vantaggi</span><span class="sxs-lookup"><span data-stu-id="f85b8-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="f85b8-134">Gli artefatti di interlacciamento della visualizzazione progressiva sono notevolmente ridotti.</span><span class="sxs-lookup"><span data-stu-id="f85b8-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="f85b8-135">Il codec Windows Media Video produce video compressi di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="f85b8-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f85b8-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="f85b8-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="f85b8-137">Selezionare questa modalità quando la risoluzione dell'output è metà o minore della risoluzione di input.</span><span class="sxs-lookup"><span data-stu-id="f85b8-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="f85b8-138">Usare, ad esempio, questa modalità quando la risoluzione del video di input è 640 x 480 pixel e la risoluzione del video di output è 320 x 240 pixel. Vantaggi</span><span class="sxs-lookup"><span data-stu-id="f85b8-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="f85b8-139">Gli artefatti di interlacciamento della visualizzazione progressiva sono notevolmente ridotti.</span><span class="sxs-lookup"><span data-stu-id="f85b8-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85b8-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="f85b8-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="f85b8-141">Selezionare questa modalità quando la risoluzione dell'output è metà o minore della risoluzione di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore.</span><span class="sxs-lookup"><span data-stu-id="f85b8-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="f85b8-142">Usare, ad esempio, questa modalità quando la risoluzione del video di input è 640 x 480 pixel a 30 frame interlacciati/sec e la risoluzione del video di output è 320 x 240 pixel a 60 frame/sec. Vantaggi</span><span class="sxs-lookup"><span data-stu-id="f85b8-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="f85b8-143">Questo produce frame progressivi di elevata qualità, perché ogni campo viene convertito in un frame e pertanto non è necessario combinare alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="f85b8-144">Viene acquisito il movimento completo dei campi interlacciati.</span><span class="sxs-lookup"><span data-stu-id="f85b8-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f85b8-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="f85b8-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="f85b8-146">Selezionare questa modalità per convertire il video di 30 fotogrammi/sec telecine in 24 fotogrammi al secondo della pellicola originale. Vantaggi</span><span class="sxs-lookup"><span data-stu-id="f85b8-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="f85b8-147">La qualità della compressione migliora significativamente perché solo 24 frame al secondo anziché 30 fotogrammi/sec devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="f85b8-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="f85b8-148">Poiché il risultato è progressivo, vengono realizzati gli stessi vantaggi di compressione e visualizzazione della deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="f85b8-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f85b8-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="f85b8-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="f85b8-150">Selezionare questa modalità quando la risoluzione dell'output verticale è metà o minore della risoluzione verticale di input e la frequenza dei <a href="wmformat-glossary.md"><em>fotogrammi</em></a> di output è due volte superiore.</span><span class="sxs-lookup"><span data-stu-id="f85b8-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="f85b8-151">Ad esempio, la risoluzione video verticale di input è 640 x 480 pixel a 30 fotogrammi interlacciati/sec e la risoluzione video verticale di output è 320 x 240 pixel a 60 frame/sec. Vantaggi</span><span class="sxs-lookup"><span data-stu-id="f85b8-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="f85b8-152">Questo produce frame progressivi di elevata qualità, perché ogni campo viene convertito in un frame e pertanto non è necessario combinare alcuna informazione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="f85b8-153">Viene acquisito il movimento completo dei campi interlacciati.</span><span class="sxs-lookup"><span data-stu-id="f85b8-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="f85b8-154">Per il contenuto misto, impostare la modalità di deinterlacciamento in base alle esigenze prima di passare campioni di un nuovo tipo.</span><span class="sxs-lookup"><span data-stu-id="f85b8-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="f85b8-155">Ad esempio, per avviare la codifica con input progressivo, non è necessario impostare alcuna modalità di deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="f85b8-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="f85b8-156">Se alcuni esempi richiedono il normale deinterlacciamento, è necessario impostare la modalità di deinterlacciamento su WM \_ DM \_ Deinterlaccia \_ Normal.</span><span class="sxs-lookup"><span data-stu-id="f85b8-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="f85b8-157">Per elaborare gli esempi progressivi aggiuntivi è necessario impostare la modalità di deinterlacciamento su WM \_ DM \_ NOTINTERLACED.</span><span class="sxs-lookup"><span data-stu-id="f85b8-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="f85b8-158">Impostazioni di telecine inverse</span><span class="sxs-lookup"><span data-stu-id="f85b8-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="f85b8-159">Per una descrizione della telecine, vedere [per usare la telecine inversa](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="f85b8-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="f85b8-160">Se si imposta la modalità di deinterlacciamento su WM \_ DM \_ Deinterlaccia \_ INVERSETELECINE, è possibile specificare il modello di telecine del primo frame di input chiamando [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="f85b8-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="f85b8-161">L'impostazione da usare è g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="f85b8-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="f85b8-162">Impostare il criterio iniziale su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f85b8-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="f85b8-163">Valore</span><span class="sxs-lookup"><span data-stu-id="f85b8-163">Value</span></span>                                              | <span data-ttu-id="f85b8-164">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f85b8-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f85b8-165">WM \_ DM \_ \_ Disabilita la \_ \_ modalità coerente</span><span class="sxs-lookup"><span data-stu-id="f85b8-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="f85b8-166">Specifica che i supporti di input sono passati attraverso il processo di telecine, ma che i frame non sono più in uno schema stimabile.</span><span class="sxs-lookup"><span data-stu-id="f85b8-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="f85b8-167">Questo in genere indica che il supporto è stato modificato dopo l'elaborazione del telecine.</span><span class="sxs-lookup"><span data-stu-id="f85b8-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="f85b8-168">Quando si usa questa impostazione, il codec tenta di ricostruire i frame originali in modo autonomo.</span><span class="sxs-lookup"><span data-stu-id="f85b8-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="f85b8-169">WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è \_ AA \_ Top</span><span class="sxs-lookup"><span data-stu-id="f85b8-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="f85b8-170">Specifica che il campo superiore del frame AA è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="f85b8-171">il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ BB \_ Top</span><span class="sxs-lookup"><span data-stu-id="f85b8-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="f85b8-172">Specifica che il campo superiore del fotogramma BB è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="f85b8-173">WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è \_ BC \_ Top</span><span class="sxs-lookup"><span data-stu-id="f85b8-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="f85b8-174">Specifica che il campo superiore del frame BC è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="f85b8-175">WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è un \_ CD- \_ Top</span><span class="sxs-lookup"><span data-stu-id="f85b8-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="f85b8-176">Specifica che il campo superiore del fotogramma CD è il primo esempio.</span><span class="sxs-lookup"><span data-stu-id="f85b8-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="f85b8-177">il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ DD \_ Top</span><span class="sxs-lookup"><span data-stu-id="f85b8-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="f85b8-178">Specifica che il campo superiore del frame DD è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="f85b8-179">WM \_ DM \_ il \_ primo \_ frame \_ nel \_ clip \_ è \_ AA \_ inferiore</span><span class="sxs-lookup"><span data-stu-id="f85b8-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="f85b8-180">Specifica che il campo inferiore del frame AA è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="f85b8-181">il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è BB in \_ \_ basso</span><span class="sxs-lookup"><span data-stu-id="f85b8-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="f85b8-182">Specifica che il campo inferiore del frame BB è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="f85b8-183">il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ BC \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="f85b8-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="f85b8-184">Specifica che il campo inferiore del frame BC è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="f85b8-185">WM \_ DM \_ it \_ First \_ frame \_ in \_ clip \_ è un \_ CD \_ inferiore</span><span class="sxs-lookup"><span data-stu-id="f85b8-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="f85b8-186">Specifica che il campo inferiore del fotogramma CD è il primo esempio.</span><span class="sxs-lookup"><span data-stu-id="f85b8-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="f85b8-187">il \_ \_ \_ primo frame di WM DM it \_ \_ nel \_ clip \_ è \_ DD \_ inferiore</span><span class="sxs-lookup"><span data-stu-id="f85b8-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="f85b8-188">Specifica che il campo inferiore del frame DD è il primo campione.</span><span class="sxs-lookup"><span data-stu-id="f85b8-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="f85b8-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f85b8-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85b8-190">**Argomenti avanzati**</span><span class="sxs-lookup"><span data-stu-id="f85b8-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





