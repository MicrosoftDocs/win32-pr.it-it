---
description: Le infrastrutture di peering e di raggruppamento dei peer consentono alle applicazioni di connettersi direttamente a un nodo (Graphing) o membro (raggruppamento), quindi scambiare i dati direttamente con il nodo. Questa connessione viene chiamata connessione diretta.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Connessioni dirette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e357b3a4ebc765a013de05234bc8fc9be20943d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312290"
---
# <a name="direct-connections"></a><span data-ttu-id="e2220-104">Connessioni dirette</span><span class="sxs-lookup"><span data-stu-id="e2220-104">Direct Connections</span></span>

<span data-ttu-id="e2220-105">Le infrastrutture di peering e di raggruppamento dei peer consentono alle applicazioni di connettersi direttamente a un nodo (Graphing) o membro (raggruppamento), quindi scambiare i dati direttamente con il nodo.</span><span class="sxs-lookup"><span data-stu-id="e2220-105">The Peer Graphing and Peer Grouping Infrastructures allow applications to connect directly to one node (Graphing) or member (Grouping), and then exchange data directly with the node.</span></span> <span data-ttu-id="e2220-106">Questa connessione viene chiamata **connessione diretta**.</span><span class="sxs-lookup"><span data-stu-id="e2220-106">This connection is called a **direct connection**.</span></span>

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a><span data-ttu-id="e2220-107">Connessioni dirette tramite l'infrastruttura di Peer Graphing</span><span class="sxs-lookup"><span data-stu-id="e2220-107">Direct Connections using the Peer Graphing Infrastructure</span></span>

<span data-ttu-id="e2220-108">Prima che sia possibile stabilire una connessione diretta tra due nodi in un grafico, è necessario registrare entrambi i nodi per l'evento di **\_ \_ \_ \_ connessione diretta a un evento del grafo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-108">Before a direct connection can be established between two nodes in a graph, both nodes must be registered for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="e2220-109">Per ricevere i dati tramite una connessione diretta, è necessario che i nodi siano registrati anche per l'evento di **\_ \_ \_ \_ dati in ingresso dell'evento del grafo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-109">To receive data over a direct connection, the nodes must also be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="e2220-110">**Peer \_ La \_ \_ \_ connessione diretta agli eventi Graph** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="e2220-110">**PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="e2220-111">Lo stato effettivo di esito positivo o negativo di una chiamata a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) viene restituito nella struttura [**\_ \_ \_ dei dati dell'evento del grafo peer**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .</span><span class="sxs-lookup"><span data-stu-id="e2220-111">The actual success or failure status of a call to [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) is returned in the [**PEER\_GRAPH\_EVENT\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) structure.</span></span>

