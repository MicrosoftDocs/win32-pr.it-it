---
description: WSDAPI (Web Services on Devices) fornisce il supporto per il profilo dei dispositivi per i servizi Web (DPWS) in Windows Vista, che consente la comunicazione dei servizi Web (WS) tra i PC basati su Windows e i dispositivi connessi alla rete.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformità della specifica WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d915a8f963ff346ad8a8fee8a2188aa69cecb8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231658"
---
# <a name="wsdapi-specification-compliance"></a>Conformità della specifica WSDAPI

WSDAPI (Web Services on Devices) fornisce il supporto per il [profilo dei dispositivi per i servizi Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) in Windows Vista, che consente la comunicazione dei servizi Web (WS) tra i PC basati su Windows e i dispositivi connessi alla rete. DPWS assembla le specifiche WS di base, ad esempio [WS-Eventing](https://schemas.xmlsoap.org/ws/2004/08/eventing/), [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/), e migliora o vincola le specifiche per fornire un set di base di funzionalità per i dispositivi con vincoli di risorse. Questa specifica di base contiene le funzionalità necessarie, ad esempio la possibilità di descrivere le proprietà del dispositivo tramite metadati e la funzionalità facoltativa, ad esempio la possibilità di rifiutare messaggi specifici per motivi di sicurezza.

L'implementazione di WSDAPI in Windows Vista è la prima versione del supporto esplicito per DPWS e è un'implementazione non gestita di DPWS che è separata e distinta dalle altre implementazioni di servizi Web, ad esempio [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/).

Gli argomenti seguenti sono di particolare interesse per i produttori di dispositivi e altri implementatori di dispositivi che creano dispositivi che interagiscono con client e host WSDAPI basati su Windows senza usare WSDAPI. In questi argomenti viene descritta l'implementazione di WSDAPI rispetto alle specifiche sottostanti. Esse coprono l'implementazione di funzionalità necessarie, funzionalità facoltative e funzionalità aggiuntive non definite nella specifica.

-   [Conformità della specifica DPWS](dpws-specification-compliance.md)
-   [Conformità specifica WS-Discovery](ws-discovery-specification-compliance.md)
-   [Conformità alla specifica WS-MetadataExchange e WS-Transfer](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funzionalità di WS-Discovery aggiuntive](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di dispositivi WSD](wsd-device-development.md)
</dt> <dt>

[Indicazioni sull'implementazione di dispositivi WSD](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
