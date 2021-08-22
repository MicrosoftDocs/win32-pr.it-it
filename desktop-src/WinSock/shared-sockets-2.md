---
description: È stata introdotta la funzione WSADuplicateSocket per abilitare la condivisione dei socket tra processi.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Socket condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3f2663aa618b1bacab40b1cb29735c972e1d8b9e9db3528ee5079a336747c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612911"
---
# <a name="shared-sockets"></a>Socket condivisi

È [**stata introdotta la funzione WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) per abilitare la condivisione dei socket tra processi. Un processo di origine **chiama WSADuplicateSocket** per ottenere una struttura [**WSAPROTOCOL \_ INFO speciale**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per un identificatore di processo di destinazione. Usa un meccanismo di comunicazione interprocesso (IPC) per passare il contenuto di questa struttura a un processo di destinazione. Il processo di destinazione usa quindi la **struttura WSAPROTOCOL \_ INFO** in una chiamata a [**WSPSocket.**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) Il descrittore del socket restituito da questa funzione sarà un descrittore di socket aggiuntivo per un socket sottostante che diventa quindi condiviso. I socket possono essere condivisi tra i thread in un determinato processo senza usare la funzione **WSADuplicateSocket** perché un descrittore di socket è valido in tutti i thread di un processo.

I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O. Tuttavia, l'interfaccia Winsock non implementa alcun tipo di controllo di accesso, quindi i processi devono coordinare qualsiasi operazione su un socket condiviso. Un esempio tipico di condivisione dei socket è l'uso di un processo per la creazione di socket e la connessione. Questo processo quindi trasla i socket ad altri processi responsabili dello scambio di informazioni.

La [**funzione WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) crea descrittori di socket e non il socket sottostante. Di conseguenza, tutti gli stati associati a un socket sono mantenuti in comune tra tutti i descrittori. Ad esempio, [**un'operazione setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) eseguita usando un descrittore è successivamente visibile usando [**un oggetto getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) da uno o tutti i descrittori. Un processo può chiamare [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) su un socket duplicato e il descrittore verrà deallocato. Il socket sottostante, tuttavia, rimane aperto fino a quando non viene **chiamato closesocket** con l'ultimo descrittore rimanente.

La notifica sui socket condivisi è soggetta ai normali vincoli delle [**funzioni WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e [**WSAEventSelect.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) L'esecuzione di una di queste chiamate usando uno dei descrittori condivisi annulla qualsiasi registrazione dell'evento precedente per il socket, indipendentemente dal descrittore usato per eseguire la registrazione. Pertanto, ad esempio, non sarebbe possibile fare in modo che il processo A riceva gli eventi FD READ e che il processo B riceva \_ gli eventi FD \_ WRITE. In situazioni in cui è necessario un coordinamento così stretto, è consigliabile che gli sviluppatori usino thread anziché processi separati.

 

 
