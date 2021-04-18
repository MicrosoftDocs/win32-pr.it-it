---
description: L'infrastruttura peer utilizza gli eventi per notificare alle applicazioni le modifiche apportate all'interno di una rete peer, ad esempio un nodo che viene aggiunto o rimosso da un grafo.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infrastruttura di eventi peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6347ad6a7dd0cf2fae4a0aa623bfda48ab0aa9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312244"
---
# <a name="peer-events-infrastructure"></a>Infrastruttura di eventi peer

L'infrastruttura peer utilizza gli eventi per notificare alle applicazioni le modifiche apportate all'interno di una rete peer, ad esempio un nodo che viene aggiunto o rimosso da un grafo. Le infrastrutture di peering e di raggruppamento dei peer utilizzano l'infrastruttura degli eventi peer.

## <a name="receiving-peer-event-notification"></a>Ricezione della notifica degli eventi peer

Un peer può registrarsi per ricevere una notifica quando viene modificato un attributo di un grafico o di un gruppo oppure si verifica un evento peer specifico. Un'applicazione peer chiama la funzione [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) o [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) e passa un handle di evento all'infrastruttura peer, creata in precedenza da una chiamata a [**CreateEvent**](graphing-reference-links.md). L'infrastruttura peer utilizza l'handle per segnalare a un'applicazione che si è verificato un evento peer.

L'applicazione passa inoltre una serie di strutture di registrazione eventi del [**\_ grafo \_ \_ peer**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) o di un [**\_ gruppo peer \_ \_**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) che indicano all'infrastruttura peer gli eventi peer specifici per cui l'applicazione richiede la notifica. L'applicazione deve inoltre specificare esattamente il numero di strutture da passare.

## <a name="peer-graphing-events"></a>Eventi di grafica peer

Un'applicazione di Graphing peer può eseguire la registrazione per ricevere la notifica per 9 eventi del grafo peer. Ogni nome di evento è preceduto da **un \_ \_ evento \_ del grafo del peer**, ad esempio **lo stato del grafo del peer è \_ \_ stato \_ modificato**. Se non specificato diversamente, le informazioni su una modifica vengono recuperate tramite [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata).

-   **Peer \_ \_Lo stato dell'evento Graph \_ \_ modificato** indica che lo stato di un grafico è stato modificato, ad esempio un nodo è stato sincronizzato con un grafo.
-   **Peer \_ La \_ Proprietà evento Graph \_ \_ modificata** indica che una proprietà di un grafico o un gruppo è stata modificata, ad esempio, il nome descrittivo di un grafico è stato modificato.
    > [!Note]  
    > Per ottenere le informazioni modificate, l'applicazione deve chiamare [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) .

     

-   **Peer \_ Il \_ record dell'evento Graph \_ \_ modificato** indica che un record è stato modificato. ad esempio, un record viene eliminato.
-   **Peer \_ La \_ \_ \_ connessione diretta agli eventi Graph** indica che è stata modificata una connessione diretta, ad esempio un nodo è connesso.
-   **Peer \_ La \_ \_ \_ connessione adiacente a un evento Graph** indica che è stata modificata una connessione a un nodo adiacente, ad esempio un nodo è connesso.
-   **Peer \_ \_ \_ \_ I dati in ingresso dell'evento Graph** indicano che i dati sono stati ricevuti da una connessione diretta o vicina.
-   **Peer \_ \_Connessione evento \_ grafico \_ richiesta** indica che l'infrastruttura di Graphing richiede una nuova connessione.
    > [!Note]  
    > Una chiamata a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) si connette a un nuovo nodo. Una chiamata a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) non restituisce dati.

     

-   **Peer \_ Il \_ nodo evento Graph \_ \_ modificato** indica che le informazioni sulla presenza del nodo sono state modificate, ad esempio un indirizzo IP è stato modificato.
-   **Peer \_ \_Evento grafico \_ sincronizzato** indica che un tipo di record specifico è sincronizzato.

