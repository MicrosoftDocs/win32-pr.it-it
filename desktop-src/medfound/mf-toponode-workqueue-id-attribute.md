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
# <a name="mf_toponode_workqueue_id-attribute"></a>\_ \_ Attributo ID WORKQUEUE MF TOPONODE \_

Specifica una coda di lavoro per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**\_ \_ \_ nodo SOURCESTREAM topologia MF**). L'attributo è facoltativo.

Il valore dell'attributo è un identificatore definito dall'applicazione per la coda di lavoro.

Le applicazioni possono utilizzare questo attributo per assegnare le code di lavoro ai rami della topologia. Ogni nodo di origine nella topologia definisce un ramo. Il ramo include ogni nodo della topologia che riceve i dati da tale nodo.

Se si imposta questo attributo, chiamare il metodo [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sulla topologia risolta. Più rami nella topologia possono condividere la stessa coda di lavoro e le code di lavoro possono essere riutilizzate tra le topologie.

> [!Note]  
> Il valore di questo attributo non corrisponde all'identificatore restituito dalla funzione [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) . Il valore dell'attributo è un identificatore definito dall'applicazione e viene usato per associare i rami della topologia alle code di lavoro. Quando la sessione multimediale alloca una nuova coda di lavoro, archivia internamente l'identificatore effettivo della coda di lavoro.

 

Se questo attributo è impostato, l'applicazione può anche assegnare il ramo a un'attività MMCSS (Multimedia Class Scheduler Service), impostando l'attributo [**della \_ classe MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) .

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

[**Classe MMCSS di MF \_ TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ taskId**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 




