---
title: Risultati dell'elaborazione della sicurezza
description: Su un canale sicuro, solo i messaggi che passano correttamente i controlli di sicurezza vengono recapitati all'applicazione.
ms.assetid: 891e1f91-406e-4997-9da6-59b5fe578d0d
keywords:
- Servizi Web per i risultati dell'elaborazione della sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf6f8964d14c8cfdca3f6bd66b2f24e9fa611d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "106300686"
---
# <a name="security-processing-results"></a>Risultati dell'elaborazione della sicurezza

Su un canale sicuro, solo i messaggi che passano correttamente i controlli di sicurezza vengono recapitati all'applicazione. Per questi messaggi, alcuni risultati della verifica della sicurezza sono allegati come proprietà del messaggio e l'applicazione può estrarre ed esaminare tali proprietà per eseguire passaggi aggiuntivi, ad esempio i controlli di autorizzazione.


La funzione [**WsGetMessageProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmessageproperty) può essere utilizzata per recuperare tutte le proprietà correlate alla sicurezza definite nell' [**ID della \_ \_ proprietà del \_ messaggio WS**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id). **WsGetMessageProperty** restituisce un errore per le query che richiedono proprietà di sicurezza non applicabili al tipo di sicurezza usato sul canale. Il messaggio continua a essere proprietario delle proprietà restituite dalla funzione di query.

I seguenti elementi API vengono usati con i risultati dell'elaborazione della sicurezza.

| Enumerazione                                                                | Descrizione                                                                                 |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**\_ID della \_ proprietà del token di sicurezza WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_token_property_id) | Definisce le chiavi per i campi e le proprietà che possono essere estratti da un token di sicurezza. |



 



| Funzione                                                         | Descrizione                                           |
|------------------------------------------------------------------|-------------------------------------------------------|
| [**WsGetSecurityTokenProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetsecuritytokenproperty) | Estrae un campo o una proprietà da un token di sicurezza. |



 



| Handle                                       | Descrizione                                     |
|----------------------------------------------|-------------------------------------------------|
| [\_token di sicurezza WS \_](ws-security-token.md) | Handle opaco che rappresenta un token di sicurezza. |



 

 

 




