---
description: 'Il codificatore Windows Media Audio codifica i flussi audio. Il codificatore supporta tre categorie di output codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.'
ms.assetid: 1f6a3a9f-b534-4a6b-b773-0315c759624e
title: Codificatore Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9f1d5b9e5f890a43958bcc304dd2d305844fdb4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331689"
---
# <a name="windows-media-audio-encoder"></a><span data-ttu-id="57cba-104">Codificatore Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="57cba-104">Windows Media Audio Encoder</span></span>

<span data-ttu-id="57cba-105">Il codificatore Windows Media Audio codifica i flussi audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-105">The Windows Media Audio encoder encodes audio streams.</span></span> <span data-ttu-id="57cba-106">Il codificatore supporta tre categorie di output codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-106">The encoder supports three categories of encoded output: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="57cba-107">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="57cba-107">Class Identifier</span></span>

<span data-ttu-id="57cba-108">L'identificatore di classe (CLSID) per il codificatore Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMAEncMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="57cba-108">The class identifier (CLSID) for the Windows Media Audio Encoder is represented by the constant **CLSID\_CWMAEncMediaObject**.</span></span> <span data-ttu-id="57cba-109">È possibile creare un'istanza del codificatore audio chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="57cba-109">You can create an instance of the audio encoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="57cba-110">Formati di input</span><span class="sxs-lookup"><span data-stu-id="57cba-110">Input Formats</span></span>

<span data-ttu-id="57cba-111">La tabella seguente illustra i tag di formato audio che rappresentano le categorie di input supportate dal codificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-111">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio encoder.</span></span> <span data-ttu-id="57cba-112">Per informazioni su come impostare i tipi di input e output per il codificatore, vedere [Configuring audio encoding](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="57cba-112">For information about how to set the input and output types for the encoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="57cba-113">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="57cba-113">Format tag constant</span></span>       | <span data-ttu-id="57cba-114">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="57cba-114">Format tag value</span></span> | <span data-ttu-id="57cba-115">Formato audio</span><span class="sxs-lookup"><span data-stu-id="57cba-115">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="57cba-116">\_PCM in formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="57cba-116">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="57cba-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="57cba-117">0x0001</span></span>           | <span data-ttu-id="57cba-118">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="57cba-118">PCM format</span></span>                                            |
| <span data-ttu-id="57cba-119">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="57cba-119">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="57cba-120">0x0003</span><span class="sxs-lookup"><span data-stu-id="57cba-120">0x0003</span></span>           | <span data-ttu-id="57cba-121">Virgola mobile IEEE</span><span class="sxs-lookup"><span data-stu-id="57cba-121">IEEE floating point</span></span>                                   |
| <span data-ttu-id="57cba-122">\_formato Wave \_ estendibile</span><span class="sxs-lookup"><span data-stu-id="57cba-122">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="57cba-123">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="57cba-123">0xFFFE</span></span>           | <span data-ttu-id="57cba-124">Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="57cba-124">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="57cba-125">Formati di output</span><span class="sxs-lookup"><span data-stu-id="57cba-125">Output Formats</span></span>

<span data-ttu-id="57cba-126">La tabella seguente illustra i tag di formato audio che rappresentano le categorie di output supportate dal codificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-126">The following table shows the audio format tags that represent the output categories supported by the Windows Media Audio encoder.</span></span>



| <span data-ttu-id="57cba-127">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="57cba-127">Format tag constant</span></span>             | <span data-ttu-id="57cba-128">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="57cba-128">Format tag value</span></span> | <span data-ttu-id="57cba-129">Formato audio</span><span class="sxs-lookup"><span data-stu-id="57cba-129">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="57cba-130">\_Formato Wave \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="57cba-130">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="57cba-131">0x0161</span><span class="sxs-lookup"><span data-stu-id="57cba-131">0x0161</span></span>           | <span data-ttu-id="57cba-132">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="57cba-132">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="57cba-133">\_Formato Wave \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="57cba-133">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="57cba-134">0x0162</span><span class="sxs-lookup"><span data-stu-id="57cba-134">0x0162</span></span>           | <span data-ttu-id="57cba-135">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="57cba-135">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="57cba-136">\_formato Wave \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="57cba-136">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="57cba-137">0x0163</span><span class="sxs-lookup"><span data-stu-id="57cba-137">0x0163</span></span>           | <span data-ttu-id="57cba-138">Windows Media Audio senza perdita di perdite</span><span class="sxs-lookup"><span data-stu-id="57cba-138">Windows Media Audio Lossless</span></span>     |



 

