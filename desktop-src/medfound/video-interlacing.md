---
description: Interlacciamento video
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Interlacciamento video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308976"
---
# <a name="video-interlacing"></a><span data-ttu-id="12f31-103">Interlacciamento video</span><span class="sxs-lookup"><span data-stu-id="12f31-103">Video Interlacing</span></span>

<span data-ttu-id="12f31-104">Questo argomento descrive come le origini e i decodificatori multimediali devono gestire il contenuto video interlacciato.</span><span class="sxs-lookup"><span data-stu-id="12f31-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="12f31-105">Per decodificare e visualizzare correttamente il video interlacciato, sono necessarie le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="12f31-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="12f31-106">Progressivo o interlacciato.</span><span class="sxs-lookup"><span data-stu-id="12f31-106">Progressive or interlaced.</span></span> <span data-ttu-id="12f31-107">Un flusso video può contenere frame progressivi, frame interlacciati o una combinazione di entrambi.</span><span class="sxs-lookup"><span data-stu-id="12f31-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="12f31-108">Dominanza del campo.</span><span class="sxs-lookup"><span data-stu-id="12f31-108">Field dominance.</span></span> <span data-ttu-id="12f31-109">La dominanza dei campi descrive il campo che viene visualizzato per primo, il campo superiore o il campo inferiore.</span><span class="sxs-lookup"><span data-stu-id="12f31-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="12f31-110">Ripetere il primo campo.</span><span class="sxs-lookup"><span data-stu-id="12f31-110">Repeat first field.</span></span> <span data-ttu-id="12f31-111">Questo flag viene usato nel riquadro a discesa 3:2, quando il frame è progressivo, ma il flusso è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="12f31-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="12f31-112">In questo contesto, il primo campo può essere il campo superiore o inferiore.</span><span class="sxs-lookup"><span data-stu-id="12f31-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="12f31-113">Campi con interfoliazione o campo singolo.</span><span class="sxs-lookup"><span data-stu-id="12f31-113">Interleaved fields or single field.</span></span> <span data-ttu-id="12f31-114">Un esempio può essere costituito da un singolo campo o da due campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="12f31-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="12f31-115">Se un esempio contiene un solo campo, l'altezza del campione è metà dell'altezza del fotogramma, perché l'esempio contiene solo metà delle righe di analisi per un frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="12f31-116">I campi con interfoliazione sono consigliati, a meno che le caratteristiche del contenuto di origine non impongano in altro modo.</span><span class="sxs-lookup"><span data-stu-id="12f31-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="12f31-117">Ognuna di queste caratteristiche può variare da un campione a quello successivo.</span><span class="sxs-lookup"><span data-stu-id="12f31-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="12f31-118">Tuttavia, i componenti video devono conoscere il contenuto complessivo prima che lo streaming venga avviato.</span><span class="sxs-lookup"><span data-stu-id="12f31-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="12f31-119">Se ad esempio il video è interlacciato, il renderer video avanzato (EVR) deve riservare memoria video per il deinterlacciamento.</span><span class="sxs-lookup"><span data-stu-id="12f31-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="12f31-120">Se il video è costituito da frame completamente progressivi, invece, il EVR può ottimizzare la pipeline di rendering.</span><span class="sxs-lookup"><span data-stu-id="12f31-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="12f31-121">L'aggiunta di un passaggio di deinterlacciamento alla pipeline comporta un aumento della latenza di rendering.</span><span class="sxs-lookup"><span data-stu-id="12f31-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="12f31-122">Le informazioni sul interlacciamento sono archiviate in due posizioni:</span><span class="sxs-lookup"><span data-stu-id="12f31-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="12f31-123">Le informazioni generali sull'interlacciamento in un flusso vengono inserite nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="12f31-124">Per ulteriori informazioni sui tipi di supporto, vedere [tipi di supporti](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="12f31-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="12f31-125">Le informazioni che possono essere modificate con ciascun campione vengono inserite nell'esempio come attributo.</span><span class="sxs-lookup"><span data-stu-id="12f31-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="12f31-126">Per ulteriori informazioni sugli esempi, vedere [esempi di supporti](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="12f31-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="12f31-127">Informazioni interlacciate nel tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="12f31-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="12f31-128">L' [**attributo \_ \_ \_ modalità di interpolazione MF mt**](mf-mt-interlace-mode-attribute.md) sul tipo di supporto descrive il modo in cui il flusso nel suo complesso è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="12f31-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="12f31-129">Il valore di questo attributo è un membro dell'enumerazione [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="12f31-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="12f31-130">Un tipo di supporto video deve sempre avere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="12f31-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="12f31-131">Se il flusso contiene solo frame progressivi, senza frame interlacciati, usare MFVideoInterlace \_ progressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="12f31-132">Se il flusso contiene solo frame interlacciati e ogni esempio contiene due campi con interfoliazione, usare MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="12f31-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="12f31-133">Se il flusso contiene solo frame interlacciati e ogni esempio contiene un solo campo, usare MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="12f31-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="12f31-134">Se i campi si alternano tra maiuscole e minuscole, non è importante quale di questi due valori venga usato.</span><span class="sxs-lookup"><span data-stu-id="12f31-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="12f31-135">Se il formato contiene solo campi superiori o solo i campi inferiore, impostare il valore corrispondente al contenuto.</span><span class="sxs-lookup"><span data-stu-id="12f31-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="12f31-136">Se il flusso contiene una combinazione di frame interlacciati e progressivi o se il valore di dominanza del campo cambia, impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="12f31-137">Usare gli attributi di esempio per descrivere ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="12f31-138">Nella tabella seguente viene riepilogato questo attributo.</span><span class="sxs-lookup"><span data-stu-id="12f31-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="12f31-139">\_modalità di \_ intreccio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="12f31-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="12f31-140">Interlacciate?</span><span class="sxs-lookup"><span data-stu-id="12f31-140">Interlaced?</span></span> | <span data-ttu-id="12f31-141">Esempi</span><span class="sxs-lookup"><span data-stu-id="12f31-141">Samples</span></span>                                  | <span data-ttu-id="12f31-142">Primo campo</span><span class="sxs-lookup"><span data-stu-id="12f31-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="12f31-143">MFVideoInterlace \_ progressive</span><span class="sxs-lookup"><span data-stu-id="12f31-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="12f31-144">No</span><span class="sxs-lookup"><span data-stu-id="12f31-144">No</span></span>          | <span data-ttu-id="12f31-145">Frame progressivo</span><span class="sxs-lookup"><span data-stu-id="12f31-145">Progressive frame</span></span>                        | <span data-ttu-id="12f31-146">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="12f31-146">Not applicable</span></span> |
| <span data-ttu-id="12f31-147">\_FieldInterleavedUpperFirst MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="12f31-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="12f31-148">Sì</span><span class="sxs-lookup"><span data-stu-id="12f31-148">Yes</span></span>         | <span data-ttu-id="12f31-149">Campi con interfoliazione</span><span class="sxs-lookup"><span data-stu-id="12f31-149">Interleaved fields</span></span>                       | <span data-ttu-id="12f31-150">Primo piano</span><span class="sxs-lookup"><span data-stu-id="12f31-150">Upper first</span></span>    |
| <span data-ttu-id="12f31-151">\_FieldInterleavedLowerFirst MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="12f31-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="12f31-152">Sì</span><span class="sxs-lookup"><span data-stu-id="12f31-152">Yes</span></span>         | <span data-ttu-id="12f31-153">Campi con interfoliazione</span><span class="sxs-lookup"><span data-stu-id="12f31-153">Interleaved fields</span></span>                       | <span data-ttu-id="12f31-154">Inferiore prima</span><span class="sxs-lookup"><span data-stu-id="12f31-154">Lower first</span></span>    |
| <span data-ttu-id="12f31-155">\_FieldSingleUpper MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="12f31-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="12f31-156">Sì</span><span class="sxs-lookup"><span data-stu-id="12f31-156">Yes</span></span>         | <span data-ttu-id="12f31-157">Campo singolo</span><span class="sxs-lookup"><span data-stu-id="12f31-157">Single field</span></span>                             | <span data-ttu-id="12f31-158">Primo piano</span><span class="sxs-lookup"><span data-stu-id="12f31-158">Upper first</span></span>    |
| <span data-ttu-id="12f31-159">\_FieldSingleLower MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="12f31-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="12f31-160">Sì</span><span class="sxs-lookup"><span data-stu-id="12f31-160">Yes</span></span>         | <span data-ttu-id="12f31-161">Campo singolo</span><span class="sxs-lookup"><span data-stu-id="12f31-161">Single field</span></span>                             | <span data-ttu-id="12f31-162">Inferiore prima</span><span class="sxs-lookup"><span data-stu-id="12f31-162">Lower first</span></span>    |
| <span data-ttu-id="12f31-163">\_MixedInterlaceOrProgressive MFVideoInterlace</span><span class="sxs-lookup"><span data-stu-id="12f31-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="12f31-164">Può variare</span><span class="sxs-lookup"><span data-stu-id="12f31-164">Can vary</span></span>    | <span data-ttu-id="12f31-165">Campi con interfoliazione o frame progressivi</span><span class="sxs-lookup"><span data-stu-id="12f31-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="12f31-166">Può variare</span><span class="sxs-lookup"><span data-stu-id="12f31-166">Can vary</span></span>       |



 

<span data-ttu-id="12f31-167">I campi con interfoliazione e i campi singoli non possono essere misti.</span><span class="sxs-lookup"><span data-stu-id="12f31-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="12f31-168">Per passare da una a un'altra è necessario modificare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="12f31-169">Flag interlacciamento negli esempi</span><span class="sxs-lookup"><span data-stu-id="12f31-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="12f31-170">Le informazioni che possono cambiare da un campione a quello successivo vengono indicate usando gli attributi di esempio.</span><span class="sxs-lookup"><span data-stu-id="12f31-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="12f31-171">Usare l'interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) per ottenere o impostare questi attributi.</span><span class="sxs-lookup"><span data-stu-id="12f31-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="12f31-172">Tutti gli attributi di interlacciamento elencati in questa sezione hanno valori booleani.</span><span class="sxs-lookup"><span data-stu-id="12f31-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="12f31-173">In effetti, ognuno di questi attributi può avere tre valori: **true**, **false** o not set.</span><span class="sxs-lookup"><span data-stu-id="12f31-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="12f31-174">Se un attributo non è impostato, il valore viene ricavato dal tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="12f31-175">Se viene impostato un attributo, il valore esegue l'override del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="12f31-176">Alcune combinazioni di flag e tipi di supporto non sono valide.</span><span class="sxs-lookup"><span data-stu-id="12f31-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12f31-177">Attributo</span><span class="sxs-lookup"><span data-stu-id="12f31-177">Attribute</span></span></th>
<th><span data-ttu-id="12f31-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f31-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12f31-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="12f31-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="12f31-180">Se <strong>true</strong>, il frame è interlacciato.</span><span class="sxs-lookup"><span data-stu-id="12f31-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="12f31-181">Se <strong>false</strong>, il frame è progressivo.</span><span class="sxs-lookup"><span data-stu-id="12f31-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="12f31-182">Impostare questo attributo su ogni campione se il tipo di supporto è MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12f31-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="12f31-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="12f31-184">Il significato di questo flag dipende dal fatto che gli esempi contengano campi con interfoliazione o singoli campi.</span><span class="sxs-lookup"><span data-stu-id="12f31-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="12f31-185">Campi con interfoliazione: se <strong>true</strong>, il campo inferiore è primo.</span><span class="sxs-lookup"><span data-stu-id="12f31-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="12f31-186">Se <strong>false</strong>, il campo superiore è primo.</span><span class="sxs-lookup"><span data-stu-id="12f31-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="12f31-187">Campi singoli: se <strong>true</strong>, l'esempio contiene un campo inferiore.</span><span class="sxs-lookup"><span data-stu-id="12f31-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="12f31-188">Se <strong>false</strong>, l'esempio contiene un campo superiore.</span><span class="sxs-lookup"><span data-stu-id="12f31-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="12f31-189">Impostare questo attributo su ogni esempio di interpolazione se il tipo di supporto è MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower o MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12f31-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="12f31-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="12f31-191">Se <strong>true</strong>, il primo campo viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="12f31-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="12f31-192">Se <strong>false</strong> o non è impostato, il primo campo non viene ripetuto.</span><span class="sxs-lookup"><span data-stu-id="12f31-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12f31-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="12f31-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="12f31-194">Se <strong>true</strong>, l'esempio contiene un solo campo.</span><span class="sxs-lookup"><span data-stu-id="12f31-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="12f31-195">Se <strong>false</strong>, l'esempio contiene campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="12f31-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="12f31-196">La tabella seguente mostra quali flag sono obbligatori, facoltativi o non consentiti in base al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="12f31-197">Tipo supporto</span><span class="sxs-lookup"><span data-stu-id="12f31-197">Media Type</span></span>         | <span data-ttu-id="12f31-198">Flag interlacciato</span><span class="sxs-lookup"><span data-stu-id="12f31-198">Interlaced Flag</span></span>                      | <span data-ttu-id="12f31-199">Flag BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="12f31-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="12f31-200">Flag RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="12f31-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="12f31-201">Flag SingleField</span><span class="sxs-lookup"><span data-stu-id="12f31-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="12f31-202">Progressivo</span><span class="sxs-lookup"><span data-stu-id="12f31-202">Progressive</span></span>        | <span data-ttu-id="12f31-203">Opzionale Se impostato, deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="12f31-204">Non impostare.</span><span class="sxs-lookup"><span data-stu-id="12f31-204">Do not set.</span></span>                              | <span data-ttu-id="12f31-205">Non impostare.</span><span class="sxs-lookup"><span data-stu-id="12f31-205">Do not set.</span></span>           | <span data-ttu-id="12f31-206">Non impostare.</span><span class="sxs-lookup"><span data-stu-id="12f31-206">Do not set.</span></span>                          |
| <span data-ttu-id="12f31-207">Campi con interfoliazione</span><span class="sxs-lookup"><span data-stu-id="12f31-207">Interleaved fields</span></span> | <span data-ttu-id="12f31-208">Opzionale Se impostato, deve essere **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="12f31-209">Opzionale Se impostato, deve corrispondere al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="12f31-210">Non impostare.</span><span class="sxs-lookup"><span data-stu-id="12f31-210">Do not set.</span></span>           | <span data-ttu-id="12f31-211">Opzionale Se impostato, deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="12f31-212">Campi singoli</span><span class="sxs-lookup"><span data-stu-id="12f31-212">Single fields</span></span>      | <span data-ttu-id="12f31-213">Opzionale Se impostato, deve essere **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="12f31-214">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12f31-214">Required.</span></span>                                | <span data-ttu-id="12f31-215">Non impostare.</span><span class="sxs-lookup"><span data-stu-id="12f31-215">Do not set.</span></span>           | <span data-ttu-id="12f31-216">Impostare su **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="12f31-217">Mixed</span><span class="sxs-lookup"><span data-stu-id="12f31-217">Mixed</span></span>              | <span data-ttu-id="12f31-218">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12f31-218">Required.</span></span>                            | <span data-ttu-id="12f31-219">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12f31-219">Required.</span></span>                                | <span data-ttu-id="12f31-220">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12f31-220">Required.</span></span>             | <span data-ttu-id="12f31-221">Opzionale Se impostato, deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="12f31-222">Nei casi in cui l'attributo è facoltativo, il tipo di supporto definisce già le informazioni.</span><span class="sxs-lookup"><span data-stu-id="12f31-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="12f31-223">È valido impostare l'attributo in modo che corrisponda, ma non obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12f31-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="12f31-224">Se, ad esempio, il tipo di supporto è MFVideoInterlace \_ progressive, significa che tutti i frame nel flusso sono progressivi.</span><span class="sxs-lookup"><span data-stu-id="12f31-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="12f31-225">Pertanto, è possibile impostare l'attributo **MFSampleExtension \_ interlacciato** su **false** o lasciare l'attributo non impostato.</span><span class="sxs-lookup"><span data-stu-id="12f31-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="12f31-226">Consigli</span><span class="sxs-lookup"><span data-stu-id="12f31-226">Recommendations</span></span>

<span data-ttu-id="12f31-227">Questa sezione contiene consigli per diversi tipi di contenuto.</span><span class="sxs-lookup"><span data-stu-id="12f31-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="12f31-228">Il video è di tutti i frame progressivi.</span><span class="sxs-lookup"><span data-stu-id="12f31-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="12f31-229">Impostare il tipo di supporto su MFVideoInterlace \_ progressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="12f31-230">Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **false** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="12f31-231">Non impostare gli attributi **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** o **MFSampleExtension \_ SingleField** .</span><span class="sxs-lookup"><span data-stu-id="12f31-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="12f31-232">Il video è tutti i campi interlacciati con la stessa dominanza del campo.</span><span class="sxs-lookup"><span data-stu-id="12f31-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="12f31-233">Gli esempi contengono campi con interfoliazione.</span><span class="sxs-lookup"><span data-stu-id="12f31-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="12f31-234">Impostare il tipo di supporto su MFVideoInterlace \_ FieldInterleavedUpperFirst o MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="12f31-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="12f31-235">Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **true** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="12f31-236">Non impostare l'attributo **MFSampleExtension \_ BottomFieldFirst** o impostare il valore su ogni frame in modo che corrisponda al tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="12f31-237">Non impostare l'attributo **MFSampleExtension \_ RepeatFirstField** o impostarlo su **false** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="12f31-238">Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **false** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="12f31-239">Il video contiene una combinazione di frame interlacciati e progressivi, con campi ripetuti e dominanza del campo variabile (ad esempio, video DVD).</span><span class="sxs-lookup"><span data-stu-id="12f31-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="12f31-240">Impostare il tipo di supporto su MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="12f31-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="12f31-241">In ogni frame impostare gli attributi **MFSampleExtension \_ Interlaced**, **MFSampleExtension \_ BottomFieldFirst** e **MFSampleExtension \_ RepeatFirstField** .</span><span class="sxs-lookup"><span data-stu-id="12f31-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="12f31-242">Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **false** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="12f31-243">Il video è interlacciato e gli esempi contengono singoli campi.</span><span class="sxs-lookup"><span data-stu-id="12f31-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="12f31-244">Impostare il tipo di supporto su MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="12f31-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="12f31-245">Impostare l'attributo **MFSampleExtension \_ BottomFieldFirst** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="12f31-246">Non impostare l'attributo **MFSampleExtension \_ interlacciato** o impostarlo su **true** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="12f31-247">Non impostare l'attributo **MFSampleExtension \_ RepeatFirstField** o impostarlo su **false** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="12f31-248">Non impostare l'attributo **MFSampleExtension \_ SingleField** o impostarlo su **true** in ogni frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="12f31-249">La maggior parte del contenuto video rientra in una di queste categorie.</span><span class="sxs-lookup"><span data-stu-id="12f31-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="12f31-250">Mapping MPEG-2</span><span class="sxs-lookup"><span data-stu-id="12f31-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="12f31-251">Per il contenuto MPEG-2, usare i mapping seguenti per convertire i flag MPEG-2 in Media Foundation gli attributi di esempio.</span><span class="sxs-lookup"><span data-stu-id="12f31-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="12f31-252">**\_struttura immagine**</span><span class="sxs-lookup"><span data-stu-id="12f31-252">**picture\_structure**</span></span>



| <span data-ttu-id="12f31-253">Valore</span><span class="sxs-lookup"><span data-stu-id="12f31-253">Value</span></span>         | <span data-ttu-id="12f31-254">Attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f31-255">frame</span><span class="sxs-lookup"><span data-stu-id="12f31-255">frame</span></span>         | <span data-ttu-id="12f31-256">**MFSampleExtension \_ SingleField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="12f31-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="12f31-257">\_campo superiore</span><span class="sxs-lookup"><span data-stu-id="12f31-257">top\_field</span></span>    | <span data-ttu-id="12f31-258">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="12f31-259">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="12f31-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="12f31-260">\_campo inferiore</span><span class="sxs-lookup"><span data-stu-id="12f31-260">bottom\_field</span></span> | <span data-ttu-id="12f31-261">**MFSampleExtension \_ SingleField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="12f31-262">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="12f31-263">**frame progressivo \_**</span><span class="sxs-lookup"><span data-stu-id="12f31-263">**progressive\_frame**</span></span>



| <span data-ttu-id="12f31-264">Valore</span><span class="sxs-lookup"><span data-stu-id="12f31-264">Value</span></span> | <span data-ttu-id="12f31-265">Attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="12f31-266">0</span><span class="sxs-lookup"><span data-stu-id="12f31-266">0</span></span>     | <span data-ttu-id="12f31-267">**MFSampleExtension \_ Interlacciato**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="12f31-268">1</span><span class="sxs-lookup"><span data-stu-id="12f31-268">1</span></span>     | <span data-ttu-id="12f31-269">**MFSampleExtension \_ Interlacciato**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="12f31-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="12f31-270">**\_primo campo \_ principale**</span><span class="sxs-lookup"><span data-stu-id="12f31-270">**top\_field\_first**</span></span>



| <span data-ttu-id="12f31-271">Valore</span><span class="sxs-lookup"><span data-stu-id="12f31-271">Value</span></span> | <span data-ttu-id="12f31-272">Attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="12f31-273">0</span><span class="sxs-lookup"><span data-stu-id="12f31-273">0</span></span>     | <span data-ttu-id="12f31-274">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="12f31-275">1</span><span class="sxs-lookup"><span data-stu-id="12f31-275">1</span></span>     | <span data-ttu-id="12f31-276">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="12f31-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="12f31-277">**Ripeti \_ primo \_ campo**</span><span class="sxs-lookup"><span data-stu-id="12f31-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="12f31-278">Valore</span><span class="sxs-lookup"><span data-stu-id="12f31-278">Value</span></span> | <span data-ttu-id="12f31-279">Attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="12f31-280">0</span><span class="sxs-lookup"><span data-stu-id="12f31-280">0</span></span>     | <span data-ttu-id="12f31-281">**MFSampleExtension \_ RepeatFirstField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="12f31-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="12f31-282">1</span><span class="sxs-lookup"><span data-stu-id="12f31-282">1</span></span>     | <span data-ttu-id="12f31-283">**MFSampleExtension \_ RepeatFirstField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="12f31-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="12f31-284">Esempi di Single-Field</span><span class="sxs-lookup"><span data-stu-id="12f31-284">Single-Field Samples</span></span>

<span data-ttu-id="12f31-285">Se il tipo di supporto è MFVideoInterlace \_ FieldSingleUpper o MFVideoInterlace \_ FieldSingleLower, significa che ogni esempio contiene un solo campo.</span><span class="sxs-lookup"><span data-stu-id="12f31-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="12f31-286">Tuttavia, il tipo di supporto descrive l'intero frame.</span><span class="sxs-lookup"><span data-stu-id="12f31-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="12f31-287">Pertanto, ogni buffer contiene solo metà del numero di righe di campo specificate nel tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="12f31-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="12f31-288">Ad esempio, se il tipo di supporto descrive il video come 720 × 480, ogni campo contiene 240 righe di analisi e quindi ogni buffer contiene solo 240 righe di pixel.</span><span class="sxs-lookup"><span data-stu-id="12f31-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="12f31-289">Se si scrive un componente che accetta i tipi di supporto con esempi di campo singolo, è necessario tenere presente questo fatto quando si accede ai dati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="12f31-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="12f31-290">La stessa regola si applica all'apertura geometrica (attributo di[ \_ \_ \_ apertura geometrica MF mt](mf-mt-geometric-aperture-attribute.md) ) e all'apertura di visualizzazione minima (attributo di[ \_ \_ \_ \_ apertura minima dello schermo MF mt](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="12f31-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="12f31-291">Queste aree vengono specificate in termini di intero frame, non dei singoli campi.</span><span class="sxs-lookup"><span data-stu-id="12f31-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="12f31-292">Mapping DirectShow</span><span class="sxs-lookup"><span data-stu-id="12f31-292">DirectShow Mappings</span></span>

<span data-ttu-id="12f31-293">In DirectShow, le informazioni di interlacciamento per campione sono contenute nel membro **dwTypeSpecificFlags** della struttura delle **\_ \_ Proprietà SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="12f31-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="12f31-294">Nella tabella seguente vengono illustrati gli attributi equivalenti per Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="12f31-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="12f31-295">Flag di esempio DirectShow</span><span class="sxs-lookup"><span data-stu-id="12f31-295">DirectShow sample flag</span></span>              | <span data-ttu-id="12f31-296">Media Foundation attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f31-297">\_cornice del flag video am con \_ \_ interfoliazione \_</span><span class="sxs-lookup"><span data-stu-id="12f31-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="12f31-298">**MFSampleExtension \_ SingleField**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="12f31-299">\_Flag video \_ am \_ Field1</span><span class="sxs-lookup"><span data-stu-id="12f31-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="12f31-300">**MFSampleExtension \_ Interlacciato**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="12f31-301">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="12f31-302">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="12f31-303">\_Flag video \_ am \_ Field2</span><span class="sxs-lookup"><span data-stu-id="12f31-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="12f31-304">**MFSampleExtension \_ Interlacciato**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="12f31-305">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="12f31-306">**MFSampleExtension \_ BottomFieldFirst**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="12f31-307">\_trama del \_ flag \_ video am</span><span class="sxs-lookup"><span data-stu-id="12f31-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="12f31-308">**MFSampleExtension \_ Interlacciato**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="12f31-309">Questo flag indica che il driver non deve deinterlacciare i due campi.</span><span class="sxs-lookup"><span data-stu-id="12f31-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="12f31-310">\_Flag video \_ am \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="12f31-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="12f31-311">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="12f31-312">Se il contenuto è interlacciato e il flag \_ FIELD1FIRST del flag video am \_ \_ non è presente, impostare questo attributo su **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="12f31-313">\_campo di \_ ripetizione del flag video \_ am \_</span><span class="sxs-lookup"><span data-stu-id="12f31-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="12f31-314">**MFSampleExtension \_ RepeatFirstField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="12f31-315">Se il \_ \_ \_ flag di campo di ripetizione del contrassegno del video am \_ non è presente, impostare questo attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="12f31-316">Se l'esempio DirectShow non contiene flag di esempio, usare il valore di **dwInterlaceFlags** dalla struttura **VIDEOINFOHEADER2** :</span><span class="sxs-lookup"><span data-stu-id="12f31-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="12f31-317">Flag interlacciamento DirectShow</span><span class="sxs-lookup"><span data-stu-id="12f31-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="12f31-318">Media Foundation attributo di esempio</span><span class="sxs-lookup"><span data-stu-id="12f31-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="12f31-319">AMINTERLACE \_ interlacciato</span><span class="sxs-lookup"><span data-stu-id="12f31-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="12f31-320">**MFSampleExtension \_ Interlacciato**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="12f31-321">\_1FIELDPERSAMPLE AMINTERLACE</span><span class="sxs-lookup"><span data-stu-id="12f31-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="12f31-322">**MFSampleExtension \_ SingleField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="12f31-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="12f31-323">\_FIELD1FIRST AMINTERLACE</span><span class="sxs-lookup"><span data-stu-id="12f31-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="12f31-324">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="12f31-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="12f31-325">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="12f31-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f31-326">Tipi di supporti video</span><span class="sxs-lookup"><span data-stu-id="12f31-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="12f31-327">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="12f31-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




