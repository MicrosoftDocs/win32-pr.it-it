---
title: Architettura (API server HTTP)
description: Gli oggetti di configurazione della sessione del server, della coda di richiesta e del gruppo di URL consentono alle applicazioni di configurare il servizio HTTP.
ms.assetid: 05a2d689-fd10-4065-85fc-2057bee42fbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc7a07cb5e0439ed82421dd413aee3b6688bc0f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400117"
---
# <a name="architecture-http-server-api"></a>Architettura (API server HTTP)

Gli oggetti di configurazione della sessione del server, della coda di richiesta e del gruppo di URL consentono alle applicazioni di configurare il servizio HTTP. Le proprietà impostate su questi oggetti eseguono l'override delle configurazioni predefinite a livello di API del server HTTP.

-   Server Session: oggetto di configurazione di primo livello che definisce le configurazioni per tutti i gruppi di URL creati nella sessione.
-   Gruppo URL: il gruppo URL, creato nella sessione del server, contiene un set di URL che ereditano le configurazioni impostate nella sessione del server. Le configurazioni del gruppo di URL eseguono l'override delle configurazioni di sessione del server se impostate dall'applicazione. Il gruppo URL definisce una parte dello spazio dei nomi su cui l'applicazione è in ascolto e configura la parte dello spazio dei nomi.
-   Request queue: questo oggetto configura le impostazioni specifiche della coda di richieste. Queste configurazioni vengono applicate a tutti gli URL nei gruppi associati alla coda di richieste.

Il diagramma seguente illustra la relazione tra gli oggetti di configurazione e l'applicazione. In genere, viene creata una singola sessione del server per ogni applicazione con uno o più gruppi di URL creati al suo interno. Le code di richiesta vengono create indipendentemente dal gruppo di URL o dalla sessione del server. I gruppi di URL devono essere associati a una coda di richieste per ricevere le richieste.

![relazione tra gli oggetti di configurazione e l'applicazione](images/architecture.png)

La funzionalità della coda di richieste denominata dell'API server HTTP versione 2,0 consente a più processi di lavoro di ricevere richieste in una coda di richieste. La coda di richieste viene creata da un processo controller che identifica i processi di lavoro a cui è stato concesso l'accesso alla coda di richieste. Per ulteriori informazioni, vedere l'argomento della [coda della richiesta denominata](named-request-queue.md) .

## <a name="property-configuration"></a>Configurazione proprietà

Per ulteriori informazioni sull'impostazione delle proprietà sugli oggetti di configurazione, vedere gli argomenti seguenti:

-   [Configurazione della coda di richieste](configuring-the-request-queue.md)
-   [Configurazione della sessione del server](configuring-the-server-session.md)
-   [Configurazione del gruppo di URL](configuring-the-url-group.md)

Nella tabella seguente sono elencate le proprietà impostate per gli oggetti di configurazione. Per ulteriori informazioni sulle configurazioni delle proprietà, vedere l'argomento [configurazione delle proprietà nella versione HTTP 2,0](configuring-properties-in-http-version-2-0.md) .



| Nome           | Proprietà                                                                                                                                                                                                                                                                      |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessione del server | HttpServerStateProperty<br/> HttpServerLoggingProperty<br/> HttpServerBandwidthProperty<br/> HttpServerTimeoutsProperty<br/> HttpServerAuthenticatonProperty<br/>                                                                               |
| Gruppo URL      | HttpServerStateProperty<br/> HttpServerAuthenticatonProperty<br/> HttpServerLoggingProperty<br/> HttpServerConnectionsProperty<br/> HttpServerBandwidthProperty<br/> HttpServerBindingProperty<br/> HttpServerTimeoutsProperty<br/> |
| Coda richiesta  | HttpServerStateProperty<br/> HttpServerQueueLengthProperty<br/> HttpServer503VerbosityProperty<br/>                                                                                                                                                         |



 

 

 





