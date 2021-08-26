---
description: Archivia e recupera informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interfaccia IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: cbb6c5b19ed6116c59642e8dc5c0aa8eabf4800b066904f2132c7d182f2b7bbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070631"
---
# <a name="ieventsubscription3-interface"></a>Interfaccia IEventSubscription3

Archivia e recupera informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende [**l'interfaccia IEventSubscription2.**](ieventsubscription2.md)

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare **l'interfaccia IEventSubscription3.** Una classe di oggetti evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3.**

## <a name="when-to-use"></a>Utilizzo

Il [sistema di eventi COM+](com--events.md) usa questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.

## <a name="members"></a>Membri

**L'interfaccia IEventSubscription3** eredita da **IEventSubscription2.** **IEventSubscription3** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'interfaccia IEventSubscription3** ha queste proprietà.



| Proprietà                                                                                  | Tipo di accesso           | Descrizione                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | Lettura/Scrittura<br/> | GUID dell'applicazione dell'oggetto classe di evento.<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | Lettura/Scrittura<br/> | GUID della partizione dell'oggetto della classe di evento.<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | Lettura/Scrittura<br/> | GUID dell'applicazione del sottoscrittore.<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | Lettura/Scrittura<br/> | GUID della partizione del Sottoscrittore.<br/>           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




