---
description: Microsoft MPEG audio decoder è una trasformazione di Media Foundation sincrona (MFT) che consente di decodificare i formati MPEG audio Elementary Stream usando la pipeline Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Decoder audio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966987"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="73bbb-103">Decoder audio MPEG</span><span class="sxs-lookup"><span data-stu-id="73bbb-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="73bbb-104">Microsoft MPEG audio decoder è una trasformazione di [Media Foundation](media-foundation-transforms.md) sincrona (MFT) che consente di decodificare i formati MPEG audio Elementary Stream usando la pipeline Media Foundation (MF).</span><span class="sxs-lookup"><span data-stu-id="73bbb-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="73bbb-105">Il decodificatore supporta i formati MPEG Elementary Stream seguenti.</span><span class="sxs-lookup"><span data-stu-id="73bbb-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="73bbb-106">MPEG-1 Audio Layer I e II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="73bbb-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="73bbb-107">2.</span><span class="sxs-lookup"><span data-stu-id="73bbb-107">2.</span></span> <span data-ttu-id="73bbb-108">MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO</span><span class="sxs-lookup"><span data-stu-id="73bbb-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="73bbb-109">MPEG-2 compatibile con le versioni precedenti, livelli I e II (ISO/IEC 13818-3), solo mono e stereo</span><span class="sxs-lookup"><span data-stu-id="73bbb-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="73bbb-110">Identificatore di classe</span><span class="sxs-lookup"><span data-stu-id="73bbb-110">Class Identifier</span></span>

<span data-ttu-id="73bbb-111">L'identificatore di classe (CLSID) del decodificatore audio MPEG è **CLSID \_ MSMPEGAudDecMFT**, definito nel file di intestazione wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="73bbb-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="73bbb-112">Tipi di supporti di input</span><span class="sxs-lookup"><span data-stu-id="73bbb-112">Input Media Types</span></span>

<span data-ttu-id="73bbb-113">Il decodificatore audio MPEG supporta gli attributi di tipo supporto di input seguenti.</span><span class="sxs-lookup"><span data-stu-id="73bbb-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="73bbb-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="73bbb-114">Attribute</span></span>                                                                               | <span data-ttu-id="73bbb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="73bbb-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73bbb-116">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="73bbb-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="73bbb-117">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="73bbb-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="73bbb-118">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="73bbb-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="73bbb-119">**\_MPEG MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="73bbb-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="73bbb-120">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="73bbb-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="73bbb-121">Opzionale In genere 1 per mono o 2 per stereo, ma può essere composto da un massimo di 6 canali.</span><span class="sxs-lookup"><span data-stu-id="73bbb-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="73bbb-122">**\_ \_ \_ maschera canale audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="73bbb-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="73bbb-123">Opzionale In genere 0x4 per mono o 0x3 per stereo, ma può anche essere una qualsiasi delle maschere di canale associate a un massimo di 6 canali (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="73bbb-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="73bbb-124">Se presente, la maschera del canale deve essere coerente con il numero di canali di input specificato.</span><span class="sxs-lookup"><span data-stu-id="73bbb-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="73bbb-125">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="73bbb-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="73bbb-126">Opzionale Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="73bbb-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="73bbb-127">Se specificato, la frequenza di campionamento dell'input deve essere una delle frequenze di campionamento MPEG valide.</span><span class="sxs-lookup"><span data-stu-id="73bbb-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="73bbb-128">Tipi di supporti di output</span><span class="sxs-lookup"><span data-stu-id="73bbb-128">Output Media Types</span></span>

<span data-ttu-id="73bbb-129">Il decodificatore audio MPEG supporta fino a quattro sottotipi di supporti di output, nell'ordine seguente.</span><span class="sxs-lookup"><span data-stu-id="73bbb-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="73bbb-130">Stereo, a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="73bbb-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="73bbb-131">Stereo a 16 bit PCM.</span><span class="sxs-lookup"><span data-stu-id="73bbb-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="73bbb-132">Mono, virgola mobile (solo se l'input è mono o dual-mono).</span><span class="sxs-lookup"><span data-stu-id="73bbb-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="73bbb-133">Mono, PCM a 16 bit (solo se l'input è mono o dual-mono).</span><span class="sxs-lookup"><span data-stu-id="73bbb-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="73bbb-134">Il decodificatore supporta sempre l'output stereo ed è enumerato come primo tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="73bbb-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="73bbb-135">Il decodificatore supporta gli attributi di tipo supporto di output seguenti.</span><span class="sxs-lookup"><span data-stu-id="73bbb-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="73bbb-136">Attributo</span><span class="sxs-lookup"><span data-stu-id="73bbb-136">Attribute</span></span>                                                                           | <span data-ttu-id="73bbb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="73bbb-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="73bbb-138">\_ \_ tipo principale MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="73bbb-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="73bbb-139">**\_Audio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="73bbb-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="73bbb-140">sottotipo MF \_ mt \_</span><span class="sxs-lookup"><span data-stu-id="73bbb-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="73bbb-141">**MFAudioFormat \_ PCM** o **MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="73bbb-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="73bbb-142">\_ \_ bit audio MF \_ mt \_ per \_ campione</span><span class="sxs-lookup"><span data-stu-id="73bbb-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="73bbb-143">16 o 32</span><span class="sxs-lookup"><span data-stu-id="73bbb-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="73bbb-144">numero \_ di \_ \_ canali audio MF mt \_</span><span class="sxs-lookup"><span data-stu-id="73bbb-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="73bbb-145">1 o 2</span><span class="sxs-lookup"><span data-stu-id="73bbb-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="73bbb-146">\_ \_ \_ maschera canale audio MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="73bbb-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="73bbb-147">0x4 per mono o 0x3 per stereo</span><span class="sxs-lookup"><span data-stu-id="73bbb-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="73bbb-148">\_ \_ campioni audio MF \_ mt \_ al \_ secondo</span><span class="sxs-lookup"><span data-stu-id="73bbb-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="73bbb-149">Uno dei seguenti: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="73bbb-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="73bbb-150">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="73bbb-150">Transform Attributes</span></span>

