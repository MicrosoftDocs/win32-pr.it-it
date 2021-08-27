---
description: La rete peer-to-peer è una tecnologia di rete serverless che consente a diversi dispositivi di rete di condividere risorse e comunicare direttamente tra loro.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Che cos'è la rete peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f6ce2175aa32e37c80c4cde5c231540a48c448360974ecbd022c21eb552ccdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034101"
---
# <a name="what-is-peer-networking"></a>Che cos'è la rete peer?

La rete peer-to-peer è una tecnologia di rete serverless che consente a diversi dispositivi di rete di condividere risorse e comunicare direttamente tra loro. Questa tecnologia è disponibile per Windows XP con Service Pack 1 (SP1) e client successivi che eseguono Advanced Networking Pack per l'infrastruttura peer-to-peer.

L'infrastruttura peer-to-peer è un set di API di rete che consentono di sviluppare applicazioni di rete decentralizzate che usano la potenza collettiva dei computer in una rete. Ad esempio, le applicazioni peer-to-peer possono essere comunicazioni collaborative, tecnologie di distribuzione dei contenuti e così via.

L'infrastruttura peer-to-peer offre una solida infrastruttura di rete in modo da potersi concentrare sullo sviluppo di applicazioni, perché l'infrastruttura viene sviluppata per l'utente.

L'infrastruttura peer-to-peer include i componenti principali seguenti:

-   [Risoluzione dei nomi peer scalabile e sicura](#scalable-and-secure-peer-name-resolution)
-   [Comunicazione multipoint efficiente](#efficient-multipoint-communication)
-   [Gestione dei dati distribuiti](#distributed-data-management)
-   [Proteggere le identità peer](#secure-peer-identities)
-   [Proteggere i gruppi peer-to-peer](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Risoluzione dei nomi peer scalabile e sicura

L'API del provider dello spazio dei nomi [Peer Name Resolution Protocol (PNRP)](pnrp-namespace-provider-api.md) è un protocollo di risoluzione da nome a IP. L'ambito o il contesto IPv6 che include tutti i peer partecipanti è denominato [cloud](clouds.md). PNRP consente ai peer di interagire tra loro all'interno di un cloud.

## <a name="efficient-multipoint-communication"></a>Comunicazione multipoint efficiente

L'infrastruttura peer-to-peer include [l'API Graphing](graphing-api.md) che fornisce una comunicazione multipoint efficiente. Come PNRP, il grafo peer-to-peer consente a un set di nodi di interagire e passare dati tra loro sotto forma di [record](records.md). Ogni record generato o aggiornato da un peer viene inviato a tutti i nodi in un grafico.

## <a name="distributed-data-management"></a>Distribuzione Gestione dati

La gestione dei dati distribuiti archivia automaticamente tutti i record inviati a un grafo peer-to-peer fino all'ora di scadenza specificata per ogni record. La rete peer-to-peer garantisce che ogni nodo in un grafo peer-to-peer abbia una visualizzazione simile del database di record. Se a un grafo peer-to-peer è associato un modello di sicurezza, il grafo contiene le informazioni seguenti:

-   Who possibile connettersi a un grafo
-   Who proteggere e convalidare i record in base a criteri definiti esternamente

## <a name="secure-peer-identities"></a>Proteggere le identità peer

L'infrastruttura peer-to-peer fornisce un'API di [Identity Manager](identity-manager-api.md) peer-to-peer che consente di creare, gestire e modificare le identità peer. Le identità peer vengono usate per definire i nomi per gli endpoint sicuri in PNRP e possono rappresentare qualsiasi risorsa che fa parte di una rete peer-to-peer, inclusi i servizi e i gruppi peer-to-peer protetti.

## <a name="secure-peer-to-peer-groups"></a>Proteggere i gruppi peer-to-peer

[L'API](grouping-api.md) di raggruppamento peer-to-peer combina le API Peer-to-Peer Graphing, Identity Manager e PNRP per formare una soluzione coesa e comoda per lo sviluppo di applicazioni di rete peer-to-peer. L'API di raggruppamento peer-to-peer usa l'API di Identity Manager peer-to-peer e uno schema di certificato autofirmato per garantire la sicurezza all'interno dell'infrastruttura di grafi. Ogni gruppo può essere risolto e registrato tramite PNRP, che consente la risoluzione dei nomi dei peer casuali all'interno di un gruppo peer-to-peer registrato. Un gruppo può essere un endpoint in PNRP, proprio come un peer.

Per una panoramica dell'infrastruttura peer-to-peer, vedere l'articolo " Introduction[to Windows XP Peer-to-Peer Networking](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".

Per una panoramica delle API nell'infrastruttura peer-to-peer, vedere l'argomento [Che cos'è l'infrastruttura peer?](what-is-the-peer-infrastructure-.md).

 

 



