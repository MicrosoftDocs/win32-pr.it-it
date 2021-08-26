---
description: Specifica una coda di lavoro per un ramo della topologia.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ba4ab55d2a70b4b0c081544ab43a78719fab537fbf478519bde1e65dfc9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955091"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>Attributo MF \_ TOPONODE \_ WORKQUEUE \_ ID

Specifica una coda di lavoro per un ramo della topologia.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo si applica ai nodi di origine (**MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). L'attributo è facoltativo.

Il valore dell'attributo è un identificatore definito dall'applicazione per la coda di lavoro.

Le applicazioni possono usare questo attributo per assegnare code di lavoro ai rami della topologia. Ogni nodo di origine nella topologia definisce un ramo. Il ramo include ogni nodo della topologia che riceve i dati da tale nodo.

Se si imposta questo attributo, chiamare il metodo [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) sulla topologia risolta. Più rami nella topologia possono condividere la stessa coda di lavoro e le code di lavoro possono essere usate nuovamente tra le topologie.

> [!Note]  
> Il valore di questo attributo non corrisponde all'identificatore restituito dalla [**funzione MFAllocateWorkQueue.**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) Il valore dell'attributo è un identificatore definito dall'applicazione e viene usato per associare i rami della topologia alle code di lavoro. Quando la sessione multimediale alloca una nuova coda di lavoro, archivia internamente l'identificatore effettivo della coda di lavoro.

 

Se questo attributo viene impostato, l'applicazione può anche assegnare il ramo a un'attività MMCSS (Multimedia Class Scheduler Service), impostando l'attributo [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS.**](mf-toponode-workqueue-mmcss-class-attribute.md)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**CLASSE MMCSS MF \_ TOPONODE \_ WORKQUEUE \_ \_**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Attributi del nodo della topologia](topology-node-attributes.md)
</dt> <dt>

[Code di lavoro](work-queues.md)
</dt> </dl>

 

 




