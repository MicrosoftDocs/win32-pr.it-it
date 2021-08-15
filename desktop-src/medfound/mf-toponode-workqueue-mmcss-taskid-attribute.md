---
description: Specifica un identificatore di attività del servizio Utilità di pianificazione classi multimediali (MMCSS) per un ramo della topologia.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf75dc911c9d00cab2d21d937ef16a43b38cc4271299c6fae4f2ed7381ec63a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739629"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>Attributo MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID

Specifica un identificatore di attività del servizio Utilità di pianificazione classi multimediali (MMCSS) per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Questo attributo è facoltativo.

Questo attributo viene ignorato a meno che non vengano impostati anche gli attributi seguenti:

-   [**ID DELLA \_ CODA DI LAVORO \_ TOPONODE MF \_**](mf-toponode-workqueue-id-attribute.md)
-   [**CLASSE \_ MMCSS MF TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)

Se l'applicazione registra uno dei propri thread con MMCSS, è possibile usare questo attributo per associare la coda di lavoro della topologia al gruppo MMCSS dell'applicazione. Impostare il valore dell'attributo uguale all'identificatore di attività ricevuto dall'applicazione quando è stata registrata con MMCSS. L'identificatore dell'attività viene restituito nel *parametro TaskIndex* della [**funzione AvSetMmThreadCharacteristics.**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) Per altre informazioni, vedere l'argomento [Funzioni di processo e thread.](../procthread/process-and-thread-functions.md)

Se si desidera che MMCSS assegni un nuovo identificatore di attività per la topologia, impostare l'attributo [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS,**](mf-toponode-workqueue-mmcss-class-attribute.md) ma non impostare l'attributo **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID.**

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 
