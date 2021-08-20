---
description: Tutti i puntatori restituiti dalle funzioni dell'infrastruttura peer devono essere liberati usando PeerGraphFreeData o PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Freeing Peer Data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9492fec9a22da8252188a75d6d4cee73d2055d29f47e25fc7d55a26cc7909c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794578"
---
# <a name="freeing-peer-data"></a>Freeing Peer Data

Tutti i puntatori restituiti dalle funzioni dell'infrastruttura peer devono essere liberati usando [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) [**o PeerFreeData.**](/windows/desktop/api/P2P/nf-p2p-peerfreedata) Queste funzioni devono essere chiamate solo per le strutture restituite direttamente da una funzione dell'infrastruttura peer. Non chiamare una funzione FreeData diversa per liberare puntatori annidati, ad esempio non chiamare una funzione FreeData sui puntatori in una struttura [**PEER \_ RECORD.**](/windows/desktop/api/P2P/ns-p2p-peer_record)

## <a name="example-of-freeing-data"></a>Esempio di freeing dei dati

Il frammento di codice seguente illustra come recuperare le proprietà associate a un grafo e quindi liberare i dati restituiti.


```C++
PEER_GRAPH_PROPERTIES  * pGraphProperties = NULL;
HRESULT hr = PeerGraphGetProperties(hGraph, &pGraphProperties);
if (SUCCEEDED(hr) && (NULL != pGraphProperties))
{
  // use pGraphProperties
  wprintf(L"%d\n", pGraphProperties->pwzGraphId);

  // release the data
  PeerGraphFreeData(pGraphProperties);
}
```



 

 



