---
description: Specifica se la pipeline esegue il trim degli esempi.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: Attributo MF_TOPOLOGY_NO_MARKIN_MARKOUT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226632"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="7f8de-103">\_ \_ Nessun \_ \_ attributo Markin per la topologia MF</span><span class="sxs-lookup"><span data-stu-id="7f8de-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="7f8de-104">Specifica se la pipeline esegue il trim degli esempi.</span><span class="sxs-lookup"><span data-stu-id="7f8de-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f8de-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="7f8de-105">Data type</span></span>

<span data-ttu-id="7f8de-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f8de-106">**UINT32**</span></span>

<span data-ttu-id="7f8de-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="7f8de-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f8de-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f8de-108">Remarks</span></span>

<span data-ttu-id="7f8de-109">Per impostazione predefinita, la pipeline rimuove gli esempi in base ai tempi di presentazione corretti.</span><span class="sxs-lookup"><span data-stu-id="7f8de-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="7f8de-110">Il trimming viene eseguito nei nodi della topologia con gli attributi [**MF \_ TOPONODE \_ Markin \_ qui**](mf-toponode-markin-here-attribute.md) e [**MF \_ TOPONODE \_ Mark out \_ here**](mf-toponode-markout-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="7f8de-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="7f8de-111">Se la **\_ topologia \_ MF \_ No Markin \_ Mark** Out attribute è impostata su **true** nella topologia, la pipeline non taglia gli esempi e gli attributi **MF \_ TOPONODE \_ Markin \_ here** e **MF \_ TOPONODE Mark out \_ \_ here** sono ignorati.</span><span class="sxs-lookup"><span data-stu-id="7f8de-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="7f8de-112">Se l'attributo non è impostato o ha il valore **false**, la pipeline esegue il trim degli esempi.</span><span class="sxs-lookup"><span data-stu-id="7f8de-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="7f8de-113">Un'applicazione potrebbe impostare la **\_ topologia MF \_ No \_ Markin \_ Mark** Out attribute su **true** se l'applicazione riceve campioni compressi dalla pipeline ed è necessario ottenere tutti i fotogrammi chiave, che altrimenti potrebbero essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="7f8de-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="7f8de-114">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="7f8de-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="7f8de-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="7f8de-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8de-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f8de-116">Requirements</span></span>



| <span data-ttu-id="7f8de-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f8de-117">Requirement</span></span> | <span data-ttu-id="7f8de-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8de-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f8de-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f8de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8de-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f8de-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7f8de-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f8de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8de-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f8de-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7f8de-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f8de-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f8de-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f8de-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8de-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f8de-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8de-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f8de-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f8de-127">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="7f8de-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7f8de-128">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="7f8de-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7f8de-129">**MF \_ TOPONODE \_ Markin \_ qui**</span><span class="sxs-lookup"><span data-stu-id="7f8de-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="7f8de-130">**TOPONODE di MF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7f8de-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="7f8de-131">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="7f8de-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




