---
description: L'infrastruttura peer usa gli eventi per notificare alle applicazioni le modifiche che si sono verificate all'interno di una rete peer, ad esempio un nodo aggiunto o rimosso da un grafo.
ms.assetid: a056da1c-b8f9-4dad-8df9-df24c6b359b7
title: Infrastruttura di eventi peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a889f59e4429e64258c047dfbf0249bb4dca125bfc3f9d659e6042dd40be9443
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775951"
---
# <a name="peer-events-infrastructure"></a>Infrastruttura di eventi peer

L'infrastruttura peer usa gli eventi per notificare alle applicazioni le modifiche che si sono verificate all'interno di una rete peer, ad esempio un nodo aggiunto o rimosso da un grafo. Le infrastrutture peer graphing e di raggruppamento peer usano l'infrastruttura di eventi peer.

## <a name="receiving-peer-event-notification"></a>Ricezione della notifica degli eventi peer

Un peer può registrarsi per ricevere una notifica quando viene modificato un attributo di un grafo o gruppo o si verifica un evento peer specifico. Un'applicazione peer chiama la funzione [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) o [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) e passa un handle di evento all'infrastruttura peer, creata in precedenza da una chiamata a [**CreateEvent.**](graphing-reference-links.md) L'infrastruttura peer usa l'handle per segnalare a un'applicazione che si è verificato un evento peer.

L'applicazione passa anche una serie di strutture [**PEER \_ GRAPH EVENT \_ \_ REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_registration) o [**PEER GROUP EVENT \_ \_ \_ REGISTRATION**](/windows/desktop/api/P2P/ns-p2p-peer_group_event_registration) che indicano all'infrastruttura peer gli eventi peer specifici per cui l'applicazione richiede la notifica. L'applicazione deve anche specificare esattamente il numero di strutture passate.

## <a name="peer-graphing-events"></a>Eventi di grafi peer

Un'applicazione peer graphing può registrarsi per ricevere notifiche per 9 eventi del grafo peer. Ogni nome di evento è preceduto da **PEER \_ GRAPH \_ \_ EVENT,** ad esempio PEER GRAPH STATUS **\_ \_ \_ CHANGED**. Se non specificato diversamente, le informazioni su una modifica vengono recuperate tramite [**PeerGraphGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)

-   **PEER \_ GRAPH \_ EVENT STATUS CHANGED \_ \_ (STATO** EVENTO GRAFO MODIFICATO) indica che lo stato di un grafo è stato modificato, ad esempio un nodo è stato sincronizzato con un grafo.
-   **PEER \_ GRAPH \_ EVENT \_ PROPERTY \_ CHANGED** indica che una proprietà di un grafo o gruppo è stata modificata, ad esempio il nome descrittivo di un grafo è stato modificato.
    > [!Note]  
    > L'applicazione deve [**chiamare PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties) per ottenere le informazioni modificate.

     

-   **PEER \_ GRAPH \_ EVENT \_ RECORD \_ CHANGED** indica che un record è stato modificato, ad esempio un record viene eliminato.
-   **PEER \_ GRAPH \_ EVENT \_ DIRECT \_ CONNECTION** indica che è stata modificata una connessione diretta, ad esempio se un nodo è connesso.
-   **PEER \_ GRAPH \_ EVENT \_ NEIGHBOR \_ CONNECTION** indica che è stata modificata una connessione a un nodo adiacente, ad esempio un nodo connesso.
-   **PEER \_ GRAPH \_ EVENT \_ INCOMING \_ DATA** indica che i dati sono stati ricevuti da una connessione diretta o adiacente.
-   **PEER \_ GRAPH \_ EVENT \_ CONNECTION \_ REQUIRED** indica che Graphing Infrastructure richiede una nuova connessione.
    > [!Note]  
    > Una chiamata a [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) si connette a un nuovo nodo. Una chiamata a [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata) non restituisce dati.

     

