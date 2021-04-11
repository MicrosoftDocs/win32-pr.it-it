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
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>\_ \_ \_ Attributo priorità elemento WORKQUEUE MF TOPONODE \_

Specifica la priorità dell'elemento di lavoro per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**). L'attributo è facoltativo.

Questo attributo richiede l'attributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) nello stesso nodo.

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
</dt> </dl>

 

 




