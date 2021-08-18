---
description: La funzione seguente viene usata con le pipe anonime.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Funzioni pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481605"
---
# <a name="pipe-functions"></a>Funzioni pipe

La funzione seguente viene usata con le pipe anonime.



| Funzione                         | Descrizione                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Crea una pipe anonima. |



 

Le funzioni seguenti vengono usate con named pipe.



| Funzione                                                                 | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Si connette a una pipe di tipo messaggio, scrive e legge dalla pipe e quindi chiude la pipe.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Consente a named pipe processo server di attendere che un processo client si connetta a un'istanza di un named pipe.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Crea un'istanza di un named pipe e restituisce un handle per le operazioni successive della pipe. Un processo client si connette a un named pipe usando la [**funzione CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**o CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Disconnette la fine del server di un'named pipe da un processo client.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Recupera il nome del computer client per l'oggetto named pipe.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Recupera l'identificatore del processo client per l'named pipe.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Recupera l'identificatore di sessione client per l'oggetto named pipe.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Recupera informazioni su un oggetto named pipe.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Recupera informazioni sull'oggetto named pipe.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Recupera l'identificatore del processo server per l'oggetto named pipe.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Recupera l'identificatore di sessione del server per l'named pipe.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Rappresenta un'applicazione client named pipe.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copia i dati da una pipe denominata o anonima in un buffer senza rimuoverli dalla pipe.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Imposta la modalità di lettura e la modalità di blocco dell'oggetto named pipe.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combina le funzioni che scrivono un messaggio in e leggono un messaggio dal named pipe in una singola operazione di rete.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Attende che sia trascorso un intervallo di timeout o che sia disponibile un'istanza del named pipe per una connessione.                                                                                                            |



 

 

 
