---
description: L'API Servizi Web nei dispositivi (WSDAPI) fornisce il supporto per il profilo dispositivi per i servizi Web (DPWS) in Windows Vista, che consente la comunicazione di servizi Web (WS) tra PC basati su Windows e dispositivi connessi di rete.
ms.assetid: 61fceca3-a33e-40f7-9370-97605a81eb06
title: Conformità alle specifiche WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52dcf649d8d2771d17f24e983a739c0119a0fe8af67f70b706ba35bcddec20d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991391"
---
# <a name="wsdapi-specification-compliance"></a>Conformità alle specifiche WSDAPI

L'API Servizi Web nei dispositivi (WSDAPI) fornisce il supporto per il profilo dispositivi per i servizi [Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS) in Windows Vista, che consente la comunicazione di servizi Web (WS) tra PC basati su Windows e dispositivi connessi di rete. DPWS assembla specifiche WS di base, ad esempio [WS-Eventing,](https://schemas.xmlsoap.org/ws/2004/08/eventing/) [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)e [WS-MetadataExchange,](https://schemas.xmlsoap.org/ws/2004/09/mex/)e le migliora o le vincola per fornire un set di funzionalità di base per i dispositivi vincolati alle risorse. Questa specifica di base contiene funzionalità necessarie, ad esempio la possibilità di descrivere le proprietà del dispositivo tramite metadati e funzionalità facoltative, ad esempio la possibilità di rifiutare messaggi specifici per motivi di sicurezza.

L'implementazione WSDAPI in Windows Vista è la prima versione del supporto esplicito per DPWS ed è un'implementazione non gestita di DPWS separata e distinta da altre implementazioni di servizi Web , ad esempio [Windows Communication Foundation](/previous-versions/dotnet/netframework-3.0/ms735119(v=vs.85)) o [WS-Management](https://schemas.xmlsoap.org/ws/2005/06/management/).

Gli argomenti seguenti sono di interesse per i produttori di dispositivi e altri implementatori di dispositivi che creano dispositivi che interoperativino con client e host WSDAPI basati su Windows senza usare WSDAPI. Questi argomenti descrivono l'implementazione di WSDAPI rispetto alle specifiche sottostanti. Vengono trattate l'implementazione delle funzionalità necessarie, delle funzionalità facoltative e delle funzionalità aggiuntive non definite nella specifica.

-   [Conformità alle specifiche DPWS](dpws-specification-compliance.md)
-   [Conformità alle specifiche di WS-Discovery](ws-discovery-specification-compliance.md)
-   [WS-MetadataExchange e WS-Transfer conformità alle specifiche](ws-metadataexchange-and-ws-transfer-specification-compliance.md)
-   [Funzionalità WS-Discovery aggiuntive](additional-ws-discovery-functionality.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sviluppo di dispositivi WSD](wsd-device-development.md)
</dt> <dt>

[Implementazione del dispositivo WSD Consigli](wsd-device-implementation-recommendations.md)
</dt> </dl>

 

 
