---
description: Le operazioni pipe, inclusi i client e i server pipe, possono chiamare una delle diverse funzioni, oltre a CallNamedPipe, per leggere e scrivere in un named pipe.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Operazioni named pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703189a129fc44b956ab65c2f70bbf88bfd22700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128139"
---
# <a name="named-pipe-operations"></a>Operazioni named pipe

La prima volta che il server pipe chiama la funzione [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) , usa il parametro *nMaxInstances* per specificare il numero massimo di istanze della pipe che possono esistere simultaneamente. Il server può chiamare ripetutamente **CreateNamedPipe** per creare istanze aggiuntive della pipe, purché non superi il numero massimo di istanze. Se la funzione ha esito positivo, ogni chiamata restituisce un handle per la fine del server di un'istanza di named pipe.

Non appena il server pipe crea un'istanza di pipe, un client pipe può connettersi ad essa chiamando la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Se è disponibile un'istanza pipe, **CreateFile** restituisce un handle per la fine client dell'istanza pipe. Se non sono disponibili istanze della pipe, un client pipe può usare la funzione [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) per attendere il completamento della disponibilità di una pipe.

Un server pipe può determinare quando un client pipe è connesso a un'istanza di pipe chiamando la funzione [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Se l'handle della pipe è in modalità di blocco-attesa, **ConnectNamedPipe** non restituisce alcun risultato finché non viene connesso un client.

I client e i server pipe possono chiamare una delle diverse funzioni, oltre a [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) , per leggere e scrivere in un named pipe. Il comportamento di queste funzioni dipende dal tipo di pipe e dalle modalità attive per l'handle di pipe specificato, come indicato di seguito:

-   Le funzioni [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) possono essere usate con pipe di tipo byte o di tipo messaggio.
-   Le funzioni [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) possono essere usate con pipe di tipo byte o di tipo messaggio se è stato aperto l'handle della pipe per le operazioni sovrapposte.
-   La funzione [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) può essere utilizzata per leggere senza rimuovere il contenuto di una pipe di tipo byte o una pipe di tipo messaggio. **PeekNamedPipe** può inoltre restituire informazioni aggiuntive sull'istanza della pipe.
-   La funzione [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) può essere usata con pipe duplex di tipo messaggio se l'handle della pipe per il processo chiamante è impostato sulla modalità di lettura del messaggio. La funzione scrive un messaggio di richiesta e legge un messaggio di risposta in un'unica operazione, migliorando le prestazioni di rete.

Il server pipe non deve eseguire un'operazione di lettura di blocco finché il client pipe non è stato avviato. In caso contrario, può verificarsi un race condition. Questo problema si verifica in genere quando il codice di inizializzazione, ad esempio quello della libreria di runtime del linguaggio C, deve bloccare ed esaminare gli handle ereditati.

Quando un client e un server completano l'utilizzo di un'istanza pipe, il server deve prima chiamare la funzione [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) , per garantire che tutti i byte o i messaggi scritti sulla pipe siano letti dal client. **FlushFileBuffers** non restituisce alcun risultato finché il client non ha letto tutti i dati dalla pipe. Il server chiama quindi la funzione [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) per chiudere la connessione al client della pipe. Questa funzione rende l'handle del client non valido, se non è già stato chiuso. Tutti i dati non letti nella pipe vengono eliminati. Dopo che il client è stato disconnesso, il server chiama la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) per chiudere il relativo handle per l'istanza della pipe. In alternativa, il server può utilizzare [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) per consentire a un nuovo client di connettersi a questa istanza della pipe.

Un processo può recuperare informazioni su un named pipe chiamando la funzione [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) , che restituisce il tipo della pipe, le dimensioni dei buffer di input e di output e il numero massimo di istanze di pipe che è possibile creare. La funzione [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) segnala le modalità di lettura e di attesa di un handle di pipe, il numero corrente di istanze di pipe e informazioni aggiuntive per le pipe che comunicano su una rete. La funzione [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) imposta la modalità di lettura e le modalità di attesa di un handle di pipe. Per i client pipe che comunicano con un server remoto, la funzione controlla anche il numero massimo di byte da raccogliere o il tempo massimo di attesa prima della trasmissione di un messaggio (presupponendo che l'handle del client non sia stato aperto con la modalità Write-through abilitata).

 

 
