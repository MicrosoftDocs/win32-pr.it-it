---
title: Impostazioni di input
description: Impostazioni di input
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK, costanti globali
- Advanced Systems Format (ASF), costanti globali
- ASF (formato avanzato dei sistemi), costanti globali
- costanti globali, elenco di
- Windows Media Format SDK, costanti
- Advanced Systems Format (ASF), costanti
- ASF (formato avanzato dei sistemi), costanti
- costanti, elenco di
- Windows Media Format SDK, impostazioni di input
- ASF (Advanced Systems Format), impostazioni di input
- ASF (formato avanzato dei sistemi), impostazioni di input
- impostazioni di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046275"
---
# <a name="input-settings"></a><span data-ttu-id="ba7ed-115">Impostazioni di input</span><span class="sxs-lookup"><span data-stu-id="ba7ed-115">Input Settings</span></span>

<span data-ttu-id="ba7ed-116">Le costanti globali seguenti vengono utilizzate per identificare le impostazioni di input per il writer.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="ba7ed-117">Costante globale</span><span class="sxs-lookup"><span data-stu-id="ba7ed-117">Global constant</span></span>                        | <span data-ttu-id="ba7ed-118">tipo di dati \_ attr WMT \_</span><span class="sxs-lookup"><span data-stu-id="ba7ed-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="ba7ed-119">Descrizione di *pValue*</span><span class="sxs-lookup"><span data-stu-id="ba7ed-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba7ed-120">g \_ wszDeinterlaceMode</span><span class="sxs-lookup"><span data-stu-id="ba7ed-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="ba7ed-121">**WMT \_ Digitare \_ DWORD** impostato su uno dei valori nella tabella modalità nell'argomento [per deinterlacciare il video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ed-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="ba7ed-122">Se impostato, specifica il tipo di contenuto interlacciato dell'input.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="ba7ed-123">Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ed-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="ba7ed-124">g \_ wszFixedFrameRate</span><span class="sxs-lookup"><span data-stu-id="ba7ed-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="ba7ed-125">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="ba7ed-126">Se impostato su true, indica al codec di non eliminare i frame durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="ba7ed-127">In questo modo la [*frequenza dei fotogrammi*](wmformat-glossary.md) del flusso video di output sarà costante.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="ba7ed-128">Non è necessario che la frequenza dei fotogrammi del flusso di input sia costante.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="ba7ed-129">g \_ wszInitialPatternForInverseTelecine</span><span class="sxs-lookup"><span data-stu-id="ba7ed-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="ba7ed-130">**WMT \_ Digitare \_ DWORD** impostato su uno dei valori nella tabella dei criteri iniziali nell'argomento [per deinterlacciare il video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ed-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="ba7ed-131">Quando la modalità di deinterlacciamento è impostata su WM \_ DM \_ deinterlacciare \_ INVERSETELECINE, questo può essere impostato per specificare il modello di input di [*telecine*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="ba7ed-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="ba7ed-132">Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ed-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="ba7ed-133">g \_ wszInterlacedCoding</span><span class="sxs-lookup"><span data-stu-id="ba7ed-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="ba7ed-134">**\_tipo WMT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="ba7ed-135">Se impostato su true, specifica che il codec deve codificare il flusso come contenuto interlacciato.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="ba7ed-136">Per altre informazioni, vedere [per usare un video interlacciato](to-use-interlaced-video.md).</span><span class="sxs-lookup"><span data-stu-id="ba7ed-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="ba7ed-137">g \_ wszJPEGCompressionQuality</span><span class="sxs-lookup"><span data-stu-id="ba7ed-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="ba7ed-138">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="ba7ed-139">Specifica il livello di qualità JPEG (da 1 a 100) da usare per l'input.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="ba7ed-140">g \_ wszWatermarkCLSID</span><span class="sxs-lookup"><span data-stu-id="ba7ed-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="ba7ed-141">**\_GUID di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="ba7ed-142">Il valore viene impostato sul GUID della filigrana.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="ba7ed-143">g \_ wszWatermarkConfig</span><span class="sxs-lookup"><span data-stu-id="ba7ed-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="ba7ed-144">**\_stringa di tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="ba7ed-145">Il valore viene impostato sulla configurazione della filigrana.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="ba7ed-146">Questo valore varia in base al limite DMO.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="ba7ed-147">Per ulteriori informazioni, consultare la documentazione del sistema di filigrana.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="ba7ed-148">Le impostazioni di input configurate per un flusso non sono salvate in modo permanente nel file scritto.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="ba7ed-149">Se si vuole che il lettore personalizzato abbia accesso a questi parametri di codifica, è necessario creare attributi personalizzati per archiviarli nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="ba7ed-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ba7ed-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ba7ed-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba7ed-151">**IWMWriterAdvanced2::GetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="ba7ed-152">**IWMWriterAdvanced2::SetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="ba7ed-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




