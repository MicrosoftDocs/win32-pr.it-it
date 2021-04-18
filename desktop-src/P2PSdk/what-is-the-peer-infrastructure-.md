---
description: L'infrastruttura peer è un set di diverse API potenti e flessibili.
ms.assetid: aed7585a-88e5-4ca3-a8c3-e2ccfe13d35d
title: Che cos'è l'infrastruttura peer?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 873717b3f90497fe9ab9f50bb9c18e6f0692a4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312209"
---
# <a name="what-is-the-peer-infrastructure"></a>Che cos'è l'infrastruttura peer?

L'infrastruttura peer è un set di diverse API potenti e flessibili. I componenti principali includono i seguenti:

-   [API di Peer Graphing](#peer-graphing-api)
-   [API di raggruppamento peer](#peer-grouping-api)
-   [API peer Identity Manager](#peer-identity-manager-api)
-   [API provider dello spazio dei nomi PNRP](#pnrp-namespace-provider-api)

## <a name="peer-graphing-api"></a>API di Peer Graphing

L'infrastruttura peer offre una tecnologia di grafica che consente di passare le informazioni in modo efficiente e affidabile tra i peer in un grafo peer. L' [API per la rappresentazione grafica dei peer](graphing-api.md) garantisce che ogni nodo disponga di una visualizzazione coerente dei dati in un grafico.

È possibile usare l' [API di Peer Graphing](graphing-api.md) per eseguire le operazioni seguenti:

-   Creare e gestire grafici peer
-   Enumerare e interagire con altri peer in un grafico peer
-   Inviare dati sotto forma di [record](records.md) a ogni nodo in un grafico peer

## <a name="peer-grouping-api"></a>API di raggruppamento peer

L' [API di raggruppamento peer](grouping-api.md) combina e migliora le API peer [PNRP](#pnrp-namespace-provider-api) e [Graphing](#peer-graphing-api) e aggiunge i due componenti seguenti:

-   Livello di multiplexing che consente a più applicazioni in esecuzione su un'entità peer di connettersi a un gruppo
-   Un modello di sicurezza specifico che garantisce che solo i peer invitati a un gruppo possano connettersi al gruppo attraverso la durata del gruppo

È possibile utilizzare l'API di raggruppamento peer per eseguire le operazioni seguenti:

-   Creare e gestire gruppi di peer sicuri
-   Enumerare e interagire con altri peer in un gruppo
-   Inviare dati sotto forma di [record](records.md) a ogni nodo in un gruppo peer

## <a name="peer-identity-manager-api"></a>API peer Identity Manager

Usando l' [API peer Identity Manager](identity-manager-api.md) è possibile creare nomi di [peer](peer-names.md) sicuri che PNRP può usare per garantire che un utente che pubblica un nome sia ufficialmente proprietario del nome. I nomi di peer sono anche denominati identità e vengono usati nell'API di raggruppamento peer per identificare gli utenti di un gruppo.

È possibile usare l' [API peer Identity Manager](identity-manager-api.md) per eseguire le operazioni seguenti:

-   Creazione, enumerazione e gestione delle identità peer.

## <a name="pnrp-namespace-provider-api"></a>API provider dello spazio dei nomi PNRP

L'infrastruttura peer fornisce una tecnologia di risoluzione dei nomi senza server denominata [API del provider dello spazio dei nomi PNRP](pnrp-namespace-provider-api.md). Utilizzando l'API del provider dello spazio dei nomi PNRP 2 PNRP, un endpoint di peer, servizio, calcolo e gruppo peer può gestire, registrare, annullare la registrazione e risolvere un altro endpoint in un [cloud](clouds.md)PNRP.

> [!Note]  
> PNRP è un acronimo del **protocollo di risoluzione dei nomi peer**.

 

 

 



