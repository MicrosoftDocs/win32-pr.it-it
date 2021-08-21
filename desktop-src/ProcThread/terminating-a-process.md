---
description: "La terminazione di un processo ha i risultati seguenti: Tutti i thread rimanenti nel processo sono contrassegnati per la terminazione. Tutte le risorse allocate dal processo vengono liberate. Tutti gli oggetti del kernel vengono chiusi. Il codice del processo viene rimosso dalla memoria. Il codice di uscita del processo è impostato. L'oggetto processo viene segnalato."
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Terminazione di un processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d1a97b2b7342b67eaab72cae244b188df4cfeafbf2875d3bd62136ab6139748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081301"
---
# <a name="terminating-a-process"></a>Terminazione di un processo

La terminazione di un processo ha i risultati seguenti:

-   Tutti i thread rimanenti nel processo sono contrassegnati per la terminazione.
-   Tutte le risorse allocate dal processo vengono liberate.
-   Tutti gli oggetti del kernel vengono chiusi.
-   Il codice del processo viene rimosso dalla memoria.
-   Il codice di uscita del processo è impostato.
-   L'oggetto processo viene segnalato.

Mentre gli handle aperti per gli oggetti del kernel vengono chiusi automaticamente al termine di un processo, gli oggetti stessi esistono fino alla chiusura di tutti gli handle aperti. Di conseguenza, un oggetto rimarrà valido dopo che un processo che lo usa terminerà se un altro processo dispone di un handle aperto.

La [**funzione GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) restituisce lo stato di terminazione di un processo. Durante l'esecuzione di un processo, lo stato di terminazione è ANCORA \_ ATTIVO. Quando un processo termina, lo stato di terminazione cambia da STILL \_ ACTIVE al codice di uscita del processo.

Quando un processo termina, lo stato dell'oggetto processo viene segnalato, rilasciando tutti i thread che erano in attesa dell'interruzione del processo. Per altre informazioni sulla sincronizzazione, vedere [Sincronizzazione dell'esecuzione di più thread.](synchronizing-execution-of-multiple-threads.md)

Quando il sistema termina un processo, non termina i processi figlio creati dal processo. La terminazione di un processo non genera notifiche per le procedure \_ hook WH CBT.

Usare la [**funzione SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) per specificare determinati aspetti della terminazione del processo all'arresto del sistema, ad esempio quando un processo deve terminare rispetto agli altri processi del sistema.

## <a name="how-processes-are-terminated"></a>Modalità di terminazione dei processi

Un processo viene eseguito fino a quando non si verifica uno degli eventi seguenti:

-   Qualsiasi thread del processo chiama la [**funzione ExitProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) Si noti che alcune implementazioni della libreria di runtime C (CRT) chiamano **ExitProcess** se il thread primario del processo restituisce .
-   L'ultimo thread del processo termina.
-   Qualsiasi thread chiama la [**funzione TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) con un handle per il processo.
-   Per i processi della [console,](/windows/console/console-control-handlers) il gestore di controllo della console predefinito chiama [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) quando la console riceve un segnale CTRL+C o CTRL+BREAK.
-   L'utente arresta il sistema o si disconnette.

Non terminare un processo a meno che i thread non siano in stati noti. Se un thread è in attesa su un oggetto kernel, non verrà terminato fino al completamento dell'attesa. Ciò può causare l'arresto dell'applicazione.

Il thread primario può evitare di terminare altri thread indirizzandoli a chiamare [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) prima di terminare il processo . Per altre informazioni, vedere [Terminazione di un thread](terminating-a-thread.md). Il thread primario può comunque chiamare [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) in un secondo momento per assicurarsi che tutti i thread siano terminati.

Il codice di uscita per un processo è il valore specificato nella chiamata a [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) o [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess)oppure il valore restituito dalla funzione main o [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) del processo. Se un processo viene terminato a causa di un'eccezione irreversibile, il codice di uscita è il valore dell'eccezione che ha causato la terminazione. Inoltre, questo valore viene usato come codice di uscita per tutti i thread in esecuzione quando si è verificata l'eccezione.

Se un processo viene terminato da [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), il sistema chiama la funzione del punto di ingresso di ogni DLL collegata con un valore che indica che il processo si sta scollegando dalla DLL. Le DLL non vengono notificate quando un processo viene terminato da [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Per altre informazioni sulle DLL, vedere [Librerie a collegamento dinamico](../dlls/dynamic-link-libraries.md).

Se un processo viene terminato da [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), tutti i thread del processo vengono terminati immediatamente senza possibilità di eseguire codice aggiuntivo. Ciò significa che il thread non esegue codice nei blocchi del gestore di terminazione. Inoltre, nessuna DLL collegata viene notificata che il processo è in corso di scollegamento. Se è necessario che un processo termini un altro processo, i passaggi seguenti offrono una soluzione migliore:

-   Fare in modo che entrambi i processi chiamino la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per creare un messaggio privato.
-   Un processo può terminare l'altro processo trasmettendo un messaggio privato usando la [**funzione BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) come indicato di seguito:

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

L'esecuzione delle [**funzioni ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)e [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) viene serializzata all'interno di uno spazio indirizzi. Si applicano le restrizioni seguenti:

-   Durante le routine di avvio del processo e di inizializzazione della DLL, è possibile creare nuovi thread, ma non iniziano l'esecuzione fino al completamento dell'inizializzazione della DLL per il processo.
-   Un solo thread alla volta può essere in una routine di inizializzazione o disconnessione della DLL.
-   La [**funzione ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) non restituisce finché non sono presenti thread nelle routine di inizializzazione o disconnessione della DLL.

 

 
