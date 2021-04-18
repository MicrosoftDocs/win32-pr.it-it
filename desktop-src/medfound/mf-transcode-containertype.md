---
description: Specifica il tipo di contenitore di un file codificato.
ms.assetid: 97fd968a-6843-4695-aece-02f9acd618fd
title: Attributo MF_TRANSCODE_CONTAINERTYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f86b8d5890a771200feda265c3878b6eb7030b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308429"
---
# <a name="mf_transcode_containertype-attribute"></a><span data-ttu-id="992b8-103">\_Attributo transcode \_ CONTAINERTYPE MF</span><span class="sxs-lookup"><span data-stu-id="992b8-103">MF\_TRANSCODE\_CONTAINERTYPE attribute</span></span>

<span data-ttu-id="992b8-104">Specifica il tipo di contenitore di un file codificato.</span><span class="sxs-lookup"><span data-stu-id="992b8-104">Specifies the container type of an encoded file.</span></span> <span data-ttu-id="992b8-105">I tipi di contenitore sono supportati da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="992b8-105">The container types are supported by Media Foundation.</span></span>

## <a name="data-type"></a><span data-ttu-id="992b8-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="992b8-106">Data type</span></span>

<span data-ttu-id="992b8-107">**GUID**</span><span class="sxs-lookup"><span data-stu-id="992b8-107">**GUID**</span></span>

<span data-ttu-id="992b8-108">Nella tabella seguente sono descritti i valori possibili per i tipi di contenitore forniti da Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="992b8-108">Possible values for the container types provided by Media Foundation are described in the following table.</span></span>



| <span data-ttu-id="992b8-109">Valore</span><span class="sxs-lookup"><span data-stu-id="992b8-109">Value</span></span>                                                                                                                                                                                                                                                                 | <span data-ttu-id="992b8-110">Significato</span><span class="sxs-lookup"><span data-stu-id="992b8-110">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="MFTranscodeContainerType_ASF"></span><span id="mftranscodecontainertype_asf"></span><span id="MFTRANSCODECONTAINERTYPE_ASF"></span><dl> <span data-ttu-id="992b8-111"><dt>**\_ASF MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-111"><dt>**MFTranscodeContainerType\_ASF**</dt></span></span> </dl>             | <span data-ttu-id="992b8-112">Contenitore di file ASF.</span><span class="sxs-lookup"><span data-stu-id="992b8-112">ASF file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MPEG4"></span><span id="mftranscodecontainertype_mpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG4"></span><dl> <span data-ttu-id="992b8-113"><dt>**\_MPEG4 MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-113"><dt>**MFTranscodeContainerType\_MPEG4**</dt></span></span> </dl>     | <span data-ttu-id="992b8-114">Contenitore di file MP4.</span><span class="sxs-lookup"><span data-stu-id="992b8-114">MP4 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_MP3"></span><span id="mftranscodecontainertype_mp3"></span><span id="MFTRANSCODECONTAINERTYPE_MP3"></span><dl> <span data-ttu-id="992b8-115"><dt>**MFTranscodeContainerType \_ MP3**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-115"><dt>**MFTranscodeContainerType\_MP3**</dt></span></span> </dl>             | <span data-ttu-id="992b8-116">Contenitore di file MP3.</span><span class="sxs-lookup"><span data-stu-id="992b8-116">MP3 file container.</span></span><br/>                                                     |
| <span id="MFTranscodeContainerType_3GP"></span><span id="mftranscodecontainertype_3gp"></span><span id="MFTRANSCODECONTAINERTYPE_3GP"></span><dl> <span data-ttu-id="992b8-117"><dt>**MFTranscodeContainerType \_ 3GP**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-117"><dt>**MFTranscodeContainerType\_3GP**</dt></span></span> </dl>             | <span data-ttu-id="992b8-118">contenitore di file 3GP.</span><span class="sxs-lookup"><span data-stu-id="992b8-118">3GP file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_AC3"></span><span id="mftranscodecontainertype_ac3"></span><span id="MFTRANSCODECONTAINERTYPE_AC3"></span><dl> <span data-ttu-id="992b8-119"><dt>**MFTranscodeContainerType \_ AC3**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-119"><dt>**MFTranscodeContainerType\_AC3**</dt></span></span> </dl>             | <span data-ttu-id="992b8-120">Contenitore di file AC3.</span><span class="sxs-lookup"><span data-stu-id="992b8-120">AC3 file container.</span></span> <br/>                                                    |
| <span id="MFTranscodeContainerType_ADTS"></span><span id="mftranscodecontainertype_adts"></span><span id="MFTRANSCODECONTAINERTYPE_ADTS"></span><dl> <span data-ttu-id="992b8-121"><dt>**\_ADTS MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-121"><dt>**MFTranscodeContainerType\_ADTS**</dt></span></span> </dl>         | <span data-ttu-id="992b8-122">Contenitore di file ADTS.</span><span class="sxs-lookup"><span data-stu-id="992b8-122">ADTS file container.</span></span> <br/>                                                   |
| <span id="MFTranscodeContainerType_MPEG2"></span><span id="mftranscodecontainertype_mpeg2"></span><span id="MFTRANSCODECONTAINERTYPE_MPEG2"></span><dl> <span data-ttu-id="992b8-123"><dt>**MFTranscodeContainerType \_ MPEG2**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-123"><dt>**MFTranscodeContainerType\_MPEG2**</dt></span></span> </dl>     | <span data-ttu-id="992b8-124">Contenitore di file MPEG2.</span><span class="sxs-lookup"><span data-stu-id="992b8-124">MPEG2 file container.</span></span> <br/>                                                  |
| <span id="MFTranscodeContainerType_FMPEG4"></span><span id="mftranscodecontainertype_fmpeg4"></span><span id="MFTRANSCODECONTAINERTYPE_FMPEG4"></span><dl> <span data-ttu-id="992b8-125"><dt>**\_FMPEG4 MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-125"><dt>**MFTranscodeContainerType\_FMPEG4**</dt></span></span> </dl> | <span data-ttu-id="992b8-126">Contenitore di file FMPEG4.</span><span class="sxs-lookup"><span data-stu-id="992b8-126">FMPEG4 file container.</span></span> <br/>                                                 |
| <span id="MFTranscodeContainerType_WAVE"></span><span id="mftranscodecontainertype_wave"></span><span id="MFTRANSCODECONTAINERTYPE_WAVE"></span><dl> <span data-ttu-id="992b8-127"><dt>**MFTranscodeContainerType \_ Wave**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-127"><dt>**MFTranscodeContainerType\_WAVE**</dt></span></span> </dl>         | <span data-ttu-id="992b8-128">Contenitore di file WAVE.</span><span class="sxs-lookup"><span data-stu-id="992b8-128">WAVE file container.</span></span><br/> <span data-ttu-id="992b8-129">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="992b8-129">Supported in Windows 8.1 and and later.</span></span><br/> |
| <span id="MFTranscodeContainerType_AVI"></span><span id="mftranscodecontainertype_avi"></span><span id="MFTRANSCODECONTAINERTYPE_AVI"></span><dl> <span data-ttu-id="992b8-130"><dt>**MFTranscodeContainerType \_ AVI**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-130"><dt>**MFTranscodeContainerType\_AVI**</dt></span></span> </dl>             | <span data-ttu-id="992b8-131">Contenitore di file AVI.</span><span class="sxs-lookup"><span data-stu-id="992b8-131">AVI file container.</span></span><br/> <span data-ttu-id="992b8-132">Supportato in Windows 8.1 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="992b8-132">Supported in Windows 8.1 and and later.</span></span><br/>  |
| <span id="MFTranscodeContainerType_AMR"></span><span id="mftranscodecontainertype_amr"></span><span id="MFTRANSCODECONTAINERTYPE_AMR"></span><dl> <span data-ttu-id="992b8-133"><dt>**\_AMR MFTranscodeContainerType**</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-133"><dt>**MFTranscodeContainerType\_AMR**</dt></span></span> </dl>             | <span data-ttu-id="992b8-134">Contenitore di file AMR.</span><span class="sxs-lookup"><span data-stu-id="992b8-134">AMR file container.</span></span> <br/>                                                    |



 

