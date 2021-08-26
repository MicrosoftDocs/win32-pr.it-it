---
title: Architettura (API server HTTP)
description: Gli oggetti di configurazione sessione server, coda richieste e gruppo DI URL consentono alle applicazioni di configurare il servizio HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3905a27708c87c43e141dd4cf8d84b2f0e7e66bc4dd189440733321ee951a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997107"
---
# <a name="architecture-http-server-api"></a>Architettura (API server HTTP)

Gli oggetti di configurazione sessione server, coda richieste e gruppo DI URL consentono alle applicazioni di configurare il servizio HTTP. Le proprietà impostate su questi oggetti eseguono l'override delle configurazioni predefinite a livello di API del server HTTP.

-   Sessione server: oggetto di configurazione di primo livello che definisce le configurazioni per tutti i gruppi di URL creati nella sessione.
-   Gruppo di URL: il gruppo di URL, creato nella sessione del server, contiene un set di URL che ereditano le configurazioni impostate nella sessione del server. Le configurazioni del gruppo di URL eseguono l'override delle configurazioni della sessione server se impostate dall'applicazione. Il gruppo di URL definisce una parte dello spazio dei nomi su cui l'applicazione è in ascolto e configura tale parte dello spazio dei nomi.
-   Coda richieste: questo oggetto configura le impostazioni specifiche per la coda di richieste. Queste configurazioni vengono applicate a tutti gli URL nei gruppi associati alla coda delle richieste.

Il diagramma seguente illustra la relazione tra gli oggetti di configurazione e l'applicazione. In genere, viene creata una singola sessione server per ogni applicazione con uno o più gruppi di URL creati al suo interno. Le code di richiesta vengono create indipendentemente dal gruppo di URL o dalla sessione del server. I gruppi di URL devono essere associati a una coda di richieste per ricevere le richieste.

![relazione tra gli oggetti di configurazione e l'applicazione](images/architecture.png)

La funzionalità della coda di richieste denominata dell'API del server HTTP versione 2.0 consente a più processi di lavoro di ricevere richieste in una coda di richieste. La coda di richieste viene creata da un processo controller che identifica i processi di lavoro a cui è stato concesso l'accesso alla coda di richieste. Per altre informazioni, vedere [l'argomento Coda di richieste](named-request-queue.md) denominate

## <a name="property-configuration"></a>Configurazione delle proprietà

Per altre informazioni sull'impostazione delle proprietà negli oggetti di configurazione, vedere gli argomenti seguenti:

-   [Configurazione della coda delle richieste](configuring-the-request-queue.md)
-   [Configurazione della sessione del server](configuring-the-server-session.md)
-   [Configurazione del gruppo di URL](configuring-the-url-group.md)

Nella tabella seguente sono elencate le proprietà impostate sugli oggetti di configurazione. Per altre informazioni sulle configurazioni delle proprietà, vedere [l'argomento Configurazione delle proprietà in HTTP versione 2.0.](configuring-properties-in-http-version-2-0.md)



| Nome           | Proprietà                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessione del server | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Gruppo di URL      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> Proprietà HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Coda richiesta  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





