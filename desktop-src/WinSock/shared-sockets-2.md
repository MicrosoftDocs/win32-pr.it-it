---
description: La funzione WSADuplicateSocket è stata introdotta per abilitare la condivisione dei socket tra i processi.
ms.assetid: f7cf40e9-f3a6-4b62-8a78-df25464e2365
title: Socket condivisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6753b01f6389254756254d2ebe196af8e2a8a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967085"
---
# <a name="shared-sockets"></a>Socket condivisi

La funzione [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) è stata introdotta per abilitare la condivisione dei socket tra i processi. Un processo di origine chiama **WSADuplicateSocket** per ottenere una speciale struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per un identificatore del processo di destinazione. Usa un meccanismo di comunicazione interprocesso (IPC) per passare il contenuto di questa struttura a un processo di destinazione. Il processo di destinazione USA quindi la struttura di **\_ informazioni WSAPROTOCOL** in una chiamata a [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket). Il descrittore di socket restituito da questa funzione sarà un descrittore di socket aggiuntivo a un socket sottostante che viene quindi condiviso. I socket possono essere condivisi tra i thread di un determinato processo senza usare la funzione **WSADuplicateSocket** perché un descrittore di socket è valido in tutti i thread di un processo.

I due (o più) descrittori che fanno riferimento a un socket condiviso possono essere usati in modo indipendente per quanto riguarda l'I/O. Tuttavia, l'interfaccia Winsock non implementa alcun tipo di controllo di accesso, quindi i processi devono coordinare qualsiasi operazione su un socket condiviso. Un esempio tipico di socket di condivisione è quello di usare un processo per creare socket e stabilire connessioni. Questo processo passa quindi i socket ad altri processi responsabili dello scambio di informazioni.

La funzione [**WSADuplicateSocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa) crea descrittori di socket e non il socket sottostante. Di conseguenza, tutti gli Stati associati a un socket vengono mantenuti in comune in tutti i descrittori. Ad esempio, un'operazione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) eseguita utilizzando un descrittore viene successivamente visualizzata utilizzando un [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) da uno o tutti i descrittori. Un processo può chiamare [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) su un socket duplicato e il descrittore verrà deallocato. Il socket sottostante, tuttavia, rimane aperto fino a quando non viene chiamato **chiamata closesocket** con l'ultimo descrittore rimanente.

La notifica sui socket condivisi è soggetta ai vincoli usuali delle funzioni [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) . Quando si esegue una di queste chiamate utilizzando uno dei descrittori condivisi, viene annullata la registrazione di eventi precedente per il socket, indipendentemente dal descrittore utilizzato per effettuare la registrazione. Quindi, ad esempio, non sarebbe possibile avere un processo di ricezione di eventi di \_ lettura FD ed elaborare B ricevere \_ eventi di scrittura FD. Per le situazioni in cui è necessario un coordinamento rigoroso, è consigliabile che gli sviluppatori usino i thread anziché processi distinti.

 

 
