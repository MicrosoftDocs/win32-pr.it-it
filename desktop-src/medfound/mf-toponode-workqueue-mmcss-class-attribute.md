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
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>\_Attributo della \_ \_ classe MMCSS \_ di MF TOPONODE WORKQUEUE

Specifica un'attività di [servizio Utilità di pianificazione classi multimediali](../procthread/multimedia-class-scheduler-service.md) (MMCSS) per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**). Questo attributo è facoltativo.

Questo attributo richiede l' [attributo \_ \_ WORKQUEUE \_ ID MF TOPONODE](mf-toponode-workqueue-id-attribute.md) . Se si imposta questo attributo, impostare anche l'attributo **MF \_ TOPONODE \_ WORKQUEUE \_ ID** impostato sullo stesso nodo.

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

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**\_ \_ ID WORKQUEUE MF \_ TOPONODE**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 
