---
description: Specifica l'ora di inizio della presentazione.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Attributo MF_TOPONODE_MEDIASTART (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320668"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="d7859-103">\_Attributo MF TOPONODE \_ MEDIASTART</span><span class="sxs-lookup"><span data-stu-id="d7859-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="d7859-104">Specifica l'ora di inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="d7859-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7859-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d7859-105">Data type</span></span>

<span data-ttu-id="d7859-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d7859-106">**UINT64**</span></span>

<span data-ttu-id="d7859-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="d7859-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="d7859-108">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="d7859-108">Get/set</span></span>

<span data-ttu-id="d7859-109">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="d7859-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="d7859-110">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="d7859-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d7859-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="d7859-111">Applies to</span></span>

[<span data-ttu-id="d7859-112">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d7859-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="d7859-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7859-113">Remarks</span></span>

<span data-ttu-id="d7859-114">Questo attributo specifica la posizione nell'origine in cui viene avviata la riproduzione, in unità 100-nanosecondi, rispetto all'avvio dell'origine.</span><span class="sxs-lookup"><span data-stu-id="d7859-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="d7859-115">Se l'attributo non è impostato, la riproduzione inizia da zero (l'inizio del file).</span><span class="sxs-lookup"><span data-stu-id="d7859-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="d7859-116">Ad esempio, per avviare la riproduzione in corrispondenza del contrassegno di 5 secondi, impostare questo attributo su 50 milioni.</span><span class="sxs-lookup"><span data-stu-id="d7859-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="d7859-117">Impostare l'attributo sui nodi di origine nella topologia (nodi con tipo uguale a **MF \_ topologia \_ SOURCESTREAM \_ nodo**).</span><span class="sxs-lookup"><span data-stu-id="d7859-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="d7859-118">Impostare l'attributo prima di chiamare [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="d7859-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="d7859-119">Se si inserisce manualmente un decodificatore nella topologia, è necessario impostare anche gli attributi [MF \_ TOPONODE \_ Markin \_ qui](mf-toponode-markin-here-attribute.md) e [MF \_ TOPONODE \_ Mark out \_ here](mf-toponode-markout-here-attribute.md) nel nodo decodificatore.</span><span class="sxs-lookup"><span data-stu-id="d7859-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="d7859-120">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="d7859-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="d7859-121">Tuttavia, i valori negativi non sono significativi.</span><span class="sxs-lookup"><span data-stu-id="d7859-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="d7859-122">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d7859-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7859-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7859-123">Requirements</span></span>



| <span data-ttu-id="d7859-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7859-124">Requirement</span></span> | <span data-ttu-id="d7859-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d7859-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d7859-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7859-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7859-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7859-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d7859-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7859-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7859-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7859-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d7859-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7859-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7859-131"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7859-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7859-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7859-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7859-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d7859-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7859-134">Tempi di presentazione sequenza</span><span class="sxs-lookup"><span data-stu-id="d7859-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="d7859-135">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="d7859-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7859-136">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="d7859-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




