---
description: Una DLL può facoltativamente specificare una funzione del punto di ingresso.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Funzione Entry-Point della libreria Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bff557bfa2aa792b420e8fe1856bbe0726921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753775"
---
# <a name="dynamic-link-library-entry-point-function"></a>Funzione Entry-Point della libreria Dynamic-Link

Una DLL può facoltativamente specificare una funzione del punto di ingresso. Se presente, il sistema chiama la funzione del punto di ingresso ogni volta che un processo o un thread carica o Scarica la DLL. Può essere utilizzato per eseguire semplici attività di inizializzazione e pulizia. Ad esempio, è possibile configurare l'archiviazione locale di thread quando viene creato un nuovo thread e pulirla quando il thread viene terminato.

Se si collega la DLL con la libreria di runtime del linguaggio C, è possibile che fornisca una funzione del punto di ingresso per l'utente e consenta di fornire una funzione di inizializzazione separata. Per ulteriori informazioni, consultare la documentazione per la libreria di Runtime.

Se si specifica un punto di ingresso personalizzato, vedere la funzione [**DllMain**](dllmain.md) . Il nome **DllMain** è un segnaposto per una funzione definita dall'utente. È necessario specificare il nome effettivo usato quando si compila la DLL. Per ulteriori informazioni, vedere la documentazione inclusa con gli strumenti di sviluppo.

## <a name="calling-the-entry-point-function"></a>Chiamata della funzione Entry-Point

Il sistema chiama la funzione del punto di ingresso quando si verifica uno degli eventi seguenti:

-   Un processo carica la DLL. Per i processi che usano il collegamento dinamico in fase di caricamento, la DLL viene caricata durante l'inizializzazione del processo. Per i processi che usano il collegamento in fase di esecuzione, la DLL viene caricata prima che [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) restituisca.
-   Un processo Scarica la DLL. La DLL viene scaricata quando il processo termina o chiama la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e il conteggio dei riferimenti diventa zero. Se il processo viene terminato come risultato della funzione [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) , il sistema non chiama la funzione del punto di ingresso della dll.
-   Un nuovo thread viene creato in un processo che ha caricato la DLL. È possibile usare la funzione [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) per disabilitare la notifica quando vengono creati i thread.
-   Un thread di un processo che ha caricato la DLL termina normalmente, non usando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Quando un processo Scarica la DLL, la funzione del punto di ingresso viene chiamata una sola volta per l'intero processo, anziché una volta per ogni thread esistente del processo. È possibile utilizzare [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) per disabilitare la notifica quando i thread vengono terminati.

Solo un thread alla volta può chiamare la funzione del punto di ingresso.

Il sistema chiama la funzione del punto di ingresso nel contesto del processo o del thread che ha causato la chiamata della funzione. Questo consente a una DLL di usare la funzione del punto di ingresso per l'allocazione della memoria nello spazio degli indirizzi virtuali del processo chiamante o per aprire gli handle accessibili al processo. La funzione del punto di ingresso può inoltre allocare memoria privata a un nuovo thread utilizzando l'archiviazione locale di thread (TLS). Per altre informazioni sull'archiviazione thread-local, vedere [archiviazione locale di thread](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Definizione della funzione Entry-Point

La funzione del punto di ingresso della DLL deve essere dichiarata con la convenzione di chiamata standard. Se il punto di ingresso della DLL non è dichiarato correttamente, la DLL non viene caricata e il sistema Visualizza un messaggio che indica che il punto di ingresso della DLL deve essere dichiarato con WINAPI.

Nel corpo della funzione è possibile gestire qualsiasi combinazione degli scenari seguenti in cui è stato chiamato il punto di ingresso della DLL:

-   Un processo carica la DLL (**\_ \_ associazione processo dll**).
-   Il processo corrente crea un nuovo thread (**\_ \_ connessione thread dll**).
-   Un thread viene chiuso normalmente (**\_ \_ scollegamento del thread dll**).
-   Un processo Scarica la DLL (**\_ \_ scollegamento del processo dll**).

La funzione del punto di ingresso deve eseguire solo attività di inizializzazione semplici. Non deve chiamare la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o una funzione che chiama queste funzioni), perché questo può creare cicli di dipendenza nell'ordine di caricamento della dll. Questo può comportare l'uso di una DLL prima che il sistema abbia eseguito il codice di inizializzazione. Analogamente, la funzione del punto di ingresso non deve chiamare la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o una funzione che chiama **FreeLibrary**) durante la terminazione del processo, perché questo può comportare l'uso di una dll dopo che il sistema ha eseguito il codice di terminazione.

Poiché è garantito il caricamento di Kernel32.dll nello spazio degli indirizzi del processo quando viene chiamata la funzione del punto di ingresso, la chiamata di funzioni in Kernel32.dll non comporta l'utilizzo della DLL prima dell'esecuzione del codice di inizializzazione. La funzione del punto di ingresso può quindi creare [oggetti di sincronizzazione](/windows/desktop/Sync/synchronization-objects) , ad esempio sezioni critiche e mutex, e usare TLS, perché queste funzioni si trovano in Kernel32.dll. Non è sicuro chiamare le funzioni del registro di sistema, ad esempio perché si trovano in Advapi32.dll.

La chiamata di altre funzioni può causare problemi difficili da diagnosticare. Ad esempio, la chiamata a user, Shell e funzioni COM può causare errori di violazione dell'accesso, perché alcune funzioni nelle DLL chiamano [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare altri componenti di sistema. Viceversa, la chiamata di tali funzioni durante la terminazione può causare errori di violazione di accesso perché il componente corrispondente potrebbe essere già stato scaricato o non inizializzato.

Nell'esempio seguente viene illustrato come strutturare la funzione del punto di ingresso della DLL.

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a>Valore restituito della funzione Entry-Point

Quando viene chiamata una funzione del punto di ingresso della DLL a causa del caricamento di un processo, la funzione restituisce **true** per indicare l'esito positivo. Per i processi che usano il collegamento in fase di caricamento, un valore restituito di **false** causa l'esito negativo dell'inizializzazione del processo e il processo viene terminato. Per i processi che usano il collegamento di run-time, un valore restituito di FALSE fa sì che la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) restituisca **null**, indicando un errore. Il sistema chiama immediatamente la funzione del punto di ingresso con **il \_ processo dll \_ scollegato** e Scarica la dll. Il valore restituito della funzione del punto di ingresso viene ignorato quando la funzione viene chiamata per qualsiasi altro motivo.

 

 
