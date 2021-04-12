---
description: Utilizzato dal servizio di notifica degli eventi di sistema di Microsoft Internet Explorer (SENS) per accedere all'archivio dati degli eventi. Questa interfaccia estende l'interfaccia IEventSystem.
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
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483597"
---
# <a name="ieventsystem2-interface"></a>Interfaccia IEventSystem2

Utilizzato dal servizio di notifica degli eventi di sistema di Microsoft Internet Explorer (SENS) per accedere all'archivio dati degli eventi. Questa interfaccia estende l'interfaccia [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .

## <a name="when-to-implement"></a>Quando implementare

Non è necessario implementare l'interfaccia **IEventSystem2** . Un oggetto sistema eventi (CLSID CEventSystem) fornito dal sistema \_ implementa **IEventSystem2**.

## <a name="when-to-use"></a>Utilizzo

Se si usa SENS, è possibile chiamare i metodi di **IEventSystem2** per aggiungere e rimuovere oggetti da e verso l'archivio eventi e per ottenere oggetti dall'archivio eventi.

Poiché [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) e l'oggetto server di pubblicazione non sono più supportati, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) non viene chiamato sul metodo [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .

## <a name="members"></a>Membri

L'interfaccia **IEventSystem2** eredita da **IEventSystem**. **IEventSystem2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IEventSystem2** dispone di questi metodi.



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

 

