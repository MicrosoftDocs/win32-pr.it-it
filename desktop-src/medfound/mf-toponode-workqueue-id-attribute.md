---
description: Specifica una coda di lavoro per un ramo della topologia.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: Attributo MF_TOPONODE_WORKQUEUE_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130138"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="6a677-103">\_ \_ Attributo ID WORKQUEUE MF TOPONODE \_</span><span class="sxs-lookup"><span data-stu-id="6a677-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="6a677-104">Specifica una coda di lavoro per un ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="6a677-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="6a677-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6a677-105">Data type</span></span>

<span data-ttu-id="6a677-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6a677-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6a677-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a677-107">Remarks</span></span>

<span data-ttu-id="6a677-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="6a677-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="6a677-109">L'attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6a677-109">The attribute is optional.</span></span>

<span data-ttu-id="6a677-110">Il valore dell'attributo è un identificatore definito dall'applicazione per la coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a677-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="6a677-111">Le applicazioni possono utilizzare questo attributo per assegnare le code di lavoro ai rami della topologia.</span><span class="sxs-lookup"><span data-stu-id="6a677-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="6a677-112">Ogni nodo di origine nella topologia definisce un ramo.</span><span class="sxs-lookup"><span data-stu-id="6a677-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="6a677-113">Il ramo include ogni nodo della topologia che riceve i dati da tale nodo.</span><span class="sxs-lookup"><span data-stu-id="6a677-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="6a677-114">Se si imposta questo attributo, chiamare il metodo [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sulla topologia risolta.</span><span class="sxs-lookup"><span data-stu-id="6a677-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="6a677-115">Più rami nella topologia possono condividere la stessa coda di lavoro e le code di lavoro possono essere riutilizzate tra le topologie.</span><span class="sxs-lookup"><span data-stu-id="6a677-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="6a677-116">Il valore di questo attributo non corrisponde all'identificatore restituito dalla funzione [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) .</span><span class="sxs-lookup"><span data-stu-id="6a677-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="6a677-117">Il valore dell'attributo è un identificatore definito dall'applicazione e viene usato per associare i rami della topologia alle code di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a677-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="6a677-118">Quando la sessione multimediale alloca una nuova coda di lavoro, archivia internamente l'identificatore effettivo della coda di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a677-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="6a677-119">Se questo attributo è impostato, l'applicazione può anche assegnare il ramo a un'attività MMCSS (Multimedia Class Scheduler Service), impostando l'attributo [**della \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6a677-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="6a677-120">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="6a677-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a677-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a677-121">Requirements</span></span>



| <span data-ttu-id="6a677-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a677-122">Requirement</span></span> | <span data-ttu-id="6a677-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6a677-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a677-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a677-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a677-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a677-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6a677-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a677-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a677-127">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a677-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a677-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a677-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a677-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a677-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a677-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a677-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a677-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6a677-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a677-132">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="6a677-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="6a677-133">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="6a677-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="6a677-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="6a677-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="6a677-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="6a677-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="6a677-136">**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a677-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="6a677-137">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="6a677-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="6a677-138">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="6a677-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="6a677-139">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="6a677-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




