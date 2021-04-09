---
description: La rete peer-to-peer è una tecnologia di rete senza server che consente a più dispositivi di rete di condividere le risorse e comunicare direttamente tra loro.
ms.assetid: d2a43d3b-2782-4777-8c65-05e2c52930d0
title: Che cos'è la rete peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c456fac9b7695a2846765ee0ccd38c1e5df646e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967528"
---
# <a name="what-is-peer-networking"></a>Che cos'è la rete peer?

La rete peer-to-peer è una tecnologia di rete senza server che consente a più dispositivi di rete di condividere le risorse e comunicare direttamente tra loro. Questa tecnologia è disponibile per i client Windows XP con Service Pack 1 (SP1) e versioni successive che eseguono Advanced Networking Pack per l'infrastruttura peer-to-peer.

L'infrastruttura peer-to-peer è un set di API di rete che consentono di sviluppare applicazioni di rete decentralizzate che usano la potenza collettiva dei computer in una rete. Ad esempio, le applicazioni peer-to-peer possono essere comunicazioni collaborative, tecnologie per la distribuzione di contenuti e così via.

L'infrastruttura peer-to-peer offre un'infrastruttura di rete solida, che consente di concentrarsi sullo sviluppo di applicazioni, poiché l'infrastruttura è stata sviluppata.

L'infrastruttura peer-to-peer include i componenti principali seguenti:

-   [Risoluzione dei nomi peer scalabile e sicura](#scalable-and-secure-peer-name-resolution)
-   [Comunicazione multipoint efficiente](#efficient-multipoint-communication)
-   [Gestione dei dati distribuiti](#distributed-data-management)
-   [Identità peer sicure](#secure-peer-identities)
-   [Gruppi peer-to-peer sicuri](#secure-peer-to-peer-groups)

## <a name="scalable-and-secure-peer-name-resolution"></a>Risoluzione dei nomi peer scalabile e sicura

L' [API del provider dello spazio dei nomi PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) è un protocollo di risoluzione da nome a indirizzo IP. L'ambito o il contesto IPv6 che include tutti i peer partecipanti è denominato [cloud](clouds.md). PNRP consente ai peer di interagire tra loro all'interno di un cloud.

## <a name="efficient-multipoint-communication"></a>Comunicazione multipoint efficiente

L'infrastruttura peer-to-peer include l' [API Graphing](graphing-api.md) che fornisce una comunicazione multipoint efficiente. Analogamente a PNRP, i grafici peer-to-peer consentono a un set di nodi di interagire e passano i dati tra loro sotto forma di [record](records.md). Ogni record generato o aggiornato da un peer viene inviato a tutti i nodi di un grafo.

## <a name="distributed-data-management"></a>Gestione dati distribuite

Gestione dati distribuiti archivia automaticamente tutti i record inviati a un grafo peer-to-peer fino alla data di scadenza specificata per ogni record. La rete peer-to-peer garantisce che ogni nodo in un grafo peer-to-peer abbia una visualizzazione simile del database di record. Se a un grafo peer-to-peer è associato un modello di sicurezza, il grafo contiene le informazioni seguenti:

-   Utenti che possono e non possono connettersi a un grafo
-   Utenti che possono proteggere e convalidare i record in base a criteri definiti esternamente

## <a name="secure-peer-identities"></a>Identità peer sicure

L'infrastruttura peer-to-peer fornisce un' [API di gestione delle identità](identity-manager-api.md) peer-to-peer che consente di creare, gestire e modificare le identità peer. Le identità peer vengono usate per definire i nomi per gli endpoint sicuri in PNRP e possono rappresentare qualsiasi risorsa che partecipa a una rete peer-to-peer, inclusi i gruppi e i servizi peer-to-peer sicuri.

## <a name="secure-peer-to-peer-groups"></a>Gruppi peer-to-peer sicuri

L' [API di raggruppamento](grouping-api.md) peer-to-peer combina le API peer-to-Peer Graphing, Identity Manager e PNRP per formare una soluzione coerente e pratica per lo sviluppo di applicazioni di rete peer-to-peer. L'API di raggruppamento peer-to-peer usa l'API di gestione delle identità peer-to-peer e uno schema di certificato autofirmato per garantire la sicurezza all'interno dell'infrastruttura di Graphing. Ogni gruppo può essere risolto e registrato tramite PNRP, che consente la risoluzione dei nomi dei peer casuali all'interno di un gruppo peer-to-peer registrato. Un gruppo può essere un endpoint in PNRP, proprio come un peer.

Per una panoramica dell'infrastruttura peer-to-peer, vedere l'articolo "[Introduzione alla rete peer-to-peer di Windows XP](https://www.microsoft.com/windowsxp/pro/techinfo/administration/p2p/introduction.asp)".

Per una panoramica delle API nell'infrastruttura peer-to-peer, vedere l'argomento relativo [all'infrastruttura peer](what-is-the-peer-infrastructure-.md).

 

 



