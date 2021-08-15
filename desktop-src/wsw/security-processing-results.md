---
title: Risultati dell'elaborazione della sicurezza
description: In un canale protetto, solo i messaggi che superano correttamente i controlli di sicurezza vengono recapitati all'applicazione.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Servizi Web dei risultati dell'elaborazione della sicurezza per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53009729b3d7f1c8ff6b9e38a054d8dbadf202b7a0caa4a92c7861232c8390a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962930"
---
# <a name="security-processing-results"></a>Risultati dell'elaborazione della sicurezza

In un canale protetto, solo i messaggi che superano correttamente i controlli di sicurezza vengono recapitati all'applicazione. Per questi messaggi, alcuni risultati della verifica di sicurezza vengono associati come proprietà del messaggio e l'applicazione può estrarre ed esaminare queste proprietà per eseguire passaggi aggiuntivi, ad esempio i controlli di autorizzazione.


La funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) può essere usata per recuperare qualsiasi proprietà correlata alla sicurezza definita in [**WS \_ MESSAGE PROPERTY \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** restituisce un errore per le query che chiedono proprietà di sicurezza non applicabili al tipo di sicurezza usato nel canale. Il messaggio continua a essere proprietario delle proprietà restituite dalla funzione di query.

Gli elementi API seguenti vengono usati con i risultati dell'elaborazione della sicurezza.

| Enumerazione                                                                | Descrizione                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**ID PROPRIETÀ TOKEN DI SICUREZZA WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Definisce le chiavi per i campi e le proprietà che possono essere estratti da un token di sicurezza. |



 



| Funzione                                                         | Descrizione                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Estrae un campo o una proprietà da un token di sicurezza. |



 



| Handle                                       | Descrizione                                     |
|----------------------------------------------|-------------------------------------------------|
| [TOKEN DI SICUREZZA WS \_ \_](ws-security-token.md) | Handle opaco che rappresenta un token di sicurezza. |



 

 

 




