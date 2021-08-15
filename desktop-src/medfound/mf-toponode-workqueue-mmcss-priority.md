---
description: Specifica la priorità relativa del thread per un ramo della topologia.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1b131e6c8b0f379e5e7951498c52f7c0d7a3eab83b75fed4ab9e8100721668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874794"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>Attributo MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY

Specifica la priorità relativa del thread per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). L'attributo è facoltativo.

Questo attributo richiede gli attributi [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) e [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) nello stesso nodo.

Il valore dell'attributo è la priorità relativa del thread della coda di lavoro per questo ramo della topologia. Il [servizio Utilità di pianificazione classi](../procthread/multimedia-class-scheduler-service.md) multimediali (MMCSS) usa la priorità relativa quando imposta la priorità del thread. Per altre informazioni, vedere [**AvSetMmThreadPriority.**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Miglioramenti della coda di lavoro e del threading](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**ID DELLA \_ CODA DI LAVORO \_ TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
