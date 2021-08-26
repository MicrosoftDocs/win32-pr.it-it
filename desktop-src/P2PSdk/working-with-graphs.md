---
description: Quando si lavora con i grafi peer, le funzioni devono essere chiamate in un ordine specifico. Il flusso delle chiamate dipende dalla creazione o dall'apertura di un grafo peer. Questo argomento identifica il flusso delle chiamate di funzione in una semplice applicazione a grafo peer.
ms.assetid: cb4f48d0-d1e2-4a4b-bd5a-6e8f66d03806
title: Uso dei grafi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdb4a40f1c086ada772239798990c3dfb24326b3e70bd768a95eacc35ee384b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034031"
---
# <a name="working-with-graphs"></a>Uso dei grafi

Quando si lavora con i grafi peer, le funzioni devono essere chiamate in un ordine specifico. Il flusso delle chiamate dipende dalla creazione o dall'apertura di un grafo peer. Questo argomento identifica il flusso delle chiamate di funzione in una semplice applicazione a grafo peer.

## <a name="starting-up-a-graph"></a>Avvio di un Graph

Prima che un'applicazione chiami una funzione nell'API Peer Graphing, è necessario chiamare [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup) per inizializzare l'API Peer Graphing per un'applicazione e quindi impostare la versione supportata.

## <a name="creating-a-peer-graph"></a>Creazione di un peer Graph

La procedura seguente identifica il flusso di chiamate per la creazione di un grafo peer.

> [!IMPORTANT]
> Solo un peer deve chiamare [**PeerGraphCreate.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) Tutti gli altri peer devono chiamare [**PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) Più chiamate a **PeerGraphCreate** invalidano un grafo.

 

-   Creare un grafo peer. Chiamare [**PeerGraphCreate.**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate)
-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione per gli eventi peer, vedere [Infrastruttura di eventi.](peer-events-infrastructure.md)

     

-   Restare in ascolto delle connessioni a un grafo peer. Chiamare [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)
-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare eventi peer e usare le connessioni.
-   Chiudere la connessione a un grafo peer. Chiamare [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="opening-a-peer-graph"></a>Apertura di un peer Graph

Il flusso delle chiamate di funzione per aprire un grafo peer dipende dal valore restituito della chiamata a [**PeerGraphOpen.**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) I valori più importanti sono **S \_ OK** e **PEER S DATA \_ \_ \_ CREATED,** illustrati nelle sezioni seguenti di questo argomento.

> [!Note]  
> Se una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) non restituisce **S OK \_ o** **PEER S DATA \_ \_ \_ CREATED,** gestire l'errore.

 

## <a name="when-peergraphopen-returns-s_ok"></a>Quando PeerGraphOpen restituisce S \_ OK

Quando una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce **S \_ OK,** sono stati aperti un grafo peer e un database esistente. La procedura seguente identifica le operazioni che è possibile eseguire per aprire un grafo peer quando una chiamata a **PeerGraphOpen** restituisce **S \_ OK**

-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione per gli eventi, vedere [Infrastruttura degli eventi.](peer-events-infrastructure.md)

     

-   Individuare un nodo. Si tratta di un processo eseguito all'esterno dell'infrastruttura peer graphing, usando un metodo o un'applicazione identificata dall'utente. L'API Peer Graphing non fornisce un meccanismo specifico per trovare un nodo del grafo iniziale a cui connettersi. Un'applicazione deve usare un altro meccanismo, ad esempio [l'API Peer Name Resolution Protocol (PNRP),](pnrp-namespace-provider-api.md) per individuare il nodo iniziale.
-   Se viene trovato un nodo, connettersi al nodo. Chiamare [**PeerGraphConnect,**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)quindi [**chiamare PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) per restare in ascolto delle connessioni al grafo peer.
    > [!Note]  
    > Se non viene trovato un nodo, non chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare gli eventi peer e usare le connessioni, a seconda che il nodo sia connesso o meno al grafo peer. Ad esempio, l'applicazione può scegliere di impostare un timeout o eseguire periodicamente l'individuazione di un nodo attivo nel grafico.
-   Chiudere la connessione al grafo peer. Chiamare [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

## <a name="when-peergraphopen-returns-peer_s_data_created"></a>Quando PeerGraphOpen restituisce PEER \_ S \_ DATA \_ CREATED

Quando [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce **PEER S DATA \_ \_ \_ CREATED,** significa che non viene trovato un database esistente per un grafo peer, viene creato un nuovo database e questa è la prima volta che viene aperto. Per usare o restare in ascolto su un grafo peer, un peer deve essere connesso e sincronizzato con un grafo peer.

La procedura seguente identifica le operazioni che è possibile eseguire per aprire un grafo peer quando una chiamata a [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen) restituisce **PEER S DATA \_ \_ \_ CREATED.**

-   Aprire un grafo peer. Chiamare [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen).
-   Eseguire la registrazione per gli eventi peer. Chiamare [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent).
    > [!Note]  
    > Per altre informazioni sulla registrazione per gli eventi peer, vedere [Infrastruttura di eventi.](peer-events-infrastructure.md)

     

-   Individuare un nodo. Si tratta di un processo eseguito all'esterno dell'infrastruttura peer graphing, usando un metodo o un'applicazione identificata dall'utente. L'API Peer Graphing non fornisce un meccanismo specifico per trovare un nodo del grafo iniziale a cui connettersi. Un'applicazione deve usare un altro meccanismo, ad esempio [l'API Peer Name Resolution Protocol (PNRP),](pnrp-namespace-provider-api.md) per individuare il nodo iniziale.
-   Se viene trovato un nodo, connettersi al nodo. Chiamare [**PeerGraphConnect,**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)quindi [**chiamare PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) per restare in ascolto delle connessioni al grafo peer.
    > [!Note]  
    > Se non viene trovato un nodo, non chiamare [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) e [**PeerGraphListen.**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)

     

-   Eseguire funzioni dipendenti dall'applicazione per il resto del tempo di esecuzione, ad esempio elaborare gli eventi peer e usare le connessioni, a seconda che il nodo sia connesso o meno al grafo peer. Ad esempio, l'applicazione può scegliere di impostare un timeout o eseguire periodicamente l'individuazione di un nodo attivo nel grafico.
-   Chiudere la connessione al grafo peer. Chiamare [**PeerGraphClose.**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)

 

 



