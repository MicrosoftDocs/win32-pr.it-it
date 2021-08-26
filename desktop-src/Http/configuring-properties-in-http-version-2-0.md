---
title: Configurazione delle proprietà
description: Configurazione delle proprietà
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 681d5707840634f86da41d3e67a1014e93b8450c668cae9ea6f3129a0fe021f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047456"
---
# <a name="configuring-properties"></a>Configurazione delle proprietà

L'API server HTTP versione 2.0 consente alle applicazioni di configurare manualmente code di richieste, sessioni server e gruppi di URL. La sessione server è l'oggetto di primo livello che contiene informazioni di configurazione che si applicano a tutti i gruppi di URL creati al loro interno. L'applicazione crea una sessione server con uno o più gruppi di URL al suo interno e quindi associa il gruppo di URL a una coda di richieste.

Per altre informazioni sugli oggetti di configurazione specifici nell'API del server HTTP versione 2.0, vedere:

-   [Configurazione della sessione del server](configuring-the-server-session.md)
-   [Configurazione del gruppo di URL](configuring-the-url-group.md)
-   [Configurazione dei timer a livello di API del server HTTP](configuring-the-http-server-api-wide-timers.md)

Le proprietà per gli oggetti di configurazione vengono impostate con [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e [**HttpSetRequestQueueProperty,**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) come illustrato nel diagramma seguente. L'associazione tra la coda di richieste e il gruppo di URL può essere modificata su richiesta, mentre l'associazione tra la sessione del server e i gruppi di URL non può essere modificata. I gruppi di URL devono essere associati a una coda di richieste per ricevere le richieste.

![proprietà per gli oggetti di configurazione](images/configpropinv2.png)

Nella tabella seguente sono elencate le proprietà che è possibile impostare per ogni oggetto di configurazione. In generale, se l'applicazione non imposta alcuna configurazione delle proprietà, vengono applicate le configurazioni predefinite dell'API server HTTP. Le proprietà di configurazione impostate dall'applicazione nella sessione del server eseguono l'override delle configurazioni a livello di API del server HTTP. Le configurazioni impostate nel gruppo di URL sostituiscono le configurazioni della sessione del server e le configurazioni della coda di richieste sostituiscono le configurazioni predefinite dell'API server HTTP.



| Oggetto Configuration | Proprietà                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessione server       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Gruppo di URL            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Coda richiesta        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Le proprietà della sessione server sono definite [nell'enumerazione \_ HTTP SERVER \_ PROPERTY.](/windows/desktop/api/Http/ne-http-http_server_property) Nella tabella seguente sono elencate le strutture di proprietà impostate per ogni tipo di proprietà e l'API server HTTP predefinita quando queste proprietà non vengono impostate dall'applicazione.



| Proprietà                                                    | Struttura                                                                     | Impostazione predefinita dell'API del server HTTP    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**INFORMAZIONI \_ \_ SULL'AUTENTICAZIONE DEL SERVER \_ HTTP**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Nessuna autenticazione          |
| HttpServerLoggingProperty                                   | [**INFORMAZIONI \_ DI REGISTRAZIONE \_ HTTP**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Nessuna registrazione                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**INFORMAZIONI \_ SUI LIMITI DI CONNESSIONE \_ \_ HTTP**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Nessun limite                   |
| HttpServerTimeoutsProperty                                  | [**INFORMAZIONI SUI \_ LIMITI \_ DI TIMEOUT \_ HTTP**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 sec.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**INFORMAZIONI SUL \_ LIMITE DI LARGHEZZA DI BANDA \_ \_ HTTP**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Nessun limite                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**INFORMAZIONI \_ SULLO STATO \_ HTTP**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | Attivato                    |
| HttpServer503VerbosityProperty                              | [**LIVELLO DI DETTAGLIO DELLA RISPOSTA HTTP \_ 503 \_ \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**INFORMAZIONI \_ \_ SULL'ASSOCIAZIONE HTTP**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | Nessuno                       |



 

Nella tabella seguente sono elencati i valori minimo e massimo per le configurazioni dell'API server HTTP.



| Proprietà                                              | Numero massimo e minimo di API del server HTTP                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = MIN \_ ALLOWED BANDWIDTH THROTTLING RATE Max = \_ \_ \_ none |
| HttpServerQueueLengthProperty                         | Min = 0xA Max = 0xFFFF                                     |



 

 

 




