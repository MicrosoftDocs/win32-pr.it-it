---
description: Creazione di topologie
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Creazione di topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4048200055066a601f9044ff109f173cb00fc4449a71ea1331b29c8be1a59b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777621"
---
# <a name="creating-topologies"></a>Creazione di topologie

In questa sezione vengono descritte alcune delle procedure generali per la creazione di una topologia.

I passaggi generali per la creazione di una topologia sono i seguenti:

1.  Creare un nuovo oggetto topologia chiamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Questa funzione restituisce un puntatore [**all'interfaccia IMFTopology della**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) topologia.

2.  Inizialmente, la topologia non contiene nodi. Per creare nodi per la topologia, chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Questa funzione restituisce un puntatore [**all'interfaccia IMFTopologyNode del**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) nodo. È necessario specificare il tipo di nodo quando si crea il nodo:

    -   Nodo di origine.

    -   Nodo di trasformazione.

    -   Nodo di output.

    -   Nodo tee.

3.  Inizializzare ogni nodo. Il processo di inizializzazione dipende dal tipo di nodo, come descritto negli argomenti seguenti.

4.  Aggiungere ogni nodo alla topologia chiamando [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Connessione i nodi. Per connettere un nodo, chiamare [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sul nodo upstream e passare un puntatore al nodo downstream.

Gli argomenti seguenti illustrano i passaggi specifici per ogni tipo di nodo.



| Argomento                                                    | Descrizione                     |
|----------------------------------------------------------|---------------------------------|
| [Creazione di nodi di origine](creating-source-nodes.md)       | Come creare un nodo di origine.    |
| [Creazione di nodi di trasformazione](creating-transform-nodes.md) | Come creare un nodo di trasformazione. |
| [Creazione di nodi di output](creating-output-nodes.md)       | Come creare un nodo di output.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



