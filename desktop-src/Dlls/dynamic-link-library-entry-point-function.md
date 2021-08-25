---
description: Una DLL può specificare facoltativamente una funzione del punto di ingresso.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: funzione Dynamic-Link Library Entry-Point
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6289f705a11dad58eca8b047ba469ee07320dedef762024cbfa04046a0677f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815839"
---
# <a name="dynamic-link-library-entry-point-function"></a>funzione Dynamic-Link Library Entry-Point

Una DLL può specificare facoltativamente una funzione del punto di ingresso. Se presente, il sistema chiama la funzione del punto di ingresso ogni volta che un processo o un thread carica o scarica la DLL. Può essere usato per eseguire attività di inizializzazione e pulizia semplici. Ad esempio, può configurare l'archiviazione locale dei thread quando viene creato un nuovo thread e pulirlo quando il thread viene terminato.

Se si collega la DLL alla libreria di runtime C, può fornire una funzione del punto di ingresso e consentire di fornire una funzione di inizializzazione separata. Per altre informazioni, vedere la documentazione della libreria di runtime.

Se si fornisce un punto di ingresso personalizzato, vedere la [**funzione DllMain.**](dllmain.md) Il nome **DllMain** è un segnaposto per una funzione definita dall'utente. È necessario specificare il nome effettivo utilizzato quando si compila la DLL. Per altre informazioni, vedere la documentazione inclusa con gli strumenti di sviluppo.

## <a name="calling-the-entry-point-function"></a>Chiamata della funzione Entry-Point

Il sistema chiama la funzione del punto di ingresso ogni volta che si verifica uno degli eventi seguenti:

-   Un processo carica la DLL. Per i processi che usano il collegamento dinamico in fase di caricamento, la DLL viene caricata durante l'inizializzazione del processo. Per i processi che usano il collegamento in fase di esecuzione, la DLL viene caricata prima che venga restituito [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
-   Un processo scarica la DLL. La DLL viene scaricata quando il processo termina o chiama la [**funzione FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e il conteggio dei riferimenti diventa zero. Se il processo termina come risultato della funzione [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateThread,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) il sistema non chiama la funzione del punto di ingresso DLL.
-   Viene creato un nuovo thread in un processo che ha caricato la DLL. È possibile usare la [**funzione DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) per disabilitare la notifica quando vengono creati thread.
-   Un thread di un processo che ha caricato la DLL termina normalmente, non usando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) o [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Quando un processo scarica la DLL, la funzione del punto di ingresso viene chiamata una sola volta per l'intero processo, anziché una volta per ogni thread esistente del processo. È possibile usare [**DisableThreadLibraryCalls per**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) disabilitare la notifica quando i thread vengono terminati.

Solo un thread alla volta può chiamare la funzione del punto di ingresso.

Il sistema chiama la funzione del punto di ingresso nel contesto del processo o del thread che ha causato la chiamata della funzione. In questo modo una DLL può usare la funzione del punto di ingresso per allocare memoria nello spazio degli indirizzi virtuali del processo chiamante o per aprire handle accessibili al processo. La funzione del punto di ingresso può anche allocare memoria privata a un nuovo thread usando l'archiviazione locale di thread (TLS). Per altre informazioni sull'archiviazione locale dei thread, vedere [Thread Local Archiviazione](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Entry-Point di funzione

La funzione del punto di ingresso dll deve essere dichiarata con la convenzione di chiamata standard. Se il punto di ingresso DLL non è dichiarato correttamente, la DLL non viene caricata e il sistema visualizza un messaggio che indica che il punto di ingresso DLL deve essere dichiarato con WINAPI.

Nel corpo della funzione è possibile gestire qualsiasi combinazione degli scenari seguenti in cui è stato chiamato il punto di ingresso DLL:

-   Un processo carica la DLL (**DLL \_ PROCESS \_ ATTACH**).
-   Il processo corrente crea un nuovo thread (**DLL \_ THREAD \_ ATTACH**).
-   Un thread viene chiuso normalmente (**DLL \_ THREAD \_ DETACH**).
-   Un processo scarica la DLL (**DLL \_ PROCESS \_ DETACH**).

La funzione del punto di ingresso deve eseguire solo attività di inizializzazione semplici. Non deve chiamare la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o una funzione che chiama queste funzioni), perché potrebbe creare cicli di dipendenza nell'ordine di caricamento della DLL. Ciò può comportare l'uso di una DLL prima che il sistema abbia eseguito il codice di inizializzazione. Analogamente, la funzione del punto di ingresso non deve chiamare la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o una funzione che chiama **FreeLibrary**) durante la terminazione del processo, perché ciò può comportare l'uso di una DLL dopo che il sistema ha eseguito il codice di terminazione.

Poiché Kernel32.dll è garantito che venga caricato nello spazio degli indirizzi del processo quando viene chiamata la funzione del punto di ingresso, la chiamata di funzioni in Kernel32.dll non comporta l'uso della DLL prima dell'esecuzione del codice di inizializzazione. Pertanto, la funzione del [](/windows/desktop/Sync/synchronization-objects) punto di ingresso può creare oggetti di sincronizzazione, ad esempio sezioni critiche e mutex, e usare TLS, perché queste funzioni si trovano in Kernel32.dll. Non è sicuro chiamare le funzioni del Registro di sistema, ad esempio, perché si trovano in Advapi32.dll.

La chiamata di altre funzioni può causare problemi difficili da diagnosticare. Ad esempio, la chiamata alle funzioni User, Shell e COM può causare errori di violazione di accesso, perché alcune funzioni nelle DLL chiamano [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare altri componenti di sistema. Al contrario, la chiamata di tali funzioni durante la terminazione può causare errori di violazione di accesso perché il componente corrispondente potrebbe essere già stato scaricato o non inizializzato.

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

## <a name="entry-point-function-return-value"></a>Entry-Point valore restituito della funzione

Quando viene chiamata una funzione del punto di ingresso dll perché un processo è in fase di caricamento, la funzione restituisce **TRUE** per indicare l'esito positivo. Per i processi che usano il collegamento in fase di caricamento, il valore restituito **FALSE** causa l'esito negativo dell'inizializzazione del processo e il processo viene terminato. Per i processi che usano il collegamento in fase di esecuzione, un valore restituito FALSE fa sì che la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) restituirà **NULL,** a indicare un errore. Il sistema chiama immediatamente la funzione del punto di ingresso con **DLL \_ PROCESS \_ DETACH** e scarica la DLL. Il valore restituito della funzione del punto di ingresso viene ignorato quando la funzione viene chiamata per qualsiasi altro motivo.

 

 
