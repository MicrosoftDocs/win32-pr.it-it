---
description: Le infrastrutture peer graphing e di raggruppamento peer consentono alle applicazioni di connettersi direttamente a un nodo (Grafi) o a un membro (raggruppamento) e quindi scambiare i dati direttamente con il nodo. Questa connessione è detta connessione diretta.
ms.assetid: 65f3d3a5-c015-4724-b9ed-45af7fde7a45
title: Connessioni dirette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f06fde65cf7597ccbec7f2968dbbf7662b4a6491ae59e6aa66b8baa587dc1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011629"
---
# <a name="direct-connections"></a>Connessioni dirette

Le infrastrutture peer graphing e di raggruppamento peer consentono alle applicazioni di connettersi direttamente a un nodo (Grafi) o a un membro (raggruppamento) e quindi scambiare i dati direttamente con il nodo. Questa connessione è detta **connessione diretta**.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Connessioni dirette tramite l'infrastruttura peer graphing

Prima di stabilire una connessione diretta tra due nodi in un grafo, entrambi i nodi devono essere registrati per l'evento **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION.** Per ricevere dati tramite una connessione diretta, i nodi devono essere registrati anche per **l'evento PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA.**

**PEER \_ GRAPH \_ EVENT \_ DIRECT \_ CONNECTION** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo. Lo stato di esito positivo o negativo effettivo di una chiamata a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) viene restituito nella struttura [**PEER GRAPH EVENT \_ \_ \_ DATA.**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data)

Per creare una connessione diretta, un'applicazione chiama [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)e quindi passa un handle al grafo, un puntatore all'identità dell'altro nodo che partecipa alla connessione e un puntatore a una struttura di indirizzi IPv6 per il nodo partecipante. L'identità del nodo e l'indirizzo IPv6 specificati nella chiamata a **PeerGraphOpenDirectConnection** devono essere registrati per l'evento **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA** oppure non possono ricevere dati inviati da un peer chiamante. In caso di esito **positivo, PeerGraphOpenDirectConnection** restituisce un ID di connessione a 64 bit. Tuttavia, il peer deve attendere l'evento **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION** prima che l'ID connessione diretta possa essere identificato come valido.

Dopo aver effettuato una connessione e confermato un ID di connessione valido, un'applicazione può chiamare [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) per inviare i dati attraverso la connessione specificata dall'ID di connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA.** I dati opachi sono disponibili come struttura [**PEER \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) nell'evento [**PEER EVENT INCOMING \_ \_ \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) restituito dall'evento **PEER GRAPH EVENT INCOMING \_ \_ \_ \_ DATA.**

Quando non è necessaria una connessione, un'applicazione chiama [**PeerGraphCloseDirectConnection con**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) l'handle del grafo e l'ID connessione.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Connessioni dirette tramite l'infrastruttura di raggruppamento peer

Le connessioni dirette all'interno dell'infrastruttura di raggruppamento peer vengono gestite in modo simile all'infrastruttura peer graphing.

Prima di stabilire una connessione diretta tra due membri di un gruppo, entrambi i membri devono registrarsi per l'evento **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION.** Se un membro del gruppo vuole ricevere dati tramite una connessione diretta, il membro del gruppo deve anche registrarsi per l'evento **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA.**

**PEER \_ GROUP \_ EVENT \_ DIRECT \_ CONNECTION** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo. Lo stato effettivo di esito positivo o negativo di una chiamata a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) viene restituito nella [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) struttura.

Per creare una connessione diretta, un'applicazione chiama [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection)e quindi passa un handle al gruppo, un puntatore all'identità dell'altro membro che parteciperà a questa connessione e un puntatore a una struttura di indirizzi IPv6 per il membro partecipante. Il membro la cui identità e l'indirizzo IPv6 sono specificati nella chiamata a **PeerGroupOpenDirectConnection** devono essere registrati per l'evento **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA** oppure il membro non può ricevere dati inviati da un peer chiamante. **PeerGroupOpenDirectConnection** restituisce un ID di connessione a 64 bit in caso di esito positivo. Tuttavia, un peer deve attendere la generazione dell'evento **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION** prima che l'ID di connessione diretta possa essere identificato come valido.

Dopo aver effettuato una connessione e confermato un ID di connessione valido, un'applicazione può chiamare [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) per inviare dati attraverso una connessione specificata dall'ID di connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA.** I dati opachi sono disponibili come struttura [**PEER \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_data) nell'evento [**PEER EVENT INCOMING \_ \_ \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) restituito dall'evento **PEER GROUP EVENT INCOMING \_ \_ \_ \_ DATA.**

Quando la connessione non è necessaria, l'applicazione chiama [**PeerGroupCloseDirectConnection con**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) l'handle del gruppo e l'ID connessione.

## <a name="example-of-a-direct-connection-for-graphing"></a>Esempio di connessione diretta per la grafi


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



 

 



