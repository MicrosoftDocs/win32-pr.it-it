---
title: Enumerazioni (infrastruttura peer)
description: Usando le enumerazioni, è possibile ottenere un elenco di tutte le entità peer specifiche che soddisfano i criteri.
ms.assetid: 81391e4f-aea1-4f5e-a32b-436a3856993b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6514866001734fb0ba0d73c94d5d4d8f8b4cfc6987d121f058a6bfcb00f792c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887631"
---
# <a name="enumerations-peer-infrastructure"></a>Enumerazioni (infrastruttura peer)

Usando le enumerazioni, è possibile ottenere un elenco di tutte le entità peer specifiche che soddisfano i criteri.

**Per ottenere un'enumerazione e recuperare i risultati**

1.  Ottenere un handle per l'enumerazione . Chiamare una **funzione PeerEnum,** ad esempio, chiamare la funzione Peer Graphing [**PeerGraphEnumRecords.**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Le **funzioni PeerEnum** creano l'enumerazione e restituiscono un handle a tale enumerazione all'applicazione chiamante. Questo handle deve essere usato per recuperare i risultati.
2.  Facoltativamente, ottenere il numero di entità nell'enumerazione . Chiamare una **funzione GetItemCount,** ad esempio [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) o [**PeerGetItemCount.**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount)
    > [!Note]  
    > È possibile usare il valore restituito dalla **funzione GetItemCount** per determinare il numero di elementi disponibili per il recupero.

     

3.  Recuperare un gruppo di risultati. Chiamare una **funzione GetNextItem,** ad esempio [**Chiamare PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).
    > [!Note]  
    > Quando un'applicazione chiama una funzione **GetNextItem,** specifica il numero di entità da restituire e quindi la funzione restituisce un puntatore a una matrice di puntatori alle entità e il numero di entità, che è sempre minore o uguale al numero specificato. Un'applicazione potrebbe dover chiamare questa funzione più volte, fino a quando il numero di entità restituite non è inferiore al numero richiesto.

     

4.  Quando i dati non sono necessari, liberare il puntatore ai dati. Chiamare una **funzione FreeData,** ad esempio [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) [**o PeerFreeData.**](/windows/desktop/api/P2P/nf-p2p-peerfreedata)
    > [!Note]  
    > Per altre informazioni, vedere [Freeing Peer Data](freeing-peer-data.md).

     

5.  Dopo che l'applicazione non ha bisogno dell'handle per l'enumerazione, rilasciarlo. Chiamare una **funzione EndEnumeration,** ad [**esempio, chiamare PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) [**o PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).

## <a name="example-of-an-enumeration"></a>Esempio di enumerazione

Il frammento di codice seguente illustra come enumerare tramite le identità disponibili.


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



 

 



