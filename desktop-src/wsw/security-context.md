---
title: Contesto di sicurezza
description: I contesti di sicurezza consentono di stabilire un contesto di sicurezza dei messaggi in base a WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contesto di sicurezza nativo -Web-Services
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06dc1754133f47cf06c5c12e7318a94525be3c821f3db52a7e7513349c3100be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083175"
---
# <a name="security-context"></a>Contesto di sicurezza

I contesti di sicurezza consentono di stabilire un contesto di sicurezza dei messaggi in base a WS-SecureConversation. Tale contesto può quindi essere usato per proteggere i messaggi come alternativa alla sicurezza singola in cui le credenziali vengono trasmesse per ogni richiesta. Il contesto di sicurezza stabilito è un metodo più efficiente per proteggere i messaggi quando vengono s scambiati più messaggi.


I contesti di sicurezza richiedono la presenza di credenziali di sicurezza bootstrap usate per proteggere i messaggi inviati nel contesto. A questo scopo è possibile utilizzare le strutture [**WS \_ KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) [**WS XML TOKEN \_ MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e [**WS USERNAME MESSAGE SECURITY \_ \_ \_ \_ BINDING.**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)

I contesti di sicurezza sono una funzionalità di sicurezza dei messaggi e vengono configurati tramite associazioni di sicurezza dei messaggi.

## <a name="client"></a>Client

Sul lato client, il contesto di sicurezza è associato a un canale specifico. Viene configurato utilizzando [**WS \_ SECURITY CONTEXT MESSAGE SECURITY \_ \_ \_ \_ BINDING**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Il comportamento e la durata del contesto sono determinati dal canale. Quando il primo messaggio viene inviato sul canale, viene stabilito il contesto di sicurezza. Successivamente, il contesto viene rinnovato in modo proattivo a intervalli configurabili. Se il server restituisce un errore che indica che il contesto richiede il rinnovo, il contesto viene rinnovato quando viene inviato il messaggio successivo. Se il canale è nello stato aperto, il contesto viene annullato da un messaggio di annullamento alla chiusura del canale.

## <a name="server"></a>Server

Nel server un contesto di sicurezza è configurato come nel client. Tuttavia, non è associato ad alcun canale specifico. Al contrario, tutti i canali creati per il listener con [**WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ impostato**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sono in grado di ricevere messaggi con uno qualsiasi dei contesti di sicurezza stabiliti nei canali di tale listener.

Quando un messaggio arriva su un canale che supporta contesti di sicurezza, il contesto utilizzato da tale messaggio può essere ottenuto chiamando la funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con [**WS \_ MESSAGE PROPERTY SECURITY \_ \_ \_ CONTEXT**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). Il valore recuperato può essere usato con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).

## <a name="metadata"></a>Metadati

La [**struttura WS \_ SECURITY CONTEXT MESSAGE SECURITY BINDING \_ \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) viene utilizzata per estrarre i criteri del contesto di sicurezza dai metadati. Per altre informazioni, vedere [Importazione di metadati.](metadata-import.md)

Gli elementi API seguenti vengono usati con i contesti di sicurezza.

| Enumerazione                                                                    | Descrizione                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**ID DELLA \_ PROPRIETÀ DEL CONTESTO DI \_ \_ SICUREZZA WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica una proprietà di un oggetto contesto di sicurezza. |



 



| Funzione                                                             | Descrizione                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Ottiene una proprietà del contesto di sicurezza specificato. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoca un contesto di sicurezza.                        |



 



| Handle                                           | Descrizione                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [CONTESTO DI \_ SICUREZZA WS \_](ws-security-context.md) | Tipo opaco utilizzato per fare riferimento a un oggetto contesto di sicurezza. |



 



| Struttura                                                               | Descrizione                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**PROPRIETÀ DEL \_ CONTESTO DI \_ SICUREZZA \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Definisce una proprietà di un contesto [di \_ sicurezza \_ WS.](ws-security-context.md) |



 

 

 




