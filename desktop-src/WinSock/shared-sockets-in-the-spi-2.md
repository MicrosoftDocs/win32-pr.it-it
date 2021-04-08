---
description: Condivisione di socket in Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Socket condivisi in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21ff0d8f73d2bd9de942d17de7f9564158d1810c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880682"
---
# <a name="shared-sockets-in-the-spi"></a>Socket condivisi in SPI

La condivisione dei socket tra i processi in Windows Sockets viene implementata come indicato di seguito. Un processo di origine chiama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) per ottenere una speciale struttura di [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Usa un meccanismo di comunicazione interprocesso (IPC) per passare il contenuto di questa struttura a un processo di destinazione. Il processo di destinazione USA quindi la struttura di **\_ informazioni WSAPROTOCOL** in una chiamata a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Il descrittore di socket restituito da questa funzione sarà un descrittore di socket aggiuntivo a un socket sottostante che viene quindi condiviso.

È responsabilità del provider di servizi eseguire qualsiasi operazione necessaria nel contesto del processo di origine e creare una struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che verrà riconosciuta quando verrà visualizzata successivamente come parametro di [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) nel contesto dei processi di destinazione. Il membro **dwProviderReserved** della struttura **di \_ informazioni WSAPROTOCOL** è disponibile per l'uso da parte del provider di servizi e può essere usato per archiviare informazioni utili sul contesto, incluso un handle duplicato.

Questo meccanismo è progettato per essere appropriato per le versioni di Windows a thread singolo e preemptive con multithreading. Si noti tuttavia che i socket possono essere condivisi tra i thread di un determinato processo senza usare la funzione [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) , perché un descrittore di socket è valido in tutti i thread di un processo.

Come descritto nell' [allocazione di descrittori](descriptor-allocation-2.md)di sezione, quando vengono allocati nuovi descrittori di socket, i provider IFS devono chiamare [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) e i provider non IFS devono chiamare [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

Nella tabella seguente è illustrato un possibile scenario per la definizione e l'utilizzo di un socket condiviso in una modalità di inserimento.

| Processo di origine                                                                                                                          | IPC    | Processo di destinazione                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) richiede l'identificatore del processo di destinazione.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) riceve la richiesta dell'identificatore del processo e risponde.                          |
| 4) riceve l'identificatore del processo.                                                                                                         | <== |                                                                               |
| 5) chiama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) per ottenere una struttura speciale per le [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . |        |                                                                               |
| 6) Invia la struttura delle **\_ informazioni di WSAPROTOCOL** alla destinazione.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) riceve la struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .        |
|                                                                                                                                         |        | 8) chiama [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) per creare il descrittore di socket condiviso. |
|                                                                                                                                         |        | 9) usa il socket condiviso per lo scambio di dati.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