<span data-ttu-id="e2220-112">Per creare una connessione diretta, un'applicazione chiama [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), quindi passa un handle al grafo, un puntatore all'identità dell'altro nodo che partecipa alla connessione e un puntatore a una struttura di indirizzi IPv6 per il nodo partecipante.</span><span class="sxs-lookup"><span data-stu-id="e2220-112">To create a direct connection, an application calls [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), and then passes a handle to the graph, a pointer to the identity of the other node that is participating in the connection, and a pointer to an IPv6 address structure for the participating node.</span></span> <span data-ttu-id="e2220-113">L'identità del nodo e l'indirizzo IPv6 specificati nella chiamata a **PeerGraphOpenDirectConnection** devono essere registrati per l'evento del **grafo peer per i \_ \_ \_ \_ dati in ingresso** o non possono ricevere dati inviati da un peer chiamante.</span><span class="sxs-lookup"><span data-stu-id="e2220-113">The node identity and IPv6 address that are specified in the call to **PeerGraphOpenDirectConnection** must be registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event, or it cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="e2220-114">In caso di esito positivo, **PeerGraphOpenDirectConnection** restituisce un ID di connessione a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e2220-114">When successful, **PeerGraphOpenDirectConnection** returns a 64-bit connection ID.</span></span> <span data-ttu-id="e2220-115">Tuttavia, il peer deve attendere l'evento **di \_ \_ \_ \_ connessione diretta all'evento del gruppo peer** prima che l'ID connessione diretta possa essere identificato come valido.</span><span class="sxs-lookup"><span data-stu-id="e2220-115">However, the peer must wait for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="e2220-116">Una volta stabilita una connessione e viene confermato un ID connessione valido, un'applicazione può chiamare [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) per inviare i dati attraverso la connessione specificata dall'ID connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **di \_ \_ \_ \_ dati in ingresso dell'evento del grafo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-116">After a connection is made and a valid connection ID is confirmed, an application can call [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) to send the data across the connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="e2220-117">I dati opachi sono disponibili come una struttura di [**\_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) nei [**\_ \_ \_ dati in arrivo**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) dell'evento peer restituiti dall'evento **\_ \_ \_ \_ dati in ingresso evento del grafo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-117">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GRAPH\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="e2220-118">Quando non è necessaria una connessione, un'applicazione chiama [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) con l'handle del grafico e l'ID connessione.</span><span class="sxs-lookup"><span data-stu-id="e2220-118">When a connection is not needed, an application calls [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) with the graph handle and the connection ID.</span></span>

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a><span data-ttu-id="e2220-119">Connessioni dirette tramite l'infrastruttura di raggruppamento dei peer</span><span class="sxs-lookup"><span data-stu-id="e2220-119">Direct Connections using the Peer Grouping Infrastructure</span></span>

<span data-ttu-id="e2220-120">Le connessioni dirette all'interno dell'infrastruttura di raggruppamento peer sono gestite in modo analogo all'infrastruttura di Graphing peer.</span><span class="sxs-lookup"><span data-stu-id="e2220-120">Direct connections within the Peer Grouping Infrastructure are handled similar to the Peer Graphing Infrastructure.</span></span>

