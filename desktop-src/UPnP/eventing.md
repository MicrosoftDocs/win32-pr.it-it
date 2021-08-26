---
title: Gestione eventi
description: Un servizio ospitato deve implementare l'interfaccia IUPnPEventSource se ha variabili di stato con eventi.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008081"
---
# <a name="eventing"></a>Gestione eventi

Un servizio ospitato deve implementare [**l'interfaccia IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) se ha variabili di stato con eventi. Questa interfaccia ha due metodi: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) [**e Unadvise.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) Questa interfaccia fornisce un meccanismo che consente all'host del dispositivo di sottoscrivere le notifiche degli eventi generate dal servizio ospitato. Non sarà presente più di un sink di evento registrato alla volta.

Un servizio ospitato deve implementare il [**metodo Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) mantenendo un riferimento [**all'interfaccia IUPnPEventSink,**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) che è stata passata come parametro. Se l'interfaccia viene trovata, il metodo **Advise** contiene un riferimento a tale interfaccia fino a quando non viene richiamato [**Undvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) o fino a quando non viene rimosso l'oggetto servizio ospitato. **Advise** viene chiamato una sola volta.

Per rimuovere la sottoscrizione, l'host del dispositivo richiama [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) e passa il puntatore all'oggetto usato quando ha chiamato [**Advise.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) Il servizio ospitato rimuove la sottoscrizione se il puntatore è uguale a quello passato a **Advise.**

Quando il valore di una variabile di stato cambia, il servizio ospitato deve segnalare che si è verificato un evento. A tale scopo, i servizi richiamano [**il metodo IUPnPEventSink::OnStateChanged.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged)

Quando l'host del dispositivo non deve più ricevere notifiche dal servizio ospitato, richiama [**IUPnPEventSource::Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), passando lo stesso puntatore all'oggetto ricevuto da [**Advise.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) L'host del dispositivo richiama questo metodo quando il dispositivo non sarà più in rete.

 

 




