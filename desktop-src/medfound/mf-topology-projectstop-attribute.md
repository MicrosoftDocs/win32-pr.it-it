---
description: Specifica l'ora di inizio per una topologia, relativa all'inizio della prima topologia nella sequenza.
ms.assetid: 1ca3709e-88ea-40ca-8da4-c2259365122b
title: Attributo MF_TOPOLOGY_PROJECTSTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5730791440131cd9efdbbb94ce15a598051f1e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528231"
---
# <a name="mf_topology_projectstop-attribute"></a><span data-ttu-id="eea46-103">\_Attributo PROJECTSTOP della topologia MF \_</span><span class="sxs-lookup"><span data-stu-id="eea46-103">MF\_TOPOLOGY\_PROJECTSTOP attribute</span></span>

<span data-ttu-id="eea46-104">Specifica l'ora di inizio per una topologia, relativa all'inizio della prima topologia nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="eea46-104">Specifies the start time for a topology, relative to the start of the first topology in the sequence.</span></span>

## <a name="data-type"></a><span data-ttu-id="eea46-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="eea46-105">Data type</span></span>

<span data-ttu-id="eea46-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="eea46-106">**UINT64**</span></span>

<span data-ttu-id="eea46-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="eea46-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eea46-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="eea46-108">Remarks</span></span>

<span data-ttu-id="eea46-109">Il valore è espresso in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="eea46-109">The value is given in units of 100 nanoseconds.</span></span>

<span data-ttu-id="eea46-110">Se la sessione multimediale è stata creata con l'attributo dell' [**\_ \_ \_ ora globale della sessione MF**](mf-session-global-time-attribute.md) uguale a **true**, tutte le topologie devono contenere l'attributo **\_ \_ PROJECTSTOP della topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="eea46-110">If the Media Session was created with the [**MF\_SESSION\_GLOBAL\_TIME**](mf-session-global-time-attribute.md) attribute equal to **TRUE**, all topologies must contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="eea46-111">In caso contrario, le topologie non devono contenere l'attributo **\_ \_ PROJECTSTOP della topologia MF** .</span><span class="sxs-lookup"><span data-stu-id="eea46-111">Otherwise, topologies must not contain the **MF\_TOPOLOGY\_PROJECTSTOP** attribute.</span></span> <span data-ttu-id="eea46-112">Per altre informazioni, vedere [tempi di presentazione della sequenza](sequence-presentation-times.md).</span><span class="sxs-lookup"><span data-stu-id="eea46-112">For more information, see [Sequence Presentation Times](sequence-presentation-times.md).</span></span>

<span data-ttu-id="eea46-113">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="eea46-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="eea46-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="eea46-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea46-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eea46-115">Requirements</span></span>



| <span data-ttu-id="eea46-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea46-116">Requirement</span></span> | <span data-ttu-id="eea46-117">Valore</span><span class="sxs-lookup"><span data-stu-id="eea46-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eea46-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea46-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eea46-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eea46-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eea46-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eea46-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eea46-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eea46-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eea46-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eea46-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eea46-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea46-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eea46-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eea46-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea46-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eea46-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eea46-126">Tempi di presentazione sequenza</span><span class="sxs-lookup"><span data-stu-id="eea46-126">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="eea46-127">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="eea46-127">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="eea46-128">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="eea46-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="eea46-129">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="eea46-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="eea46-130">**\_PROJECTSTART topologia MF \_**</span><span class="sxs-lookup"><span data-stu-id="eea46-130">**MF\_TOPOLOGY\_PROJECTSTART**</span></span>](mf-topology-projectstart-attribute.md)
</dt> </dl>

 

 