## <a name="interfaces"></a><span data-ttu-id="57cba-139">Interfacce</span><span class="sxs-lookup"><span data-stu-id="57cba-139">Interfaces</span></span>

<span data-ttu-id="57cba-140">Un oggetto di utilizzo del contenuto audio espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="57cba-140">An audio endoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="57cba-141">Un codificatore Windows Media Audio si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="57cba-141">A Windows Media Audio encoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="57cba-142">Nella tabella seguente vengono illustrate le condizioni in base alle quali un codificatore audio si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="57cba-142">The following table shows the conditions under which an audio encoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="57cba-143">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="57cba-143">Operating system</span></span> | <span data-ttu-id="57cba-144">Comportamento del codificatore</span><span class="sxs-lookup"><span data-stu-id="57cba-144">Encoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57cba-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="57cba-145">Windows XP</span></span>       | <span data-ttu-id="57cba-146">Un codificatore Windows Media Audio si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="57cba-146">A Windows Media Audio encoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="57cba-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57cba-147">Windows Vista</span></span>    | <span data-ttu-id="57cba-148">Per impostazione predefinita, un codificatore Windows Media Audio si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="57cba-148">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="57cba-149">Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un codificatore audio, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="57cba-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio encoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="57cba-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57cba-150">Windows 7</span></span>        | <span data-ttu-id="57cba-151">Per impostazione predefinita, un codificatore Windows Media Audio si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="57cba-151">By default, a Windows Media Audio encoder behaves as a DMO.</span></span> <span data-ttu-id="57cba-152">Se si ottiene un'interfaccia **IMFTransform** su un codificatore audio, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="57cba-152">If you obtain an **IMFTransform** interface on an audio encoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="encoder-properties"></a><span data-ttu-id="57cba-153">Proprietà del codificatore</span><span class="sxs-lookup"><span data-stu-id="57cba-153">Encoder Properties</span></span>

