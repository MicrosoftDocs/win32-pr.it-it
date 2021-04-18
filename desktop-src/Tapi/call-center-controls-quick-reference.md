---
description: Le interfacce del Call Center forniscono metodi che accodano e distribuiscono le chiamate all'interno di un Call Center.
ms.assetid: 0b9a455d-a614-4698-90ab-e81f020fad3e
title: Riferimento rapido ai controlli Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfc34f1f30fc1f06d543cb7d5fa811517040523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312733"
---
# <a name="call-center-controls-quick-reference"></a>Riferimento rapido ai controlli Call Center

Le interfacce del Call Center forniscono metodi che accodano e distribuiscono le chiamate all'interno di un Call Center. TAPI 3. x definisce cinque oggetti principali del Call Center: ACDGroup, Agent, AgentHandler, AgentSession e Queue. Tutti questi oggetti possono essere estesi per fornire metodi specifici dell'implementazione. Inoltre, l'interfaccia [**ITTAPICallCenter**](/windows/win32/api/tapi3cc/nn-tapi3cc-ittapicallcenter) nell'oggetto TAPI fornisce metodi per enumerare gli oggetti AgentHandler.



| Interfaccia Call Center                              | Descrizione                                                              |
|----------------------------------------------------|--------------------------------------------------------------------------|
| [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup)                   | Ottiene le informazioni sul nome e sulla coda per un gruppo ACD.                        |
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Ottiene la descrizione degli eventi del gruppo ACD.                                    |
| [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent)                         | Fornisce metodi per impostare e ottenere informazioni relative a un agente.         |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Interfaccia di notifica per [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                   |
| [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)           | Fornisce metodi per creare oggetti agente ed enumerare gruppi ACD.       |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Ottiene la descrizione degli eventi AgentHandler.                                 |
| [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession)           | Fornisce metodi per impostare e ottenere informazioni relative a una sessione di Agent. |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Interfaccia di notifica per [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).     |
| [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue)                         | Ottiene e imposta le informazioni relative a una coda.                            |
| [**ITQueueEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueueevent)               | Ottiene informazioni relative a un evento della coda.                               |
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)             | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).                             |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)                   | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).                                   |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler)     | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler).                     |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession)     | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession).                     |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)                   | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).                                   |



 

Le interfacce seguenti enumerano gli elementi TAPI 3. x in base agli standard COM. Queste interfacce costituiscono oggetti autonomi e vengono riepilogate anche con gli oggetti correlati.



| Interfaccia Enumerator                           | Descrizione                                          |
|------------------------------------------------|------------------------------------------------------|
| [**IEnumACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumacdgroup)         | Enumera [**ITACDGroup**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroup).         |
| [**IEnumAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagent)               | Enumera [**ITAgent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagent).               |
| [**IEnumAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagenthandler) | Enumera [**ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler). |
| [**IEnumAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumagentsession) | Enumera [**ITAgentSession**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsession). |
| [**IEnumQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-ienumqueue)               | Enumera [**ITQueue**](/windows/win32/api/tapi3cc/nn-tapi3cc-itqueue).               |



 

Le interfacce di evento (notifica) consentono a un'applicazione TAPI 3. x di rispondere agli eventi asincroni. È necessario chiamare il metodo [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e impostare una maschera di filtro eventi per abilitare la ricezione degli eventi di richiesta. Se non si chiama **ITTAPI::p UT \_ EventFilter**, l'applicazione non riceverà alcun evento.



| Interfaccia evento                                    | Descrizione                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------|
| [**ITACDGroupEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itacdgroupevent)         | Recupera la descrizione degli eventi del gruppo ACD (Automatic Call Distribution). |
| [**ITAgentEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentevent)               | Recupera la descrizione degli eventi di Agent.                                   |
| [**ITAgentHandlerEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandlerevent) | Recupera la descrizione degli eventi del gestore agenti.                           |
| [**ITAgentSessionEvent**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagentsessionevent) | Recupera la descrizione degli eventi di sessione di Agent.                           |



 

 

 
