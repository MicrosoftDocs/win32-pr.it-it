---
description: Le funzioni seguenti vengono usate con il debug.
ms.assetid: 95a838a2-f138-4682-b733-3f363b6c4a4b
title: Funzioni di debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfafdf5a453d262e75c4ab87356cbe34cfbb8574b520d353de0e66057903087f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162672"
---
# <a name="debugging-functions"></a>Funzioni di debug

Le funzioni seguenti vengono usate con il debug.



| Funzione                                                           | Descrizione                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [**CheckRemoteDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-checkremotedebuggerpresent)   | Determina se è in corso il debug del processo specificato.                         |
| [**ContinueDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent)                   | Consente a un debugger di continuare un thread che in precedenza ha segnalato un evento di debug. |
| [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)                   | Consente a un debugger di connettersi a un processo attivo ed eseguirne il debug.                     |
| [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)           | Arresta il debug del processo specificato da parte del debugger.                            |
| [**Debugbreak**](/windows/win32/api/debugapi/nf-debugapi-debugbreak)                                   | Causa un'eccezione del punto di interruzione nel processo corrente.                      |
| [**DebugBreakProcess**](/windows/desktop/api/WinBase/nf-winbase-debugbreakprocess)                     | Causa un'eccezione del punto di interruzione nel processo specificato.                    |
| [**DebugSetProcessKillOnExit**](/windows/desktop/api/WinBase/nf-winbase-debugsetprocesskillonexit)     | Imposta l'azione da eseguire alla chiusura del thread chiamante.                      |
| [**Errore irreversibile**](/windows/desktop/api/WinBase/nf-winbase-fatalexit)                                     | Trasferisce il controllo di esecuzione al debugger.                                        |
| [**FlushInstructionCache**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-flushinstructioncache)             | Scarica la cache delle istruzioni per il processo specificato.                            |
| [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext)                       | Recupera il contesto del thread specificato.                                      |
| [**GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-getthreadselectorentry)           | Recupera una voce della tabella dei descrittori per il selettore e il thread specificati.           |
| [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent)                     | Determina se il processo chiamante è in fase di debug da un debugger in modalità utente.   |
| [**Outputdebugstring**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)                     | Invia una stringa al debugger per la visualizzazione.                                         |
| [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory)                     | Legge i dati da un'area di memoria in un processo specificato.                           |
| [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)                       | Imposta il contesto per il thread specificato.                                          |
| [**WaitForDebugEvent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent)                     | Attende che si verifichi un evento di debug in un processo in fase di debug.                   |
| [**Wow64GetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadcontext)             | Recupera il contesto del thread WOW64 specificato.                                |
| [**Wow64GetThreadSelectorEntry**](/windows/desktop/api/WinBase/nf-winbase-wow64getthreadselectorentry) | Recupera una voce della tabella dei descrittori per il selettore e il thread WOW64 specificati.     |
| [**Wow64SetThreadContext**](/windows/desktop/api/WinBase/nf-winbase-wow64setthreadcontext)             | Imposta il contesto del thread WOW64 specificato.                                     |
| [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory)                   | Scrive i dati in un'area di memoria in un processo specificato.                            |



 

 

 
