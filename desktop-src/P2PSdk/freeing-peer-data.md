---
description: Tutti i puntatori restituiti dalle funzioni dell'infrastruttura peer devono essere liberati tramite PeerGraphFreeData o PeerFreeData.
ms.assetid: c7669404-2550-4f0d-908e-540d9a34008f
title: Liberare dati peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1addb0533d5d05e329e19bfe27a89f5616473a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050023"
---
# <a name="freeing-peer-data"></a>Liberare dati peer

Tutti i puntatori restituiti dalle funzioni dell'infrastruttura peer devono essere liberati tramite [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata). Queste funzioni devono essere chiamate solo per le strutture che vengono restituite direttamente da una funzione dell'infrastruttura peer. Non chiamare una funzione FreeData diversa per liberare puntatori annidati, ad esempio, non chiamare una funzione FreeData sui puntatori in una struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) .

## <a name="example-of-freeing-data"></a>Esempio di liberazione dei dati

Il frammento di codice seguente illustra come recuperare le proprietà associate a un grafo, quindi liberare i dati restituiti.


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



 

 



