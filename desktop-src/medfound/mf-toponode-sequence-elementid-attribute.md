---
description: Specifica l'elemento che contiene il nodo di origine.
ms.assetid: f5fa5c10-8f30-43bd-8054-a39996f807a3
title: Attributo MF_TOPONODE_SEQUENCE_ELEMENTID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3cd2c66c40a0bc3776d2fd2b7d78535cf24b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308439"
---
# <a name="mf_toponode_sequence_elementid-attribute"></a><span data-ttu-id="b7d99-103">\_ \_ Attributo ElementID della sequenza MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="b7d99-103">MF\_TOPONODE\_SEQUENCE\_ELEMENTID attribute</span></span>

<span data-ttu-id="b7d99-104">Specifica l'elemento che contiene il nodo di origine.</span><span class="sxs-lookup"><span data-stu-id="b7d99-104">Specifies the element that contains this source node.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7d99-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b7d99-105">Data type</span></span>

<span data-ttu-id="b7d99-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b7d99-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d99-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7d99-107">Remarks</span></span>

<span data-ttu-id="b7d99-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="b7d99-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span>

<span data-ttu-id="b7d99-109">La pipeline multimediale usa questo attributo per individuare quando le origini multimediali fanno parte dello stesso elemento.</span><span class="sxs-lookup"><span data-stu-id="b7d99-109">The media pipeline uses this attribute to discover when media sources are part of the same element.</span></span> <span data-ttu-id="b7d99-110">La pipeline considera tutti i nodi di origine che fanno parte dello stesso elemento che hanno lo stesso clock.</span><span class="sxs-lookup"><span data-stu-id="b7d99-110">The pipeline treats all source nodes that are part of the same element as having the same clock.</span></span>

<span data-ttu-id="b7d99-111">Quando la pipeline Accoda una nuova topologia che contiene nodi di origine che fanno parte di un elemento presente nella topologia precedente, la pipeline considera questi nodi di origine come aventi lo stesso clock dei nodi di origine di tale elemento nella topologia precedente.</span><span class="sxs-lookup"><span data-stu-id="b7d99-111">When the pipeline queues up a new topology that contains source nodes that are part of an element that is present in the previous topology, the pipeline treats these source nodes as having the same clock as the source nodes from that element in the previous topology.</span></span>

> [!Note]  
> <span data-ttu-id="b7d99-112">La pipeline multimediale non corregge i timestamp per i nodi di origine con frequenze di clock diverse.</span><span class="sxs-lookup"><span data-stu-id="b7d99-112">The media pipeline does not correct time stamps for source nodes with different clock rates.</span></span>

 

<span data-ttu-id="b7d99-113">Un'origine multimediale che può fornire topologie deve implementare l'interfaccia [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) o l'interfaccia [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) .</span><span class="sxs-lookup"><span data-stu-id="b7d99-113">A media source that can provide topologies should implement the [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) interface or the [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource) interface.</span></span> <span data-ttu-id="b7d99-114">Un'origine multimediale che fornisce topologie deve impostare l' **attributo \_ \_ \_ ElementID della sequenza MF TOPONODE** in ogni nodo di origine creato.</span><span class="sxs-lookup"><span data-stu-id="b7d99-114">A media source that provides topologies should set the **MF\_TOPONODE\_SEQUENCE\_ELEMENTID** attribute on every source node that it creates.</span></span>

<span data-ttu-id="b7d99-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b7d99-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d99-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7d99-116">Requirements</span></span>



| <span data-ttu-id="b7d99-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d99-117">Requirement</span></span> | <span data-ttu-id="b7d99-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b7d99-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d99-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7d99-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d99-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7d99-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b7d99-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d99-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7d99-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7d99-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7d99-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d99-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d99-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d99-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7d99-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d99-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b7d99-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7d99-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="b7d99-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b7d99-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="b7d99-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b7d99-129">**IMFMediaSourceTopologyProvider**</span><span class="sxs-lookup"><span data-stu-id="b7d99-129">**IMFMediaSourceTopologyProvider**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
</dt> <dt>

[<span data-ttu-id="b7d99-130">**IMFSequencerSource**</span><span class="sxs-lookup"><span data-stu-id="b7d99-130">**IMFSequencerSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)
</dt> <dt>

[<span data-ttu-id="b7d99-131">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b7d99-131">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b7d99-132">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="b7d99-132">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7d99-133">Origine sequencer</span><span class="sxs-lookup"><span data-stu-id="b7d99-133">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




