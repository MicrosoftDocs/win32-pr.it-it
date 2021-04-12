---
description: Gli eventi sono una parte essenziale della gestione delle chiamate in TAPI 3. La gestione degli eventi include quattro fasi.
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: Eventi (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a9a7d994c7bc9f8019224d826d586d698bc605
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529071"
---
# <a name="events-telephony-api"></a>Eventi (API di telefonia)

Gli eventi sono una parte essenziale della gestione delle chiamate in TAPI 3. La gestione degli eventi include quattro fasi.

**Per eseguire la registrazione e abilitare la ricezione di eventi**

1.  Implementare il metodo [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) . Questo metodo viene chiamato da TAPI quando si verifica un evento. In genere, questa implementazione non supera **AddRef** il puntatore all'interfaccia **IDispatch** , quindi Invia un post al message pump dell'applicazione.
2.  Registrare l'interfaccia in uscita [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification) usando le interfacce [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) e [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint) standard com e passare il metodo [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) un puntatore a [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event).
3.  Chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) per indicare a TAPI gli eventi che l'applicazione gestirà. Il filtro eventi è costituito dai membri **o** dell'enumerazione di [**\_ eventi TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) .
    > [!Note]  
    > È necessario chiamare il metodo **ITTAPI::p UT \_ EventFilter** per impostare la maschera di filtro eventi e abilitare la ricezione di eventi. Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento.

     

È anche necessario chiamare il metodo [**ITTAPI:: RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) per ogni oggetto Address su cui l'applicazione gestirà le chiamate.

Per un elenco di tutte le interfacce eventi, vedere [interfacce eventi](./event-interfaces.md) . Vedere [registrare gli eventi](register-events.md) per esempi di codice che illustrano il processo di registrazione e [ricevono una chiamata](receive-a-call.md) per un esempio di codice che mostra un uso di eventi.

 

 
