---
description: Creazione di topologie
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Creazione di topologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401546"
---
# <a name="creating-topologies"></a>Creazione di topologie

In questa sezione vengono descritte alcune delle procedure generali per la creazione di una topologia.

La procedura generale per la creazione di una topologia è la seguente:

1.  Creare un nuovo oggetto topologia chiamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Questa funzione restituisce un puntatore all'interfaccia [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) della topologia.

2.  Inizialmente, la topologia non contiene alcun nodo. Per creare nodi per la topologia, chiamare [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Questa funzione restituisce un puntatore all'interfaccia [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) del nodo. Quando si crea il nodo, è necessario specificare il tipo di nodo:

    -   Nodo di origine.

    -   Nodo Transform.

    -   Nodo di output.

    -   Nodo tee.

3.  Inizializzare ogni nodo. Il processo di inizializzazione dipende dal tipo di nodo, come descritto negli argomenti seguenti.

4.  Aggiungere ogni nodo alla topologia chiamando [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Connettere i nodi. Per connettere un nodo, chiamare [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) sul nodo upstream e passare un puntatore al nodo downstream.

Negli argomenti seguenti vengono illustrati i passaggi specifici per ogni tipo di nodo.



| Argomento                                                    | Descrizione                     |
|----------------------------------------------------------|---------------------------------|
| [Creazione di nodi di origine](creating-source-nodes.md)       | Come creare un nodo di origine.    |
| [Creazione di nodi di trasformazione](creating-transform-nodes.md) | Creazione di un nodo Transform. |
| [Creazione di nodi di output](creating-output-nodes.md)       | Come creare un nodo di output.   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Topologie](topologies.md)
</dt> </dl>

 

 



