---
description: Gli eventi sono una parte fondamentale della gestione delle chiamate in TAPI 3. La gestione degli eventi include quattro fasi.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventi (API Di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b2cf181f10373505a0fe50d3c9efa7358b3ccb749acb723d8314dee27ff9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660861"
---
# <a name="events-telephony-api"></a>Eventi (API Di telefonia)

Gli eventi sono una parte fondamentale della gestione delle chiamate in TAPI 3. La gestione degli eventi include quattro fasi.

**Per registrarsi per e abilitare la ricezione di eventi**

1.  Implementare [**il metodo ITTAPIEventNotification::Event.**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) TapI chiama questo metodo quando si verifica un evento. In genere, questa implementazione non esegue altro che **AddRef** del puntatore a interfaccia **IDispatch,** quindi esegue il post nel message pump dell'applicazione.
2.  Registrare l'interfaccia in uscita [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) usando le interfacce [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) standard COM e passare al metodo [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un puntatore a [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Chiamare il [**metodo ITTAPI::p ut \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) per indicare a TAPI quali eventi verranno gestiti dall'applicazione. Il filtro eventi è costituito da **membri OR** ed dell'enumerazione [**\_ TAPI EVENT.**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
    > [!Note]  
    > È necessario chiamare il **metodo ITTAPI::p ut \_ EventFilter** per impostare la maschera del filtro eventi e abilitare la ricezione degli eventi. Se non si chiama **ITTAPI::p ut \_ EventFilter,** l'applicazione non riceverà eventi.

     

È anche necessario chiamare il [**metodo ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) per ogni oggetto indirizzo su cui l'applicazione gestirà le chiamate.

Per un elenco di tutte le interfacce [eventi,](./event-interfaces.md) vedere Interfacce eventi. Vedere [Registrare eventi](register-events.md) per esempi di codice che illustrano il processo di registrazione e [Ricevere](receive-a-call.md) una chiamata per un esempio di codice che illustra un uso degli eventi.

 

 
