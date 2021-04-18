---
description: Specifica le dimensioni minime del pacchetto, in byte, per un file ASF (Advanced Systems Format).
ms.assetid: 8c62db36-1332-4565-9fc0-885b9fc148e1
title: Attributo MF_PD_ASF_FILEPROPERTIES_MIN_PACKET_SIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15e7b9016184096696ffd74cde6bd51f305778e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309537"
---
# <a name="mf_pd_asf_fileproperties_min_packet_size-attribute"></a><span data-ttu-id="2a5d8-103">\_Attributo delle \_ \_ \_ dimensioni minime del \_ pacchetto \_ MF PD ASF FileProperties</span><span class="sxs-lookup"><span data-stu-id="2a5d8-103">MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE attribute</span></span>

<span data-ttu-id="2a5d8-104">Specifica le dimensioni minime del pacchetto, in byte, per un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2a5d8-104">Specifies the minimum packet size, in bytes, for an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a5d8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a5d8-105">Data type</span></span>

<span data-ttu-id="2a5d8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a5d8-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a5d8-107">Remarks</span></span>

<span data-ttu-id="2a5d8-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2a5d8-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="2a5d8-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a5d8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a5d8-110">Requirements</span></span>



| <span data-ttu-id="2a5d8-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a5d8-111">Requirement</span></span> | <span data-ttu-id="2a5d8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2a5d8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a5d8-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a5d8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2a5d8-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2a5d8-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a5d8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2a5d8-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2a5d8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2a5d8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a5d8-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a5d8-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a5d8-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a5d8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a5d8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a5d8-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a5d8-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2a5d8-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="2a5d8-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="2a5d8-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2a5d8-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2a5d8-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="2a5d8-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2a5d8-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="2a5d8-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2a5d8-126">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="2a5d8-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




