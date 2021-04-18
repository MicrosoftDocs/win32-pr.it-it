---
description: Specifica la dimensione media del buffer necessaria per un file ASF (Advanced Systems Format) con velocità in bit variabile (VBR).
ms.assetid: 508d8670-5f5f-422b-9fa1-150115e2dbb8
title: Attributo MF_PD_ASF_METADATA_V8_BUFFERAVERAGE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f1efcb464ee62a1f3838c1a684e3c87dc58227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308465"
---
# <a name="mf_pd_asf_metadata_v8_bufferaverage-attribute"></a><span data-ttu-id="51d59-103">\_ \_ \_ \_ Attributo BUFFERAVERAGE dei metadati MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="51d59-103">MF\_PD\_ASF\_METADATA\_V8\_BUFFERAVERAGE attribute</span></span>

<span data-ttu-id="51d59-104">Specifica la dimensione media del buffer necessaria per un file ASF (Advanced Systems Format) con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="51d59-104">Specifies the average buffer size needed for a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="51d59-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="51d59-105">Data type</span></span>

<span data-ttu-id="51d59-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="51d59-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="51d59-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="51d59-107">Remarks</span></span>

<span data-ttu-id="51d59-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="51d59-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="51d59-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo che si applica al descrittore di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="51d59-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute that applies to the presentation descriptor for ASF content.</span></span>

> [!Note]  
> <span data-ttu-id="51d59-110">Questo attributo si applica solo ai file creati dalla versione 8 di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="51d59-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="51d59-111">Corrisponde all'attributo **BufferAverage** in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="51d59-111">It corresponds to the **BufferAverage** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="51d59-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51d59-112">Requirements</span></span>



| <span data-ttu-id="51d59-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d59-113">Requirement</span></span> | <span data-ttu-id="51d59-114">Valore</span><span class="sxs-lookup"><span data-stu-id="51d59-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d59-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d59-115">Minimum supported client</span></span><br/> | <span data-ttu-id="51d59-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51d59-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="51d59-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51d59-117">Minimum supported server</span></span><br/> | <span data-ttu-id="51d59-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51d59-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="51d59-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51d59-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="51d59-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="51d59-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d59-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51d59-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d59-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51d59-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51d59-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="51d59-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="51d59-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="51d59-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="51d59-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="51d59-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="51d59-126">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="51d59-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="51d59-127">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="51d59-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="51d59-128">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="51d59-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




