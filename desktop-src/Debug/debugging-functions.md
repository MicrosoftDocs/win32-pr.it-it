---
description: Le funzioni seguenti vengono utilizzate con il debug.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Funzioni di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39bf5f81b08e3a7b324f276fc1a7b5d256d40819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304416"
---
# <a name="debugging-functions"></a>Funzioni di debug

Le funzioni seguenti vengono utilizzate con il debug.



| Funzione                                                           | Descrizione                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Determina se è in corso il debug del processo specificato.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Consente a un debugger di continuare un thread che ha segnalato in precedenza un evento di debug. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Consente a un debugger di connettersi a un processo attivo ed eseguirne il debug.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Arresta il debug del processo specificato da parte del debugger.                            |
| [**DebugBreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Causa l'eccezione di un punto di interruzione nel processo corrente.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Causa l'eccezione di un punto di interruzione nel processo specificato.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Imposta l'azione da eseguire quando il thread chiamante viene chiuso.                      |
| [**FatalExit**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Trasferisce il controllo di esecuzione al debugger.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Svuota la cache di istruzioni per il processo specificato.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Recupera il contesto del thread specificato.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Recupera una voce della tabella descrittore per il selettore e il thread specificati.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Determina se il processo chiamante viene sottoposto a debug da un debugger in modalità utente.   |
| [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Invia una stringa al debugger per la visualizzazione.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Legge i dati da un'area di memoria in un processo specificato.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Imposta il contesto per il thread specificato.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Attende il verificarsi di un evento di debug in un processo di cui è in corso il debug.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Recupera il contesto del thread WOW64 specificato.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Recupera una voce della tabella descrittore per il selettore specificato e il thread WOW64.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Imposta il contesto del thread WOW64 specificato.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Scrive i dati in un'area di memoria in un processo specificato.                            |



 

 

 
