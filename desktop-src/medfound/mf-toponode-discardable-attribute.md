---
description: Specifica se la pipeline può eliminare campioni da un nodo di topologia.
ms.assetid: 8be20446-4876-4d6f-b0db-2eb1ffaef9aa
title: Attributo MF_TOPONODE_DISCARDABLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56d76e00a0f70735211cf06aca0adc00238ae5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318044"
---
# <a name="mf_toponode_discardable-attribute"></a><span data-ttu-id="d3094-103">Attributo annullabile MF \_ TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="d3094-103">MF\_TOPONODE\_DISCARDABLE attribute</span></span>

<span data-ttu-id="d3094-104">Specifica se la pipeline può eliminare campioni da un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="d3094-104">Specifies whether the pipeline can drop samples from a topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="d3094-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d3094-105">Data type</span></span>

<span data-ttu-id="d3094-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="d3094-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="d3094-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3094-107">Remarks</span></span>

<span data-ttu-id="d3094-108">Questo attributo si applica a tutti i tipi di nodo.</span><span class="sxs-lookup"><span data-stu-id="d3094-108">This attribute applies to all node types.</span></span> <span data-ttu-id="d3094-109">In genere si imposta questo attributo sui nodi tee per indicare che gli output secondari non sono essenziali.</span><span class="sxs-lookup"><span data-stu-id="d3094-109">Typically you would set this attribute on tee nodes, to indicate that the secondary outputs are not essential.</span></span>

<span data-ttu-id="d3094-110">Il valore dell'attributo è una matrice di indici per i flussi di output nel nodo.</span><span class="sxs-lookup"><span data-stu-id="d3094-110">The value of the attribute is an array of indexes to output streams on the node.</span></span>

<span data-ttu-id="d3094-111">Se questo attributo è impostato, la pipeline potrebbe eliminare campioni dai flussi di output specificati, se il flusso è in ritardo.</span><span class="sxs-lookup"><span data-stu-id="d3094-111">If this attribute is set, the pipeline might drop samples from the specified output streams, if the stream is falling behind.</span></span>

<span data-ttu-id="d3094-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d3094-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3094-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3094-113">Requirements</span></span>



| <span data-ttu-id="d3094-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3094-114">Requirement</span></span> | <span data-ttu-id="d3094-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d3094-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3094-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3094-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d3094-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3094-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d3094-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3094-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d3094-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d3094-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3094-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3094-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3094-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3094-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3094-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3094-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3094-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3094-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3094-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="d3094-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="d3094-125">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="d3094-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="d3094-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="d3094-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="d3094-127">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="d3094-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




