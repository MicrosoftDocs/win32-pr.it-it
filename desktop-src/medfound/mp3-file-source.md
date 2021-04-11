---
description: L'origine file MP3 analizza i file MP3.
ms.assetid: 37362642-1b8a-4fb3-950d-ed1afe3696e5
title: Origine file MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2241e3b99d5a1918be8ff0182a9eca8939c12ce2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130498"
---
# <a name="mp3-file-source"></a><span data-ttu-id="b3cbe-103">Origine file MP3</span><span class="sxs-lookup"><span data-stu-id="b3cbe-103">MP3 File Source</span></span>

<span data-ttu-id="b3cbe-104">L'origine file MP3 analizza i file MP3.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-104">The MP3 file source parses MP3 files.</span></span>

<span data-ttu-id="b3cbe-105">I buffer di output del file MP3 contengono i frame audio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-105">The MP3 file source outputs buffers that contain MPEG-1 audio frames.</span></span> <span data-ttu-id="b3cbe-106">Non decodifica l'audio.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-106">It does not decode the audio.</span></span>

## <a name="file-extensions-and-mime-types"></a><span data-ttu-id="b3cbe-107">Estensioni di file e tipi MIME</span><span class="sxs-lookup"><span data-stu-id="b3cbe-107">File Extensions and MIME Types</span></span>

<span data-ttu-id="b3cbe-108">L'origine file MP3 è l'origine multimediale predefinita per la seguente estensione del nome file:</span><span class="sxs-lookup"><span data-stu-id="b3cbe-108">The MP3 file source is the default media source for the following file name extension:</span></span>

-   <span data-ttu-id="b3cbe-109">mp3</span><span class="sxs-lookup"><span data-stu-id="b3cbe-109">.mp3</span></span>

<span data-ttu-id="b3cbe-110">È anche l'origine multimediale predefinita per i tipi MIME seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-110">It is also the default media source for the following MIME types.</span></span>

-   <span data-ttu-id="b3cbe-111">audio/MPEG</span><span class="sxs-lookup"><span data-stu-id="b3cbe-111">audio/mpeg</span></span>
-   <span data-ttu-id="b3cbe-112">audio/x-MP3</span><span class="sxs-lookup"><span data-stu-id="b3cbe-112">audio/x-mp3</span></span>
-   <span data-ttu-id="b3cbe-113">audio/x-MPEG</span><span class="sxs-lookup"><span data-stu-id="b3cbe-113">audio/x-mpeg</span></span>

## <a name="media-types"></a><span data-ttu-id="b3cbe-114">Tipi di supporto</span><span class="sxs-lookup"><span data-stu-id="b3cbe-114">Media Types</span></span>

<span data-ttu-id="b3cbe-115">Il tipo di supporto offerto dall'origine file MP3 contiene gli attributi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-115">The media type offered by the MP3 file source contains the following attributes.</span></span>



