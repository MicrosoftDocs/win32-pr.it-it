---
description: L'API Peer Graphing consente alle applicazioni di passare i dati tra peer in modo efficiente e affidabile. I concetti di base della tecnologia dei grafi peer sono i nodi di un grafo peer e le comunicazioni degli eventi.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informazioni sull'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735bf7993744aa8d1e76b8c5d98e8d6856bb4e1757224cd0c98f2e7b1b6f710b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011789"
---
# <a name="about-the-graphing-api"></a>Informazioni sull'API Graphing

L'API Peer Graphing consente alle applicazioni di passare i dati tra peer in modo efficiente e affidabile. I concetti di base della tecnologia dei grafi peer sono **i nodi** di un grafo peer e le comunicazioni degli eventi.

## <a name="nodes"></a>Nodi

Un nodo rappresenta un'istanza specifica di un peer in una rete. L'infrastruttura DELL'API Peer Graphing garantisce che ogni nodo abbia una visualizzazione coerente dei dati in un grafo. Un nodo ha le funzionalità seguenti:

-   Può connettersi a un nodo diverso e formare una rete interrelata denominata grafo peer.
-   Può condividere dati con altri nodi in un grafico sotto forma di [record](records.md).
-   È possibile creare connessioni dirette separate dai grafici peer stabiliti tramite [l'API Di raggruppamento peer](about-the-grouping-api.md).
    > [!Note]  
    > Le connessioni dirette consentono ai nodi di inviare dati privati tra loro.

     

## <a name="event-notices"></a>Avvisi per gli eventi

L'API Peer Graphing ha un'infrastruttura di eventi che consente a un'applicazione di registrare e ricevere la notifica di un evento peer all'interno dell'infrastruttura API Peer Graphing. Quando un elemento cambia all'interno di un grafo peer, un'applicazione invia un avviso di evento per identificare che si è verificata una modifica.

 

 



