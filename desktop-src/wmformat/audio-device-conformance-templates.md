---
title: Modelli di conformità del dispositivo audio
description: Modelli di conformità del dispositivo audio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media Format SDK, modelli di conformità del dispositivo
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- ASF (Advanced Systems Format), modelli di conformità dei dispositivi
- Windows Media Format SDK, modelli di conformità del dispositivo audio
- Modelli di conformità dei sistemi avanzati (ASF), modelli di conformità dei dispositivi audio
- ASF (formato avanzato dei sistemi), modelli di conformità del dispositivo audio
- Windows Media Audio 9 codec, modelli di conformità del dispositivo audio
- codec, Windows Media Audio 9 codec
- modelli di conformità del dispositivo, video
- modelli di conformità del dispositivo audio
- modelli, modelli di conformità dei dispositivi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329895"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="7e496-114">Modelli di conformità del dispositivo audio</span><span class="sxs-lookup"><span data-stu-id="7e496-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="7e496-115">La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7e496-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="7e496-116">Stringa modello</span><span class="sxs-lookup"><span data-stu-id="7e496-116">Template string</span></span> | <span data-ttu-id="7e496-117">Intervallo di velocità in bit</span><span class="sxs-lookup"><span data-stu-id="7e496-117">Bit rate range</span></span>     | <span data-ttu-id="7e496-118">Note</span><span class="sxs-lookup"><span data-stu-id="7e496-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e496-119">L1</span><span class="sxs-lookup"><span data-stu-id="7e496-119">"L1"</span></span>            | <span data-ttu-id="7e496-120">64 Kbps 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="7e496-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="7e496-121">Questo modello è destinato a dispositivi solo audio vincolati.</span><span class="sxs-lookup"><span data-stu-id="7e496-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="7e496-122">L2</span><span class="sxs-lookup"><span data-stu-id="7e496-122">"L2"</span></span>            | <span data-ttu-id="7e496-123"><= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="7e496-123"><= 160 Kbps</span></span>     | <span data-ttu-id="7e496-124">Questo modello corrisponde alla classe 4 nel Windows Media Audio Porting Kit, che supporta l'intera implementazione del decodificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="7e496-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="7e496-125">L3</span><span class="sxs-lookup"><span data-stu-id="7e496-125">"L3"</span></span>            | <span data-ttu-id="7e496-126"><= 384 kbps</span><span class="sxs-lookup"><span data-stu-id="7e496-126"><= 384 Kbps</span></span>     | <span data-ttu-id="7e496-127">Questo modello corrisponde alla classe 4 nel Windows Media Audio Porting Kit, che supporta l'intera implementazione del decodificatore Windows Media Audio. L'intervallo della velocità in bit è l'unica differenza tra questo modello e L2.</span><span class="sxs-lookup"><span data-stu-id="7e496-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="7e496-128">L</span><span class="sxs-lookup"><span data-stu-id="7e496-128">"L"</span></span>             | <span data-ttu-id="7e496-129">Tutte le velocità in bit</span><span class="sxs-lookup"><span data-stu-id="7e496-129">All bit rates</span></span>      | <span data-ttu-id="7e496-130">Questo modello è da usare solo con personal computer e viene in genere usato per presentare le funzionalità complete del codec.</span><span class="sxs-lookup"><span data-stu-id="7e496-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="7e496-131">La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Voice.</span><span class="sxs-lookup"><span data-stu-id="7e496-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="7e496-132">Stringa modello</span><span class="sxs-lookup"><span data-stu-id="7e496-132">Template string</span></span> | <span data-ttu-id="7e496-133">Intervallo di velocità in bit</span><span class="sxs-lookup"><span data-stu-id="7e496-133">Bit rate range</span></span> | <span data-ttu-id="7e496-134">Note</span><span class="sxs-lookup"><span data-stu-id="7e496-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e496-135">S1</span><span class="sxs-lookup"><span data-stu-id="7e496-135">"S1"</span></span>            | <span data-ttu-id="7e496-136"><= 20 kbps</span><span class="sxs-lookup"><span data-stu-id="7e496-136"><= 20 Kbps</span></span>  | <span data-ttu-id="7e496-137">Questo modello è destinato solo ai dispositivi con complessità molto bassa. Questo modello è solo sintesi vocale.</span><span class="sxs-lookup"><span data-stu-id="7e496-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="7e496-138">S2</span><span class="sxs-lookup"><span data-stu-id="7e496-138">"S2"</span></span>            | <span data-ttu-id="7e496-139"><= 20 kbps</span><span class="sxs-lookup"><span data-stu-id="7e496-139"><= 20 Kbps</span></span>  | <span data-ttu-id="7e496-140">Si tratta del modello consigliato per la maggior parte delle applicazioni. Questo modello supporta combinazioni di riconoscimento vocale e musica.</span><span class="sxs-lookup"><span data-stu-id="7e496-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="7e496-141">La tabella seguente elenca i modelli di conformità dei dispositivi e i parametri associati per il codec Windows Media Audio 9 Professional o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7e496-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="7e496-142">Stringa modello</span><span class="sxs-lookup"><span data-stu-id="7e496-142">Template string</span></span> | <span data-ttu-id="7e496-143">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7e496-143">Properties</span></span>                                                                                   | <span data-ttu-id="7e496-144">Note</span><span class="sxs-lookup"><span data-stu-id="7e496-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e496-145">M1</span><span class="sxs-lookup"><span data-stu-id="7e496-145">"M1"</span></span>            | <span data-ttu-id="7e496-146">Velocità in bit <= 384 velocità KbpsSampling <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="7e496-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="7e496-147">Canali <= 5,1</span><span class="sxs-lookup"><span data-stu-id="7e496-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="7e496-148">Questo modello è consigliato per i film standard con audio surround.</span><span class="sxs-lookup"><span data-stu-id="7e496-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="7e496-149">M2</span><span class="sxs-lookup"><span data-stu-id="7e496-149">"M2"</span></span>            | <span data-ttu-id="7e496-150">Velocità in bit <= 768 velocità KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="7e496-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="7e496-151">Canali <= 5,1</span><span class="sxs-lookup"><span data-stu-id="7e496-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="7e496-152">Questo modello è consigliato per i filmati ad alta definizione con audio surround.</span><span class="sxs-lookup"><span data-stu-id="7e496-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="7e496-153">M3</span><span class="sxs-lookup"><span data-stu-id="7e496-153">"M3"</span></span>            | <span data-ttu-id="7e496-154">Velocità in bit <= 1.500 velocità KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="7e496-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="7e496-155">Canali <= 7,1</span><span class="sxs-lookup"><span data-stu-id="7e496-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="7e496-156">Questo modello è consigliato per i filmati ad alta definizione con audio surround a 8 canali, ad esempio il contenuto codificato per la presentazione nei teatri.</span><span class="sxs-lookup"><span data-stu-id="7e496-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="7e496-157">"M"</span><span class="sxs-lookup"><span data-stu-id="7e496-157">"M"</span></span>             | <span data-ttu-id="7e496-158">Tutte le frequenze di campionamento ratesAll bit</span><span class="sxs-lookup"><span data-stu-id="7e496-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="7e496-159">Tutti i canali</span><span class="sxs-lookup"><span data-stu-id="7e496-159">All channels</span></span><br/>                           | <span data-ttu-id="7e496-160">Questo modello è da usare solo con personal computer e viene in genere usato per presentare le funzionalità complete del codec. Si tratta anche della designazione del modello per tutti gli audio codificati con il codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="7e496-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7e496-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e496-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e496-162">**Parametri del modello di conformità del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="7e496-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="7e496-163">**Combinazioni consigliate per il modello di conformità dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="7e496-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="7e496-164">**Modelli di conformità del dispositivo video**</span><span class="sxs-lookup"><span data-stu-id="7e496-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





