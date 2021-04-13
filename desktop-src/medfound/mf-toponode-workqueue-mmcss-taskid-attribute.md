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
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>\_TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId

Specifica un identificatore di attività MMCSS (Multimedia Class Scheduler Service) per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**). Questo attributo è facoltativo.

Questo attributo viene ignorato a meno che non vengano impostati anche gli attributi seguenti:

-   [**\_ \_ ID WORKQUEUE MF \_ TOPONODE**](mf-toponode-workqueue-id-attribute.md)
-   [**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)

Se l'applicazione registra uno dei propri thread con MMCSS, è possibile usare questo attributo per associare la coda di lavoro della topologia al gruppo MMCSS dell'applicazione. Impostare il valore dell'attributo uguale all'identificatore di attività ricevuto dall'applicazione quando è stato registrato con MMCSS. L'identificatore di attività viene restituito nel parametro *TaskIndex* della funzione [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Per ulteriori informazioni, vedere l'argomento [funzioni di processo e thread](../procthread/process-and-thread-functions.md).

Se si desidera che MMCSS assegni un nuovo identificatore di attività per la topologia, impostare l'attributo della [**\_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , ma non impostare l'attributo **MF \_ TOPONODE \_ WORKQUEUE \_ \_** MMCSS taskId.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 
