---
description: Specifica l'offset, in byte, dall'inizio di un file di formato Advanced Systems (ASF) all'inizio del primo pacchetto di dati.
ms.assetid: 5145d952-19d9-4bf8-9046-0b5d28f5e641
title: Attributo MF_PD_ASF_DATA_START_OFFSET (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 125ae1263467afe7e0aa9017e8049b13796538fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884185"
---
# <a name="mf_pd_asf_data_start_offset-attribute"></a><span data-ttu-id="3707b-103">\_Attributo di \_ \_ \_ offset avvio dati \_ MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="3707b-103">MF\_PD\_ASF\_DATA\_START\_OFFSET attribute</span></span>

<span data-ttu-id="3707b-104">Specifica l'offset, in byte, dall'inizio di un file di formato Advanced Systems (ASF) all'inizio del primo pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="3707b-104">Specifies the offset, in bytes, from the start of an Advanced Systems Format (ASF) file to the start of the first data packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="3707b-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3707b-105">Data type</span></span>

<span data-ttu-id="3707b-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="3707b-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="3707b-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="3707b-107">Remarks</span></span>

<span data-ttu-id="3707b-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="3707b-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="3707b-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="3707b-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="3707b-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3707b-110">Requirements</span></span>



| <span data-ttu-id="3707b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3707b-111">Requirement</span></span> | <span data-ttu-id="3707b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="3707b-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3707b-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3707b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3707b-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3707b-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3707b-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3707b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3707b-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3707b-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3707b-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3707b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="3707b-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="3707b-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3707b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3707b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3707b-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3707b-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3707b-121">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="3707b-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="3707b-122">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="3707b-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="3707b-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3707b-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="3707b-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="3707b-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="3707b-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="3707b-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




