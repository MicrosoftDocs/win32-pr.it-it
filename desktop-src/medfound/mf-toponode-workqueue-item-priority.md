---
description: Specifica la priorità dell'elemento di lavoro per un ramo della topologia.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff67e48bda6ac00baeab9418b80d366c23808713b4689a013949b364f09b6e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739835"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>Attributo MF \_ TOPONODE \_ WORKQUEUE \_ ITEM \_ PRIORITY

Specifica la priorità dell'elemento di lavoro per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). L'attributo è facoltativo.

Questo attributo richiede [l'attributo \_ MF TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) nello stesso nodo.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
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
</dt> </dl>

 

 




