---
description: Specifica l'ora di arresto per una topologia, relativa all'inizio della prima topologia nella sequenza.
ms.assetid: 7669f97e-87ad-4a64-a2a5-62b8ce450d80
title: Attributo MF_TOPOLOGY_PROJECTSTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34a7e3d50bd89e0fdfc032f9854c1a183276f04a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880225"
---
# <a name="mf_topology_projectstart-attribute"></a><span data-ttu-id="63140-103">\_Attributo PROJECTSTART della topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="63140-103">MF\_TOPOLOGY\_PROJECTSTART attribute</span></span>

<span data-ttu-id="63140-104">Specifica l'ora di arresto per una topologia, relativa all'inizio della prima topologia nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="63140-104">Specifies the stop time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="63140-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="63140-105">Data type</span></span>

<span data-ttu-id="63140-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="63140-106">**UINT64**</span></span>

<span data-ttu-id="63140-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="63140-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63140-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="63140-108">Remarks</span></span>

<span data-ttu-id="63140-109">Il valore è espresso in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="63140-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="63140-110">Se la sessione multimediale è stata creata con l'attributo dell' [**\_ \_ \_ ora globale della sessione MF**](mf-session-global-time-attribute.md) uguale a **true**, tutte le topologie devono contenere l'attributo **\_ \_ PROJECTSTART della topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="63140-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="63140-111">In caso contrario, le topologie non devono contenere l'attributo **\_ \_ PROJECTSTART della topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="63140-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTART** attribute.</span></span> <span data-ttu-id="63140-112">Per altre informazioni, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="63140-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="63140-113">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="63140-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="63140-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="63140-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="63140-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63140-115">Requirements</span></span>



| <span data-ttu-id="63140-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63140-116">Requirement</span></span> | <span data-ttu-id="63140-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63140-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63140-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63140-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63140-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63140-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="63140-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63140-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63140-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63140-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="63140-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63140-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63140-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="63140-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63140-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63140-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63140-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63140-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="63140-126">Tempi di presentazione sequenza</span><span class="sxs-lookup"><span data-stu-id="63140-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="63140-127">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="63140-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="63140-128">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="63140-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="63140-129">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="63140-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="63140-130">**\_PROJECTSTOP topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="63140-130">**MF\_TOPOLOGY\_PROJECTSTOP**</span></span>](mf-topology-projectstop-attribute.md)
</dt> </dl>

 

 




