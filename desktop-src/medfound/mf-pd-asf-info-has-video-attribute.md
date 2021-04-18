---
description: Specifica se un file ASF (Advanced Systems Format) contiene almeno un flusso video.
ms.assetid: 98411c75-519f-4ace-999f-1ea22457ed4a
title: Attributo MF_PD_ASF_INFO_HAS_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1a11f672ec4063d14131946ef4e1a820cc3ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315019"
---
# <a name="mf_pd_asf_info_has_video-attribute"></a><span data-ttu-id="1dbac-103">L' \_ attributo video di MF PD \_ ASF \_ \_ è stato \_ associato</span><span class="sxs-lookup"><span data-stu-id="1dbac-103">MF\_PD\_ASF\_INFO\_HAS\_VIDEO attribute</span></span>

<span data-ttu-id="1dbac-104">Specifica se un file ASF (Advanced Systems Format) contiene almeno un flusso video.</span><span class="sxs-lookup"><span data-stu-id="1dbac-104">Specifies whether an Advanced Systems Format (ASF) file contains at least one video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1dbac-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1dbac-105">Data type</span></span>

<span data-ttu-id="1dbac-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1dbac-106">**UINT32**</span></span>

<span data-ttu-id="1dbac-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="1dbac-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dbac-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dbac-108">Remarks</span></span>

<span data-ttu-id="1dbac-109">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="1dbac-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="1dbac-110">Se il valore è **true**, il file contiene almeno un flusso video.</span><span class="sxs-lookup"><span data-stu-id="1dbac-110">If the value is **TRUE**, the file has at least one video stream.</span></span> <span data-ttu-id="1dbac-111">In caso contrario, il file non contiene flussi video.</span><span class="sxs-lookup"><span data-stu-id="1dbac-111">Otherwise, the file does not contain any video streams.</span></span>

<span data-ttu-id="1dbac-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="1dbac-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dbac-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dbac-113">Requirements</span></span>



| <span data-ttu-id="1dbac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dbac-114">Requirement</span></span> | <span data-ttu-id="1dbac-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1dbac-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dbac-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dbac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1dbac-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dbac-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1dbac-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1dbac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1dbac-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1dbac-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1dbac-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dbac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1dbac-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dbac-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dbac-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dbac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dbac-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1dbac-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1dbac-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1dbac-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1dbac-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1dbac-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1dbac-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1dbac-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1dbac-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="1dbac-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1dbac-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="1dbac-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




