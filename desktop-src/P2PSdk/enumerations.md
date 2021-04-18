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
# <a name="enumerations-peer-infrastructure"></a><span data-ttu-id="eb157-103">Enumerazioni (infrastruttura peer)</span><span class="sxs-lookup"><span data-stu-id="eb157-103">Enumerations (Peer Infrastructure)</span></span>

<span data-ttu-id="eb157-104">Utilizzando le enumerazioni, è possibile ottenere un elenco di tutte le entità peer specifiche che soddisfano i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="eb157-104">By using Enumerations, you can obtain a list of all the specific peer entities that match your criteria.</span></span>

<span data-ttu-id="eb157-105">**Per ottenere un'enumerazione e recuperare i risultati**</span><span class="sxs-lookup"><span data-stu-id="eb157-105">**To obtain an enumeration and retrieve the results**</span></span>

1.  <span data-ttu-id="eb157-106">Ottenere un handle per l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="eb157-106">Obtain a handle to the enumeration.</span></span> <span data-ttu-id="eb157-107">Chiamare una funzione **PeerEnum** , ad esempio, chiamare la funzione [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing.</span><span class="sxs-lookup"><span data-stu-id="eb157-107">Call a **PeerEnum** function, for example, call the [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords) Peer Graphing function.</span></span> <span data-ttu-id="eb157-108">Le funzioni **PeerEnum** creano l'enumerazione e restituiscono un handle a tale enumerazione all'applicazione chiamante.</span><span class="sxs-lookup"><span data-stu-id="eb157-108">The **PeerEnum** functions create the enumeration, and return a handle to that enumeration to the calling application.</span></span> <span data-ttu-id="eb157-109">Questo handle deve essere utilizzato per recuperare i risultati.</span><span class="sxs-lookup"><span data-stu-id="eb157-109">This handle must be used to retrieve the results.</span></span>
2.  <span data-ttu-id="eb157-110">Facoltativamente, ottenere il numero di entità nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="eb157-110">Optionally, obtain the number of entities in the enumeration.</span></span> <span data-ttu-id="eb157-111">Chiamare una funzione **GetItemCount** , ad esempio, chiamare [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) o [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span><span class="sxs-lookup"><span data-stu-id="eb157-111">Call a **GetItemCount** function, for example, call [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount) or [**PeerGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergetitemcount).</span></span>
    > [!Note]  
    > <span data-ttu-id="eb157-112">È possibile utilizzare il valore restituito dalla funzione **GetItemCount** per determinare il numero di elementi disponibili per il recupero.</span><span class="sxs-lookup"><span data-stu-id="eb157-112">You can use the value returned by the **GetItemCount** function to determine the number of items available to retrieve.</span></span>

     

3.  <span data-ttu-id="eb157-113">Recuperare un gruppo di risultati.</span><span class="sxs-lookup"><span data-stu-id="eb157-113">Retrieve a group of results.</span></span> <span data-ttu-id="eb157-114">Chiamare una funzione **GetNextItem** , ad esempio, chiamare [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span><span class="sxs-lookup"><span data-stu-id="eb157-114">Call a **GetNextItem** function, for example, call [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem).</span></span>
    > [!Note]  
    > <span data-ttu-id="eb157-115">Quando un'applicazione chiama una funzione **GetNextItem** , specifica il numero di entità da restituire, quindi la funzione restituisce un puntatore a una matrice di puntatori alle entità e il numero di entità, che è sempre minore o uguale al numero specificato.</span><span class="sxs-lookup"><span data-stu-id="eb157-115">When an application calls a **GetNextItem** function, it specifies the number of entities to return, and then the function returns a pointer to an array of pointers to the entities, and the number of entities, which is always less than or equal to the number specified.</span></span> <span data-ttu-id="eb157-116">Un'applicazione potrebbe dover chiamare questa funzione molte volte, fino a quando il numero di entità restituite è inferiore al numero richiesto.</span><span class="sxs-lookup"><span data-stu-id="eb157-116">An application might need to call this function many times—until the number of entities returned is less than the number requested.</span></span>

     

4.  <span data-ttu-id="eb157-117">Quando i dati non sono necessari, liberare il puntatore ai dati.</span><span class="sxs-lookup"><span data-stu-id="eb157-117">After the data is not needed, free the pointer to the data.</span></span> <span data-ttu-id="eb157-118">Chiamare una funzione **Freedata** , ad esempio, chiamare [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) o [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span><span class="sxs-lookup"><span data-stu-id="eb157-118">Call a **FreeData** function, for example, call [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata) or [**PeerFreeData**](/windows/desktop/api/P2P/nf-p2p-peerfreedata).</span></span>
    > [!Note]  
    > <span data-ttu-id="eb157-119">Per ulteriori informazioni, vedere [liberazione di dati peer](freeing-peer-data.md).</span><span class="sxs-lookup"><span data-stu-id="eb157-119">For more information, see [Freeing Peer Data](freeing-peer-data.md).</span></span>

     

5.  <span data-ttu-id="eb157-120">Quando l'applicazione non necessita dell'handle per l'enumerazione, rilasciarla.</span><span class="sxs-lookup"><span data-stu-id="eb157-120">After the application does not need the handle to the enumeration, release it.</span></span> <span data-ttu-id="eb157-121">Chiamare una funzione **EndEnumeration** , ad esempio, chiamare [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) o [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span><span class="sxs-lookup"><span data-stu-id="eb157-121">Call an **EndEnumeration** function, for example, call [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration) or [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration).</span></span>

## <a name="example-of-an-enumeration"></a><span data-ttu-id="eb157-122">Esempio di enumerazione</span><span class="sxs-lookup"><span data-stu-id="eb157-122">Example of an Enumeration</span></span>

<span data-ttu-id="eb157-123">Il frammento di codice seguente illustra come eseguire l'enumerazione tramite le identità disponibili.</span><span class="sxs-lookup"><span data-stu-id="eb157-123">The following code snippet shows you how to enumerate through available identities.</span></span>


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



 

 



