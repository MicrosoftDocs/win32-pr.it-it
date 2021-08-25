---
description: "L'API Peer Graphing usa le funzioni seguenti:"
ms.assetid: cd05d4da-ca65-471b-bb97-82885f22e6f9
title: Funzioni dell'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26c40770e8fcbc18b08ccb73dcfea5f1f6c4eab65be615ed76d8088ddc90954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776221"
---
# <a name="graphing-api-functions"></a>Funzioni dell'API Graphing

L'API Peer Graphing usa le funzioni seguenti:

## <a name="initialization-and-cleanup-functions"></a>Funzioni di inizializzazione e pulizia



| Funzione                                       | Descrizione                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphShutdown**](/windows/desktop/api/P2P/nf-p2p-peergraphshutdown) | Pulisce tutte le risorse allocate dalla chiamata a [**PeerGraphStartup.**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)                     |
| [**PeerGraphStartup**](/windows/desktop/api/P2P/nf-p2p-peergraphstartup)   | Indica all'infrastruttura peer graphing quale versione dei protocolli peer richiede l'applicazione chiamante. |



 

## <a name="graph-creation-and-access-functions"></a>Graph Funzioni di creazione e accesso



| Funzione                                   | Descrizione                                                                                                                                                                                                           |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphClose**](/windows/desktop/api/P2P/nf-p2p-peergraphclose)   | Invalida l'handle del grafo peer restituito da una chiamata a [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) o [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)e chiude tutte le connessioni di rete per il grafo peer specificato. |
| [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate) | Crea un nuovo grafo peer.                                                                                                                                                                                             |
| [**PeerGraphDelete**](/windows/desktop/api/P2P/nf-p2p-peergraphdelete) | Elimina i dati associati a un grafico peer specificato.                                                                                                                                                              |
| [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten) | Indica che un grafo peer deve iniziare a essere in ascolto delle connessioni in ingresso.                                                                                                                                          |
| [**PeerGraphOpen**](/windows/desktop/api/P2P/nf-p2p-peergraphopen)     | Apre un grafo peer creato in precedenza dal nodo locale o da un nodo remoto.                                                                                                                              |



 

## <a name="graph-and-node-information-functions"></a>Graph e funzioni di informazioni sui nodi



| Funzione                                                         | Descrizione                                                                                                                                                        |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEnumNodes**](/windows/desktop/api/P2P/nf-p2p-peergraphenumnodes)                 | Crea e restituisce un handle di enumerazione utilizzato per enumerare i nodi in un grafico peer.                                                                             |
| [**PeerGraphGetNodeInfo**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnodeinfo)             | Recupera informazioni su un nodo specifico.                                                                                                                       |
| [**PeerGraphGetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphgetproperties)         | Recupera le proprietà del grafo peer corrente.                                                                                                                       |
| [**PeerGraphGetStatus**](/windows/desktop/api/P2P/nf-p2p-peergraphgetstatus)                 | Restituisce lo stato corrente del grafo peer.                                                                                                                      |
| [**PeerGraphSetNodeAttributes**](/windows/desktop/api/P2P/nf-p2p-peergraphsetnodeattributes) | Imposta gli attributi della struttura [**PEER \_ NODE \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_node_info) per il nodo locale.                                                                |
| [**PeerGraphSetPresence**](/windows/desktop/api/P2P/nf-p2p-peergraphsetpresence)             | Attiva o disattiva in modo esplicito la pubblicazione di record di presenza per un nodo specifico. Questa funzione può eseguire l'override delle impostazioni di presenza nelle proprietà del grafo peer. |
| [**PeerGraphSetProperties**](/windows/desktop/api/P2P/nf-p2p-peergraphsetproperties)         | Imposta le proprietà del grafo peer.                                                                                                                                    |



 

## <a name="record-management-functions"></a>Funzioni di gestione dei record



