---
title: Autorizzazione servizio
description: Un'applicazione può implementare l'autorizzazione personalizzata per i messaggi in arrivo in un host del servizio.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Servizi Web di autorizzazione del servizio per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109841"
---
# <a name="service-authorization"></a>Autorizzazione servizio

Un'applicazione può implementare l'autorizzazione personalizzata per i messaggi in arrivo in un host del servizio.


Un host del servizio riceve un callback di sicurezza [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) come parte dell'ENDPOINT DEL [**\_ SERVIZIO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) che viene passato alla [**funzione WsCreateServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) Questo callback viene richiamato quando [viene ricevuto il \_ messaggio WS.](ws-message.md)

L'applicazione può basarsi su questo callback per implementare l'autorizzazione personalizzata per i messaggi in arrivo nell'host del servizio. Se l'autorizzazione non riesce, la funzione di callback di sicurezza restituisce un errore HR e l'host del servizio interrompe il canale.

Per un'implementazione di esempio, vedere l'esempio di nome utente su [SSL, HttpCalculatorWithUserNameOverSslServiceExample.](httpcalculatorwithusernameoversslserviceexample.md)

 

 




