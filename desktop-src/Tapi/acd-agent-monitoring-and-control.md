---
description: Il monitoraggio e il controllo dello stato dell'agente ACD nelle stazioni sono supportati tramite queste funzioni lineGetAgentCaps lineGetAgentStatus lineGetAgentGroupList lineGetAgentActivityList lineSetAgentGroup lineSetAgentState e lineSetAgentActivity.
ms.assetid: 2851fe54-f807-4cef-b6ca-2dcc7e1ae6fb
title: Monitoraggio e controllo dell'agente ACD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8986fc31e8b30e8b32c4b347a26abfa46adbd426c20c506553ae2f41ea879a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872658"
---
# <a name="acd-agent-monitoring-and-control"></a>Monitoraggio e controllo dell'agente ACD

Il monitoraggio e il controllo dello stato dell'agente ACD nelle stazioni sono supportati tramite queste funzioni: [**lineGetAgentCaps,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) [**lineGetAgentStatus,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) [**lineGetAgentGroupList,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) [**lineGetAgentActivityList,**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) [**lineSetAgentGroup,**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup) [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate)e [**lineSetAgentActivity.**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity)

Il [**messaggio LINE \_ AGENTSTATUS**](line-agentstatus.md) viene usato per indicare quando le informazioni sull'agente sono state modificate.

Questi controlli sono associati a un indirizzo anziché a una riga perché molti sistemi ACD vengono implementati con code ACD diverse associate ai pulsanti sul terminale telefonico (e aspetti di chiamata separati). Inoltre, i telefoni dell'agente ACD possono spesso avere aspetti di chiamata separati per le chiamate personali.

Dal punto di vista dell'architettura, la funzionalità ACD deve essere implementata in un'applicazione basata su server. Le funzioni client citate in precedenza, anziché il mapping al provider di servizi di telefonia, vengono trasmesse a un'applicazione server registrata (usando l'opzione [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)) come gestore per tali funzioni. Il [**messaggio LINE \_ PROXYREQUEST**](line-proxyrequest.md) viene usato per segnalare all'applicazione del gestore quando è stata effettuata una richiesta. Chiama la [**funzione lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) per restituire risultati e dati. Le applicazioni del gestore possono anche chiamare [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) per generare messaggi LINE \_ AGENTSTATUS quando necessario. Nel caso di un CENTRALINO legacy o un ACD autonomo che implementa la funzionalità ACD, il provider di servizi di telefonia per il commutatore deve includere un'applicazione server proxy che accetta le richieste e le instrada (possibilmente usando funzioni [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) o un'interfaccia privata) al provider di servizi, che le indirizza al commutatore.

 

 



