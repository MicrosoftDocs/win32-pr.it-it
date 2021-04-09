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
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>\_Attributo di \_ \_ priorità MMCSS \_ di MF TOPONODE WORKQUEUE

Specifica la priorità del thread relativo per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**). L'attributo è facoltativo.

Questo attributo richiede gli attributi di classe [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) nello stesso nodo.

Il valore dell'attributo è la priorità del thread relativa della coda di lavoro per questo ramo della topologia. Il [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) usa la priorità relativa quando imposta la priorità del thread. Per ulteriori informazioni, vedere [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ \_ ID WORKQUEUE MF \_ TOPONODE**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
