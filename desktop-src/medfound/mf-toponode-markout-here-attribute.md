---
description: Specifica se la pipeline applica Mark-out a questo nodo. Mark-out è il punto in cui termina una presentazione. Se i componenti della pipeline generano dati oltre il punto di contrassegno, non viene eseguito il rendering dei dati.
ms.assetid: adf2361a-90c7-4650-a486-5c450a41ab54
title: Attributo MF_TOPONODE_MARKOUT_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c5dc21f39f45aa04860f3374bead54d260f0821
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308443"
---
# <a name="mf_toponode_markout_here-attribute"></a><span data-ttu-id="ca5ff-105">\_Attributo TOPONODE di \_ contrassegno \_ MF</span><span class="sxs-lookup"><span data-stu-id="ca5ff-105">MF\_TOPONODE\_MARKOUT\_HERE attribute</span></span>

<span data-ttu-id="ca5ff-106">Specifica se la pipeline applica Mark-out a questo nodo.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-106">Specifies whether the pipeline applies mark-out at this node.</span></span> <span data-ttu-id="ca5ff-107">Mark-out è il punto in cui termina una presentazione.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-107">Mark-out is the point where a presentation ends.</span></span> <span data-ttu-id="ca5ff-108">Se i componenti della pipeline generano dati oltre il punto di contrassegno, non viene eseguito il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-108">If pipeline components generate data past the mark-out point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="ca5ff-109">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ca5ff-109">Data type</span></span>

<span data-ttu-id="ca5ff-110">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ca5ff-110">**UINT32**</span></span>

<span data-ttu-id="ca5ff-111">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-111">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca5ff-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca5ff-112">Remarks</span></span>

<span data-ttu-id="ca5ff-113">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-113">This attribute applies to all node types.</span></span>

<span data-ttu-id="ca5ff-114">Se questo attributo è **true**, la pipeline Media Foundation rimuove gli esempi di output da questo nodo in modo da corrispondere all'ora di fine della presentazione.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-114">If this attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the stop time for the presentation.</span></span> <span data-ttu-id="ca5ff-115">Il caricatore della topologia imposta questo attributo quando risolve una topologia.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-115">The topology loader sets this attribute when it resolves a topology.</span></span> <span data-ttu-id="ca5ff-116">Per la maggior parte delle applicazioni non è necessario impostare o recuperare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-116">Most applications do not need to set or retrieve this attribute.</span></span>

<span data-ttu-id="ca5ff-117">È consigliabile che questo attributo sia impostato su **true** esattamente per un nodo in ogni ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-117">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="ca5ff-118">Un ramo della topologia è definito come il percorso da un nodo di origine a un nodo di output.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-118">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="ca5ff-119">All'interno di un ramo, \_ gli \_ attributi TOPONODE \_ e [MF TOPONODE Markin \_ \_ \_ here](mf-toponode-markin-here-attribute.md) devono essere impostati nello stesso nodo del branch.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-119">Within a branch, the MF\_TOPONODE\_MARKOUT\_HERE and [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="ca5ff-120">Non possono essere impostati su nodi diversi all'interno dello stesso ramo.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-120">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="ca5ff-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ca5ff-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5ff-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca5ff-122">Requirements</span></span>



| <span data-ttu-id="ca5ff-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca5ff-123">Requirement</span></span> | <span data-ttu-id="ca5ff-124">Valore</span><span class="sxs-lookup"><span data-stu-id="ca5ff-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5ff-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5ff-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ca5ff-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca5ff-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ca5ff-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca5ff-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ca5ff-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ca5ff-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca5ff-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca5ff-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca5ff-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca5ff-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5ff-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca5ff-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5ff-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ca5ff-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ca5ff-133">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ca5ff-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ca5ff-134">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ca5ff-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ca5ff-135">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="ca5ff-135">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ca5ff-136">**MF \_ TOPONODE \_ Markin \_ qui**</span><span class="sxs-lookup"><span data-stu-id="ca5ff-136">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="ca5ff-137">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="ca5ff-137">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




