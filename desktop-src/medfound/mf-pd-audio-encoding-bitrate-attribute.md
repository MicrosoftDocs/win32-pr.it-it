---
description: Specifica la velocità in bit per la codifica audio per la presentazione, in bit al secondo. Questo attributo si applica ai descrittori di presentazione.
ms.assetid: 700f61f4-a0d7-4b69-ace5-356e4e29b93d
title: Attributo MF_PD_AUDIO_ENCODING_BITRATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49566ecb225482ef6513e056de8ba11763de603e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232385"
---
# <a name="mf_pd_audio_encoding_bitrate-attribute"></a><span data-ttu-id="b8ac3-104">\_ \_ \_ Attributo velocità in bit codifica audio MF PD \_</span><span class="sxs-lookup"><span data-stu-id="b8ac3-104">MF\_PD\_AUDIO\_ENCODING\_BITRATE attribute</span></span>

<span data-ttu-id="b8ac3-105">Specifica la velocità in bit per la codifica audio per la presentazione, in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-105">Specifies the audio encoding bit rate for the presentation, in bits per second.</span></span> <span data-ttu-id="b8ac3-106">Questo attributo si applica ai descrittori di presentazione.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-106">This attribute applies to presentation descriptors.</span></span>

## <a name="data-type"></a><span data-ttu-id="b8ac3-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b8ac3-107">Data type</span></span>

<span data-ttu-id="b8ac3-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b8ac3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b8ac3-109">Remarks</span></span>

<span data-ttu-id="b8ac3-110">L'attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-110">The attribute is optional.</span></span> <span data-ttu-id="b8ac3-111">Per alcuni formati sono disponibili schemi di codifica più complessi che non possono essere riepilogati utilizzando questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-111">Some formats have more complex encoding schemes that cannot be summarized by using this attribute.</span></span> <span data-ttu-id="b8ac3-112">Per i file di formato Advanced Systems (ASF), i seguenti attributi descrivono collettivamente la velocità in bit di codifica:</span><span class="sxs-lookup"><span data-stu-id="b8ac3-112">For Advanced Systems Format (ASF) files, the following attributes collectively describe the encoding bit rate:</span></span>

-   [<span data-ttu-id="b8ac3-113">**\_velocità in \_ \_ \_ bit max PD ASF FileProperties \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-113">**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE**</span></span>](mf-pd-asf-fileproperties-max-bitrate-attribute.md)
-   [<span data-ttu-id="b8ac3-114">**\_velocità in \_ \_ \_ \_ bit dei dati media \_ di MF SD ASF EXTSTRMPROP**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-114">**MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)
-   [<span data-ttu-id="b8ac3-115">**\_velocità in \_ \_ \_ \_ bit massima dei dati di EXTSTRMPROP \_ MF SD ASF**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-115">**MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_DATA\_BITRATE**</span></span>](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)
-   [<span data-ttu-id="b8ac3-116">**\_velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-116">**MF\_SD\_ASF\_STREAMBITRATES\_BITRATE**</span></span>](mf-sd-asf-streambitrates-bitrate-attribute.md)

<span data-ttu-id="b8ac3-117">I formati di terze parti potrebbero usare altri attributi personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-117">Third-party formats might use other custom attributes.</span></span>

<span data-ttu-id="b8ac3-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b8ac3-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ac3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8ac3-119">Requirements</span></span>



| <span data-ttu-id="b8ac3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8ac3-120">Requirement</span></span> | <span data-ttu-id="b8ac3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b8ac3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ac3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8ac3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ac3-123">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b8ac3-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="b8ac3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8ac3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ac3-125">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="b8ac3-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b8ac3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8ac3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ac3-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ac3-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ac3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8ac3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ac3-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b8ac3-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b8ac3-130">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b8ac3-131">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b8ac3-132">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b8ac3-132">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b8ac3-133">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="b8ac3-133">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




