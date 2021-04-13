---
description: Funzioni di trasporto dati esposte da Ws2spi. h.
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: Funzioni di trasporto dati generiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526173"
---
# <a name="generic-data-transport-functions"></a>Funzioni di trasporto dati generiche

In questa sezione sono elencate le funzioni di trasporto dei dati esposte da Ws2spi. h.



| Funzione                                                   | Descrizione                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | Una connessione in ingresso viene riconosciuta e associata a un socket creato immediatamente. Il socket originale viene restituito allo stato di ascolto. Questa funzione consente inoltre l'accettazione condizionale. |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | Esegue la versione asincrona di [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)).                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | Assegna un nome locale a un socket senza nome.                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | Annulla una chiamata di blocco Windows Socket in attesa.                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | Si disconnette dal provider di servizi Windows Sockets sottostante.                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | Rimuove un socket dalla tabella di riferimento dell'oggetto per processo. Solo i blocchi in caso di \_ indugio sono impostati con un timeout diverso da zero in un socket di blocco.                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | Avvia una connessione sul socket specificato. Questa funzione consente inoltre lo scambio di dati di connessione e la specifica QoS.                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | Restituisce una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che può essere utilizzata per creare un nuovo descrittore di socket per un socket condiviso.                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | Individua le occorrenze di eventi di rete.                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | Associa gli eventi di rete a un oggetto evento.                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | Ottiene lo stato di completamento dell'operazione sovrapposta.                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | Recupera il nome del peer connesso al socket specificato.                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | Recupera l'indirizzo locale a cui è associato il socket specificato.                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | Recupera le opzioni associate al socket specificato.                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | Fornisce parametri QoS basati su un nome di servizio noto.                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | Fornisce il controllo per i socket.                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | Aggiunge un nodo foglia a una sessione multipoint.                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | Resta in attesa delle connessioni in ingresso su un socket specificato.                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | Riceve i dati da un socket connesso o non connesso. Questa funzione supporta l'I/O a dispersione/raccolta, i socket sovrapposti e fornisce il parametro flags come IN/OUT.                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | Termina la ricezione su un socket e recupera i dati di disconnessione se il socket è orientato alla connessione.                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | Riceve i dati da un socket connesso o non connesso. Questa funzione supporta l'I/O a dispersione/raccolta, i socket sovrapposti e fornisce il parametro flags come IN/OUT.                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | Esegue il multiplexing di I/O sincrono.                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | Invia i dati a un socket connesso. Questa funzione è adatta anche a dispersione/raccolta I/O e socket sovrapposti.                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | Avvia la terminazione di una connessione socket ed eventualmente invia i dati di disconnessione.                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | Invia i dati a un socket connesso o non connesso. Questa funzione è adatta anche a dispersione/raccolta I/O e socket sovrapposti.                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | Archivia le opzioni associate al socket specificato.                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | Arresta parte di una connessione full-duplex.                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | Funzione di creazione di socket che accetta una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) come input e consente la creazione di socket sovrapposti.                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | Inizializza il provider del servizio Windows Sockets sottostante.                                                                                                                                            |



 

 

 
