---
description: I seguenti GUID definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).
ms.assetid: db973b41-1e5c-4bc8-921d-5e9312eb21cb
title: GUID estensione payload ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7dbd27212c8f4812360ba22f89a717659307f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524665"
---
# <a name="asf-payload-extension-guids"></a><span data-ttu-id="919e4-103">GUID estensione payload ASF</span><span class="sxs-lookup"><span data-stu-id="919e4-103">ASF Payload Extension GUIDs</span></span>

<span data-ttu-id="919e4-104">I seguenti GUID definiscono le estensioni del payload per i flussi ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="919e4-104">The following GUIDs define payload extensions for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="919e4-105">Costante</span><span class="sxs-lookup"><span data-stu-id="919e4-105">Constant</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="919e4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="919e4-106">Description</span></span>                                                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFSampleExtension_SampleDuration"></span><span id="mfasfsampleextension_sampleduration"></span><span id="MFASFSAMPLEEXTENSION_SAMPLEDURATION"></span><dl> <span data-ttu-id="919e4-107"><dt>**\_SampleDuration MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-107"><dt>**MFASFSampleExtension\_SampleDuration**</dt></span></span> </dl>         | <span data-ttu-id="919e4-108">I dati indicano la durata, in millisecondi, dell'esempio contenuto nell'oggetto buffer.</span><span class="sxs-lookup"><span data-stu-id="919e4-108">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span><br/>                                                                       |
| <span id="MFASFSampleExtension_OutputCleanPoint"></span><span id="mfasfsampleextension_outputcleanpoint"></span><span id="MFASFSAMPLEEXTENSION_OUTPUTCLEANPOINT"></span><dl> <span data-ttu-id="919e4-109"><dt>**\_OutputCleanPoint MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-109"><dt>**MFASFSampleExtension\_OutputCleanPoint**</dt></span></span> </dl> | <span data-ttu-id="919e4-110">I dati indicano se l'esempio è un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="919e4-110">The data indicates whether the sample is a key frame.</span></span> <span data-ttu-id="919e4-111">Un valore pari a zero indica che l'esempio non è un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="919e4-111">A value of zero indicates that the sample is not a key frame.</span></span> <span data-ttu-id="919e4-112">Un valore diverso da zero indica che si tratta di un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="919e4-112">A nonzero value indicates that it is a key frame.</span></span><br/> |
| <span id="MFASFSampleExtension_SMPTE"></span><span id="mfasfsampleextension_smpte"></span><span id="MFASFSAMPLEEXTENSION_SMPTE"></span><dl> <span data-ttu-id="919e4-113"><dt>**\_SMPTE MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-113"><dt>**MFASFSampleExtension\_SMPTE**</dt></span></span> </dl>                                             | <span data-ttu-id="919e4-114">I dati sono un codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="919e4-114">The data is a SMPTE time code.</span></span><br/>                                                                                                                                        |
| <span id="MFASFSampleExtension_FileName"></span><span id="mfasfsampleextension_filename"></span><span id="MFASFSAMPLEEXTENSION_FILENAME"></span><dl> <span data-ttu-id="919e4-115"><dt>**\_Nome file MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-115"><dt>**MFASFSampleExtension\_FileName**</dt></span></span> </dl>                                 | <span data-ttu-id="919e4-116">I dati nell'estensione di esempio specificano il nome del file da cui è stato utilizzato il contenuto del campione.</span><span class="sxs-lookup"><span data-stu-id="919e4-116">The data in the sample extension specifies the name of the file from which the content in the sample was taken.</span></span><br/>                                                       |
| <span id="MFASFSampleExtension_ContentType"></span><span id="mfasfsampleextension_contenttype"></span><span id="MFASFSAMPLEEXTENSION_CONTENTTYPE"></span><dl> <span data-ttu-id="919e4-117"><dt>**\_ContentType MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-117"><dt>**MFASFSampleExtension\_ContentType**</dt></span></span> </dl>                     | <span data-ttu-id="919e4-118">I dati identificano il tipo di contenuto contenuto nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="919e4-118">The data identifies the type of content that the sample contains.</span></span><br/>                                                                                                     |
| <span id="MFASFSampleExtension_PixelAspectRatio"></span><span id="mfasfsampleextension_pixelaspectratio"></span><span id="MFASFSAMPLEEXTENSION_PIXELASPECTRATIO"></span><dl> <span data-ttu-id="919e4-119"><dt>**\_PixelAspectRatio MFASFSampleExtension**</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-119"><dt>**MFASFSampleExtension\_PixelAspectRatio**</dt></span></span> </dl> | <span data-ttu-id="919e4-120">I dati indicano le proporzioni in pixel del contenuto nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="919e4-120">The data indicates the pixel aspect ratio of the content in the sample.</span></span><br/>                                                                                               |



## <a name="requirements"></a><span data-ttu-id="919e4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="919e4-121">Requirements</span></span>



| <span data-ttu-id="919e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="919e4-122">Requirement</span></span> | <span data-ttu-id="919e4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="919e4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="919e4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="919e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="919e4-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="919e4-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="919e4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="919e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="919e4-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="919e4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="919e4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="919e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="919e4-129"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="919e4-129"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919e4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="919e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919e4-131">**IMFASFStreamConfig::AddPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="919e4-131">**IMFASFStreamConfig::AddPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension)
</dt> <dt>

[<span data-ttu-id="919e4-132">**IMFASFStreamConfig::GetPayloadExtension**</span><span class="sxs-lookup"><span data-stu-id="919e4-132">**IMFASFStreamConfig::GetPayloadExtension**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension)
</dt> <dt>

[<span data-ttu-id="919e4-133">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="919e4-133">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




