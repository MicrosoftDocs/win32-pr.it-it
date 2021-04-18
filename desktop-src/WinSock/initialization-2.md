---
description: Il \_32.dll WS2 carica la dll di interfaccia del provider di servizi nel sistema utilizzando i meccanismi standard di caricamento della libreria dinamica di Microsoft Windows e la inizializza chiamando WSPStartup.
ms.assetid: 6df28d93-8757-45b3-8f05-86381c3be64e
title: Inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d6ef10db421ef15f2bb94eb67e96fc2cfc5924
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306949"
---
# <a name="initialization"></a>Inizializzazione

Il *\_32.dllWS2* carica la dll di interfaccia del provider di servizi nel sistema utilizzando i meccanismi standard di caricamento della libreria dinamica di Microsoft Windows e la inizializza chiamando [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Questa operazione viene in genere attivata da un'applicazione che chiama [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) o [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) per creare un nuovo socket da associare a un provider di servizi la cui dll di interfaccia non è attualmente caricata in memoria. Il percorso della DLL dell'interfaccia di ogni provider di servizi viene archiviato dal *Ws2 \_32.dll* al momento dell'installazione del provider di servizi. Per ulteriori informazioni, vedere [funzioni di installazione e configurazione](installation-and-configuration-functions-2.md) .

Nel corso del tempo potrebbero esistere versioni diverse per le dll, le applicazioni e i provider di servizi Winsock. Le nuove versioni possono definire nuove funzionalità e nuovi parametri per le strutture di dati e i parametri di bit e così via. I numeri di versione indicano pertanto come interpretare diverse strutture di dati.

Per consentire la combinazione e la corrispondenza ottimali delle diverse versioni delle applicazioni, delle versioni di WS2 \_32.dll e delle versioni dei provider di servizi da parte di fornitori diversi, SPI fornisce un meccanismo di negoziazione della versione da utilizzare tra i *\_32.dllWS2* e i provider di servizi. Questa negoziazione della versione viene gestita da [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Fondamentalmente, il *Ws2 \_32.dll* passa al provider di servizi i numeri di versione più elevati con cui è compatibile. Il provider di servizi confronta questo oggetto con un intervallo di numeri di versione supportato. Se questi intervalli si sovrappongono, il provider di servizi restituisce un valore all'interno della parte sovrapposta dell'intervallo come risultato della negoziazione. In genere, deve essere il valore massimo possibile. Se gli intervalli non si sovrappongono, le due entità sono incompatibili e la funzione restituisce un errore.

[**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) deve essere chiamato almeno una volta da ogni processo client e può essere chiamato più volte da WS2 \_32.dll o da altre entità. Per ogni chiamata **WSPStartup** riuscita, è necessario chiamare un [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) corrispondente. Il provider di servizi deve mantenere un conteggio dei riferimenti in base al processo. Per ogni chiamata a **WSPStartup** , il chiamante può specificare qualsiasi numero di versione supportato dalla dll SP.

Un provider di servizi deve archiviare il puntatore alla tabella dispatch del client ricevuta come parametro [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) in base al processo. Se un determinato processo chiama **WSPStartup** più volte, il provider di servizi deve utilizzare solo il puntatore alla tabella dispatch fornito più di recente.

Come parte del processo di inizializzazione del provider di servizi, WS2 \_32.dll recupera la tabella dispatch del provider di servizi tramite il parametro *lpProcTable* per ottenere punti di ingresso al resto delle funzioni SPI specificate in questo documento.

L'utilizzo di una tabella dispatch (in contrapposizione ai normali meccanismi DLL per l'accesso ai punti di ingresso) svolge due finalità:

-   È più utile per la32.dll WS2, \_ in quanto è possibile effettuare una singola chiamata per individuare l'intero set di punti di ingresso.
-   Consente ai provider di servizi su più livelli formati in catene di protocolli di funzionare in modo più efficiente.

## <a name="initializing-protocol-chains"></a>Inizializzazione di catene di protocollo

Quando viene installata la struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per una catena di protocolli, viene specificato anche il percorso del primo provider a livelli nella catena. Quando viene inizializzata una catena di protocolli, WS2 \_32.dll utilizza questo percorso per caricare la dll del provider e quindi richiama [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup). Poiché **WSPStartup** include un puntatore alla struttura delle **\_ informazioni di WSAPROTOCOL** della catena come uno dei parametri, i provider sovrapposti possono determinare il tipo di catena in cui vengono inizializzate e l'identità del livello inferiore successivo nella catena. Un provider su più livelli caricherà a sua volta il provider del protocollo successivo nella catena e lo inizializza con una chiamata a **WSPStartup** e così via. Ogni volta che il livello inferiore successivo è un altro provider a più livelli, nella chiamata **WSPStartup** è necessario fare riferimento alla struttura delle **\_ informazioni WSAPROTOCOL** della catena. Quando il livello inferiore successivo è un protocollo di base (che indica la fine della catena), la struttura di **\_ informazioni WSAPROTOCOL** della catena non viene più propagata verso il basso. Al contrario, il livello corrente deve fare riferimento a una struttura di **\_ informazioni WSAPROTOCOL** che corrisponde al protocollo che deve essere utilizzato dal provider di base. Pertanto, il provider di base non ha alcun concetto di essere associato a una catena di protocolli.

La tabella dispatch fornita da un determinato provider a più livelli consente, in molti casi, di duplicare i punti di ingresso di un provider sottostante. Il provider su più livelli inserisce solo i propri punti di ingresso per le funzioni di cui è necessario essere direttamente in relazione. Si noti, tuttavia, che è imperativo che un provider su più livelli non modifichi il contenuto della tabella di chiamata ricevuta durante la chiamata di [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) sul livello inferiore successivo in una catena di protocolli. Queste chiamate devono essere apportate direttamente alla DLL di Windows Sockets 2.

 

 