Dopo che un'applicazione riceve la notifica che si è verificato un evento peer, l'applicazione chiama [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)e passa l'handle di evento peer restituito da [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent). L'infrastruttura peer restituisce un puntatore a una struttura di [**\_ dati dell' \_ evento \_ del grafo peer**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) che contiene i dati richiesti. Questa funzione deve essere chiamata fino a quando non viene restituito **\_ \_ alcun \_ \_ dato di evento peer S** .

Quando un'applicazione non richiede una notifica degli eventi peer, l'applicazione chiama [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)e passa l'handle di evento peer restituito da [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) quando l'applicazione è registrata.

## <a name="handling-graph-connection-referrals"></a>Gestione dei riferimenti di connessione al grafo

Quando viene chiamato [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) , il peer connesso riceve una notifica di esito positivo o negativo tramite l'evento di **\_ \_ \_ \_ connessione adiacente all'evento del grafo peer** asincrono. Se la connessione non è riuscita a causa di problemi di rete specifici, ad esempio un firewall configurato in modo errato, viene generato l'evento di **\_ \_ \_ \_ connessione adiacente all'evento del grafo del peer** , con lo stato della connessione impostato su **\_ connessione peer \_ non riuscita**.

Tuttavia, quando un peer riceve un riferimento quando tenta di connettersi a un nodo occupato, viene generata **la \_ \_ \_ \_ connessione adiacente all'evento del grafo del peer** sul peer connesso, con lo stato della connessione impostato su **\_ connessione peer \_ non riuscito**. Il peer di connessione può essere fatto riferimento a un altro nodo che a sua volta è occupato e può inviare un riferimento e lo stesso evento e lo stesso stato vengono generati sul peer di connessione. Questa catena di riferimenti che generano stato degli eventi di **\_ connessione peer \_ non riuscita** può continuare fino a quando non viene esaurito il numero massimo di tentativi di connessione. Il peer non dispone di un meccanismo per determinare la differenza tra un tentativo di connessione completo e il riferimento alla connessione.

Per risolvere questo problema, gli sviluppatori devono considerare l'utilizzo degli eventi di modifica dello stato del grafo peer per determinare se il tentativo di connessione riuscito. Se l'evento non viene ricevuto entro un periodo di tempo specifico, l'applicazione può presupporre che il peer di connessione venga sottoposta a riferimento e che l'applicazione peer debba prendere in considerazione il tentativo di connessione a un errore.

## <a name="peer-grouping-events"></a>Eventi di raggruppamento peer

Un'applicazione di raggruppamento peer può registrarsi per ricevere notifiche per 8 eventi peer. Ogni nome di evento è preceduto da **un \_ \_ \_ evento di gruppo peer**. ad esempio, **lo stato dell'evento del gruppo peer è \_ \_ \_ stato \_ modificato**. Se non specificato diversamente, le informazioni su una modifica vengono recuperate tramite [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata).

-   **Peer \_ \_Stato evento \_ gruppo \_ modificato** indica che lo stato del gruppo è stato modificato. Esistono due valori di stato possibili: **stato del gruppo peer in \_ \_ \_ ascolto**, che indica che il gruppo non dispone di connessioni ed è in attesa di nuovi membri e **\_ lo stato del gruppo peer \_ dispone di \_ connessioni**, che indica che il gruppo dispone di almeno una connessione. Questo valore di stato può essere ottenuto chiamando [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) dopo la generazione di questo evento.
-   **Peer \_ \_Proprietà evento \_ gruppo \_ modificata** indica che le proprietà del gruppo sono state modificate o aggiornate dall'autore del gruppo.
-   **Peer \_ Il record degli eventi di gruppo è stato \_ \_ \_ modificato** indica che è stata eseguita un'operazione di record. Questo evento viene generato quando un peer che partecipa al gruppo pubblica, aggiorna o Elimina un record. Questo evento, ad esempio, viene generato quando un'applicazione di chat invia un messaggio di chat.
-   **Peer \_ Il \_ membro evento gruppo \_ \_ modificato** indica che lo stato di un membro all'interno del gruppo è stato modificato. Le modifiche dello stato includono:
    -   **Peer \_ MEMBRO \_ connesso**. Un peer si è connesso al gruppo.
    -   **Peer \_ MEMBRO \_ disconnesso**. Un peer è stato disconnesso dal gruppo.
    -   **Peer \_ MEMBRO \_ aggiunto**. Sono state pubblicate nuove informazioni di appartenenza per un peer.
    -   **Peer \_ MEMBRO \_ aggiornato**. Un peer è stato aggiornato con nuove informazioni, ad esempio un nuovo indirizzo IP.
-   **Peer \_ \_ \_ \_ connessione adiacente all'evento di gruppo**. I peer che parteciperanno alle connessioni adiacenti all'interno del gruppo devono registrarsi per questo evento. Si noti che la registrazione per questo evento non consente al peer di ricevere dati. la registrazione per questo evento garantisce la notifica solo quando viene ricevuta una richiesta di connessione vicina.
-   **Peer \_ \_ \_ \_ connessione diretta agli eventi di gruppo**. I peer che parteciperanno alle connessioni dirette all'interno del gruppo devono registrarsi per questo evento. Si noti che la registrazione per questo evento non consente al peer di ricevere dati. la registrazione per questo evento garantisce la notifica solo quando viene ricevuta una richiesta di connessione diretta.
-   **Peer \_ RAGGRUPPAre \_ \_ \_ i dati in ingresso dell'evento**. Per questo evento, i peer che riceveranno dati tramite un router adiacente o una connessione diretta devono registrarsi. Quando viene generato questo evento, i dati opachi trasmessi dall'altro peer partecipante possono essere ottenuti chiamando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Si noti che per ricevere questo evento, è necessario che il peer sia stato registrato in precedenza per la connessione **\_ \_ \_ diretta \_ eventi del gruppo peer** o per l' **\_ evento del gruppo \_ \_ \_ peer**.
-   **Peer \_ \_connessione evento \_ gruppo \_ non riuscita**. Connessione non riuscita per qualche motivo. Non vengono forniti dati quando viene generato questo evento e [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) non deve essere chiamato.

Dopo che un'applicazione riceve la notifica che si è verificato un evento peer (esclusa la **\_ connessione all'evento del gruppo peer \_ \_ \_ non riuscita**), l'applicazione chiama [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)e passa l'handle dell'evento peer restituito da [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). L'infrastruttura peer restituisce un puntatore a una struttura di [**\_ dati degli \_ eventi \_ del gruppo peer**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) che contiene i dati richiesti. Questa funzione deve essere chiamata fino a quando non viene restituito **\_ \_ alcun \_ \_ dato di evento peer S** . Quando un'applicazione non richiede più la notifica per un evento peer, è necessario effettuare una chiamata a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), passando l'handle di evento peer restituito da **PeerGroupRegisterEvent** quando l'applicazione è registrata per l'evento specifico.

