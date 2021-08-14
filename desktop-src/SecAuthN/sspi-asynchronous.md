---
title: SSPI asincrono
description: Panoramica dell'intestazione SSPI asincrona.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e2fe4e6cc8358ec39c402bccdf8562d613ac952547687142cb3553d04c8f0ce6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917166"
---
# <a name="asynchronous-sspi"></a>SSPI asincrono

L'intestazione SSPI asincrona include funzioni che supportano oggetti contesto asincrono, consentendo ai chiamanti di stabilire contesti di sicurezza tra client server e remoti contemporaneamente tramite un ciclo di vita delle chiamate SSPI asincrone.

## <a name="async-context-management-types"></a>Tipi di gestione del contesto asincrono

| Nome oggetto | Descrizione |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Callback utilizzato per notificare il completamento di una chiamata SSPI asincrona. |


## <a name="async-context-management-functions"></a>Funzioni di gestione del contesto asincrono

| Nome API | Descrizione |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Crea un'istanza di SspiAsyncContext che viene usata per tenere traccia della chiamata asincrona. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Contrassegna un contesto asincrono per il riutilizzo. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registra un callback che viene notificato al completamento della chiamata asincrona. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Determina se un contesto asincrono specificato richiede una notifica al completamento della chiamata. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Ottiene lo stato corrente di una chiamata asincrona associata al contesto fornito.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libera un contesto creato nella chiamata alla funzione SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Funzioni SSPI asincrone

Le funzioni seguenti accettano un contesto asincrono oltre a tutti gli stessi parametri della controparte sincrona.

| Nome API | Descrizione |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Acquisisce in modo asincrono un handle per le credenziali preesistenti di un'entità di sicurezza. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Consente al componente server di un'applicazione di trasporto di stabilire in modo asincrono un contesto di sicurezza tra il server e un client remoto. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Inizializza un contesto di sicurezza asincrono. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Elimina le strutture di dati locali associate al contesto di sicurezza specificato avviato da una chiamata precedente alla funzione SspiInitializeSecurityContextAsync o alla funzione SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libera un handle di credenziali. |

## <a name="api-sample"></a>Esempio di API

Un flusso di chiamata tipico funziona come segue:
1) Creare un contesto SspiAsyncContext per tenere traccia della chiamata [usando SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registrare [un oggetto SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) per il contesto
3) Effettuare la chiamata asincrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) Al callback recuperare il risultato usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Eliminare SspiAsyncContext usando [SspiDeleteSecurityContextAsync.](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) Se si riutilizza il contesto [con SspiReinitAsyncContext,](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)tornare al passaggio 2.

L'esempio seguente illustra una chiamata di SspiAcceptSecurityContextAsync. L'esempio attende il completamento della chiamata e recupera il risultato.

In un handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync vengono chiamati più volte fino a SEC_E_OK restituito. SspiReinitAsyncContext è stato fornito per semplificare l'uso e per facilitare le prestazioni in questo caso.

Le asserzioni vengono usate per evidenziare ciò che ci si aspetterebbe in caso di esito positivo.

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a>Vedere anche

[Intestazione sspi.h](/windows/win32/api/sspi/)

[Funzioni SSPI](/windows/win32/api/sspi/#functions)

[Strutture SSPI](/windows/win32/api/sspi/#structures)


