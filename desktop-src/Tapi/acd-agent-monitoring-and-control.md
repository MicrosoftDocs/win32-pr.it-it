---
description: Il monitoraggio e il controllo dello stato dell'agente ACD sulle stazioni sono supportati tramite queste funzioni lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState e lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Monitoraggio e controllo degli agenti ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52d3cf9387819bada069920099b19da65e6a1e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057959"
---
# <a name="acd-agent-monitoring-and-control"></a>Monitoraggio e controllo degli agenti ACD

Il monitoraggio e il controllo dello stato dell'agente ACD sulle stazioni sono supportati tramite queste funzioni: [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa), [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa), [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista), [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista), [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup), [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)e [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).

Il messaggio di [**riga \_ AGENTSTATUS**](line-agentstatus.md) viene utilizzato per indicare quando le informazioni sull'agente sono state modificate.

Questi controlli sono associati a un indirizzo anziché a una riga, perché molti sistemi ACD sono implementati con code di ACD diverse associate a pulsanti sul terminale telefonico (e in presenza di chiamate separate). Inoltre, i telefoni degli agenti ACD possono spesso avere un aspetto di chiamata separato per le chiamate personali.

L'architettura, la funzionalità ACD deve essere implementata in un'applicazione basata su server. Le funzioni client menzionate in precedenza, anziché eseguire il mapping al provider di servizi di telefonia, vengono trasmesse a un'applicazione server che ha registrato (usando un'opzione di [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) come gestore per tali funzioni. Il messaggio [**line \_ PROXYREQUEST**](line-proxyrequest.md) viene usato per segnalare all'applicazione handler quando è stata effettuata una richiesta; chiama la funzione [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per restituire i risultati e i dati. Le applicazioni di gestione possono anche chiamare [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) per generare messaggi della riga \_ AGENTSTATUS quando richiesto. Nel caso di un sistema PBX legacy o di un ACD autonomo che implementa la funzionalità ACD, il provider di servizi di telefonia per il Commuter deve includere un'applicazione server proxy che accetta le richieste e le instrada, eventualmente usando le funzioni [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) o un'interfaccia privata, per il provider di servizi, che li instrada al Commuter.

 

 