<span data-ttu-id="57cba-154">Il codificatore Windows Media Audio supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="57cba-154">The Windows Media Audio encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="57cba-155">Proprietà</span><span class="sxs-lookup"><span data-stu-id="57cba-155">Property</span></span></th>
<th><span data-ttu-id="57cba-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57cba-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="57cba-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-157"><a href="mfpkey-avgconstrainedproperty.md"><strong>MFPKEY_AVGCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="57cba-158">Specifica se il codificatore usa la codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="57cba-158">Specifies whether the encoder uses average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="57cba-159">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-160">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-161">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-161">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-162"><a href="mfpkey-bmaxproperty.md"><strong>MFPKEY_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="57cba-163">Specifica la finestra del buffer, in millisecondi, di un flusso con velocità in bit limitata (VBR) a livello di picco.</span><span class="sxs-lookup"><span data-stu-id="57cba-163">Specifies the buffer window, in milliseconds, of a constrained variable-bit-rate (VBR) stream at its peak bit rate.</span></span><br/> <dl> <span data-ttu-id="57cba-164">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-164">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-165">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-165">Standard, Professional.</span></span><br />
<span data-ttu-id="57cba-166">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-166">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-167"><a href="mfpkey-checkdataconsistency2pproperty.md"><strong>MFPKEY_CHECKDATACONSISTENCY2P</strong></a></span></span></td>
<td><span data-ttu-id="57cba-168">Specifica se il codificatore deve verificare la coerenza dei dati tra i passaggi quando si esegue la codifica VBR a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="57cba-168">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <br/> <dl> <span data-ttu-id="57cba-169">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-169">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-170">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-170">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-171">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-171">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-172"><a href="mfpkey-constraindeclatencyproperty.md"><strong>MFPKEY_CONSTRAINDECLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-173">Specifica se il codificatore è vincolato da un requisito di latenza del decodificatore massimo.</span><span class="sxs-lookup"><span data-stu-id="57cba-173">Specifies whether the encoder is constrained by a maximum decoder latency requirement.</span></span><br/> <dl> <span data-ttu-id="57cba-174">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-174">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-175">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-175">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-176">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-176">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-177"><a href="mfpkey-constrainenccomplexityproperty.md"><strong>MFPKEY_CONSTRAINENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-178">Specifica se la complessità dell'algoritmo di codifica è vincolata.</span><span class="sxs-lookup"><span data-stu-id="57cba-178">Specifies whether the complexity of the encoding algorithm is constrained.</span></span><br/> <dl> <span data-ttu-id="57cba-179">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-180">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-180">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-181">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-181">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-182"><a href="mfpkey-constrainenclatencyproperty.md"><strong>MFPKEY_CONSTRAINENCLATENCY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-183">Specifica se il codificatore è vincolato da un requisito di latenza massima.</span><span class="sxs-lookup"><span data-stu-id="57cba-183">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span><br/> <dl> <span data-ttu-id="57cba-184">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-184">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-185">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-185">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-186">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-186">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-187"><a href="mfpkey-constrain-enumerated-vbrqualityproperty.md"><strong>MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-188">Specifica se le modalità enumerate dal codificatore sono limitate a quelle che soddisfano un requisito di qualità.</span><span class="sxs-lookup"><span data-stu-id="57cba-188">Specifies whether modes enumerated by the encoder are limited to those that meet a quality requirement.</span></span><br/> <dl> <span data-ttu-id="57cba-189">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-189">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-190">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-190">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-191">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-192"><a href="mfpkey-decodercomplexityprofileproperty.md"><strong>MFPKEY_DECODERCOMPLEXITYPROFILE</strong></a></span></span></td>
<td><span data-ttu-id="57cba-193">Specifica il profilo di complessità del contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="57cba-193">Specifies the complexity profile of the encoded content.</span></span><br/> <dl> <span data-ttu-id="57cba-194">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-194">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-195">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-195">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-196">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-196">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-197"><a href="mfpkey-desired-vbrqualityproperty.md"><strong>MFPKEY_DESIRED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-198">Specifica il livello di qualità desiderato per la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="57cba-198">Specifies the desired quality level for VBR encoding.</span></span><br/> <dl> <span data-ttu-id="57cba-199">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-199">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-200">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-200">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-201">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-201">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-202"><a href="mfpkey-dyn-allow-noisesubproperty.md"><strong>MFPKEY_DYN_ALLOW_NOISESUB</strong></a></span></span></td>
<td><span data-ttu-id="57cba-203">Specifica se il codificatore utilizza la sostituzione del rumore.</span><span class="sxs-lookup"><span data-stu-id="57cba-203">Specifies whether the encoder uses noise substitution.</span></span><br/> <dl> <span data-ttu-id="57cba-204">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-204">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-205">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-205">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-206">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-206">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-207"><a href="mfpkey-dyn-allow-pcmrangelimitingproperty.md"><strong>MFPKEY_DYN_ALLOW_PCMRANGELIMITING</strong></a></span></span></td>
<td><span data-ttu-id="57cba-208">Specifica se il codificatore usa la limitazione dell'intervallo PCM.</span><span class="sxs-lookup"><span data-stu-id="57cba-208">Specifies whether the encoder uses PCM range limiting.</span></span><br/> <dl> <span data-ttu-id="57cba-209">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-209">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-210">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-210">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-211">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-211">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-212"><a href="mfpkey-dyn-bandtrunc-bwceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWCEIL</strong></a></span></span></td>
<td><span data-ttu-id="57cba-213">Specifica la larghezza di banda massima codificata consentita dal troncamento della banda nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="57cba-213">Specifies the maximum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="57cba-214">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-214">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-215">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-215">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-216">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-216">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-217"><a href="mfpkey-dyn-bandtrunc-bwfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_BWFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="57cba-218">Specifica la larghezza di banda minima codificata consentita dal troncamento della banda nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="57cba-218">Specifies the minimum coded bandwidth allowed by band truncation in the encoder.</span></span><br/> <dl> <span data-ttu-id="57cba-219">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-219">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-220">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-220">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-221">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-221">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-222"><a href="mfpkey-dyn-bandtrunc-qceilproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QCEIL</strong></a></span></span></td>
<td><span data-ttu-id="57cba-223">Specifica la qualità a cui è consentita una larghezza di banda minima codificata.</span><span class="sxs-lookup"><span data-stu-id="57cba-223">Specifies the quality at which minimum coded bandwidth is allowed.</span></span> <br/> <dl> <span data-ttu-id="57cba-224">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-224">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-225">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-225">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-226">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-226">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-227"><a href="mfpkey-dyn-bandtrunc-qfloorproperty.md"><strong>MFPKEY_DYN_BANDTRUNC_QFLOOR</strong></a></span></span></td>
<td><span data-ttu-id="57cba-228">Specifica la qualità di massima consentita per la larghezza di banda codificata.</span><span class="sxs-lookup"><span data-stu-id="57cba-228">Specifies the quality at which maximum coded bandwidth is allowed.</span></span><br/> <dl> <span data-ttu-id="57cba-229">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-229">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-230">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-230">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-231">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-231">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-232"><a href="mfpkey-dyn-bandtruncationproperty.md"><strong>MFPKEY_DYN_BANDTRUNCATION</strong></a></span></span></td>
<td><span data-ttu-id="57cba-233">Specifica se il codificatore esegue il troncamento della banda.</span><span class="sxs-lookup"><span data-stu-id="57cba-233">Specifies whether the encoder performs band truncation.</span></span><br/> <dl> <span data-ttu-id="57cba-234">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-234">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-235">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-235">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-236">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-236">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-237"><a href="mfpkey-dyn-simplemaskproperty.md"><strong>MFPKEY_DYN_SIMPLEMASK</strong></a></span></span></td>
<td><span data-ttu-id="57cba-238">Specifica se il codificatore usa lo stile di calcolo della maschera eseguito dalla versione 7 del codificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-238">Specifies whether the encoder uses the style of mask computation performed by version 7 of the Windows Media Audio encoder.</span></span><br/> <dl> <span data-ttu-id="57cba-239">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-239">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-240">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-240">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-241">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-241">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-242"><a href="mfpkey-dyn-stereo-preprocproperty.md"><strong>MFPKEY_DYN_STEREO_PREPROC</strong></a></span></span></td>
<td><span data-ttu-id="57cba-243">Specifica se il codificatore esegue l'elaborazione di immagini stereo.</span><span class="sxs-lookup"><span data-stu-id="57cba-243">Specifies whether the encoder performs stereo image processing.</span></span> <br/> <dl> <span data-ttu-id="57cba-244">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-244">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-245">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-245">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-246">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-246">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-247"><a href="mfpkey-dyn-vbr-bavgproperty.md"><strong>MFPKEY_DYN_VBR_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="57cba-248">Specifica la finestra del buffer, in millisecondi, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="57cba-248">Specifies the buffer window, in milliseconds, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="57cba-249">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-249">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-250">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-250">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-251">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-251">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-252"><a href="mfpkey-dyn-vbr-ravgproperty.md"><strong>MFPKEY_DYN_VBR_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="57cba-253">Specifica la velocità in bit media, in bit al secondo, per un codificatore configurato per l'utilizzo della codifica VBR media controllabile.</span><span class="sxs-lookup"><span data-stu-id="57cba-253">Specifies the average bit rate, in bits per second, for an encoder that is configured to use average-controllable VBR encoding.</span></span><br/> <dl> <span data-ttu-id="57cba-254">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-254">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-255">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-255">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-256">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-256">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-257"><a href="mfpkey-enccomplexityproperty.md"><strong>MFPKEY_ENCCOMPLEXITY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-258">Specifica la complessità dell'algoritmo di codifica.</span><span class="sxs-lookup"><span data-stu-id="57cba-258">Specifies the complexity of the encoding algorithm.</span></span><br/> <dl> <span data-ttu-id="57cba-259">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-259">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-260">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-260">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-261">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-261">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-262"><a href="mfpkey-endofpassproperty.md"><strong>MFPKEY_ENDOFPASS</strong></a></span></span></td>
<td><span data-ttu-id="57cba-263">Specifica la fine di un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="57cba-263">Specifies the end of an encoding pass.</span></span><br/> <dl> <span data-ttu-id="57cba-264">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-264">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-265">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-265">Standard, Professional.</span></span><br />
<span data-ttu-id="57cba-266">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-266">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-267"><a href="mfpkey-enhanced-wmaproperty.md"><strong>MFPKEY_ENHANCED_WMA</strong></a></span></span></td>
<td><span data-ttu-id="57cba-268">Specifica se il codificatore principale utilizza &quot; la &quot; funzionalità più.</span><span class="sxs-lookup"><span data-stu-id="57cba-268">Specifies whether the core encoder uses the &quot;Plus&quot; feature.</span></span><br/> <dl> <span data-ttu-id="57cba-269">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-269">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-270">Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-270">Professional.</span></span><br />
<span data-ttu-id="57cba-271">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-271">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-272"><a href="mfpkey-maxdeclatencymsproperty.md"><strong>MFPKEY_MAXDECLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="57cba-273">Specifica la latenza massima per il decodificatore, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="57cba-273">Specifies the maximum latency for the decoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="57cba-274">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-274">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-275">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-275">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-276">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-276">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-277"><a href="mfpkey-maxenclatencymsproperty.md"><strong>MFPKEY_MAXENCLATENCYMS</strong></a></span></span></td>
<td><span data-ttu-id="57cba-278">Specifica la latenza massima per il codificatore, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="57cba-278">Specifies the maximum latency for the encoder, in milliseconds.</span></span><br/> <dl> <span data-ttu-id="57cba-279">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-279">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-280">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-280">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-281">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-281">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-282"><a href="mfpkey-most-recently-enumerated-vbrqualityproperty.md"><strong>MFPKEY_MOST_RECENTLY_ENUMERATED_VBRQUALITY</strong></a></span></span></td>
<td><span data-ttu-id="57cba-283">Specifica il livello di qualità VBR del tipo di output enumerato più di recente.</span><span class="sxs-lookup"><span data-stu-id="57cba-283">Specifies the VBR quality level of the most recently enumerated output type.</span></span><br/> <dl> <span data-ttu-id="57cba-284">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-284">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-285">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-285">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-286">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-286">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-287"><a href="mfpkey-passesrecommendedproperty.md"><strong>MFPKEY_PASSESRECOMMENDED</strong></a></span></span></td>
<td><span data-ttu-id="57cba-288">Specifica il numero massimo di passaggi supportati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="57cba-288">Specifies the maximum number of passes supported by the encoder.</span></span><br/> <dl> <span data-ttu-id="57cba-289">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-289">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-290">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-290">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-291">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-291">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-292"><a href="mfpkey-passesusedproperty.md"><strong>MFPKEY_PASSESUSED</strong></a></span></span></td>
<td><span data-ttu-id="57cba-293">Specifica il numero di passaggi che il codificatore utilizzerà per codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="57cba-293">Specifies the number of passes that the encoder will use to encode the content.</span></span><br/> <dl> <span data-ttu-id="57cba-294">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-294">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-295">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-295">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-296">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-296">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-297"><a href="mfpkey-peakconstrainedproperty.md"><strong>MFPKEY_PEAKCONSTRAINED</strong></a></span></span></td>
<td><span data-ttu-id="57cba-298">Specifica se il codificatore è vincolato da una velocità in bit di picco.</span><span class="sxs-lookup"><span data-stu-id="57cba-298">Specifies whether the encoder is constrained by a peak bit rate.</span></span><br/> <dl> <span data-ttu-id="57cba-299">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-299">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-300">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-300">Standard, Professional.</span></span><br />
<span data-ttu-id="57cba-301">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-301">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-302"><a href="mfpkey-preferred-framesizeproperty.md"><strong>MFPKEY_PREFERRED_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="57cba-303">Specifica il numero preferito di campioni per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="57cba-303">Specifies the preferred number of samples per frame.</span></span><br/> <dl> <span data-ttu-id="57cba-304">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-304">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-305">Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-305">Professional.</span></span><br />
<span data-ttu-id="57cba-306">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-306">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-307"><a href="mfpkey-requesting-a-framesizeproperty.md"><strong>MFPKEY_REQUESTING_A_FRAMESIZE</strong></a></span></span></td>
<td><span data-ttu-id="57cba-308">Specifica se il codificatore deve utilizzare una dimensione del frame preferita.</span><span class="sxs-lookup"><span data-stu-id="57cba-308">Specifies whether the encoder should use a preferred frame size.</span></span><br/> <dl> <span data-ttu-id="57cba-309">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-309">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-310">Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-310">Professional.</span></span><br />
<span data-ttu-id="57cba-311">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-311">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-312"><a href="mfpkey-rmaxproperty.md"><strong>MFPKEY_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="57cba-313">Specifica la velocità in bit del picco, in bit al secondo, usata per la codifica con velocità in bit (VBR) a 2 passaggi vincolata.</span><span class="sxs-lookup"><span data-stu-id="57cba-313">Specifies the peak bit rate, in bits per second, used for constrained 2-pass variable-bit-rate (VBR) encoding.</span></span> <br/> <dl> <span data-ttu-id="57cba-314">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-314">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-315">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-315">Standard, Professional.</span></span><br />
<span data-ttu-id="57cba-316">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-316">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-317"><a href="mfpkey-stat-bavgproperty.md"><strong>MFPKEY_STAT_BAVG</strong></a></span></span></td>
<td><span data-ttu-id="57cba-318">Specifica la finestra media del buffer, in millisecondi, di un flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="57cba-318">Specifies the average buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="57cba-319">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-319">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-320">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-320">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-321">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-321">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-322"><a href="mfpkey-stat-bmaxproperty.md"><strong>MFPKEY_STAT_BMAX</strong></a></span></span></td>
<td><span data-ttu-id="57cba-323">Specifica la finestra massima del buffer, in millisecondi, di un flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="57cba-323">Specifies the maximum buffer window, in milliseconds, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="57cba-324">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-324">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-325">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-325">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-326">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-326">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-327"><a href="mfpkey-stat-ravgproperty.md"><strong>MFPKEY_STAT_RAVG</strong></a></span></span></td>
<td><span data-ttu-id="57cba-328">Specifica la velocità in bit media, in bit al secondo, di un flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="57cba-328">Specifies the average bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="57cba-329">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-329">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-330">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-330">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-331">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-331">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-332"><a href="mfpkey-stat-rmaxproperty.md"><strong>MFPKEY_STAT_RMAX</strong></a></span></span></td>
<td><span data-ttu-id="57cba-333">Specifica la velocità in bit massima, in bit al secondo, di un flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="57cba-333">Specifies the maximum bit rate, in bits per second, of an encoded stream.</span></span><br/> <dl> <span data-ttu-id="57cba-334">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-334">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-335">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-335">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-336">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-336">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-337"><a href="mfpkey-vbrenabledproperty.md"><strong>MFPKEY_VBRENABLED</strong></a></span></span></td>
<td><span data-ttu-id="57cba-338">Specifica se il codificatore usa la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="57cba-338">Specifies whether the encoder uses VBR encoding.</span></span><br/> <dl> <span data-ttu-id="57cba-339">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-339">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-340">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-340">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-341">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-341">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-342"><a href="mfpkey-wma-elementary-streamproperty.md"><strong>MFPKEY_WMA_ELEMENTARY_STREAM</strong></a></span></span></td>
<td><span data-ttu-id="57cba-343">Questa proprietà non è attualmente utilizzata dal codec Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-343">This property is currently not used by the Windows Media Audio codec.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-344"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="57cba-345">Specifica il livello di volume medio del contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-345">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="57cba-346">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-346">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-347">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-347">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-348">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-348">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-349"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="57cba-350">Specifica il livello di volume massimo che si verifica nel contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="57cba-350">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="57cba-351">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-351">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-352">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-352">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-353">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-353">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-354"><a href="mfpkey-wmaenc-avgbytespersecproperty.md"><strong>MFPKEY_WMAENC_AVGBYTESPERSEC</strong></a></span></span></td>
<td><span data-ttu-id="57cba-355">Specifica il numero medio di byte al secondo per l'audio con codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="57cba-355">Specifies the average bytes per second for VBR encoded audio.</span></span><br/> <dl> <span data-ttu-id="57cba-356">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-356">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-357">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-357">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-358">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="57cba-358">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-359"><a href="mfpkey-wmaenc-bufferlesscbrproperty.md"><strong>MFPKEY_WMAENC_BUFFERLESSCBR</strong></a></span></span></td>
<td><span data-ttu-id="57cba-360">Specifica se il codificatore deve produrre 1 pacchetto WMA per fotogramma.</span><span class="sxs-lookup"><span data-stu-id="57cba-360">Specifies whether the encoder should produce 1 WMA packet per frame.</span></span><br/> <dl> <span data-ttu-id="57cba-361">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-361">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-362">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-362">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-363">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-363">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-364"><a href="mfpkey-wmaenc-generate-drc-paramsproperty.md"><strong>MFPKEY_WMAENC_GENERATE_DRC_PARAMS</strong></a></span></span></td>
<td><span data-ttu-id="57cba-365">Specifica se il codificatore deve generare parametri dinamici per il controllo degli intervalli.</span><span class="sxs-lookup"><span data-stu-id="57cba-365">Specifies whether the encoder should generate dynamic range control parameters.</span></span><br/> <dl> <span data-ttu-id="57cba-366">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-366">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-367">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="57cba-367">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="57cba-368">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-368">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="57cba-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-369"><a href="mfpkey-wmaenc-origwaveformatproperty.md"><strong>MFPKEY_WMAENC_ORIGWAVEFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="57cba-370">Specifica la struttura <strong>WAVEFORMATEX</strong> che descrive il contenuto audio di input.</span><span class="sxs-lookup"><span data-stu-id="57cba-370">Specifies the <strong>WAVEFORMATEX</strong> structure describing the input audio content.</span></span><br/> <dl> <span data-ttu-id="57cba-371">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-371">Windows XP and later.</span></span><br />
<span data-ttu-id="57cba-372">Standard, Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-372">Standard, Professional.</span></span><br />
<span data-ttu-id="57cba-373">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-373">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="57cba-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span><span class="sxs-lookup"><span data-stu-id="57cba-374"><a href="mfpkey-wmaenc-rtspdifproperty.md"><strong>MFPKEY_WMAENC_RTSPDIF</strong></a></span></span></td>
<td><span data-ttu-id="57cba-375">Specifica se il codificatore deve abilitare la codifica S/PDIF in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="57cba-375">Specifies whether the encoder should enable real-time S/PDIF encoding .</span></span><br/> <dl> <span data-ttu-id="57cba-376">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57cba-376">Windows Vista and later.</span></span><br />
<span data-ttu-id="57cba-377">Professional.</span><span class="sxs-lookup"><span data-stu-id="57cba-377">Professional.</span></span><br />
<span data-ttu-id="57cba-378">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="57cba-378">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="57cba-379">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57cba-379">Requirements</span></span>



| <span data-ttu-id="57cba-380">Requisito</span><span class="sxs-lookup"><span data-stu-id="57cba-380">Requirement</span></span> | <span data-ttu-id="57cba-381">Valore</span><span class="sxs-lookup"><span data-stu-id="57cba-381">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57cba-382">Client</span><span class="sxs-lookup"><span data-stu-id="57cba-382">Client</span></span><br/> | <span data-ttu-id="57cba-383">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="57cba-383">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="57cba-384">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57cba-384">Header</span></span><br/> | <dl> <span data-ttu-id="57cba-385"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57cba-385"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="57cba-386">DLL</span><span class="sxs-lookup"><span data-stu-id="57cba-386">DLL</span></span><br/>    | <dl> <span data-ttu-id="57cba-387"><dt>Wmadmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57cba-387"><dt>Wmadmoe.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="57cba-388">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57cba-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cba-389">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="57cba-389">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="57cba-390">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="57cba-390">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




