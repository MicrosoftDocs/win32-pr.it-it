---
description: Specifica la velocità in bit più elevata in un file ASF (Advanced Systems Format) con velocità in bit variabile (VBR).
ms.assetid: a31f447d-b718-4f8d-b0d5-643497339557
title: Attributo MF_PD_ASF_METADATA_V8_VBRPEAK (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d987815fea919bb46bbe5758e48d6eb22dad8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529550"
---
# <a name="mf_pd_asf_metadata_v8_vbrpeak-attribute"></a><span data-ttu-id="f4fa9-103">\_ \_ \_ \_ Attributo VBRPEAK dei metadati MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="f4fa9-103">MF\_PD\_ASF\_METADATA\_V8\_VBRPEAK attribute</span></span>

<span data-ttu-id="f4fa9-104">Specifica la velocità in bit più elevata in un file ASF (Advanced Systems Format) con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="f4fa9-104">Specifies the highest momentary bit rate in a variable bit rate (VBR) Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4fa9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f4fa9-105">Data type</span></span>

<span data-ttu-id="f4fa9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f4fa9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4fa9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4fa9-107">Remarks</span></span>

<span data-ttu-id="f4fa9-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="f4fa9-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="f4fa9-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo.</span><span class="sxs-lookup"><span data-stu-id="f4fa9-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute.</span></span>

> [!Note]  
> <span data-ttu-id="f4fa9-110">Questo attributo si applica solo ai file creati dalla versione 8 di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f4fa9-110">This attribute applies only to files created by version 8 of the Windows Media Format SDK.</span></span> <span data-ttu-id="f4fa9-111">Corrisponde all'attributo **VBRPeak** in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f4fa9-111">It corresponds to the **VBRPeak** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f4fa9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4fa9-112">Requirements</span></span>



| <span data-ttu-id="f4fa9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4fa9-113">Requirement</span></span> | <span data-ttu-id="f4fa9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f4fa9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fa9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fa9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fa9-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4fa9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f4fa9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fa9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fa9-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4fa9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f4fa9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4fa9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fa9-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa9-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fa9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4fa9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fa9-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4fa9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4fa9-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f4fa9-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f4fa9-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f4fa9-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f4fa9-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f4fa9-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f4fa9-126">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="f4fa9-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f4fa9-127">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="f4fa9-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f4fa9-128">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="f4fa9-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




