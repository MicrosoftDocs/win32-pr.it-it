---
description: Archivia e recupera informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interfaccia IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 332f123756d1340352524852aa5bcb38fce09612f52554facaf6e5c8c2398e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047483"
---
# <a name="ieventsubscription2-interface"></a>Interfaccia IEventSubscription2

Archivia e recupera informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende [**l'interfaccia IEventSubscription.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare **l'interfaccia IEventSubscription2.** Una classe di oggetto evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2.**

## <a name="when-to-use"></a>Utilizzo

Il [sistema com+ Events](com--events.md) usa questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.

## <a name="members"></a>Membri

**L'interfaccia IEventSubscription2** eredita da **IEventSubscription**. **IEventSubscription2** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IEventSubscription2.**



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**Filtercriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lettura/Scrittura<br/> | Criteri di filtro che regolano la sottoscrizione.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Lettura/Scrittura<br/> | Moniker del sottoscrittore.<br/>                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




