---
description: Specifica un identificatore di attività MMCSS (Multimedia Class Scheduler Service) per un ramo della topologia.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: Attributo MF_TOPONODE_WORKQUEUE_MMCSS_TASKID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527409"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="ae2b3-103">\_TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId</span><span class="sxs-lookup"><span data-stu-id="ae2b3-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="ae2b3-104">Specifica un identificatore di attività MMCSS (Multimedia Class Scheduler Service) per un ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae2b3-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ae2b3-105">Data type</span></span>

<span data-ttu-id="ae2b3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ae2b3-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae2b3-107">Remarks</span></span>

<span data-ttu-id="ae2b3-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="ae2b3-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-109">This attribute is optional.</span></span>

<span data-ttu-id="ae2b3-110">Questo attributo viene ignorato a meno che non vengano impostati anche gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae2b3-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="ae2b3-111">**\_ \_ ID WORKQUEUE MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="ae2b3-112">**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="ae2b3-113">Se l'applicazione registra uno dei propri thread con MMCSS, è possibile usare questo attributo per associare la coda di lavoro della topologia al gruppo MMCSS dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="ae2b3-114">Impostare il valore dell'attributo uguale all'identificatore di attività ricevuto dall'applicazione quando è stato registrato con MMCSS.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="ae2b3-115">L'identificatore di attività viene restituito nel parametro *TaskIndex* della funzione [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) .</span><span class="sxs-lookup"><span data-stu-id="ae2b3-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="ae2b3-116">Per ulteriori informazioni, vedere l'argomento [funzioni di processo e thread](../procthread/process-and-thread-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ae2b3-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="ae2b3-117">Se si desidera che MMCSS assegni un nuovo identificatore di attività per la topologia, impostare l'attributo della [**\_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , ma non impostare l'attributo **MF \_ TOPONODE \_ WORKQUEUE \_ \_** MMCSS taskId.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="ae2b3-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ae2b3-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae2b3-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae2b3-119">Requirements</span></span>



| <span data-ttu-id="ae2b3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae2b3-120">Requirement</span></span> | <span data-ttu-id="ae2b3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ae2b3-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ae2b3-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae2b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae2b3-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae2b3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ae2b3-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae2b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae2b3-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae2b3-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ae2b3-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae2b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae2b3-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae2b3-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae2b3-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae2b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae2b3-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ae2b3-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae2b3-130">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ae2b3-131">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ae2b3-132">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="ae2b3-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="ae2b3-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="ae2b3-134">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="ae2b3-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="ae2b3-135">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="ae2b3-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
