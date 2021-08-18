---
description: Funzioni di trasporto dati esposte da Ws2spi.h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funzioni di trasporto dati generiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d13b067713fe6a2600d6667ebe7eac058c5fcae87fc5bfd14311b3a263b862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132354"
---
# <a name="generic-data-transport-functions"></a>Funzioni di trasporto dati generiche

Questa sezione elenca le funzioni di trasporto dati esposte da Ws2spi.h.



| Funzione                                                   | Descrizione                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Una connessione in ingresso viene confermata e associata a un socket creato immediatamente. Il socket originale viene restituito allo stato di ascolto. Questa funzione consente anche l'accettazione condizionale. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Esegue la versione asincrona [**di WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Assegna un nome locale a un socket senza nome.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Annulla un blocco in sospeso Windows socket.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Si disconnette dal provider di Windows Sockets sottostante.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Rimuove un socket dalla tabella di riferimento dell'oggetto per processo. Si blocca solo se SO LINGER è impostato con un timeout diverso da \_ zero in un socket di blocco.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Avvia una connessione sul socket specificato. Questa funzione consente anche lo scambio di dati di connessione e specifica QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Restituisce una [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che può essere usata per creare un nuovo descrittore di socket per un socket condiviso.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Individua le occorrenze degli eventi di rete.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Associa gli eventi di rete a un oggetto evento.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Ottiene lo stato di completamento dell'operazione sovrapposta.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera il nome del peer connesso al socket specificato.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera l'indirizzo locale a cui è associato il socket specificato.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera le opzioni associate al socket specificato.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Fornisce i parametri QoS in base a un nome di servizio noto.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Fornisce il controllo per i socket.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Unisce un nodo foglia a una sessione multipoint.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Rimane in ascolto delle connessioni in ingresso su un socket specificato.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Riceve dati da un socket connesso o non connesso. Questa funzione supporta l'I/O a dispersione/raccolta, i socket sovrapposti e fornisce il parametro flags come IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Termina la ricezione in un socket e recupera i dati di disconnessione se il socket è orientato alla connessione.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Riceve dati da un socket connesso o non connesso. Questa funzione supporta l'I/O a dispersione/raccolta, i socket sovrapposti e fornisce il parametro flags come IN/OUT.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Esegue il multiplexing di I/O sincrono.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Invia i dati a un socket connesso. Questa funzione supporta anche l'I/O a dispersione/raccolta e i socket sovrapposti.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Avvia la terminazione di una connessione socket e facoltativamente invia i dati di disconnessione.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Invia dati a un socket connesso o non connesso. Questa funzione supporta anche l'I/O a dispersione/raccolta e i socket sovrapposti.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Archivia le opzioni associate al socket specificato.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Arresta parte di una connessione full-duplex.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Funzione di creazione di socket che accetta una [**struttura WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) come input e consente la creazione di socket sovrapposti.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inizializza il provider di Windows Sockets sottostante.                                                                                                                                            |



 

 

 
