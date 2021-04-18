---
description: Quando si utilizzano i grafici peer, è necessario chiamare le funzioni in un ordine specifico. Il flusso di chiamate varia a seconda che si stia creando o aprendo un grafo peer. In questo argomento viene identificato il flusso di chiamate di funzione in una semplice applicazione di peer Graph.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Utilizzo dei grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4328b7a0109139421cf03c72a7228a3dc17e375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312199"
---
# <a name="working-with-graphs"></a>Utilizzo dei grafici

Quando si utilizzano i grafici peer, è necessario chiamare le funzioni in un ordine specifico. Il flusso di chiamate varia a seconda che si stia creando o aprendo un grafo peer. In questo argomento viene identificato il flusso di chiamate di funzione in una semplice applicazione di peer Graph.

## <a name="starting-up-a-graph"></a>Avvio di un grafico

Prima che un'applicazione chiami una funzione nell'API Graphing peer, è necessario chiamare [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) per inizializzare l'API per la rappresentazione grafica dei peer per un'applicazione, quindi impostare la versione supportata.

## <a name="creating-a-peer-graph"></a>Creazione di un grafico peer

La procedura seguente identifica il flusso di chiamate per la creazione di un grafico peer.

> [!IMPORTANT]
> Solo un peer deve chiamare [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate). Tutti gli altri peer devono chiamare [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). Più chiamate a **PeerGraphCreate** invalidano un grafo.

 

-   Creare un grafico peer. Chiamare [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).
-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione per gli eventi peer, vedere [infrastruttura degli eventi](peer-events-infrastructure.md).

     

-   Ascolto delle connessioni a un grafo peer. Chiamare [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).
-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare gli eventi del peer e utilizzare le connessioni.
-   Chiude la connessione a un grafico peer. Chiamare [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="opening-a-peer-graph"></a>Apertura di un grafico a più peer

Il flusso di chiamate di funzione per aprire un grafico peer dipende dal valore restituito della chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen). I valori più importanti sono **s \_ OK** e i **dati di peer \_ s \_ \_ creati**, descritti nelle sezioni seguenti di questo argomento.

> [!Note]  
> Se una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) non restituisce i dati **s \_ OK** o **peer \_ s \_ \_ creati**, gestire l'errore.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Quando PeerGraphOpen restituisce \_ OK

Quando una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce **\_ OK**, è stato aperto un grafico peer e un database esistente. Nella procedura riportata di seguito vengono identificate le operazioni che è possibile eseguire per aprire un grafico peer quando una chiamata a **PeerGraphOpen** restituisce **\_ OK**

-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione degli eventi, vedere [infrastruttura degli eventi](peer-events-infrastructure.md).

     

-   Individuare un nodo. Si tratta di un processo eseguito all'esterno dell'infrastruttura di Peer Graphing, usando un metodo o un'applicazione identificata dall'utente. L'API di Graphing peer non fornisce un meccanismo specifico per trovare un nodo grafico iniziale a cui connettersi. Un'applicazione deve usare un altro meccanismo, ad esempio l'API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , per individuare il nodo iniziale.
-   Se viene trovato un nodo, connettersi. Chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), quindi chiamare [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) per restare in ascolto delle connessioni al grafo peer.
    > [!Note]  
    > Se non viene trovato alcun nodo, non chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare gli eventi del peer e utilizzare le connessioni, a seconda che il nodo sia connesso o meno al grafo peer. Ad esempio, l'applicazione può scegliere di timeout o eseguire periodicamente l'individuazione per un nodo attivo nel grafico.
-   Chiudere la connessione al grafo peer. Chiamare [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Quando PeerGraphOpen restituisce \_ \_ i dati dei peer \_ creati

Quando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce i **dati del peer \_ S \_ \_ creati**, significa che non viene trovato un database esistente per un grafo peer, viene creato un nuovo database e questa è la prima volta che viene aperta. Per utilizzare o restare in ascolto su un grafo peer, un peer deve essere connesso e sincronizzato con un grafo peer.

Nella procedura riportata di seguito vengono identificate le operazioni che è possibile eseguire per aprire un grafico peer quando una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce i **dati del peer \_ S \_ \_ creati**.

-   Aprire un grafico peer. Chiamare [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).
-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione per gli eventi peer, vedere [infrastruttura degli eventi](peer-events-infrastructure.md).

     

-   Individuare un nodo. Si tratta di un processo eseguito all'esterno dell'infrastruttura di Peer Graphing, usando un metodo o un'applicazione identificata dall'utente. L'API di Graphing peer non fornisce un meccanismo specifico per trovare un nodo grafico iniziale a cui connettersi. Un'applicazione deve usare un altro meccanismo, ad esempio l'API [PNRP (Peer Name Resolution Protocol)](pnrp-namespace-provider-api.md) , per individuare il nodo iniziale.
-   Se viene trovato un nodo, connettersi. Chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect), quindi chiamare [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) per restare in ascolto delle connessioni al grafo peer.
    > [!Note]  
    > Se non viene trovato alcun nodo, non chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare gli eventi del peer e utilizzare le connessioni, a seconda che il nodo sia connesso o meno al grafo peer. Ad esempio, l'applicazione può scegliere di timeout o eseguire periodicamente l'individuazione per un nodo attivo nel grafico.
-   Chiudere la connessione al grafo peer. Chiamare [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose).

 

 



