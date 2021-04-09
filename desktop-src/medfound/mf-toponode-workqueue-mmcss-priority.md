---
description: Specifica la priorità del thread relativo per un ramo della topologia.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: Attributo MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130135"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="9abd4-103">\_Attributo di \_ \_ priorità MMCSS \_ di MF TOPONODE WORKQUEUE</span><span class="sxs-lookup"><span data-stu-id="9abd4-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="9abd4-104">Specifica la priorità del thread relativo per un ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="9abd4-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="9abd4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="9abd4-105">Data type</span></span>

<span data-ttu-id="9abd4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9abd4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9abd4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="9abd4-107">Remarks</span></span>

<span data-ttu-id="9abd4-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="9abd4-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="9abd4-109">L'attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9abd4-109">The attribute is optional.</span></span>

<span data-ttu-id="9abd4-110">Questo attributo richiede gli attributi di classe [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) nello stesso nodo.</span><span class="sxs-lookup"><span data-stu-id="9abd4-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="9abd4-111">Il valore dell'attributo è la priorità del thread relativa della coda di lavoro per questo ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="9abd4-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="9abd4-112">Il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) usa la priorità relativa quando imposta la priorità del thread.</span><span class="sxs-lookup"><span data-stu-id="9abd4-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="9abd4-113">Per ulteriori informazioni, vedere [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span><span class="sxs-lookup"><span data-stu-id="9abd4-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="9abd4-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9abd4-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9abd4-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9abd4-115">Requirements</span></span>



| <span data-ttu-id="9abd4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9abd4-116">Requirement</span></span> | <span data-ttu-id="9abd4-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9abd4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9abd4-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9abd4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9abd4-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9abd4-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9abd4-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9abd4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9abd4-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9abd4-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9abd4-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9abd4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9abd4-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9abd4-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9abd4-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9abd4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9abd4-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9abd4-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9abd4-126">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="9abd4-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="9abd4-127">Miglioramenti della coda di lavoro e del threading</span><span class="sxs-lookup"><span data-stu-id="9abd4-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="9abd4-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="9abd4-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="9abd4-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="9abd4-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="9abd4-130">**\_ \_ ID WORKQUEUE MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="9abd4-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="9abd4-131">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="9abd4-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
