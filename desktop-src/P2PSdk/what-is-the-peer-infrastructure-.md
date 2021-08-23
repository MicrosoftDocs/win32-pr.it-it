---
description: L'infrastruttura peer è un set di diverse API potenti e flessibili.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Che cos'è l'infrastruttura peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e80a5cdcc190fe47ea0a37efd5348ec5f718eaff654543c68bd6e9d355d4d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119287641"
---
# <a name="what-is-the-peer-infrastructure"></a>Che cos'è l'infrastruttura peer?

L'infrastruttura peer è un set di diverse API potenti e flessibili. I componenti principali includono quanto segue:

-   [Peer Graphing API](#peer-graphing-api)
-   [API di raggruppamento peer](#peer-grouping-api)
-   [API di Gestione identità peer](#peer-identity-manager-api)
-   [API del provider dello spazio dei nomi PNRP](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>Peer Graphing API

L'infrastruttura peer offre una tecnologia di grafi che consente di passare informazioni in modo efficiente e affidabile tra peer in un grafo peer. [L'API Peer Graphing](graphing-api.md) garantisce che ogni nodo abbia una visualizzazione coerente dei dati in un grafo.

È possibile usare [l'API Peer Graphing](graphing-api.md) per eseguire le operazioni seguenti:

-   Creare e gestire grafici peer
-   Enumerare e interagire con altri peer in un grafo peer
-   Inviare dati sotto forma di [record](records.md) a ogni nodo in un grafo peer

## <a name="peer-grouping-api"></a>API di raggruppamento peer

[L'API di raggruppamento](grouping-api.md) peer combina e migliora le API [Peer PNRP](#pnrp-namespace-provider-api) e [Graphing](#peer-graphing-api) e aggiunge i due componenti seguenti:

-   Un livello di multiplexing che consente a più applicazioni in esecuzione in un'entità peer di connettersi a un gruppo
-   Un modello di sicurezza specifico che garantisce che solo i peer invitati a un gruppo possano connettersi al gruppo per tutta la durata del gruppo

È possibile usare l'API di raggruppamento peer per eseguire le operazioni seguenti:

-   Creare e gestire gruppi peer protetti
-   Enumerare e interagire con altri peer in un gruppo
-   Inviare dati sotto forma di [record](records.md) a ogni nodo in un gruppo peer

## <a name="peer-identity-manager-api"></a>API di Gestione identità peer

Usando [l'API di Gestione](identity-manager-api.md) identità peer è possibile creare nomi [peer](peer-names.md) sicuri che PNRP può usare per assicurarsi che una persona che pubblica un nome sia ufficialmente proprietaria del nome. I nomi dei peer sono detti anche identità e vengono usati nell'API di raggruppamento di peer per identificare le persone in un gruppo.

È possibile usare [l'API di Gestione identità](identity-manager-api.md) peer per eseguire le operazioni seguenti:

-   Creare, enumerare e gestire le identità peer.

## <a name="pnrp-namespace-provider-api"></a>API del provider dello spazio dei nomi PNRP

L'infrastruttura peer fornisce una tecnologia di risoluzione dei nomi serverless denominata API del provider dello spazio dei [nomi PNRP.](pnrp-namespace-provider-api.md) Usando l'API del provider dello spazio dei nomi PNRP Winsock 2, un peer, un servizio, un dispositivo di elaborazione e un endpoint del gruppo peer possono gestire, registrare, annullare la registrazione e risolvere un altro endpoint in un [cloud](clouds.md)PNRP.

> [!Note]  
> PNRP è l'acronimo del **protocollo di risoluzione dei nomi peer**.

 

 

 



