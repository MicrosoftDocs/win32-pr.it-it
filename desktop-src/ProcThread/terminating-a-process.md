---
description: "Il termine di un processo presenta i risultati seguenti: gli eventuali thread rimanenti nel processo sono contrassegnati per la terminazione. Tutte le risorse allocate dal processo vengono liberate. Tutti gli oggetti kernel sono chiusi. Il codice del processo viene rimosso dalla memoria. Il codice di uscita del processo è impostato. L'oggetto processo viene segnalato."
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Terminazione di un processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311954"
---
# <a name="terminating-a-process"></a>Terminazione di un processo

Il termine di un processo presenta i risultati seguenti:

-   Tutti i thread rimanenti del processo sono contrassegnati per la terminazione.
-   Tutte le risorse allocate dal processo vengono liberate.
-   Tutti gli oggetti kernel sono chiusi.
-   Il codice del processo viene rimosso dalla memoria.
-   Il codice di uscita del processo è impostato.
-   L'oggetto processo viene segnalato.

Mentre gli handle aperti agli oggetti kernel vengono chiusi automaticamente al termine di un processo, gli oggetti stessi sono presenti finché tutti gli handle aperti non vengono chiusi. Pertanto, un oggetto rimarrà valido dopo che un processo che lo usa termina se un altro processo ha un handle aperto.

La funzione [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) restituisce lo stato di terminazione di un processo. Mentre un processo è in esecuzione, il relativo stato di terminazione è ancora \_ attivo. Al termine di un processo, lo stato di chiusura passa da ancora \_ attivo al codice di uscita del processo.

Quando un processo termina, lo stato dell'oggetto processo viene segnalato, che rilascia tutti i thread in attesa dell'interruzione del processo. Per ulteriori informazioni sulla sincronizzazione, vedere [sincronizzazione dell'esecuzione di più thread](synchronizing-execution-of-multiple-threads.md).

Quando il sistema termina un processo, non termina i processi figlio creati dal processo. Se si termina un processo, non vengono generate notifiche per \_ le procedure hook di WH CBT.

Utilizzare la funzione [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) per specificare determinati aspetti della terminazione del processo al momento dell'arresto del sistema, ad esempio quando un processo deve terminare rispetto agli altri processi nel sistema.

## <a name="how-processes-are-terminated"></a>Modalità di terminazione dei processi

Un processo viene eseguito fino a quando non si verifica uno degli eventi seguenti:

-   Qualsiasi thread del processo chiama la funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) . Si noti che alcune implementazioni della libreria di runtime C (CRT) chiamano **ExitProcess** se il thread principale del processo restituisce.
-   L'ultimo thread del processo viene terminato.
-   Qualsiasi thread chiama la funzione [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un handle per il processo.
-   Per i processi della console, il [gestore di controllo della console](/windows/console/console-control-handlers) predefinito chiama [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) quando la console riceve un segnale CTRL + C o CTRL + INTERR.
-   L'utente arresta il sistema o si disconnette.

Non terminare un processo a meno che i relativi thread non siano in stati noti. Se un thread è in attesa di un oggetto kernel, non verrà terminato fino al completamento dell'attesa. Questa operazione può causare l'interruzione della risposta dell'applicazione.

Il thread primario può evitare di terminare altri thread indirizzando questi alla chiamata di [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) prima di causare la terminazione del processo (per altre informazioni, vedere [terminazione di un thread](terminating-a-thread.md)). Il thread primario può comunque chiamare [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) in un secondo momento per assicurarsi che tutti i thread vengano terminati.

Il codice di uscita per un processo è il valore specificato nella chiamata a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)oppure il valore restituito dalla funzione Main o [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) del processo. Se un processo viene terminato a causa di un'eccezione irreversibile, il codice di uscita corrisponde al valore dell'eccezione che ha causato la chiusura. Inoltre, questo valore viene usato come codice di uscita per tutti i thread in esecuzione quando si è verificata l'eccezione.

Se un processo viene terminato da [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), il sistema chiama la funzione del punto di ingresso di ogni DLL collegata con un valore che indica che il processo viene scollegato dalla dll. Le dll non ricevono notifiche quando un processo viene terminato da [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Per altre informazioni sulle dll, vedere [librerie a collegamento dinamico](../dlls/dynamic-link-libraries.md).

Se un processo viene terminato da [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), tutti i thread del processo vengono interrotti immediatamente senza alcuna possibilità di eseguire codice aggiuntivo. Ciò significa che il thread non esegue codice nei blocchi del gestore di terminazione. Inoltre, nessuna DLL collegata riceve una notifica che indica che il processo è scollegato. Se è necessario che un processo termini un altro processo, i passaggi seguenti offrono una soluzione migliore:

-   In entrambi i processi viene chiamata la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per creare un messaggio privato.
-   Un processo può terminare l'altro processo trasmettendo un messaggio privato usando la funzione [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) come segue:

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   Il processo che riceve il messaggio privato chiama [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) per terminare l'esecuzione.

L'esecuzione delle funzioni [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)e [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) viene serializzata in uno spazio di indirizzi. Si applicano le restrizioni seguenti:

-   Durante le routine di avvio del processo e di inizializzazione della DLL, è possibile creare nuovi thread, ma non avviare l'esecuzione fino a quando non viene completata l'inizializzazione della DLL per il processo.
-   Solo un thread alla volta può trovarsi in una routine di inizializzazione o scollegamento della DLL.
-   La funzione [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) non restituisce alcun risultato finché non sono presenti thread nelle routine di inizializzazione o scollegamento della dll.

 

 
