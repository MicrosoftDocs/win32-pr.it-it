---
description: Specifica se la pipeline applica Mark-in a questo nodo.
ms.assetid: 406145e8-e00e-460d-b282-85face457605
title: Attributo MF_TOPONODE_MARKIN_HERE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa355cc070a7371ff2e294b3ca3ad558a4749b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308446"
---
# <a name="mf_toponode_markin_here-attribute"></a><span data-ttu-id="ea29c-103">\_ \_ Attributo Markin qui MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="ea29c-103">MF\_TOPONODE\_MARKIN\_HERE attribute</span></span>

<span data-ttu-id="ea29c-104">Specifica se la pipeline applica Mark-in a questo nodo.</span><span class="sxs-lookup"><span data-stu-id="ea29c-104">Specifies whether the pipeline applies mark-in at this node.</span></span> <span data-ttu-id="ea29c-105">Mark-in è il punto in cui inizia una presentazione.</span><span class="sxs-lookup"><span data-stu-id="ea29c-105">Mark-in is the point where a presentation starts.</span></span> <span data-ttu-id="ea29c-106">Se i componenti della pipeline generano dati prima del punto di contrassegno, non viene eseguito il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="ea29c-106">If pipeline components generate data before the mark-in point, the data is not rendered.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea29c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ea29c-107">Data type</span></span>

<span data-ttu-id="ea29c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ea29c-108">**UINT32**</span></span>

<span data-ttu-id="ea29c-109">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="ea29c-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea29c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea29c-110">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ea29c-111">Per la maggior parte delle applicazioni non è necessario usare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ea29c-111">Most applications do not need to use this attribute.</span></span> <span data-ttu-id="ea29c-112">Se necessario, la [sessione multimediale](media-session.md) imposta automaticamente questo attributo.</span><span class="sxs-lookup"><span data-stu-id="ea29c-112">The [Media Session](media-session.md) automatically sets this attribute if needed.</span></span>

 

<span data-ttu-id="ea29c-113">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="ea29c-113">This attribute applies to all node types.</span></span> <span data-ttu-id="ea29c-114">Se l'attributo è **true**, la pipeline Media Foundation rimuove gli esempi di output da questo nodo in modo che corrispondano all'ora di inizio della presentazione.</span><span class="sxs-lookup"><span data-stu-id="ea29c-114">If the attribute is **TRUE**, the Media Foundation pipeline trims the output samples from this node to match the start time for the presentation.</span></span> <span data-ttu-id="ea29c-115">Il caricatore della topologia imposta questo attributo quando risolve una topologia.</span><span class="sxs-lookup"><span data-stu-id="ea29c-115">The topology loader sets this attribute when it resolves a topology.</span></span>

<span data-ttu-id="ea29c-116">È consigliabile che questo attributo sia impostato su **true** esattamente per un nodo in ogni ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="ea29c-116">It is recommended that exactly one node in every branch of the topology should have this attribute set to **TRUE**.</span></span> <span data-ttu-id="ea29c-117">Un ramo della topologia è definito come il percorso da un nodo di origine a un nodo di output.</span><span class="sxs-lookup"><span data-stu-id="ea29c-117">A topology branch is defined as the path from a source node to an output node.</span></span> <span data-ttu-id="ea29c-118">All'interno di un ramo, gli attributi [ \_ TOPONODE \_ \_ ](mf-toponode-markout-here-attribute.md) e MF TOPONODE Markin \_ \_ \_ here devono essere impostati nello stesso nodo del branch.</span><span class="sxs-lookup"><span data-stu-id="ea29c-118">Within a branch, the [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) and MF\_TOPONODE\_MARKIN\_HERE attributes must be set on the same node in the branch.</span></span> <span data-ttu-id="ea29c-119">Non possono essere impostati su nodi diversi all'interno dello stesso ramo.</span><span class="sxs-lookup"><span data-stu-id="ea29c-119">They cannot be set on different nodes within the same branch.</span></span>

<span data-ttu-id="ea29c-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ea29c-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea29c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea29c-121">Requirements</span></span>



| <span data-ttu-id="ea29c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea29c-122">Requirement</span></span> | <span data-ttu-id="ea29c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="ea29c-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea29c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea29c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ea29c-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea29c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ea29c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea29c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ea29c-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ea29c-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ea29c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea29c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea29c-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea29c-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea29c-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea29c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea29c-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea29c-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ea29c-132">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ea29c-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ea29c-133">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ea29c-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ea29c-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="ea29c-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ea29c-135">**TOPONODE di MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ea29c-135">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="ea29c-136">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="ea29c-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