<span data-ttu-id="e2220-121">Prima di stabilire una connessione diretta tra due membri di un gruppo, è necessario che entrambi i membri si registrino per l'evento di **\_ \_ \_ \_ connessione diretta all'evento del gruppo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-121">Before a direct connection can be established between two members in a group, both members must register for the **PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** event.</span></span> <span data-ttu-id="e2220-122">Se un membro del gruppo desidera ricevere dati tramite una connessione diretta, è necessario che il membro del gruppo si registri anche per l'evento di **\_ \_ \_ \_ dati in ingresso dell'evento del gruppo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-122">If a group member wants to receive data over a direct connection, the group member must also register for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="e2220-123">**Peer \_ La \_ \_ \_ connessione diretta agli eventi di gruppo** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="e2220-123">**PEER\_GROUP\_EVENT\_DIRECT\_CONNECTION** is an event that is an event that notifies an application whether or not a direct connection attempt succeeds or fails.</span></span> <span data-ttu-id="e2220-124">Lo stato effettivo di esito positivo o negativo di una chiamata a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) viene restituito nella struttura [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .</span><span class="sxs-lookup"><span data-stu-id="e2220-124">The actual success or failure status of a call to [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) is returned in the [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) structure.</span></span>

<span data-ttu-id="e2220-125">Per creare una connessione diretta, un'applicazione chiama [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), quindi passa un handle al gruppo, un puntatore all'identità dell'altro membro che parteciperà alla connessione e un puntatore a una struttura di indirizzi IPv6 per il membro partecipante.</span><span class="sxs-lookup"><span data-stu-id="e2220-125">To create a direct connection, an application calls [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), and then passes a handle to the group, a pointer to the identity of the other member that will participate in this connection, and a pointer to an IPv6 address structure for the participating member.</span></span> <span data-ttu-id="e2220-126">Il membro i cui indirizzi Identity e IPv6 sono specificati nella chiamata a **PeerGroupOpenDirectConnection** deve essere registrato per l'evento di **dati in ingresso dell' \_ evento del gruppo \_ \_ \_ peer** oppure il membro non può ricevere i dati inviati da un peer chiamante.</span><span class="sxs-lookup"><span data-stu-id="e2220-126">The member whose identity and IPv6 address are specified in the call to **PeerGroupOpenDirectConnection** must be registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event, or the member cannot receive data sent by a calling peer.</span></span> <span data-ttu-id="e2220-127">Quando ha esito positivo, **PeerGroupOpenDirectConnection** restituisce un ID connessione a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="e2220-127">**PeerGroupOpenDirectConnection** returns a 64-bit connection ID when successful.</span></span> <span data-ttu-id="e2220-128">Tuttavia, un peer deve attendere la generazione dell'evento di **\_ \_ \_ \_ connessione diretta a un evento del grafico peer** prima che l'ID connessione diretta possa essere identificato come valido.</span><span class="sxs-lookup"><span data-stu-id="e2220-128">However, a peer must wait for the **PEER\_GRAPH\_EVENT\_DIRECT\_CONNECTION** event to be raised before the direct connection ID can be identified as valid.</span></span>

<span data-ttu-id="e2220-129">Una volta stabilita una connessione e viene confermato un ID connessione valido, un'applicazione può chiamare [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) per inviare i dati attraverso una connessione specificata dall'ID connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **di \_ \_ \_ \_ dati in ingresso dell'evento del gruppo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-129">After a connection is made and a valid connection ID is confirmed, then an application can call [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) to send data across a connection specified by the valid connection ID to the participating peer—if the participating peer is registered for the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span> <span data-ttu-id="e2220-130">I dati opachi sono disponibili come una struttura di [**\_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) nei [**\_ \_ \_ dati in arrivo**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) dell'evento peer restituiti dall'evento **\_ \_ \_ \_ dati in ingresso evento del gruppo peer** .</span><span class="sxs-lookup"><span data-stu-id="e2220-130">The opaque data is available as a [**PEER\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) structure in the [**PEER\_EVENT\_INCOMING\_DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) returned by the **PEER\_GROUP\_EVENT\_INCOMING\_DATA** event.</span></span>

<span data-ttu-id="e2220-131">Quando la connessione non è necessaria, l'applicazione chiama [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) con l'handle di gruppo e l'ID connessione.</span><span class="sxs-lookup"><span data-stu-id="e2220-131">When the connection is not needed, the application calls [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) with the group handle and the connection ID.</span></span>

## <a name="example-of-a-direct-connection-for-graphing"></a><span data-ttu-id="e2220-132">Esempio di connessione diretta per la rappresentazione grafica</span><span class="sxs-lookup"><span data-stu-id="e2220-132">Example of a Direct Connection for Graphing</span></span>


```C++
#include <p2p.h>

#pragma comment(lib, "p2pgraph.lib")

//-----------------------------------------------------------------------------
// Function: CreateDirectConnection
//
// Purpose:  Demonstrate how to create a direct connection.
//
// Arguments:
//           hGraph - the graph in which to create the connection
//           pwzId  - the peer identification string
//
// Returns:  ULONGLONG - the connection id or 0
//

ULONGLONG CreateDirectConnection(HGRAPH hGraph, PCWSTR pwzId)
{
    HRESULT   hr = S_OK;

    ULONGLONG ullConnection = 0; // the connection id to return

    HPEERENUM hPeerEnum = NULL;
 
    hr = PeerGraphEnumNodes(hGraph, pwzId, &hPeerEnum);

    if (SUCCEEDED(hr))
    {
        ULONG cItem = 1; // want only one matching result

        PEER_NODE_INFO ** ppNodeInfo = NULL;

        hr = PeerGraphGetNextItem(hPeerEnum, &cItem, (PVOID**) &ppNodeInfo);

        if (SUCCEEDED(hr))
        {
            if ((cItem > 0) && (NULL != ppNodeInfo))
            {
                if ((*ppNodeInfo)->cAddresses > 0)
                {
                    hr = PeerGraphOpenDirectConnection(hGraph, pwzId,
                            &(*ppNodeInfo)->pAddresses[0], &ullConnection);
                }
                PeerGraphFreeData(ppNodeInfo);
            }
        }
        PeerGraphEndEnumeration(hPeerEnum);
    }
    return ullConnection;
}

```



 

 



