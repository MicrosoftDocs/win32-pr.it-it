---
description: Connessione e disconnessione di nodi della topologia
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Connessione e disconnessione di nodi della topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305475"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Connessione e disconnessione di nodi della topologia

Per una topologia funzionante, è necessario che il nodo di origine e il nodo di output siano connessi. Per connettere due nodi della topologia, trascinare l'output del nodo di un nodo nell'input del nodo dell'altro nodo. TopoEdit Visualizza la connessione al nodo come linea nera. Equivale a connettere i nodi della topologia chiamando il metodo [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .

La topologia può essere risolta solo se la connessione al nodo è valida. ovvero se i tipi di supporti dei due nodi sono compatibili. Per informazioni sulla risoluzione delle topologie, vedere la pagina relativa alla [risoluzione di una topologia con TopoEdit](resolving-a-topology-with-topoedit.md).

Se si tenta di effettuare una connessione da un nodo già connesso, la nuova connessione al nodo sostituisce quella precedente.

Per eliminare una connessione, selezionare la connessione al nodo e premere il tasto CANC o scegliere **Elimina** dal menu **topologia** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di topologie tramite TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



