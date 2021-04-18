---
description: Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription.
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
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305222"
---
# <a name="ieventsubscription2-interface"></a>Interfaccia IEventSubscription2

Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare l'interfaccia **IEventSubscription2** . Una classe di oggetti evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.

## <a name="when-to-use"></a>Utilizzo

Il sistema [degli eventi com+](com--events.md) utilizza questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.

## <a name="members"></a>Membri

L'interfaccia **IEventSubscription2** eredita da **IEventSubscription**. **IEventSubscription2** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IEventSubscription2** ha queste proprietà.



| Proprietà                                                                      | Tipo di accesso           | Descrizione                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**FilterCriteria**](ieventsubscription2-filtercriteria.md)<br/>       | Lettura/Scrittura<br/> | Criteri di filtro che governano la sottoscrizione.<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | Lettura/Scrittura<br/> | Moniker del Sottoscrittore.<br/>                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




