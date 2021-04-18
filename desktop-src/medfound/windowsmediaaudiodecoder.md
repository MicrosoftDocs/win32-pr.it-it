---
description: Il decodificatore Windows Media Audio decodifica i flussi audio codificati dal codificatore Windows Media Audio.
ms.assetid: 2d8e4a97-34a7-4eee-9567-7ae98fa282b9
title: Decodificatore Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f11242f237b8d9709baea6d445a8426236913c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325954"
---
# <a name="windows-media-audio-decoder"></a><span data-ttu-id="a509e-103">Decodificatore Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="a509e-103">Windows Media Audio Decoder</span></span>

<span data-ttu-id="a509e-104">Il decodificatore Windows Media Audio decodifica i flussi audio codificati dal [**codificatore Windows Media Audio**](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="a509e-104">The Windows Media Audio decoder decodes audio streams that were encoded by the [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md).</span></span> <span data-ttu-id="a509e-105">Il codificatore e il decodificatore supportano tre categorie di audio codificato: Windows Media Audio standard, Windows Media Audio Professional e Windows Media Audio Lossless.</span><span class="sxs-lookup"><span data-stu-id="a509e-105">The encoder and decoder support three categories of encoded audio: Windows Media Audio Standard, Windows Media Audio Professional, and Windows Media Audio Lossless.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a509e-106">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="a509e-106">Class Identifier</span></span>

<span data-ttu-id="a509e-107">L'identificatore di classe (CLSID) per il decodificatore Windows Media Audio è rappresentato dalla costante **CLSID \_ CWMADecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="a509e-107">The class identifier (CLSID) for the Windows Media Audio decoder is represented by the constant **CLSID\_CWMADecMediaObject**.</span></span> <span data-ttu-id="a509e-108">È possibile creare un'istanza del decodificatore audio chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="a509e-108">You can create an instance of the audio decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="a509e-109">Formati di input</span><span class="sxs-lookup"><span data-stu-id="a509e-109">Input Formats</span></span>

<span data-ttu-id="a509e-110">La tabella seguente illustra i tag di formato audio che rappresentano le categorie di input supportate dal decodificatore Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="a509e-110">The following table shows the audio format tags that represent the input categories supported by the Windows Media Audio decoder.</span></span> <span data-ttu-id="a509e-111">Per informazioni su come impostare i tipi di input e output per il decodificatore, vedere [configurazione della decodifica audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="a509e-111">For information about how to set the input and output types for the decoder, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>



| <span data-ttu-id="a509e-112">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="a509e-112">Format tag constant</span></span>             | <span data-ttu-id="a509e-113">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="a509e-113">Format tag value</span></span> | <span data-ttu-id="a509e-114">Formato audio</span><span class="sxs-lookup"><span data-stu-id="a509e-114">Audio format</span></span>                     |
|---------------------------------|------------------|----------------------------------|
| <span data-ttu-id="a509e-115">\_Formato Wave \_ WMAUDIO2</span><span class="sxs-lookup"><span data-stu-id="a509e-115">WAVE\_FORMAT\_WMAUDIO2</span></span>          | <span data-ttu-id="a509e-116">0x0161</span><span class="sxs-lookup"><span data-stu-id="a509e-116">0x0161</span></span>           | <span data-ttu-id="a509e-117">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="a509e-117">Windows Media Audio Standard</span></span>     |
| <span data-ttu-id="a509e-118">\_Formato Wave \_ WMAUDIO3</span><span class="sxs-lookup"><span data-stu-id="a509e-118">WAVE\_FORMAT\_WMAUDIO3</span></span>          | <span data-ttu-id="a509e-119">0x0162</span><span class="sxs-lookup"><span data-stu-id="a509e-119">0x0162</span></span>           | <span data-ttu-id="a509e-120">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="a509e-120">Windows Media Audio Professional</span></span> |
| <span data-ttu-id="a509e-121">\_formato Wave \_ WMAUDIO \_ Lossless</span><span class="sxs-lookup"><span data-stu-id="a509e-121">WAVE\_FORMAT\_WMAUDIO\_LOSSLESS</span></span> | <span data-ttu-id="a509e-122">0x0163</span><span class="sxs-lookup"><span data-stu-id="a509e-122">0x0163</span></span>           | <span data-ttu-id="a509e-123">Windows Media Audio senza perdita di perdite</span><span class="sxs-lookup"><span data-stu-id="a509e-123">Windows Media Audio Lossless</span></span>     |



 

## <a name="output-formats"></a><span data-ttu-id="a509e-124">Formati di output</span><span class="sxs-lookup"><span data-stu-id="a509e-124">Output Formats</span></span>

<span data-ttu-id="a509e-125">La tabella seguente illustra i tag di formato audio che rappresentano i tipi di output supportati dal **Decodificatore Windows Media Audio**.</span><span class="sxs-lookup"><span data-stu-id="a509e-125">The following table shows the audio format tags that represent the output types supported by the **Windows Media Audio Decoder**.</span></span> <span data-ttu-id="a509e-126">Per informazioni su come impostare i tipi di input e output per il decodificatore, vedere [Configuring audio encoding](configuringaudioencoding.md).</span><span class="sxs-lookup"><span data-stu-id="a509e-126">For information about how to set the input and output types for the decoder, see [Configuring Audio Encoding](configuringaudioencoding.md).</span></span>



| <span data-ttu-id="a509e-127">Costante tag di formato</span><span class="sxs-lookup"><span data-stu-id="a509e-127">Format tag constant</span></span>       | <span data-ttu-id="a509e-128">Valore del tag di formato</span><span class="sxs-lookup"><span data-stu-id="a509e-128">Format tag value</span></span> | <span data-ttu-id="a509e-129">Formato audio</span><span class="sxs-lookup"><span data-stu-id="a509e-129">Audio format</span></span>                                          |
|---------------------------|------------------|-------------------------------------------------------|
| <span data-ttu-id="a509e-130">\_PCM in formato Wave \_</span><span class="sxs-lookup"><span data-stu-id="a509e-130">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="a509e-131">0x0001</span><span class="sxs-lookup"><span data-stu-id="a509e-131">0x0001</span></span>           | <span data-ttu-id="a509e-132">Formato PCM</span><span class="sxs-lookup"><span data-stu-id="a509e-132">PCM format</span></span>                                            |
| <span data-ttu-id="a509e-133">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="a509e-133">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="a509e-134">0x0003</span><span class="sxs-lookup"><span data-stu-id="a509e-134">0x0003</span></span>           | <span data-ttu-id="a509e-135">Virgola mobile IEEE</span><span class="sxs-lookup"><span data-stu-id="a509e-135">IEEE floating point</span></span>                                   |
| <span data-ttu-id="a509e-136">\_formato Wave \_ estendibile</span><span class="sxs-lookup"><span data-stu-id="a509e-136">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="a509e-137">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="a509e-137">0xFFFE</span></span>           | <span data-ttu-id="a509e-138">Formato PCM/IEEE nella struttura **WAVEFORMATEXTENSIBLE**</span><span class="sxs-lookup"><span data-stu-id="a509e-138">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="a509e-139">Interfacce</span><span class="sxs-lookup"><span data-stu-id="a509e-139">Interfaces</span></span>

<span data-ttu-id="a509e-140">Un oggetto Decoder audio espone l'interfaccia **IMediaObject** in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia **IMFTransform** in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="a509e-140">An audio decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="a509e-141">Un decodificatore Windows Media Audio si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a509e-141">A Windows Media Audio decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="a509e-142">Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore audio si comporta come DMO o MFT.</span><span class="sxs-lookup"><span data-stu-id="a509e-142">The following table shows the conditions under which an audio decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="a509e-143">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a509e-143">Operating system</span></span> | <span data-ttu-id="a509e-144">Comportamento del decodificatore</span><span class="sxs-lookup"><span data-stu-id="a509e-144">Decoder behavior</span></span>                                                                                                                                                                      |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a509e-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a509e-145">Windows XP</span></span>       | <span data-ttu-id="a509e-146">Un decodificatore Windows Media Audio si comporta sempre come DMO.</span><span class="sxs-lookup"><span data-stu-id="a509e-146">A Windows Media Audio decoder always behaves as a DMO.</span></span>                                                                                                                                |
| <span data-ttu-id="a509e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a509e-147">Windows Vista</span></span>    | <span data-ttu-id="a509e-148">Per impostazione predefinita, un decodificatore Windows Media Audio si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="a509e-148">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="a509e-149">Se si ottiene un'interfaccia **IMFTransform** o un'interfaccia **IPropertyStore** su un decodificatore audio, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="a509e-149">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on an audio decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="a509e-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a509e-150">Windows 7</span></span>        | <span data-ttu-id="a509e-151">Per impostazione predefinita, un decodificatore Windows Media Audio si comporta come DMO.</span><span class="sxs-lookup"><span data-stu-id="a509e-151">By default, a Windows Media Audio decoder behaves as a DMO.</span></span> <span data-ttu-id="a509e-152">Se si ottiene un'interfaccia **IMFTransform** su un decodificatore audio, si comporta come un MFT.</span><span class="sxs-lookup"><span data-stu-id="a509e-152">If you obtain an **IMFTransform** interface on an audio decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="properties"></a><span data-ttu-id="a509e-153">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a509e-153">Properties</span></span>

<span data-ttu-id="a509e-154">Il decodificatore Windows Media Audio supporta le seguenti proprietà.</span><span class="sxs-lookup"><span data-stu-id="a509e-154">The Windows Media Audio decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a509e-155">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a509e-155">Property</span></span></th>
<th><span data-ttu-id="a509e-156">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a509e-156">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a509e-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-157"><a href="mfpkey-decoder-maxnumpcmsampleswithpaddedsilenceproperty.md"><strong>MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence</strong></a></span></span></td>
<td><span data-ttu-id="a509e-158">Specifica il numero massimo di campioni PCM aggiuntivi che potrebbero essere restituiti alla fine della decodifica di un file.</span><span class="sxs-lookup"><span data-stu-id="a509e-158">Specifies the maximum number of additional PCM samples that might be returned at the end of decoding a file.</span></span><br/> <dl> <span data-ttu-id="a509e-159">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-159">Windows Vista and later.</span></span><br />
<span data-ttu-id="a509e-160">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="a509e-160">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-161">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a509e-161">Read-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a509e-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-162"><a href="mfpkey-wmadec-drcmodeproperty.md"><strong>MFPKEY_WMADEC_DRCMODE</strong></a></span></span></td>
<td><span data-ttu-id="a509e-163">Specifica la modalità di controllo dell'intervallo dinamico che viene utilizzata dal decodificatore audio.</span><span class="sxs-lookup"><span data-stu-id="a509e-163">Specifies the dynamic-range control mode that the audio decoder will use.</span></span><br/> <dl> <span data-ttu-id="a509e-164">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-164">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-165">Standard, Professional, lossless.</span><span class="sxs-lookup"><span data-stu-id="a509e-165">Standard, Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-166">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-166">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a509e-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-167"><a href="mfpkey-wmadec-folddown-matrixproperty.md"><strong>MFPKEY_WMADEC_FOLDDOWN_MATRIX</strong></a></span></span></td>
<td><span data-ttu-id="a509e-168">Specifica i coefficienti di riduzione forniti dall'autore per la decodifica dell'audio multicanale per un numero di canali inferiore rispetto al contenuto del flusso codificato.</span><span class="sxs-lookup"><span data-stu-id="a509e-168">Specifies the author-supplied fold-down coefficients for decoding multichannel audio for fewer channels than the encoded stream contains.</span></span> <br/> <dl> <span data-ttu-id="a509e-169">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-169">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-170">Professionale</span><span class="sxs-lookup"><span data-stu-id="a509e-170">Professional</span></span><br />
<span data-ttu-id="a509e-171">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-171">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a509e-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-172"><a href="mfpkey-wmadec-hiresoutputproperty.md"><strong>MFPKEY_WMADEC_HIRESOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="a509e-173">Specifica se il decodificatore audio deve fornire un output a risoluzione elevata.</span><span class="sxs-lookup"><span data-stu-id="a509e-173">Specifies whether the audio decoder should deliver high-resolution output.</span></span><br/> <dl> <span data-ttu-id="a509e-174">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-174">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-175">Professionale, senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="a509e-175">Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-176">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-176">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a509e-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-177"><a href="mfpkey-wmadec-ltrtoutputproperty.md"><strong>MFPKEY_WMADEC_LTRTOUTPUT</strong></a></span></span></td>
<td><span data-ttu-id="a509e-178">Specifica se il decodificatore audio deve eseguire Lt-Rt riduzioni.</span><span class="sxs-lookup"><span data-stu-id="a509e-178">Specifies whether the audio decoder should perform Lt-Rt fold down.</span></span><br/> <dl> <span data-ttu-id="a509e-179">Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-179">Windows Vista and later.</span></span><br />
<span data-ttu-id="a509e-180">Professional.</span><span class="sxs-lookup"><span data-stu-id="a509e-180">Professional.</span></span><br />
<span data-ttu-id="a509e-181">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-181">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a509e-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-182"><a href="mfpkey-wmadec-spkrcfgproperty.md"><strong>MFPKEY_WMADEC_SPKRCFG</strong></a></span></span></td>
<td><span data-ttu-id="a509e-183">Specifica la configurazione dell'altoparlante nel computer client.</span><span class="sxs-lookup"><span data-stu-id="a509e-183">Specifies the speaker configuration on the client computer.</span></span><br/> <dl> <span data-ttu-id="a509e-184">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-184">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-185">Professional.</span><span class="sxs-lookup"><span data-stu-id="a509e-185">Professional.</span></span><br />
<span data-ttu-id="a509e-186">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-186">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a509e-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-187"><a href="mfpkey-wmadrc-avgrefproperty.md"><strong>MFPKEY_WMADRC_AVGREF</strong></a></span></span></td>
<td><span data-ttu-id="a509e-188">Specifica il livello di volume medio del contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="a509e-188">Specifies the average volume level of audio content.</span></span><br/> <dl> <span data-ttu-id="a509e-189">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-189">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-190">Professionale, senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="a509e-190">Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-191">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-191">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a509e-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-192"><a href="mfpkey-wmadrc-avgtargetproperty.md"><strong>MFPKEY_WMADRC_AVGTARGET</strong></a></span></span></td>
<td><span data-ttu-id="a509e-193">Specifica il livello di volume medio desiderato per il contenuto audio di output.</span><span class="sxs-lookup"><span data-stu-id="a509e-193">Specifies the desired average volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="a509e-194">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-194">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-195">Professionale, senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="a509e-195">Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-196">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-196">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a509e-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-197"><a href="mfpkey-wmadrc-peakrefproperty.md"><strong>MFPKEY_WMADRC_PEAKREF</strong></a></span></span></td>
<td><span data-ttu-id="a509e-198">Specifica il livello di volume massimo che si verifica nel contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="a509e-198">Specifies the highest volume level occurring in audio content.</span></span><br/> <dl> <span data-ttu-id="a509e-199">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-199">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-200">Professionale, senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="a509e-200">Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-201">Proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-201">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a509e-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span><span class="sxs-lookup"><span data-stu-id="a509e-202"><a href="mfpkey-wmadrc-peaktargetproperty.md"><strong>MFPKEY_WMADRC_PEAKTARGET</strong></a></span></span></td>
<td><span data-ttu-id="a509e-203">Specifica il livello di volume massimo desiderato per il contenuto audio di output.</span><span class="sxs-lookup"><span data-stu-id="a509e-203">Specifies the desired maximum volume level of output audio content.</span></span><br/> <dl> <span data-ttu-id="a509e-204">Windows XP e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a509e-204">Windows XP and later.</span></span><br />
<span data-ttu-id="a509e-205">Professionale, senza perdita di perdite.</span><span class="sxs-lookup"><span data-stu-id="a509e-205">Professional, Lossless.</span></span><br />
<span data-ttu-id="a509e-206">Sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="a509e-206">Write-only.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="a509e-207">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a509e-207">Requirements</span></span>



| <span data-ttu-id="a509e-208">Requisito</span><span class="sxs-lookup"><span data-stu-id="a509e-208">Requirement</span></span> | <span data-ttu-id="a509e-209">Valore</span><span class="sxs-lookup"><span data-stu-id="a509e-209">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a509e-210">Client</span><span class="sxs-lookup"><span data-stu-id="a509e-210">Client</span></span><br/> | <span data-ttu-id="a509e-211">Windows XP, Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="a509e-211">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="a509e-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a509e-212">Header</span></span><br/> | <dl> <span data-ttu-id="a509e-213"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a509e-213"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="a509e-214">DLL</span><span class="sxs-lookup"><span data-stu-id="a509e-214">DLL</span></span><br/>    | <dl> <span data-ttu-id="a509e-215"><dt>Wmadmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a509e-215"><dt>Wmadmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a509e-216">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a509e-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a509e-217">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="a509e-217">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a509e-218">Implementazione del codec</span><span class="sxs-lookup"><span data-stu-id="a509e-218">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




