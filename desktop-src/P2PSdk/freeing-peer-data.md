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
# <a name="freeing-peer-data"></a><span data-ttu-id="f0d11-103">Liberare dati peer</span><span class="sxs-lookup"><span data-stu-id="f0d11-103">Freeing Peer Data</span></span>

<span data-ttu-id="f0d11-104">Tutti i puntatori restituiti dalle funzioni dell'infrastruttura peer devono essere liberati tramite [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="f0d11-104">All pointers that the Peer Infrastructure functions return must be freed by using [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span> <span data-ttu-id="f0d11-105">Queste funzioni devono essere chiamate solo per le strutture che vengono restituite direttamente da una funzione dell'infrastruttura peer.</span><span class="sxs-lookup"><span data-stu-id="f0d11-105">These functions must only be called for structures that are directly returned by a Peer Infrastructure function.</span></span> <span data-ttu-id="f0d11-106">Non chiamare una funzione FreeData diversa per liberare puntatori annidati, ad esempio, non chiamare una funzione FreeData sui puntatori in una struttura di [**\_ record peer**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="f0d11-106">Do not call a different FreeData function to free nested pointers, for example, do not call a FreeData function on the pointers in a [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span>

## <a name="example-of-freeing-data"></a><span data-ttu-id="f0d11-107">Esempio di liberazione dei dati</span><span class="sxs-lookup"><span data-stu-id="f0d11-107">Example of Freeing Data</span></span>

<span data-ttu-id="f0d11-108">Il frammento di codice seguente illustra come recuperare le proprietà associate a un grafo, quindi liberare i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="f0d11-108">The following code snippet shows you how to retrieve the properties associated with a graph, and then free the data that is returned.</span></span>


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



 

 



