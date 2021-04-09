---
title: Gestione eventi
description: Un servizio ospitato deve implementare l'interfaccia IUPnPEventSource se dispone di variabili di stato evento.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a6382ee88d2ca5168c94eac20727bbfee4a598
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856270"
---
# <a name="eventing"></a>Gestione eventi

Un servizio ospitato deve implementare l'interfaccia [**IUPnPEventSource**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) se dispone di variabili di stato evento. Questa interfaccia dispone di due metodi: [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) e [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Questa interfaccia fornisce un meccanismo che consente all'host del dispositivo di sottoscrivere le notifiche degli eventi generate dal servizio ospitato. Non verrà registrato più di un sink di evento alla volta.

Un servizio ospitato deve implementare il metodo [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) mantenendo un riferimento all'interfaccia [**IUPnPEventSink**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) , che è stata passata come parametro. Se l'interfaccia viene trovata, il metodo **Advise** include un riferimento a tale interfaccia finché non viene richiamato [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) o finché l'oggetto servizio ospitato non viene rimosso. Il metodo **Advise** viene chiamato una sola volta.

Per rimuovere la sottoscrizione, l'host del dispositivo richiama [**Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) e passa il puntatore all'oggetto utilizzato quando viene chiamato [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). Il servizio ospitato rimuove la sottoscrizione se il puntatore è uguale a quello passato a **Advise**.

Quando viene modificato il valore di una variabile di stato, il servizio ospitato deve segnalare che si è verificato un evento. Il servizio esegue questa operazione richiamando il metodo [**IUPnPEventSink:: OnStateChanged**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) .

Quando l'host del dispositivo non deve più ricevere notifiche dal servizio ospitato, richiama [**IUPnPEventSource:: Unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), passando lo stesso puntatore a un oggetto ricevuto da [**Advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). L'host del dispositivo richiama questo metodo quando il dispositivo non si trova più nella rete.

 

 