## <a name="example-of-registering-for-peer-graphing-events"></a>Esempio di registrazione per gli eventi di Graphing peer

Nell'esempio di codice riportato di seguito viene illustrato come eseguire la registrazione con gli eventi di grafica peer.


```C++
//-----------------------------------------------------------------------------
// Function: RegisterForEvents
//
// Purpose:  Registers the EventCallback function so it can be called for only
//           the events that are specified.
//
// Returns:  HRESULT
//
HRESULT RegisterForEvents()
{
    HPEEREVENT  g_hPeerEvent = NULL;        // The one PeerEvent handle
    HANDLE      g_hEvent = NULL;            // Handle signaled by Graphing when we have an event
    HRESULT hr = S_OK;
    PEER_GRAPH_EVENT_REGISTRATION regs[] = {
        { PEER_GRAPH_EVENT_RECORD_CHANGED, 0 },
        { PEER_GRAPH_EVENT_NODE_CHANGED,   0 },
        { PEER_GRAPH_EVENT_STATUS_CHANGED, 0 },
        { PEER_GRAPH_EVENT_DIRECT_CONNECTION, 0 },
        { PEER_GRAPH_EVENT_INCOMING_DATA, 0 },
    };

    g_hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
    if (g_hEvent == NULL)
    {
        wprintf(L"CreateEvent call failed.\n");
        hr = E_OUTOFMEMORY;
    }
    else
    {
        hr = PeerGraphRegisterEvent(g_hGraph, g_hEvent, celems(regs), regs,  &g_hPeerEvent);
        if (FAILED(hr))
        {
           wprintf(L"PeerGraphRegisterEvent call failed.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    if (SUCCEEDED(hr))
    {
        if (!RegisterWaitForSingleObject(&g_hWait, g_hEvent, EventCallback, NULL, INFINITE, WT_EXECUTEDEFAULT))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            wprintf(L"Could not set up event callback.\n");
            CloseHandle(g_hEvent);
            g_hEvent = NULL;
        }
    }

    return hr;
}
```



 

 



