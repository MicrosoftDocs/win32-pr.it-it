---
title: protezione estesa
description: La protezione estesa è un meccanismo che consente di associare un canale protetto esterno, ad esempio SSL ai protocolli di autenticazione del canale interno, ad esempio Kerberos-APREQ e l'autenticazione dell'intestazione HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Protezione estesa nativa-servizi Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895bdfecf994f6673c2ed7e7367bc3a7b5bd70c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298457"
---
# <a name="extended-protection"></a>protezione estesa

La protezione estesa è un meccanismo che consente di associare un canale protetto esterno, ad esempio SSL ai protocolli di autenticazione del canale interno, ad esempio Kerberos-APREQ e l'autenticazione dell'intestazione HTTP.

Il concetto di protezione estesa è definito in RFC2743.

La protezione estesa, se disponibile, viene configurata automaticamente nel client, ma potrebbe richiedere la configurazione nel server per scenari non predefiniti.

## <a name="supported-configurations"></a>Configurazioni supportate

La protezione estesa è supportata quando si utilizza l' [**\_ associazione di \_ canale \_ WS http**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) con le associazioni di sicurezza utilizzando protocolli di autenticazione integrata di Windows, ad esempio [**WS \_ http \_ header \_ auth \_ Security \_ Binding**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) e [**WS \_ Kerberos \_ APREQ \_ message \_ Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)binding. Viene configurato tramite le proprietà di [**sicurezza**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)seguenti:

-   [**\_criteri di \_ \_ protezione estesa \_ della proprietà di sicurezza WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_scenario di \_ \_ protezione estesa \_ della proprietà WS Security \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_identità del \_ \_ servizio proprietà di sicurezza \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

Sono possibili le seguenti configurazioni che coinvolgono la protezione estesa:

Client

-   [**WS \_ L'associazione di \_ sicurezza del trasporto \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) viene utilizzata con il binding di sicurezza del [**\_ messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o [**WS \_ http \_ header \_ auth \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). In questa configurazione l'associazione di autenticazione è associata alla connessione SSL tramite un token di protezione esteso che viene estratto automaticamente dalla connessione SSL.
-   Non viene utilizzato SSL e viene impostata l'associazione di sicurezza per l' [**\_ \_ autenticazione dell'intestazione \_ \_ \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . Il binding di autenticazione viene associato tramite il nome dell'entità server (SPN), che è autonatically determinato [**dall' \_ \_ Indirizzo WS endpoint**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Server

-   [**WS \_ L'associazione di \_ sicurezza del trasporto \_ \_ SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) viene utilizzata con il binding di sicurezza del [**\_ messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o [**WS \_ http \_ header \_ auth \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). In questa configurazione l'associazione di autenticazione è associata alla connessione SSL tramite un token di protezione esteso che viene estratto dalla connessione SSL e convalidato automaticamente.
-   Non viene utilizzato SSL e viene impostata l'associazione di sicurezza per l' [**\_ \_ autenticazione dell'intestazione \_ \_ \_ http ws**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . Il binding di autenticazione è associato tramite il nome dell'entità server (SPN), che deve essere fornito tramite le [**identità del servizio di \_ proprietà di sicurezza \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Quando viene ricevuto un messaggio, il nome SPN viene estratto e convalidato per una corrispondenza esatta con i nomi di servizio forniti. La mancata fornitura di SPN equivale a [**impostare \_ \_ mai i \_ criteri \_ di protezione estesa di WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   Non viene utilizzato SSL, viene specificato il [**\_ \_ \_ \_ \_ server associato dello scenario di protezione estesa WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) e viene utilizzata l' [**\_ \_ \_ \_ \_ associazione di sicurezza del messaggio WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) . In questa configurazione, [**le \_ \_ identità del \_ servizio \_ proprietà di sicurezza WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) non devono essere impostate. Non viene eseguito alcun controllo SPN oltre a ciò che viene eseguito come parte del protocollo Kerberos.
-   [**WS \_ Viene specificato lo \_ scenario di protezione estesa \_ \_ \_ SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) e viene utilizzato il binding di sicurezza del [**\_ messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) o l' [**associazione di sicurezza di autenticazione di WS \_ http \_ header \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) . [**WS \_ È necessario impostare le \_ \_ \_ identità del servizio proprietà di sicurezza**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) .

## <a name="supported-platforms"></a>Piattaforme supportate

La protezione estesa è supportata sulle piattaforme con supporto nel sistema operativo. Windows 7 e Windows Server 2008 R2 offrono supporto incorporato. Altre piattaforme possono richiedere un aggiornamento.

Se il sistema operativo del server non fornisce tale supporto, le informazioni di protezione estese inviate dal client verranno ignorate. Di conseguenza, i client che usano la protezione estesa possono comunicare con un server di questo tipo, ma il vantaggio di sicurezza va perso. Nel client, l' [**\_ associazione di \_ \_ sicurezza del \_ \_ messaggio WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) combinata con il binding di sicurezza del [**\_ \_ trasporto \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) supporta solo la protezione estesa in vista e versioni successive.

Nota: la protezione estesa non disponibile non impedisce l'uso di una particolare configurazione.

## <a name="interoperability"></a>Interoperabilità

Un server configurato in modo predefinito può comunicare con client SOAP, indipendentemente dal fatto che usino o meno la protezione estesa. L'unica eccezione è data dai client Windows XP e Windows Server 2003 WWSAPI che sono stati aggiornati per supportare la protezione estesa e utilizzano sia l' [**associazione di sicurezza del \_ messaggio WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) che l' [**\_ \_ \_ \_ associazione di sicurezza del trasporto WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Per supportare tali client, i [**\_ criteri di protezione estesa WS non devono \_ \_ \_ mai**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) essere specificati dal server. I server configurati con i **criteri di protezione estesa WS rifiuteranno \_ \_ \_ \_ sempre** la comunicazione da client che non utilizzano la protezione estesa. Nel client, l' **\_ associazione di \_ \_ sicurezza del \_ \_ messaggio WS Kerberos APREQ** combinata con il binding di sicurezza del **\_ \_ trasporto \_ \_ WS SSL** comporterà l'invio del messaggio tramite la codifica di trasferimento Chunked HTTP in vista e versioni successive. Ciò può causare problemi di interoperabilità con i server che non supportano il trasferimento Chunked.

Le seguenti enumerazioni/costanti fanno parte della protezione estesa:

-   [**\_criteri di \_ protezione \_ estesa WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**\_scenario di \_ protezione \_ estesa WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

I strutture seguenti fanno parte della protezione estesa:

-   [**\_identità di \_ sicurezza del servizio WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