<span data-ttu-id="73bbb-151">Il decodificatore MPEG audio implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="73bbb-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="73bbb-152">Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="73bbb-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="73bbb-153">Attributo</span><span class="sxs-lookup"><span data-stu-id="73bbb-153">Attribute</span></span>                                                                               | <span data-ttu-id="73bbb-154">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73bbb-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73bbb-155">**Codecapis \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="73bbb-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="73bbb-156">Specifica se l'audio a 2 canali da decodificare è dual mono o meno.</span><span class="sxs-lookup"><span data-stu-id="73bbb-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="73bbb-157">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="73bbb-157">Read-only.</span></span> <span data-ttu-id="73bbb-158">Impostato dal MFT.</span><span class="sxs-lookup"><span data-stu-id="73bbb-158">Set by the MFT.</span></span> <span data-ttu-id="73bbb-159">Per ulteriori informazioni, vedere [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="73bbb-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="73bbb-160">**Codecapis \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="73bbb-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="73bbb-161">Specifica il modo in cui il decodificatore riproduce audio mono doppio.</span><span class="sxs-lookup"><span data-stu-id="73bbb-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="73bbb-162">Il valore predefinito è **eAVDecAudioDualMonoReproMode \_ Left \_ mono**.</span><span class="sxs-lookup"><span data-stu-id="73bbb-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="73bbb-163">Lettura/Scrittura.</span><span class="sxs-lookup"><span data-stu-id="73bbb-163">Read/Write.</span></span> <span data-ttu-id="73bbb-164">Le applicazioni possono impostare questa proprietà per modificare il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="73bbb-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="73bbb-165">Per ulteriori informazioni, vedere [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="73bbb-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="73bbb-166">**Codecapis \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="73bbb-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="73bbb-167">Specifica la velocità in bit del flusso compresso.</span><span class="sxs-lookup"><span data-stu-id="73bbb-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="73bbb-168">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="73bbb-168">Read-only.</span></span> <span data-ttu-id="73bbb-169">Impostato dal MFT.</span><span class="sxs-lookup"><span data-stu-id="73bbb-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="73bbb-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73bbb-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bbb-171">Oggetti codec</span><span class="sxs-lookup"><span data-stu-id="73bbb-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
