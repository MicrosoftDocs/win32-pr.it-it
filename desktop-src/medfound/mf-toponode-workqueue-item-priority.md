---
description: Specifica la priorità dell'elemento di lavoro per un ramo della topologia.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: Attributo MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226376"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="f6650-103">\_ \_ \_ Attributo priorità elemento WORKQUEUE MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="f6650-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="f6650-104">Specifica la priorità dell'elemento di lavoro per un ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="f6650-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6650-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f6650-105">Data type</span></span>

<span data-ttu-id="f6650-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6650-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f6650-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6650-107">Remarks</span></span>

<span data-ttu-id="f6650-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="f6650-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="f6650-109">L'attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f6650-109">The attribute is optional.</span></span>

<span data-ttu-id="f6650-110">Questo attributo richiede l'attributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) nello stesso nodo.</span><span class="sxs-lookup"><span data-stu-id="f6650-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="f6650-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f6650-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6650-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6650-112">Requirements</span></span>



| <span data-ttu-id="f6650-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6650-113">Requirement</span></span> | <span data-ttu-id="f6650-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f6650-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6650-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6650-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f6650-116">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6650-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6650-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6650-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f6650-118">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6650-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f6650-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6650-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6650-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6650-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6650-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6650-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6650-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f6650-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6650-123">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="f6650-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6650-124">Miglioramenti della coda di lavoro e del threading</span><span class="sxs-lookup"><span data-stu-id="f6650-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="f6650-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f6650-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f6650-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="f6650-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="f6650-127">**\_ \_ ID WORKQUEUE MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="f6650-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