## <a name="getset"></a><span data-ttu-id="992b8-135">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="992b8-135">Get/set</span></span>

<span data-ttu-id="992b8-136">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="992b8-136">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="992b8-137">Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="992b8-137">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="992b8-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="992b8-138">Remarks</span></span>

<span data-ttu-id="992b8-139">Questo attributo viene utilizzato sia con la funzionalità di transcodifica veloce che con l'oggetto sink writer.</span><span class="sxs-lookup"><span data-stu-id="992b8-139">This attribute is used with both the Fast Transcode feature and the sink writer object.</span></span>

<span data-ttu-id="992b8-140">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="992b8-140">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="fast-transcode"></a><span data-ttu-id="992b8-141">Transcodifica veloce</span><span class="sxs-lookup"><span data-stu-id="992b8-141">Fast Transcode</span></span>

<span data-ttu-id="992b8-142">Prima di compilare la topologia transcodifica, l'applicazione deve impostare l'attributo del contenitore sul profilo transcode.</span><span class="sxs-lookup"><span data-stu-id="992b8-142">The application must set the container attribute on the transcode profile before building the transcode topology.</span></span> <span data-ttu-id="992b8-143">Il generatore di topologie analizza questo attributo e carica il sink multimediale appropriato nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="992b8-143">The topology builder analyses this attribute and loads the appropriate media sink in the pipeline.</span></span> <span data-ttu-id="992b8-144">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="992b8-144">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="992b8-145">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="992b8-145">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
-   [<span data-ttu-id="992b8-146">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="992b8-146">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)

### <a name="sink-writer"></a><span data-ttu-id="992b8-147">Writer sink</span><span class="sxs-lookup"><span data-stu-id="992b8-147">Sink Writer</span></span>

<span data-ttu-id="992b8-148">Questo attributo può essere usato per configurare il tipo di contenitore di file per il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="992b8-148">This attribute can be used to configure the file-container type for the sink writer.</span></span> <span data-ttu-id="992b8-149">Per altre informazioni, vedere [sink writer Attributes](sink-writer-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="992b8-149">For more information, see [Sink Writer Attributes](sink-writer-attributes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="992b8-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="992b8-150">Requirements</span></span>



| <span data-ttu-id="992b8-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="992b8-151">Requirement</span></span> | <span data-ttu-id="992b8-152">Valore</span><span class="sxs-lookup"><span data-stu-id="992b8-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="992b8-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="992b8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="992b8-154">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="992b8-154">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="992b8-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="992b8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="992b8-156">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="992b8-156">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="992b8-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="992b8-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="992b8-158"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="992b8-158"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992b8-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="992b8-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992b8-160">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="992b8-160">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="992b8-161">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="992b8-161">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 




