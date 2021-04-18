---
description: Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).
ms.assetid: 9a6b6402-ff53-4399-8616-06b7768a8737
title: Attributo MF_TRANSCODE_ENCODINGPROFILE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020344cb2c2f6fc4a539c7cdbc8df0dc69d80d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527408"
---
# <a name="mf_transcode_encodingprofile-attribute"></a><span data-ttu-id="cbbcb-103">\_Attributo transcode \_ ENCODINGPROFILE MF</span><span class="sxs-lookup"><span data-stu-id="cbbcb-103">MF\_TRANSCODE\_ENCODINGPROFILE attribute</span></span>

<span data-ttu-id="cbbcb-104">Specifica il profilo di conformità del dispositivo per la codifica di file ASF (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="cbbcb-104">Specifies the device conformance profile for encoding Advanced Streaming Format (ASF) files.</span></span>

## <a name="data-type"></a><span data-ttu-id="cbbcb-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cbbcb-105">Data type</span></span>

<span data-ttu-id="cbbcb-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cbbcb-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="cbbcb-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="cbbcb-107">Get/set</span></span>

<span data-ttu-id="cbbcb-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span><span class="sxs-lookup"><span data-stu-id="cbbcb-108">To get this attribute, call [**IMFAttributes::GetAllocatedString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getallocatedstring).</span></span>

<span data-ttu-id="cbbcb-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="cbbcb-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="remarks"></a><span data-ttu-id="cbbcb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbbcb-110">Remarks</span></span>

<span data-ttu-id="cbbcb-111">Usare questo attributo per la transcodifica in un dispositivo che supporta Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-111">Use this attribute when transcoding to a device that supports Windows Media.</span></span> <span data-ttu-id="cbbcb-112">Se questo attributo è impostato, il codificatore utilizzerà il profilo di conformità del dispositivo, o modello, per i codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-112">If this attribute is set, the encoder will use the device conformance profile, or template, for Windows Media codecs.</span></span> <span data-ttu-id="cbbcb-113">Impostare l'attributo sul profilo transcode prima di compilare la topologia transcodifica.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-113">Set the attribute on the transcode profile before building the transcode topology.</span></span>

<span data-ttu-id="cbbcb-114">Il valore di questo attributo può essere una qualsiasi delle stringhe di modello di conformità elencate negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbbcb-114">The value of this attribute can be any of the conformance template strings listed in the following topics:</span></span>

-   [<span data-ttu-id="cbbcb-115">Modelli di conformità del dispositivo audio</span><span class="sxs-lookup"><span data-stu-id="cbbcb-115">Audio Device Conformance Templates</span></span>](../wmformat/audio-device-conformance-templates.md)
-   [<span data-ttu-id="cbbcb-116">Modelli di conformità del dispositivo video</span><span class="sxs-lookup"><span data-stu-id="cbbcb-116">Video Device Conformance Templates</span></span>](../wmformat/video-device-conformance-templates.md)

<span data-ttu-id="cbbcb-117">Per Windows Media Video codifica, il generatore di topologia utilizza questo attributo per impostare la proprietà [**MFPKEY \_ DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-117">For Windows Media Video encoding, the topology builder uses this attribute to set the [**MFPKEY\_DECODERCOMPLEXITYREQUESTED**](mfpkey-decodercomplexityrequestedproperty.md) property on the encoder.</span></span> <span data-ttu-id="cbbcb-118">Il codificatore tenterà di utilizzare il modello specificato per codificare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-118">The encoder will attempt to use the specified template to encode the content.</span></span> <span data-ttu-id="cbbcb-119">Per ottenere il modello effettivo, attraversare i nodi della topologia transcodifica per ottenere un puntatore al nodo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-119">To get the actual template, traverse the nodes of the transcode topology to get a pointer to the encoder node.</span></span> <span data-ttu-id="cbbcb-120">Ottenere quindi il valore della proprietà [**\_ DECODERCOMPLEXITYPROFILE di MFPKEY**](mfpkey-decodercomplexityprofileproperty.md) dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-120">Then get the value of the [**MFPKEY\_DECODERCOMPLEXITYPROFILE**](mfpkey-decodercomplexityprofileproperty.md) property from the encoder.</span></span>

<span data-ttu-id="cbbcb-121">Il generatore di topologia usa inoltre il valore di questo attributo per impostare la proprietà "DeviceConformanceTemplate" sul sink multimediale ASF.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-121">The topology builder also uses the value of this attribute to set the "DeviceConformanceTemplate" property on the ASF media sink.</span></span>

<span data-ttu-id="cbbcb-122">Se questo attributo è impostato, l'oggetto di metadati del file ASF viene sempre generato indipendentemente dal valore specificato dall'applicazione dell'attributo [MF \_ transcode \_ Skip \_ Metadata \_ Transfer](mf-transcode-skip-metadata-transfer.md) .</span><span class="sxs-lookup"><span data-stu-id="cbbcb-122">If this attribute is set, the metadata object of the ASF file is always generated irrespective of the application-specified value of the [MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER](mf-transcode-skip-metadata-transfer.md) attribute.</span></span>

<span data-ttu-id="cbbcb-123">I valori tipici di questo attributo includono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cbbcb-123">Typical values for this attribute include the following:</span></span>



| <span data-ttu-id="cbbcb-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cbbcb-124">Value</span></span>   | <span data-ttu-id="cbbcb-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbbcb-125">Description</span></span>                      |
|---------|----------------------------------|
| <span data-ttu-id="cbbcb-126">Asia Pacifico</span><span class="sxs-lookup"><span data-stu-id="cbbcb-126">"AP"</span></span>    | <span data-ttu-id="cbbcb-127">Video profilo avanzato</span><span class="sxs-lookup"><span data-stu-id="cbbcb-127">Advanced profile video</span></span>           |
| <span data-ttu-id="cbbcb-128">MP</span><span class="sxs-lookup"><span data-stu-id="cbbcb-128">"MP"</span></span>    | <span data-ttu-id="cbbcb-129">Video del profilo principale</span><span class="sxs-lookup"><span data-stu-id="cbbcb-129">Main profile video</span></span>               |
| <span data-ttu-id="cbbcb-130">SP</span><span class="sxs-lookup"><span data-stu-id="cbbcb-130">"SP"</span></span>    | <span data-ttu-id="cbbcb-131">Video di profilo semplice</span><span class="sxs-lookup"><span data-stu-id="cbbcb-131">Simple profile video</span></span>             |
| <span data-ttu-id="cbbcb-132">"MP@LL"</span><span class="sxs-lookup"><span data-stu-id="cbbcb-132">"MP@LL"</span></span> | <span data-ttu-id="cbbcb-133">Profilo principale, video di livello medio</span><span class="sxs-lookup"><span data-stu-id="cbbcb-133">Main profile, medium level video</span></span> |
| <span data-ttu-id="cbbcb-134">L2</span><span class="sxs-lookup"><span data-stu-id="cbbcb-134">"L2"</span></span>    | <span data-ttu-id="cbbcb-135">Profilo audio, <= 160 Kbps</span><span class="sxs-lookup"><span data-stu-id="cbbcb-135">Audio profile, <= 160 Kbps</span></span>    |



 

<span data-ttu-id="cbbcb-136">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cbbcb-136">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbbcb-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cbbcb-137">Requirements</span></span>



| <span data-ttu-id="cbbcb-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbbcb-138">Requirement</span></span> | <span data-ttu-id="cbbcb-139">Valore</span><span class="sxs-lookup"><span data-stu-id="cbbcb-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cbbcb-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbbcb-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cbbcb-141">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cbbcb-141">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cbbcb-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cbbcb-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cbbcb-143">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbbcb-143">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cbbcb-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cbbcb-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbbcb-145"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbbcb-145"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbbcb-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbbcb-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbbcb-147">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cbbcb-147">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cbbcb-148">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="cbbcb-148">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="cbbcb-149">**IMFTranscodeProfile::GetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="cbbcb-149">**IMFTranscodeProfile::GetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getaudioattributes)
</dt> <dt>

[<span data-ttu-id="cbbcb-150">**IMFTranscodeProfile::SetAudioAttributes**</span><span class="sxs-lookup"><span data-stu-id="cbbcb-150">**IMFTranscodeProfile::SetAudioAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
</dt> <dt>

[<span data-ttu-id="cbbcb-151">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="cbbcb-151">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getvideoattributes)
</dt> <dt>

[<span data-ttu-id="cbbcb-152">**IMFTranscodeProfile::GetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="cbbcb-152">**IMFTranscodeProfile::GetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