-   **PEER \_ GRAPH \_ EVENT NODE CHANGED \_ \_ indica** che le informazioni sulla presenza del nodo sono state modificate, ad esempio un indirizzo IP è stato modificato.
-   **PEER \_ GRAPH \_ EVENT \_ SYNCHRONIZED** indica che un tipo di record specifico è sincronizzato.

Dopo che un'applicazione riceve la notifica che si è verificato un evento peer, chiama [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)e passa l'handle dell'evento peer restituito da [**PeerGraphRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) L'infrastruttura peer restituisce un puntatore a una [**struttura PEER GRAPH EVENT \_ \_ \_ DATA**](/windows/desktop/api/P2P/ns-p2p-peer_graph_event_data) che contiene i dati richiesti. Questa funzione deve essere chiamata fino a **quando non \_ viene restituito PEER S NO \_ EVENT \_ \_ DATA.**

Quando un'applicazione non richiede una notifica degli eventi peer, chiama [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent)e passa l'handle dell'evento peer restituito da [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent) quando l'applicazione è registrata.

## <a name="handling-graph-connection-referrals"></a>Gestione delle Graph di connessione

Quando [**viene chiamato PeerGraphConnect,**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) il peer di connessione viene informato dell'esito positivo o negativo tramite l'evento **ASINCRONO PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION.** Se la connessione non è riuscita a causa di problemi di rete specifici (ad esempio un firewall non configurato correttamente), viene generato l'evento **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION,** con lo stato della connessione impostato su **PEER CONNECTION \_ \_ FAILED**.

Tuttavia, quando un peer riceve una segnalazione quando tenta di connettersi a un nodo occupato, viene generata la connessione **PEER GRAPH EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION** sul peer di connessione, con lo stato di connessione impostato su **PEER CONNECTION \_ \_ FAILED.** Il peer che si connette può fare riferimento a un altro nodo che è occupato e può inviare una segnalazione e lo stesso evento e lo stesso stato vengono generati sul peer di connessione. Questa catena di segnalazioni che comportano lo stato **dell'evento PEER \_ CONNECTION \_ FAILED** può continuare fino all'esaurimento del numero massimo di tentativi di connessione. Il peer non dispone di un meccanismo per determinare la differenza tra un tentativo di connessione completo e la segnalazione della connessione.

Per risolvere questo problema, gli sviluppatori devono prendere in considerazione l'uso degli eventi di modifica dello stato del grafo peer per determinare se il tentativo di connessione è stato eseguito. Se l'evento non viene ricevuto entro un periodo di tempo specifico, l'applicazione può presupporre che venga fatto riferimento al peer di connessione e che l'applicazione peer consideri il tentativo di connessione come errore.

## <a name="peer-grouping-events"></a>Eventi di raggruppamento peer

Un'applicazione di raggruppamento peer può registrarsi per ricevere notifiche per 8 eventi peer. Ogni nome di evento è preceduto da **PEER \_ GROUP \_ EVENT, \_** ad esempio PEER GROUP EVENT STATUS **\_ \_ \_ \_ CHANGED**. Se non specificato diversamente, le informazioni su una modifica vengono recuperate tramite [**PeerGroupGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)

