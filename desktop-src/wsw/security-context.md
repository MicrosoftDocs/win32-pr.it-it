---
title: Contesto di sicurezza
description: I contesti di sicurezza consentono di stabilire un contesto di sicurezza del messaggio in base a WS-SecureConversation.
ms.assetid: bea92650-21bd-41d4-9dba-043d6779d85f
keywords:
- Contesto di sicurezza nativo-servizi Web
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff86ea12ae7a4b8bd554e25cde534cba3b4dcb4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339675"
---
# <a name="security-context"></a>Contesto di sicurezza

I contesti di sicurezza consentono di stabilire un contesto di sicurezza del messaggio in base a WS-SecureConversation. Tale contesto può quindi essere utilizzato per proteggere i messaggi come alternativa alla sicurezza di un singolo punto in cui le credenziali vengono trasmesse per ogni richiesta. Il contesto di sicurezza stabilito è un metodo più efficiente per proteggere i messaggi quando vengono scambiati più messaggi.


I contesti di sicurezza richiedono la presenza di credenziali di sicurezza bootstrap utilizzate per proteggere i messaggi inviati nel contesto. Per questo scopo è possibile usare l'associazione di [**\_ sicurezza del messaggio WS Kerberos \_ \_ \_ \_ APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding), l'associazione di sicurezza dei messaggi del [**\_ \_ token WS \_ \_ \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)e le strutture di [**\_ \_ \_ \_ associazione di sicurezza dei messaggi WS nomeutente**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding) .

I contesti di sicurezza sono una funzionalità di sicurezza dei messaggi e vengono configurati tramite associazioni di sicurezza dei messaggi.

## <a name="client"></a>Client

Sul lato client, il contesto di sicurezza è associato a un canale specifico. Viene configurato utilizzando l' [**associazione di \_ \_ sicurezza del \_ messaggio \_ \_ del contesto di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding). Il comportamento e la durata del contesto sono determinati dal canale. Quando il primo messaggio viene inviato sul canale, viene stabilito il contesto di sicurezza. Successivamente, il contesto viene rinnovato in modo proattivo a un intervallo configurabile. Se il server restituisce un errore che indica che il contesto richiede il rinnovo, il contesto viene rinnovato quando viene inviato il messaggio successivo. Se il canale si trova nello stato aperto, il contesto viene annullato da un messaggio di annullamento quando il canale viene chiuso.

## <a name="server"></a>Server

Sul server, un contesto di sicurezza viene configurato in modo analogo a quello del client. Tuttavia, non è associato a un canale particolare. Al contrario, tutti i canali creati per il listener con il set di [**associazioni di sicurezza del messaggio del \_ contesto di sicurezza \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding) sono in grado di ricevere messaggi con uno dei contesti di sicurezza stabiliti nei canali del listener.

Quando un messaggio arriva su un canale che supporta i contesti di sicurezza, il contesto utilizzato da tale messaggio può essere ottenuto chiamando la funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) con [**il \_ \_ contesto di \_ sicurezza \_ della proprietà del messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). Il valore recuperato può essere usato con [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext) e [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty).

## <a name="metadata"></a>Metadati

La struttura del vincolo di sicurezza del messaggio del contesto di sicurezza WS viene utilizzata per estrarre i criteri del contesto di sicurezza dai metadati. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) Per altre informazioni, vedere [importazione di metadati](metadata-import.md).

I seguenti elementi API vengono utilizzati con i contesti di sicurezza.

| Enumerazione                                                                    | Descrizione                                         |
|--------------------------------------------------------------------------------|-----------------------------------------------------|
| [**\_ID della \_ proprietà del contesto di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_context_property_id) | Identifica una proprietà di un oggetto contesto di sicurezza. |



 



| Funzione                                                             | Descrizione                                        |
|----------------------------------------------------------------------|----------------------------------------------------|
| [**WsGetSecurityContextProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritycontextproperty) | Ottiene una proprietà del contesto di sicurezza specificato. |
| [**WsRevokeSecurityContext**](/windows/desktop/api/WebServices/nf-webservices-wsrevokesecuritycontext)           | Revoca un contesto di sicurezza.                        |



 



| Handle                                           | Descrizione                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [\_contesto di sicurezza WS \_](ws-security-context.md) | Tipo opaco utilizzato per fare riferimento a un oggetto contesto di sicurezza. |



 



| Struttura                                                               | Descrizione                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**\_proprietà del \_ contesto di sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_property) | Definisce una proprietà di un [ \_ \_ contesto di sicurezza WS](ws-security-context.md). |



 

 

 




