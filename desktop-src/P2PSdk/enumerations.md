---
title: Enumerazioni (infrastruttura peer)
description: Utilizzando le enumerazioni, è possibile ottenere un elenco di tutte le entità peer specifiche che soddisfano i criteri specificati.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c90a6806c9fdf7b776980abbaaa3f28643c49360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312281"
---
# <a name="enumerations-peer-infrastructure"></a>Enumerazioni (infrastruttura peer)

Utilizzando le enumerazioni, è possibile ottenere un elenco di tutte le entità peer specifiche che soddisfano i criteri specificati.

**Per ottenere un'enumerazione e recuperare i risultati**

1.  Ottenere un handle per l'enumerazione. Chiamare una funzione **PeerEnum** , ad esempio, chiamare la funzione [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing. Le funzioni **PeerEnum** creano l'enumerazione e restituiscono un handle a tale enumerazione all'applicazione chiamante. Questo handle deve essere utilizzato per recuperare i risultati.
2.  Facoltativamente, ottenere il numero di entità nell'enumerazione. Chiamare una funzione **GetItemCount** , ad esempio, chiamare [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) o [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).
    > [!Note]  
    > È possibile utilizzare il valore restituito dalla funzione **GetItemCount** per determinare il numero di elementi disponibili per il recupero.

     

3.  Recuperare un gruppo di risultati. Chiamare una funzione **GetNextItem** , ad esempio, chiamare [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Quando un'applicazione chiama una funzione **GetNextItem** , specifica il numero di entità da restituire, quindi la funzione restituisce un puntatore a una matrice di puntatori alle entità e il numero di entità, che è sempre minore o uguale al numero specificato. Un'applicazione potrebbe dover chiamare questa funzione molte volte, fino a quando il numero di entità restituite è inferiore al numero richiesto.

     

4.  Quando i dati non sono necessari, liberare il puntatore ai dati. Chiamare una funzione **Freedata** , ad esempio, chiamare [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).
    > [!Note]  
    > Per ulteriori informazioni, vedere [liberazione di dati peer](freeing-peer-data.md).

     

5.  Quando l'applicazione non necessita dell'handle per l'enumerazione, rilasciarla. Chiamare una funzione **EndEnumeration** , ad esempio, chiamare [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) o [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Esempio di enumerazione

Il frammento di codice seguente illustra come eseguire l'enumerazione tramite le identità disponibili.


```C++
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: EnumIdentities
//
// Purpose:  Demonstrate how to enumerate identities.
//
// Returns:  HRESULT
//

HRESULT EnumIdentities(void)
{
    HPEERENUM hPeerEnum = NULL;
    HRESULT hr = PeerEnumIdentities(&hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cIdentities = 0;
        hr = PeerGetItemCount(hPeerEnum, &cIdentities);

        if (SUCCEEDED(hr))
        {
            ULONG i;

            for (i = 0; i < cIdentities; i++)
            {
                ULONG cItem = 1; // process one result at a time
                PEER_NAME_PAIR ** ppNamePair = NULL; // pointer to an array of pointers

                hr = PeerGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNamePair);

                if (SUCCEEDED(hr) && (1 == cItem))
                {
                    wprintf(L"%s [%s]\r\n", (*ppNamePair)->pwzFriendlyName, (*ppNamePair)->pwzPeerName);
                    PeerFreeData(ppNamePair);
                }
            }
        }
        PeerEndEnumeration(hPeerEnum);
    }
 
    return hr;
}
```



 

 