-   **PEER \_ GROUP \_ EVENT \_ STATUS \_ CHANGED** indica che lo stato del gruppo è stato modificato. Sono possibili due valori di stato: **PEER \_ GROUP STATUS \_ \_ LISTENING,** che indica che il gruppo non ha connessioni ed è in attesa di nuovi membri, e **PEER GROUP STATUS HAS \_ \_ \_ CONNECTIONS,** che indica che il gruppo ha almeno una connessione. Questo valore di stato può essere ottenuto chiamando [**PeerGroupGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergroupgetstatus) dopo la generazione di questo evento.
-   **PEER \_ GROUP \_ EVENT \_ PROPERTY \_ CHANGED** indica che le proprietà del gruppo sono state modificate o aggiornate dall'autore del gruppo.
-   **PEER \_ GROUP \_ EVENT \_ RECORD \_ CHANGED** indica che è stata eseguita un'operazione di record. Questo evento viene generato quando un peer che partecipa al gruppo pubblica, aggiorna o elimina un record. Ad esempio, questo evento viene generato quando un'applicazione di chat invia un messaggio di chat.
-   **PEER \_ GROUP \_ EVENT \_ MEMBER \_ CHANGED** indica che lo stato di un membro all'interno del gruppo è stato modificato. Le modifiche dello stato includono:
    -   **PEER \_ MEMBRO \_ CONNESSO.** Un peer si è connesso al gruppo.
    -   **PEER \_ MEMBRO \_ DISCONNESSO.** Un peer si è disconnesso dal gruppo.
    -   **PEER \_ MEMBRO \_ AGGIUNTO** A . Sono state pubblicate nuove informazioni di appartenenza per un peer.
    -   **PEER \_ MEMBRO \_ AGGIORNATO.** Un peer è stato aggiornato con nuove informazioni, ad esempio un nuovo indirizzo IP.
-   **PEER \_ GROUP \_ EVENT \_ NEIGHBOR \_ CONNECTION**. I peer che parteciperanno alle connessioni adiacenti all'interno del gruppo devono registrarsi per questo evento. Si noti che la registrazione per questo evento non consente al peer di ricevere dati. La registrazione per questo evento garantisce la notifica solo quando viene ricevuta una richiesta per una connessione adiacente.
-   **PEER \_ GROUP \_ EVENT \_ DIRECT \_ CONNECTION**. I peer che parteciperanno alle connessioni dirette all'interno del gruppo devono registrarsi per questo evento. Si noti che la registrazione per questo evento non consente al peer di ricevere dati. La registrazione per questo evento garantisce la notifica solo quando viene ricevuta una richiesta per una connessione diretta.
-   **PEER \_ RAGGRUPPARE \_ I DATI IN INGRESSO DEGLI \_ \_ EVENTI**. I peer che riceveranno i dati tramite una connessione adiacente o diretta devono registrarsi per questo evento. Quando viene generato questo evento, i dati opachi trasmessi dall'altro peer partecipante possono essere ottenuti chiamando [**PeerGroupGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) Si noti che per ricevere questo evento, il peer deve essere stato registrato in precedenza per **PEER GROUP EVENT DIRECT \_ \_ \_ \_ CONNECTION** o **PEER GROUP EVENT NEIGHBOR \_ \_ \_ \_ CONNECTION**.
-   **PEER \_ GROUP \_ EVENT \_ CONNECTION \_ FAILED**. Una connessione non è riuscita per qualche motivo. Non vengono forniti dati quando viene generato questo evento e [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) non deve essere chiamato.

Dopo che un'applicazione riceve la notifica che si è verificato un evento peer (escluso **PEER GROUP EVENT CONNECTION \_ \_ \_ \_ FAILED),** l'applicazione chiama [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata)e passa l'handle di evento peer restituito da [**PeerGroupRegisterEvent.**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent) L'infrastruttura peer restituisce un puntatore a una [**struttura PEER GROUP EVENT \_ \_ \_ DATA**](/windows/win32/api/p2p/ns-p2p-peer_group_event_data-r1) che contiene i dati richiesti. Questa funzione deve essere chiamata fino a **quando non \_ viene restituito PEER S \_ NO \_ EVENT \_** DATA. Quando un'applicazione non richiede più la notifica per un evento peer, è necessario eseguire una chiamata a [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent), passando l'handle di evento peer restituito da **PeerGroupRegisterEvent** quando l'applicazione è registrata per l'evento specifico.

## <a name="example-of-registering-for-peer-graphing-events"></a>Esempio di registrazione per gli eventi di peer graphing

L'esempio di codice seguente illustra come eseguire la registrazione con gli eventi peer graphing.


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



 

 



