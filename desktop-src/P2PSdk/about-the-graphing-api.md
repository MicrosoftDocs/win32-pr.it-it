---
description: L'API per la rappresentazione grafica dei peer consente alle applicazioni di passare i dati tra i peer in modo efficiente e affidabile. I concetti di base della tecnologia di peer Graph sono i nodi di un grafo peer e le notifiche degli eventi.
ms.assetid: c3530134-bde3-4a9a-b433-4f198430a607
title: Informazioni sull'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b08e320f1c8d176d0bd34cc7a9a9422c6cfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312304"
---
# <a name="about-the-graphing-api"></a>Informazioni sull'API Graphing

L'API per la rappresentazione grafica dei peer consente alle applicazioni di passare i dati tra i peer in modo efficiente e affidabile. I concetti di base della tecnologia di peer Graph sono i **nodi** di un grafo peer e le notifiche degli eventi.

## <a name="nodes"></a>Nodi

Un nodo rappresenta un'istanza specifica di un peer in una rete. L'infrastruttura dell'API per la rappresentazione di peering garantisce che ogni nodo disponga di una visualizzazione coerente dei dati in un grafico. Un nodo presenta le funzionalità seguenti:

-   Può connettersi a un nodo diverso e formare una rete interconnessa denominata grafico a più peer.
-   Può condividere dati con altri nodi in un grafico sotto forma di [record](records.md).
-   Consente di creare connessioni dirette separate dai grafici peer stabiliti tramite l'API di [raggruppamento](about-the-grouping-api.md)peer.
    > [!Note]  
    > Le connessioni dirette consentono ai nodi di inviare i dati privati tra loro.

     

## <a name="event-notices"></a>Notifiche degli eventi

L'API per la grafica di peering dispone di un'infrastruttura di eventi che consente a un'applicazione di registrare e ricevere l'avviso di un evento peer nell'infrastruttura dell'API per la rappresentazione di Peer Graphing. Quando viene modificato un elemento in un grafico peer, un'applicazione invia una notifica di evento per identificare che si è verificata una modifica.

 

 



