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
# <a name="direct-connections"></a>Connessioni dirette

Le infrastrutture di peering e di raggruppamento dei peer consentono alle applicazioni di connettersi direttamente a un nodo (Graphing) o membro (raggruppamento), quindi scambiare i dati direttamente con il nodo. Questa connessione viene chiamata **connessione diretta**.

## <a name="direct-connections-using-the-peer-graphing-infrastructure"></a>Connessioni dirette tramite l'infrastruttura di Peer Graphing

Prima che sia possibile stabilire una connessione diretta tra due nodi in un grafico, è necessario registrare entrambi i nodi per l'evento di **\_ \_ \_ \_ connessione diretta a un evento del grafo peer** . Per ricevere i dati tramite una connessione diretta, è necessario che i nodi siano registrati anche per l'evento di **\_ \_ \_ \_ dati in ingresso dell'evento del grafo peer** .

**Peer \_ La \_ \_ \_ connessione diretta agli eventi Graph** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo. Lo stato effettivo di esito positivo o negativo di una chiamata a [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection) viene restituito nella struttura [**\_ \_ \_ dei dati dell'evento del grafo peer**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) .

Per creare una connessione diretta, un'applicazione chiama [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection), quindi passa un handle al grafo, un puntatore all'identità dell'altro nodo che partecipa alla connessione e un puntatore a una struttura di indirizzi IPv6 per il nodo partecipante. L'identità del nodo e l'indirizzo IPv6 specificati nella chiamata a **PeerGraphOpenDirectConnection** devono essere registrati per l'evento del **grafo peer per i \_ \_ \_ \_ dati in ingresso** o non possono ricevere dati inviati da un peer chiamante. In caso di esito positivo, **PeerGraphOpenDirectConnection** restituisce un ID di connessione a 64 bit. Tuttavia, il peer deve attendere l'evento **di \_ \_ \_ \_ connessione diretta all'evento del gruppo peer** prima che l'ID connessione diretta possa essere identificato come valido.

Una volta stabilita una connessione e viene confermato un ID connessione valido, un'applicazione può chiamare [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata) per inviare i dati attraverso la connessione specificata dall'ID connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **di \_ \_ \_ \_ dati in ingresso dell'evento del grafo peer** . I dati opachi sono disponibili come una struttura di [**\_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) nei [**\_ \_ \_ dati in arrivo**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) dell'evento peer restituiti dall'evento **\_ \_ \_ \_ dati in ingresso evento del grafo peer** .

Quando non è necessaria una connessione, un'applicazione chiama [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) con l'handle del grafico e l'ID connessione.

## <a name="direct-connections-using-the-peer-grouping-infrastructure"></a>Connessioni dirette tramite l'infrastruttura di raggruppamento dei peer

Le connessioni dirette all'interno dell'infrastruttura di raggruppamento peer sono gestite in modo analogo all'infrastruttura di Graphing peer.

Prima di stabilire una connessione diretta tra due membri di un gruppo, è necessario che entrambi i membri si registrino per l'evento di **\_ \_ \_ \_ connessione diretta all'evento del gruppo peer** . Se un membro del gruppo desidera ricevere dati tramite una connessione diretta, è necessario che il membro del gruppo si registri anche per l'evento di **\_ \_ \_ \_ dati in ingresso dell'evento del gruppo peer** .

**Peer \_ La \_ \_ \_ connessione diretta agli eventi di gruppo** è un evento che notifica a un'applicazione se un tentativo di connessione diretta ha esito positivo o negativo. Lo stato effettivo di esito positivo o negativo di una chiamata a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) viene restituito nella struttura [**PEER_GROUP_EVENT_DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) .

Per creare una connessione diretta, un'applicazione chiama [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), quindi passa un handle al gruppo, un puntatore all'identità dell'altro membro che parteciperà alla connessione e un puntatore a una struttura di indirizzi IPv6 per il membro partecipante. Il membro i cui indirizzi Identity e IPv6 sono specificati nella chiamata a **PeerGroupOpenDirectConnection** deve essere registrato per l'evento di **dati in ingresso dell' \_ evento del gruppo \_ \_ \_ peer** oppure il membro non può ricevere i dati inviati da un peer chiamante. Quando ha esito positivo, **PeerGroupOpenDirectConnection** restituisce un ID connessione a 64 bit. Tuttavia, un peer deve attendere la generazione dell'evento di **\_ \_ \_ \_ connessione diretta a un evento del grafico peer** prima che l'ID connessione diretta possa essere identificato come valido.

Una volta stabilita una connessione e viene confermato un ID connessione valido, un'applicazione può chiamare [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) per inviare i dati attraverso una connessione specificata dall'ID connessione valido al peer partecipante, se il peer partecipante è registrato per l'evento **di \_ \_ \_ \_ dati in ingresso dell'evento del gruppo peer** . I dati opachi sono disponibili come una struttura di [**\_ dati peer**](/windows/desktop/api/P2P/ns-p2p-peer_data) nei [**\_ \_ \_ dati in arrivo**](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data) dell'evento peer restituiti dall'evento **\_ \_ \_ \_ dati in ingresso evento del gruppo peer** .

Quando la connessione non è necessaria, l'applicazione chiama [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) con l'handle di gruppo e l'ID connessione.

## <a name="example-of-a-direct-connection-for-graphing"></a>Esempio di connessione diretta per la rappresentazione grafica


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



 

 



