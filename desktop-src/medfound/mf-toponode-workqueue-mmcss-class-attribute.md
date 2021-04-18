---
description: Specifica un'attività di servizio Utilità di pianificazione classi multimediali (MMCSS) per un ramo della topologia.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: Attributo MF_TOPONODE_WORKQUEUE_MMCSS_CLASS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308431"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="159cf-103">\_Attributo della \_ \_ classe MMCSS \_ di MF TOPONODE WORKQUEUE</span><span class="sxs-lookup"><span data-stu-id="159cf-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="159cf-104">Specifica un'attività di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per un ramo della topologia.</span><span class="sxs-lookup"><span data-stu-id="159cf-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="159cf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="159cf-105">Data type</span></span>

<span data-ttu-id="159cf-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="159cf-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="159cf-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="159cf-107">Remarks</span></span>

<span data-ttu-id="159cf-108">Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**).</span><span class="sxs-lookup"><span data-stu-id="159cf-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="159cf-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="159cf-109">This attribute is optional.</span></span>

<span data-ttu-id="159cf-110">Questo attributo richiede l' [attributo \_ \_ WORKQUEUE \_ ID MF TOPONODE](mf-toponode-workqueue-id-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="159cf-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="159cf-111">Se si imposta questo attributo, impostare anche l'attributo **MF \_ TOPONODE \_ WORKQUEUE \_ ID** impostato sullo stesso nodo.</span><span class="sxs-lookup"><span data-stu-id="159cf-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="159cf-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="159cf-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="159cf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="159cf-113">Requirements</span></span>



| <span data-ttu-id="159cf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="159cf-114">Requirement</span></span> | <span data-ttu-id="159cf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="159cf-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="159cf-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159cf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="159cf-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="159cf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="159cf-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159cf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="159cf-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="159cf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="159cf-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="159cf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="159cf-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="159cf-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="159cf-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="159cf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159cf-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="159cf-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="159cf-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="159cf-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="159cf-125">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="159cf-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="159cf-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="159cf-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="159cf-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="159cf-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="159cf-128">**\_ \_ ID WORKQUEUE MF \_ TOPONODE**</span><span class="sxs-lookup"><span data-stu-id="159cf-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="159cf-129">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**</span><span class="sxs-lookup"><span data-stu-id="159cf-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="159cf-130">Attributi del nodo della topologia</span><span class="sxs-lookup"><span data-stu-id="159cf-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="159cf-131">Code di lavoro</span><span class="sxs-lookup"><span data-stu-id="159cf-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
