---
title: Configurazione delle proprietà
description: Configurazione delle proprietà
ms.assetid: 9d659887-a696-4344-9c71-a2cc6131d8b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f898467f92f669596b4a8b1a4e68581c343ea883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395930"
---
# <a name="configuring-properties"></a>Configurazione delle proprietà

L'API server HTTP versione 2,0 consente alle applicazioni di configurare manualmente le code di richieste, le sessioni server e i gruppi di URL. La sessione del server è l'oggetto di livello superiore che contiene le informazioni di configurazione applicabili a tutti i gruppi di URL creati al suo interno. L'applicazione crea una sessione del server con uno o più gruppi di URL al suo interno e quindi associa il gruppo di URL a una coda di richieste.

Per ulteriori informazioni sugli oggetti di configurazione specifici nell'API server HTTP versione 2,0, vedere:

-   [Configurazione della sessione del server](configuring-the-server-session.md)
-   [Configurazione del gruppo di URL](configuring-the-url-group.md)
-   [Configurazione dei timer wide dell'API del server HTTP](configuring-the-http-server-api-wide-timers.md)

Le proprietà per gli oggetti di configurazione sono impostate con [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty), [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) e [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) , come illustrato nella figura seguente. L'associazione tra la coda delle richieste e il gruppo di URL può essere modificata su richiesta, mentre l'associazione tra la sessione del server e i gruppi di URL non può essere modificata. Per ricevere le richieste, è necessario associare i gruppi di URL a una coda di richieste.

![Proprietà per gli oggetti di configurazione](images/configpropinv2.png)

Nella tabella seguente sono elencate le proprietà che è possibile impostare per ogni oggetto di configurazione. In generale, se l'applicazione non imposta alcuna configurazione di proprietà, vengono applicate le configurazioni predefinite dell'API del server HTTP. Le proprietà di configurazione impostate dall'applicazione nella sessione del server eseguono l'override delle configurazioni a livello di API del server HTTP. Le configurazioni impostate nel gruppo URL sostituiscono le configurazioni di sessione del server e le configurazioni della coda di richieste sostituiscono le configurazioni predefinite dell'API del server HTTP.



| Oggetto Configuration | Proprietà                                                                                                                                                      |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sessione del server       | HttpServerStateProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerTimeoutsProperty HttpServerAuthenticationProperty                           |
| Gruppo URL            | HttpServerStateProperty HttpServerAuthenticationProperty HttpServerLoggingProperty HttpServerQosProperty HttpServerBindingProperty HttpServerTimeoutsProperty |
| Coda richiesta        | HttpServerStateProperty HttpServerQueueLengthProperty HttpServer503VerbosityProperty                                                                          |



 

Le proprietà della sessione del server sono definite nell'enumerazione delle [ \_ \_ proprietà del server http](/windows/desktop/api/Http/ne-http-http_server_property) . Nella tabella seguente sono elencate le strutture di proprietà impostate per ogni tipo di proprietà e l'impostazione predefinita dell'API del server HTTP quando tali proprietà non sono impostate dall'applicazione.



| Proprietà                                                    | Struttura                                                                     | Impostazione predefinita API server HTTP    |
|-------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------|
| HttpServerAuthenticatonProperty                             | [**\_informazioni di \_ autenticazione \_ Server http**](/windows/desktop/api/Http/ns-http-http_server_authentication_info) | Nessuna autenticazione          |
| HttpServerLoggingProperty                                   | [**\_informazioni di registrazione http \_**](/windows/desktop/api/Http/ns-http-http_logging_info)                              | Nessuna registrazione                 |
| HttpServerQosProperty->HttpQosSettingTypeConnectionLimit | [**\_informazioni sul \_ limite di connessione HTTP \_**](/windows/desktop/api/Http/ns-http-http_connection_limit_info)           | Nessun limite                   |
| HttpServerTimeoutsProperty                                  | [**\_informazioni sul \_ limite di timeout http \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)                 | 120 sec.                   |
| HttpServerQosProperty->HttpQosSettingTypeBandwidth       | [**informazioni sul limite della larghezza di \_ banda http \_ \_**](/windows/desktop/api/Http/ns-http-http_bandwidth_limit_info)             | Nessun limite                   |
| HttpServerQueueLengthProperty                               | ULONG                                                                         | 1000                       |
| HttpServerStateProperty                                     | [**\_informazioni sullo stato http \_**](/windows/desktop/api/Http/ns-http-http_state_info)                                  | Abilitato                    |
| HttpServer503VerbosityProperty                              | [**Livello \_ di \_ dettaglio della risposta HTTP 503 \_**](/windows/desktop/api/Http/ne-http-http_503_response_verbosity)         | HttpResponseVerbosityBasic |
| HttpServerBindingProperty                                   | [**\_informazioni sul binding HTTP \_**](/windows/desktop/api/Http/ns-http-http_binding_info)                              | nessuno                       |



 

La tabella seguente elenca i valori minimo e massimo per le configurazioni dell'API del server HTTP.



| Proprietà                                              | Valore massimo e minimo API server HTTP                        |
|-------------------------------------------------------|------------------------------------------------------------|
| HttpServerQosProperty->HttpQosSettingTypeBandwidth | Min = velocità minima di \_ limitazione della larghezza di banda consentita \_ \_ \_ Max = None |
| HttpServerQueueLengthProperty                         | Min = 0xA max = 0xFFFF                                     |



 

 

 




