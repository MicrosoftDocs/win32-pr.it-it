---
description: Condivisione di socket in Windows Sockets (Winsock).
ms.assetid: dad31820-6f60-4c3b-9cdf-e301a5ffce48
title: Socket condivisi nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab0992768a7f3b38f27e4d40c54673e63e855687d0e9b9162e8b9e3cd1d1711d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559699"
---
# <a name="shared-sockets-in-the-spi"></a>Socket condivisi nell'spi

La condivisione dei socket tra processi Windows Socket viene implementata come segue. Un processo di origine [**chiama WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) per ottenere una struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) speciale. Usa un meccanismo di comunicazione interprocesso (IPC) per passare il contenuto di questa struttura a un processo di destinazione. Il processo di destinazione usa quindi la **struttura WSAPROTOCOL \_ INFO** in una chiamata a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Il descrittore di socket restituito da questa funzione sarà un descrittore di socket aggiuntivo per un socket sottostante che diventa quindi condiviso.

È responsabilità del provider di servizi eseguire tutte le operazioni necessarie nel contesto del processo di origine e creare una struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) che verrà riconosciuta quando successivamente viene visualizzata come parametro per [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) nel contesto dei processi di destinazione. Il **membro dwProviderReserved** della struttura **WSAPROTOCOL \_ INFO** è disponibile per l'uso del provider di servizi e può essere usato per archiviare informazioni di contesto utili, incluso un handle duplicato.

Questo meccanismo è progettato per essere appropriato per le versioni a thread singolo e preemptive multithreading di Windows. Si noti tuttavia che i socket possono essere condivisi tra i thread in un determinato processo senza usare la funzione [**WSPDuplicateSocket,**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) poiché un descrittore di socket è valido in tutti i thread di un processo.

Come descritto nella sezione Allocazione descrittori [,](descriptor-allocation-2.md)quando vengono allocati nuovi descrittori socket i provider IFS devono chiamare [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle) e i provider non IFS devono chiamare [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle).

Nella tabella seguente è illustrato uno scenario possibile per stabilire e usare un socket condiviso in modalità handoff.

| Processo di origine                                                                                                                          | IPC    | Processo di destinazione                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------|
| 1) [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket), [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                                                                 |        |                                                                               |
| 2) Richiede l'identificatore del processo di destinazione.                                                                                                  | ==> |                                                                               |
|                                                                                                                                         |        | 3) Riceve la richiesta dell'identificatore di processo e risponde.                          |
| 4) Riceve l'identificatore del processo.                                                                                                         | <== |                                                                               |
| 5) Chiama [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85)) per ottenere una struttura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) speciale. |        |                                                                               |
| 6) Invia la **struttura WSAPROTOCOL \_ INFO** alla destinazione.                                                                                     |        |                                                                               |
|                                                                                                                                         | ==> | 7) Riceve la [**struttura WSAPROTOCOL \_ INFO.**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)        |
|                                                                                                                                         |        | 8) Chiama [**WSPSocket per**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) creare il descrittore del socket condiviso. |
|                                                                                                                                         |        | 9)Usa un socket condiviso per lo scambio di dati.                                       |
| 10) [ **WSPClosesocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                          | <== |                                                                               |



 

 

 
