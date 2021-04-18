---
description: Un punto di ingresso facoltativo in una libreria a collegamento dinamico (DLL). Quando il sistema avvia o termina un processo o un thread, chiama la funzione del punto di ingresso per ogni DLL caricata usando il primo thread del processo.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: Punto di ingresso DllMain (Process. h)
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313387"
---
# <a name="dllmain-entry-point"></a>Punto di ingresso DllMain

Un punto di ingresso facoltativo in una libreria a collegamento dinamico (DLL). Quando il sistema avvia o termina un processo o un thread, chiama la funzione del punto di ingresso per ogni DLL caricata usando il primo thread del processo. Il sistema chiama anche la funzione del punto di ingresso per una DLL quando viene caricata o scaricata usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="example"></a>Esempio

```cpp
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

Questo è un esempio dalla [libreria a collegamento dinamico Entry-Point funzione](dynamic-link-library-entry-point-function.md).


> [!WARNING]
> Esistono limiti significativi sulle operazioni che è possibile eseguire in modo sicuro in un punto di ingresso della DLL. Vedere [le procedure consigliate generali](dynamic-link-library-best-practices.md) per specifiche API di Windows che non sono sicure per la chiamata a DllMain. Se è necessario solo l'inizializzazione più semplice, eseguire questa operazione in una funzione di inizializzazione per la DLL. È possibile richiedere alle applicazioni di chiamare la funzione di inizializzazione dopo l'esecuzione di DllMain e prima di chiamare qualsiasi altra funzione nella DLL.

 

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hinstDLL* \[ in\]
</dt> <dd>

Handle per il modulo DLL. Il valore è l'indirizzo di base della DLL. Il **HINSTANCE** di una dll è uguale a quello di **hmodule** della dll, pertanto *hinstDLL* può essere usato nelle chiamate a funzioni che richiedono un handle del modulo.

</dd> <dt>

*fdwReason* \[ in\]
</dt> <dd>

Codice motivo che indica il motivo per cui viene chiamata la funzione del punto di ingresso della DLL. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                                | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**Dll \_ di \_Connessione processo**</dt> <dt>1</dt> </dl> | La DLL viene caricata nello spazio degli indirizzi virtuali del processo corrente in seguito all'avvio del processo o a seguito di una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Le dll possono utilizzare questa opportunità per inizializzare tutti i dati dell'istanza o per utilizzare la funzione [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) per allocare un indice TLS (thread local storage).<br/> Il parametro *lpReserved* indica se la dll viene caricata in modo statico o dinamico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Dll \_ di \_Scollegamento processo**</dt> <dt>0</dt> </dl> | La DLL viene scaricata dallo spazio degli indirizzi virtuali del processo chiamante perché è stata caricata senza esito positivo o il conteggio dei riferimenti ha raggiunto zero (i processi sono stati interrotti o sono stati chiamati [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) una volta per ogni chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).<br/> Il parametro *lpReserved* indica se la dll viene scaricata in seguito a una chiamata [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , a un errore di caricamento o alla chiusura del processo.<br/> La DLL può usare questa opportunità per chiamare la funzione [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) per liberare tutti gli indici TLS allocati usando [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) e per liberare i dati locali dei thread.<br/> Si noti che il thread che riceve la notifica di **\_ \_ scollegamento del processo dll** non è necessariamente lo stesso thread che ha ricevuto la notifica di **\_ \_ collegamento del processo dll** .<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**Dll \_ di \_Connessione thread**</dt> <dt>2</dt> </dl>    | Il processo corrente sta creando un nuovo thread. In tal caso, il sistema chiama la funzione del punto di ingresso di tutte le dll attualmente associate al processo. La chiamata viene effettuata nel contesto del nuovo thread. Le dll possono usare questa opportunità per inizializzare uno slot TLS per il thread. Un thread che chiama la funzione del punto di ingresso della dll con **\_ \_ connessione del processo dll** non chiama la funzione del punto di ingresso della dll con la **connessione al \_ thread \_ della dll**. <br/> Si noti che la funzione del punto di ingresso di una DLL viene chiamata con questo valore solo dai thread creati dopo che il processo ha caricato la DLL. Quando una DLL viene caricata usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), i thread esistenti non chiamano la funzione del punto di ingresso della dll appena caricata.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**Dll \_ di \_Scollegamento thread**</dt> <dt>3</dt> </dl>    | Un thread è in uscita pulito. Se la DLL ha archiviato un puntatore alla memoria allocata in uno slot TLS, deve usare questa opportunità per liberare la memoria. Il sistema chiama la funzione del punto di ingresso di tutte le dll attualmente caricate con questo valore. La chiamata viene effettuata nel contesto del thread in uscita.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[ in\]
</dt> <dd>

Se *fdwReason* è **un \_ processo \_ dll**, *lpvReserved* è **null** per i carichi dinamici e non null per i caricamenti statici.

Se *fdwReason* è **dll \_ processo di \_ disconnessione**, *LpvReserved* è **null** se è stato chiamato [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) o il caricamento della dll non è riuscito e non **null** se il processo viene terminato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Quando il sistema chiama la funzione **DllMain** con il valore di **\_ \_ associazione processo dll** , la funzione restituisce **true** se ha esito positivo o **false** se l'inizializzazione ha esito negativo. Se il valore restituito è **false** quando **DllMain** viene chiamato perché il processo utilizza la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , **LoadLibrary** restituisce null. Il sistema chiama immediatamente la funzione del punto di ingresso con **il \_ processo dll \_ scollegato** e Scarica la dll. Se il valore restituito è **false** quando **DllMain** viene chiamato durante l'inizializzazione del processo, il processo viene terminato con un errore. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Quando il sistema chiama la funzione **DllMain** con qualsiasi valore diverso da **dll \_ processo di \_ associazione**, il valore restituito viene ignorato.

## <a name="remarks"></a>Commenti

**DllMain** è un segnaposto per il nome della funzione definita dalla libreria. È necessario specificare il nome effettivo usato quando si compila la DLL. Per ulteriori informazioni, vedere la documentazione inclusa con gli strumenti di sviluppo.

Durante l'avvio del processo iniziale o dopo una chiamata a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), il sistema esegue l'analisi dell'elenco delle DLL caricate per il processo. Per ogni DLL che non è già stata chiamata con il valore di **\_ \_ associazione processo dll** , il sistema chiama la funzione del punto di ingresso della dll. Questa chiamata viene eseguita nel contesto del thread che ha causato la modifica dello spazio degli indirizzi del processo, ad esempio il thread principale del processo o il thread che ha chiamato **LoadLibrary**. L'accesso al punto di ingresso viene serializzato dal sistema in base a un intero processo. I thread in *DllMain* contengono il blocco del caricatore, quindi non è possibile caricare o inizializzare in modo dinamico altre dll.

Se la funzione del punto di ingresso della DLL restituisce FALSE dopo una notifica di **\_ \_ collegamento del processo dll** , riceve una notifica di **\_ \_ scollegamento del processo dll** e la dll viene scaricata immediatamente. Tuttavia, se il codice di **\_ \_ collegamento del processo dll** genera un'eccezione, la funzione del punto di ingresso non riceverà la notifica di **\_ \_ scollegamento del processo dll** .

Esistono casi in cui la funzione del punto di ingresso viene chiamata per un thread di terminazione anche se la funzione del punto di ingresso non è mai stata chiamata con la **\_ \_ connessione del thread dll** per il thread:

-   Il thread era il thread iniziale del processo, quindi il sistema ha chiamato la funzione del punto di ingresso con il valore di **\_ \_ associazione del processo dll** .
-   Il thread era già in esecuzione quando è stata eseguita una chiamata alla funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , quindi il sistema non ha mai chiamato la funzione del punto di ingresso.

Quando una DLL viene scaricata da un processo in seguito a un caricamento non riuscito della DLL, alla chiusura del processo o a una chiamata a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), il sistema non chiama la funzione del punto di ingresso della dll con il valore di **\_ \_ scollegamento del thread dll** per i singoli thread del processo. Alla DLL viene inviata solo una notifica di **\_ \_ scollegamento del processo dll** . Le dll possono avere questa opportunità per pulire tutte le risorse per tutti i thread noti alla DLL.

Quando si gestisce lo **\_ \_ scollegamento del processo DLL**, una dll deve liberare risorse, ad esempio la memoria heap, solo se la dll viene scaricata dinamicamente (il parametro *lpReserved* è **null**). Se il processo viene terminato (il parametro *lpvReserved* è diverso da **null**), tutti i thread nel processo eccetto il thread corrente sono già stati interrotti o sono stati terminati in modo esplicito da una chiamata alla funzione [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) , che potrebbe lasciare alcune risorse di processo, ad esempio heap in uno stato incoerente. In questo caso non è sicuro che la DLL ripulisca le risorse. Al contrario, la DLL deve consentire al sistema operativo di recuperare la memoria.

Se si termina un processo chiamando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) o [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), le DLL di tale processo non ricevono notifiche di **\_ \_ scollegamento dei processi dll** . Se si termina un thread chiamando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), le DLL di tale thread non ricevono notifiche di **\_ \_ scollegamento dei thread dll** .

La funzione del punto di ingresso deve eseguire solo attività di inizializzazione o terminazione semplici. Non deve chiamare la funzione [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (o una funzione che chiama queste funzioni), perché questo può creare cicli di dipendenza nell'ordine di caricamento della dll. Questo può comportare l'uso di una DLL prima che il sistema abbia eseguito il codice di inizializzazione. Analogamente, la funzione del punto di ingresso non deve chiamare la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (o una funzione che chiama **FreeLibrary**) durante la terminazione del processo, perché questo può comportare l'uso di una dll dopo che il sistema ha eseguito il codice di terminazione.

Poiché è garantito il caricamento di Kernel32.dll nello spazio degli indirizzi del processo quando viene chiamata la funzione del punto di ingresso, la chiamata di funzioni in Kernel32.dll non comporta l'utilizzo della DLL prima dell'esecuzione del codice di inizializzazione. La funzione del punto di ingresso può quindi chiamare funzioni in Kernel32.dll che non caricano altre dll. Ad esempio, *DllMain* può creare [oggetti di sincronizzazione](/windows/desktop/Sync/synchronization-objects) come sezioni critiche e mutex e usare TLS. Sfortunatamente, non è disponibile un elenco completo di funzioni sicure in Kernel32.dll.

La chiamata di funzioni che richiedono dll diverse da Kernel32.dll può causare problemi difficili da diagnosticare. Ad esempio, la chiamata a user, Shell e funzioni COM può causare errori di violazione dell'accesso, perché alcune funzioni caricano altri componenti di sistema. Viceversa, la chiamata di funzioni come queste durante la terminazione può causare errori di violazione di accesso perché il componente corrispondente potrebbe essere già stato scaricato o non inizializzato.

Poiché le notifiche DLL vengono serializzate, le funzioni del punto di ingresso non devono tentare di comunicare con altri thread o processi. Di conseguenza, possono verificarsi deadlock.

Per informazioni sulle procedure consigliate per la scrittura di una DLL, vedere https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Se la DLL è collegata alla libreria di runtime C (CRT), il punto di ingresso fornito da CRT chiama i costruttori e i distruttori per gli oggetti C++ globali e statici. Pertanto, queste restrizioni per *DllMain* si applicano anche a costruttori e distruttori e a qualsiasi codice chiamato da essi.

Si consiglia di chiamare [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) quando si riceve il **\_ \_ collegamento al processo dll**, a meno che la dll non sia collegata alla libreria di runtime C statica (CRT).


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Elabora. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzione Entry-Point libreria a collegamento dinamico](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[Funzioni della libreria a collegamento dinamico](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
