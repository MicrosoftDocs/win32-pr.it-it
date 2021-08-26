---
description: Usato da Microsoft Internet Explorer System Event Notification Service (SENS) per accedere all'archivio dati degli eventi. Questa interfaccia estende l'interfaccia IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interfaccia IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6ecee3137750da9f86b61696799a3a7c6e7177beb2b92fb386712a6c90f69d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070601"
---
# <a name="ieventsystem2-interface"></a>Interfaccia IEventSystem2

Usato da Microsoft Internet Explorer System Event Notification Service (SENS) per accedere all'archivio dati degli eventi. Questa interfaccia estende [**l'interfaccia IEventSystem.**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare **l'interfaccia IEventSystem2.** Un oggetto del sistema di eventi fornito dal sistema (CLSID \_ CEventSystem) implementa **IEventSystem2.**

## <a name="when-to-use"></a>Utilizzo

Se si usa SENS, è possibile chiamare i metodi di **IEventSystem2** per aggiungere e rimuovere oggetti da e verso l'archivio eventi e per ottenere oggetti dall'archivio eventi.

Poiché [**IEventPublisher e**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) l'oggetto publisher non sono più supportati, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) non viene chiamato sul [**metodo ChangedPublisher.**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher)

## <a name="members"></a>Membri

**L'interfaccia IEventSystem2** eredita da **IEventSystem**. **IEventSystem2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IEventSystem2** include questi metodi.



| Metodo                                                                         | Descrizione                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | Recupera il numero di versione del sistema di eventi.<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

