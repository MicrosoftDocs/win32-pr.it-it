---
description: La funzione seguente viene usata con le pipe anonime.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Funzioni pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2413157ca76af56b5344327e1d3a9e93f86253f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315596"
---
# <a name="pipe-functions"></a>Funzioni pipe

La funzione seguente viene usata con le pipe anonime.



| Funzione                         | Descrizione                |
|----------------------------------|----------------------------|
| [**Non**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Crea una pipe anonima. |



 

Le funzioni seguenti vengono utilizzate con le named pipe.



| Funzione                                                                 | Descrizione                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Consente di connettersi a una pipe del tipo di messaggio, scrivere e leggere dalla pipe, quindi chiudere la pipe.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Consente a un processo del server named pipe di attendere che un processo client si connetta a un'istanza di un named pipe.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Crea un'istanza di un named pipe e restituisce un handle per le successive operazioni della pipe. Un processo client si connette a un named pipe tramite la funzione [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Disconnette l'entità finale del server di un'istanza di named pipe da un processo client.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Recupera il nome del computer client per il named pipe specificato.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Recupera l'identificatore del processo client per il named pipe specificato.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Recupera l'identificatore di sessione del client per il named pipe specificato.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Recupera informazioni su un named pipe specificato.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Recupera le informazioni relative al named pipe specificato.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Recupera l'identificatore del processo server per il named pipe specificato.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Recupera l'identificatore di sessione del server per la named pipe specificata.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Rappresenta un'applicazione client named pipe.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copia i dati da una pipe denominata o anonima in un buffer senza rimuoverli dalla pipe.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Imposta la modalità di lettura e la modalità di blocco del named pipe specificato.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combina le funzioni che scrivono e leggono un messaggio dal named pipe specificato in un'unica operazione di rete.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Attende il completamento di un intervallo di timeout oppure un'istanza del named pipe specificato è disponibile per una connessione.                                                                                                            |



 

 

 
