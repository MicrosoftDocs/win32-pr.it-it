---
description: Specifica l'ora di arresto della presentazione.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Attributo MF_TOPONODE_MEDIASTOP (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320716"
---
# <a name="mf_toponode_mediastop-attribute"></a><span data-ttu-id="1890f-103">\_Attributo MF TOPONODE \_ MEDIASTOP</span><span class="sxs-lookup"><span data-stu-id="1890f-103">MF\_TOPONODE\_MEDIASTOP attribute</span></span>

<span data-ttu-id="1890f-104">Specifica l'ora di arresto della presentazione.</span><span class="sxs-lookup"><span data-stu-id="1890f-104">Specifies the stop time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="1890f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1890f-105">Data type</span></span>

<span data-ttu-id="1890f-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="1890f-106">**UINT64**</span></span>

<span data-ttu-id="1890f-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="1890f-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="1890f-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="1890f-108">Get/set</span></span>

<span data-ttu-id="1890f-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="1890f-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="1890f-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="1890f-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="1890f-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="1890f-111">Applies to</span></span>

[<span data-ttu-id="1890f-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1890f-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="1890f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1890f-113">Remarks</span></span>

<span data-ttu-id="1890f-114">Questo attributo specifica la posizione nell'origine in cui la riproduzione viene arrestata, in unità 100-nanosecondi, rispetto all'avvio dell'origine.</span><span class="sxs-lookup"><span data-stu-id="1890f-114">This attribute specifies the position in the source where playback stops, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="1890f-115">Se l'attributo non è impostato, la riproduzione viene arrestata alla fine dell'origine.</span><span class="sxs-lookup"><span data-stu-id="1890f-115">If the attribute is not set, playback stops at the end of the source.</span></span> <span data-ttu-id="1890f-116">Ad esempio, per arrestare la riproduzione al contrassegno di 5 secondi, impostare questo attributo su 50 milioni.</span><span class="sxs-lookup"><span data-stu-id="1890f-116">For example, to stop playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="1890f-117">Impostare l'attributo sui nodi di origine nella topologia (nodi con tipo uguale a **MF \_ topologia \_ SOURCESTREAM \_ nodo**).</span><span class="sxs-lookup"><span data-stu-id="1890f-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="1890f-118">Impostare l'attributo prima di chiamare [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="1890f-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="1890f-119">Se si inserisce manualmente un decodificatore nella topologia, è necessario impostare anche gli attributi [MF \_ TOPONODE \_ Markin \_ qui](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ Mark out \_ here](mf-toponode-markout-here-attribute.md) nel nodo decodificatore.</span><span class="sxs-lookup"><span data-stu-id="1890f-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="1890f-120">Dopo aver impostato la topologia, l'impostazione di questo attributo non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1890f-120">After the topology is set, setting this attribute has no effect.</span></span>

<span data-ttu-id="1890f-121">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="1890f-121">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="1890f-122">Tuttavia, i valori negativi non sono significativi.</span><span class="sxs-lookup"><span data-stu-id="1890f-122">However, negative values are not meaningful.</span></span>

<span data-ttu-id="1890f-123">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1890f-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1890f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1890f-124">Requirements</span></span>



| <span data-ttu-id="1890f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1890f-125">Requirement</span></span> | <span data-ttu-id="1890f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="1890f-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1890f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1890f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1890f-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1890f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1890f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1890f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1890f-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1890f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1890f-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1890f-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1890f-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1890f-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1890f-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1890f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1890f-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1890f-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1890f-135">Tempi di presentazione sequenza</span><span class="sxs-lookup"><span data-stu-id="1890f-135">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="1890f-136">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="1890f-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="1890f-137">**MF \_ TOPONODE \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="1890f-137">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




