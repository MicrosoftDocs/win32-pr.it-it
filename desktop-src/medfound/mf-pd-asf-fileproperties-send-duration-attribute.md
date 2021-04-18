---
description: Specifica l'intervallo di tempo, in unità di 100 nanosecondi, necessario per l'invio di un file ASF (Advanced Systems Format). Un tempo di invio dei pacchetti indica il momento in cui il pacchetto deve essere recapitato in rete. Non è l'ora di presentazione del pacchetto.
ms.assetid: 2bd427e2-106d-4997-86aa-fae221e429eb
title: Attributo MF_PD_ASF_FILEPROPERTIES_SEND_DURATION (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deed3f78208a0f0c7e555e8113f05ac0800cdb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315028"
---
# <a name="mf_pd_asf_fileproperties_send_duration-attribute"></a><span data-ttu-id="c81ba-105">\_ \_ \_ \_ Attributo Duration dell'invio delle proprietà del FileProperties ASF di MF PD \_</span><span class="sxs-lookup"><span data-stu-id="c81ba-105">MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION attribute</span></span>

<span data-ttu-id="c81ba-106">Specifica l'intervallo di tempo, in unità di 100 nanosecondi, necessario per l'invio di un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c81ba-106">Specifies the time, in 100-nanosecond units, needed to send an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c81ba-107">L'ora di *invio* di un pacchetto è l'ora in cui il pacchetto deve essere recapitato in rete.</span><span class="sxs-lookup"><span data-stu-id="c81ba-107">A packet's *send time* is the time when the packet should be delivered over the network.</span></span> <span data-ttu-id="c81ba-108">Non è l'ora di presentazione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="c81ba-108">It is not the presentation time of the packet.</span></span>

## <a name="data-type"></a><span data-ttu-id="c81ba-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c81ba-109">Data type</span></span>

<span data-ttu-id="c81ba-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c81ba-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="c81ba-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c81ba-111">Remarks</span></span>

<span data-ttu-id="c81ba-112">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="c81ba-112">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c81ba-113">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="c81ba-113">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81ba-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c81ba-114">Requirements</span></span>



| <span data-ttu-id="c81ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81ba-115">Requirement</span></span> | <span data-ttu-id="c81ba-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c81ba-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c81ba-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c81ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c81ba-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c81ba-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c81ba-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c81ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c81ba-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c81ba-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c81ba-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c81ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c81ba-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c81ba-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c81ba-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c81ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81ba-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c81ba-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c81ba-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="c81ba-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c81ba-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="c81ba-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c81ba-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c81ba-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c81ba-128">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="c81ba-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c81ba-129">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c81ba-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c81ba-130">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="c81ba-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