| Funzione                                                                     | Descrizione                                                                                                                         |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphAddRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphaddrecord)                             | Aggiunge un nuovo record a un grafo peer. Un record aggiunto con questa funzione viene inviato a ogni nodo in un grafico peer.                          |
| [**PeerGraphDeleteRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphdeleterecord)                       | Contrassegna un record come eliminato all'interno di un grafico peer.                                                                                      |
| [**PeerGraphEnumRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphenumrecords)                         | Crea e restituisce un handle di enumerazione utilizzato per enumerare i record di un tipo specifico di record, utente o entrambi.                    |
| [**PeerGraphGetRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphgetrecord)                             | Recupera un record specifico in base all'ID record specificato.                                                                       |
| [**PeerGraphSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphsearchrecords)                     | Cerca record specifici nel grafico peer.                                                                                       |
| [**PeerGraphUpdateRecord**](/windows/desktop/api/P2P/nf-p2p-peergraphupdaterecord)                       | Aggiorna un record nel grafico peer e quindi lo propaga a ogni nodo nel grafico peer.                                       |
| [**PeerGraphValidateDeferredRecords**](/windows/desktop/api/P2P/nf-p2p-peergraphvalidatedeferredrecords) | Indica all'infrastruttura peer graphing che è il momento di inviare nuovamente tutti i record posticilati per la convalida del modulo di sicurezza. |



 

## <a name="export-and-import-functions"></a>Funzioni di esportazione e importazione



| Funzione                                                   | Descrizione                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase) | Esporta un database a grafo peer in un file che è possibile spostare in un computer diverso. |
| [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase) | Importa un file che contiene le informazioni da un database a grafo peer.             |



 

## <a name="utility-and-support-functions"></a>Funzioni di utilità e supporto



| Funzione                                                                     | Descrizione                                                                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peergraphendenumeration)                   | Rilascia un handle di enumerazione e libera le risorse associate a un'enumerazione.                                           |
| [**PeerGraphFreeData**](/windows/desktop/api/P2P/nf-p2p-peergraphfreedata)                               | Libera le risorse restituite da diverse funzioni dell'API Peer Graphing.                                                           |
| [**PeerGraphGetItemCount**](/windows/desktop/api/P2P/nf-p2p-peergraphgetitemcount)                       | Recupera il numero di elementi in un'enumerazione .                                                                                  |
| [**PeerGraphGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergraphgetnextitem)                         | Ottiene l'elemento o gli elementi successivi in un'enumerazione creata da una chiamata a funzioni specifiche, che restituiscono un'enumerazione peer.        |
| [**PeerGraphPeerTimeToUniversalTime**](/windows/desktop/api/P2P/nf-p2p-peergraphpeertimetouniversaltime) | Converte il valore dell'ora di riferimento gestito dal grafico peer in un valore di ora localizzato appropriato per la visualizzazione nel computer del peer. |
| [**PeerGraphUniversalTimeToPeerTime**](/windows/desktop/api/P2P/nf-p2p-peergraphuniversaltimetopeertime) | Converte un valore di ora universale dal computer del peer a un valore di ora del grafico peer comune.                                       |



 

## <a name="connection-functions"></a>Funzioni di connessione



| Funzione                                                                 | Descrizione                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PeerGraphCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphclosedirectconnection) | Chiude una connessione diretta specificata.                                                                                                                                                                                                          |
| [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect)                             | Tenta di stabilire una connessione a un nodo specificato in un grafico peer. Questa funzione avvia un'operazione asincrona.                                                                                                                             |
| [**PeerGraphEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergraphenumconnections)             | Crea e restituisce un handle di enumerazione utilizzato per enumerare le connessioni di un nodo locale.                                                                                                                                                   |
| [**PeerGraphOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergraphopendirectconnection)   | Consente a un'applicazione di stabilire una connessione diretta con un nodo in un grafo peer. La connessione può essere stabilita solo se il nodo a cui si connette l'applicazione ha sottoscritto l'evento **PEER GRAPH EVENT DIRECT \_ \_ \_ \_ CONNECTION.** |
| [**PeerGraphSendData**](/windows/desktop/api/P2P/nf-p2p-peergraphsenddata)                           | Invia dati a un nodo adiacente o a un nodo direttamente connesso.                                                                                                                                                                                    |



 

## <a name="events-infrastructure-functions"></a>Funzioni dell'infrastruttura eventi



| Funzione                                                     | Descrizione                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**PeerGraphGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergraphgeteventdata)       | Recupera gli eventi peer.                                                                                       |
| [**PeerGraphRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphregisterevent)     | Registra la richiesta di un peer per ricevere una notifica delle modifiche associate a un grafo peer e al tipo di evento.            |
| [**PeerGraphUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergraphunregisterevent) | Richiede all'applicazione di non ricevere più una notifica delle modifiche associate a un grafico peer e a un tipo di record. |



 

 

 