| <span data-ttu-id="b3cbe-116">Attributo</span><span class="sxs-lookup"><span data-stu-id="b3cbe-116">Attribute</span></span>                                                                                    | <span data-ttu-id="b3cbe-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3cbe-117">Description</span></span>                                                                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b3cbe-118">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-118">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="b3cbe-119">Uguale a **MFMediaType \_ audio**.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-119">Equal to **MFMediaType\_Audio**.</span></span>                                                                                                                   |
| [<span data-ttu-id="b3cbe-120">**sottotipo MF \_ mt \_**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-120">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="b3cbe-121">Uguale a **MFAudioFormat \_ MP3** o **MFAudioFormat \_ MPEG**.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-121">Equal to **MFAudioFormat\_MP3** or **MFAudioFormat\_MPEG**.</span></span>                                                                                        |
| [<span data-ttu-id="b3cbe-122">**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-122">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="b3cbe-123">Numero medio di byte al secondo.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-123">Average number of bytes per second.</span></span>                                                                                                                |
| [<span data-ttu-id="b3cbe-124">**\_ \_ \_ allineamento blocchi audio MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-124">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="b3cbe-125">Uguale a 1.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-125">Equal to 1.</span></span>                                                                                                                                        |
| [<span data-ttu-id="b3cbe-126">**numero \_ di \_ \_ canali audio MF mt \_**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-126">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="b3cbe-127">Numero dei canali audio.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-127">Number of audio channels.</span></span>                                                                                                                          |
| [<span data-ttu-id="b3cbe-128">**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-128">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="b3cbe-129">Numero di campioni audio al secondo.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-129">Number of audio samples per second.</span></span>                                                                                                                |
| [<span data-ttu-id="b3cbe-130">**\_ \_ dati utente MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-130">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                      | <span data-ttu-id="b3cbe-131">Contiene la parte di una struttura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) visualizzata dopo il membro **wfx** della struttura.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-131">Contains the portion of a [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure that appears after the **wfx** member of the structure.</span></span> |



 

## <a name="interfaces"></a><span data-ttu-id="b3cbe-132">Interfacce</span><span class="sxs-lookup"><span data-stu-id="b3cbe-132">Interfaces</span></span>

<span data-ttu-id="b3cbe-133">L'origine file MP3 espone le interfacce seguenti tramite [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span><span class="sxs-lookup"><span data-stu-id="b3cbe-133">The MP3 file source exposes the following interfaces through [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)):</span></span>

-   [<span data-ttu-id="b3cbe-134">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-134">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="b3cbe-135">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-135">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
-   [<span data-ttu-id="b3cbe-136">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-136">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

<span data-ttu-id="b3cbe-137">Espone inoltre le interfacce seguenti tramite [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span><span class="sxs-lookup"><span data-stu-id="b3cbe-137">In addition, it exposes the following interfaces through [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3cbe-138">GUID servizio</span><span class="sxs-lookup"><span data-stu-id="b3cbe-138">Service GUID</span></span></th>
<th><span data-ttu-id="b3cbe-139">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="b3cbe-139">Interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3cbe-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b3cbe-140"><strong>MF_METADATA_PROVIDER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b3cbe-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3cbe-141"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3cbe-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b3cbe-142"><strong>MF_PROPERTY_HANDLER_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b3cbe-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span><span class="sxs-lookup"><span data-stu-id="b3cbe-143"><a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore"><strong>IPropertyStore</strong></a>
</span></span><blockquote>
[!Note]<br />
<span data-ttu-id="b3cbe-144">Vedere <a href="shell-metadata-providers.md">provider di metadati della shell</a>.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-144">See <a href="shell-metadata-providers.md">Shell Metadata Providers</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3cbe-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b3cbe-145"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b3cbe-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3cbe-146"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3cbe-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="b3cbe-147"><strong>MF_RATE_CONTROL_SERVICE</strong></span></span></td>
<td><span data-ttu-id="b3cbe-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3cbe-148"><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b3cbe-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3cbe-149">Requirements</span></span>



| <span data-ttu-id="b3cbe-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cbe-150">Requirement</span></span> | <span data-ttu-id="b3cbe-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b3cbe-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b3cbe-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbe-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cbe-153">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b3cbe-153">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b3cbe-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbe-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cbe-155">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b3cbe-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b3cbe-156">DLL</span><span class="sxs-lookup"><span data-stu-id="b3cbe-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3cbe-157"><dt>Mf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbe-157"><dt>Mf.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3cbe-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3cbe-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3cbe-159">Origini e sink multimediali</span><span class="sxs-lookup"><span data-stu-id="b3cbe-159">Media Sources and Sinks</span></span>](media-sources-and-sinks.md)
</dt> <dt>

[<span data-ttu-id="b3cbe-160">Origini supporti</span><span class="sxs-lookup"><span data-stu-id="b3cbe-160">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="b3cbe-161">Resolver di origine</span><span class="sxs-lookup"><span data-stu-id="b3cbe-161">Source Resolver</span></span>](source-resolver.md)
</dt> <dt>

[<span data-ttu-id="b3cbe-162">Formati multimediali supportati in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3cbe-162">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

 
