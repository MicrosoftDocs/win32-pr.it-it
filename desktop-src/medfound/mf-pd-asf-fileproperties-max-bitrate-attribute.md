---
description: Specifica la velocità in bit massima istantanea, in bit al secondo, per un file di formato Advanced Systems (ASF).
ms.assetid: 07e94448-13a9-4ea5-9ac7-a1e35668e0a0
title: Attributo MF_PD_ASF_FILEPROPERTIES_MAX_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14b2c4d8b3061a0865bf3b2f3c2a4c1597c2c76f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881618"
---
# <a name="mf_pd_asf_fileproperties_max_bitrate-attribute"></a><span data-ttu-id="c7fbf-103">\_Attributo della \_ velocità in bit di max PD ASF \_ FileProperties \_ \_</span><span class="sxs-lookup"><span data-stu-id="c7fbf-103">MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_BITRATE attribute</span></span>

<span data-ttu-id="c7fbf-104">Specifica la velocità in bit massima istantanea, in bit al secondo, per un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="c7fbf-104">Specifies the maximum instantaneous bit rate, in bits per second, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7fbf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c7fbf-105">Data type</span></span>

<span data-ttu-id="c7fbf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c7fbf-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c7fbf-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7fbf-107">Remarks</span></span>

<span data-ttu-id="c7fbf-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c7fbf-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="c7fbf-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fbf-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7fbf-110">Requirements</span></span>



| <span data-ttu-id="c7fbf-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fbf-111">Requirement</span></span> | <span data-ttu-id="c7fbf-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c7fbf-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fbf-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fbf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c7fbf-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7fbf-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c7fbf-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7fbf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c7fbf-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7fbf-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c7fbf-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7fbf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7fbf-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fbf-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fbf-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7fbf-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fbf-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7fbf-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7fbf-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="c7fbf-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c7fbf-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="c7fbf-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c7fbf-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c7fbf-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c7fbf-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="c7fbf-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7fbf-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c7fbf-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c7fbf-126">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="c7fbf-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




