---
description: Consente di specificare la quantità di tempo, in millisecondi, per il buffering dei dati prima di riprodurre un file con estensione ASF (Advanced Systems Format).
ms.assetid: 6aebe1cf-bd45-4b02-a3c8-6599bb683d7c
title: Attributo MF_PD_ASF_FILEPROPERTIES_PREROLL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502ba715cc2802f9710d579e0c7afd6477b83454
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232533"
---
# <a name="mf_pd_asf_fileproperties_preroll-attribute"></a><span data-ttu-id="5140d-103">\_Attributo PREroll di MF PD \_ ASF \_ FileProperties \_</span><span class="sxs-lookup"><span data-stu-id="5140d-103">MF\_PD\_ASF\_FILEPROPERTIES\_PREROLL attribute</span></span>

<span data-ttu-id="5140d-104">Consente di specificare la quantità di tempo, in millisecondi, per il buffering dei dati prima di riprodurre un file con estensione ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="5140d-104">Specifies the amount of time, in milliseconds, to buffer data before playing an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="5140d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5140d-105">Data type</span></span>

<span data-ttu-id="5140d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="5140d-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="5140d-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5140d-107">Remarks</span></span>

<span data-ttu-id="5140d-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="5140d-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="5140d-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="5140d-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="5140d-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5140d-110">Requirements</span></span>



| <span data-ttu-id="5140d-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5140d-111">Requirement</span></span> | <span data-ttu-id="5140d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5140d-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5140d-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5140d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5140d-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5140d-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5140d-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5140d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5140d-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5140d-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5140d-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5140d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5140d-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="5140d-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5140d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5140d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5140d-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5140d-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5140d-121">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="5140d-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="5140d-122">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="5140d-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="5140d-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5140d-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="5140d-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="5140d-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="5140d-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="5140d-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="5140d-126">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="5140d-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




