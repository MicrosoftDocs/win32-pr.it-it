---
description: Connessione e disconnessione di nodi di topologia
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Connessione e disconnessione di nodi di topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6113f4648d0aafbe41dc13090dc83807f746f0acc945f76eca0acf1b4898913f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118064627"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Connessione e disconnessione di nodi di topologia

Perché una topologia funzioni, è necessario che il nodo di origine e il nodo di output siano connessi. Per connettere due nodi di topologia, trascinare l'output del nodo di un nodo nell'input del nodo dell'altro nodo. TopoEdit visualizza la connessione del nodo come linea nera. Equivale a connettere i nodi della topologia chiamando il [**metodo IMFTopologyNode::ConnectOutput.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput)

La topologia può essere risolta solo se la connessione del nodo è valida. cio, se i tipi di supporto dei due nodi sono compatibili. Per informazioni sulla risoluzione delle topologie, vedere Risoluzione di [una topologia con TopoEdit](resolving-a-topology-with-topoedit.md).

Se si tenta di stabilire una connessione da un nodo già connesso, la nuova connessione al nodo sostituisce quella precedente.

Per eliminare una connessione, selezionare la connessione del nodo e premere CANC oppure **scegliere Elimina** dal menu **Topologia.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoModifica](topoedit.md)
</dt> </dl>

 

 



