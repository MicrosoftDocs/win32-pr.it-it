---
title: SSPI asincrono
description: Panoramica dell'intestazione SSPI asincrona.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316216"
---
# <a name="asynchronous-sspi"></a><span data-ttu-id="d4c55-103">SSPI asincrono</span><span class="sxs-lookup"><span data-stu-id="d4c55-103">Asynchronous SSPI</span></span>

<span data-ttu-id="d4c55-104">L'intestazione SSPI asincrona include funzioni che supportano gli oggetti di contesto asincrono, consentendo ai chiamanti di stabilire contesti di sicurezza tra server e client remoti simultaneamente tramite un ciclo di vita delle chiamate SSPI asincrono.</span><span class="sxs-lookup"><span data-stu-id="d4c55-104">The asynchronous SSPI header includes functions that support async context objects, allowing callers to establish security contexts between server and remote clients concurrently through an async SSPI call lifecycle.</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="d4c55-105">Tipi di gestione del contesto asincrono</span><span class="sxs-lookup"><span data-stu-id="d4c55-105">Async context management types</span></span>

| <span data-ttu-id="d4c55-106">Nome oggetto</span><span class="sxs-lookup"><span data-stu-id="d4c55-106">Object Name</span></span> | <span data-ttu-id="d4c55-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c55-107">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d4c55-108">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="d4c55-108">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="d4c55-109">Callback utilizzato per notificare il completamento di una chiamata SSPI asincrona.</span><span class="sxs-lookup"><span data-stu-id="d4c55-109">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="d4c55-110">Funzioni di gestione del contesto asincrono</span><span class="sxs-lookup"><span data-stu-id="d4c55-110">Async context management functions</span></span>

| <span data-ttu-id="d4c55-111">Nome API</span><span class="sxs-lookup"><span data-stu-id="d4c55-111">API Name</span></span> | <span data-ttu-id="d4c55-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c55-112">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d4c55-113">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="d4c55-113">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="d4c55-114">Crea un'istanza di SspiAsyncContext che viene utilizzata per tenere traccia della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="d4c55-114">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="d4c55-115">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="d4c55-115">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="d4c55-116">Contrassegna un contesto asincrono per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="d4c55-116">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="d4c55-117">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="d4c55-117">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="d4c55-118">Registra un callback che riceve una notifica sul completamento della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="d4c55-118">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="d4c55-119">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="d4c55-119">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="d4c55-120">Determina se un contesto asincrono specificato richiede una notifica al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d4c55-120">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="d4c55-121">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="d4c55-121">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="d4c55-122">Ottiene lo stato corrente di una chiamata asincrona associata al contesto fornito.</span><span class="sxs-lookup"><span data-stu-id="d4c55-122">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="d4c55-123">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="d4c55-123">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="d4c55-124">Libera un contesto creato nella chiamata alla funzione SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="d4c55-124">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="d4c55-125">Funzioni SSPI asincrone</span><span class="sxs-lookup"><span data-stu-id="d4c55-125">Async SSPI functions</span></span>

<span data-ttu-id="d4c55-126">Le funzioni seguenti accettano un contesto asincrono, oltre a tutti gli stessi parametri della relativa controparte sincrona.</span><span class="sxs-lookup"><span data-stu-id="d4c55-126">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="d4c55-127">Nome API</span><span class="sxs-lookup"><span data-stu-id="d4c55-127">API Name</span></span> | <span data-ttu-id="d4c55-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c55-128">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="d4c55-129">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="d4c55-129">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="d4c55-130">Acquisisce in modo asincrono un handle per le credenziali preesistenti di un'entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d4c55-130">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="d4c55-131">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="d4c55-131">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="d4c55-132">Consente al componente server di un'applicazione di trasporto di stabilire in modo asincrono un contesto di sicurezza tra il server e un client remoto.</span><span class="sxs-lookup"><span data-stu-id="d4c55-132">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="d4c55-133">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="d4c55-133">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="d4c55-134">Inizializza un contesto di sicurezza asincrono.</span><span class="sxs-lookup"><span data-stu-id="d4c55-134">Initializes an async security context.</span></span> |
| [<span data-ttu-id="d4c55-135">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="d4c55-135">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="d4c55-136">Elimina le strutture di dati locali associate al contesto di sicurezza specificato avviato da una chiamata precedente alla funzione SspiInitializeSecurityContextAsync o SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="d4c55-136">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="d4c55-137">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="d4c55-137">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="d4c55-138">Libera un handle di credenziale.</span><span class="sxs-lookup"><span data-stu-id="d4c55-138">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="d4c55-139">Esempio di API</span><span class="sxs-lookup"><span data-stu-id="d4c55-139">API Sample</span></span>

<span data-ttu-id="d4c55-140">Un tipico flusso di chiamate funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d4c55-140">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="d4c55-141">Creare il contesto SspiAsyncContext per tenere traccia della chiamata mediante [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="d4c55-141">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="d4c55-142">Registrare un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) per il contesto</span><span class="sxs-lookup"><span data-stu-id="d4c55-142">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="d4c55-143">Eseguire la chiamata asincrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="d4c55-143">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="d4c55-144">Su callback recuperare il risultato usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="d4c55-144">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="d4c55-145">Eliminare SspiAsyncContext usando [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="d4c55-145">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="d4c55-146">Se si riutilizza il contesto con [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), tornare al passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="d4c55-146">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="d4c55-147">Nell'esempio seguente viene illustrata una chiamata di SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="d4c55-147">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="d4c55-148">L'esempio attende il completamento della chiamata e recupera il risultato.</span><span class="sxs-lookup"><span data-stu-id="d4c55-148">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="d4c55-149">In un handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync vengono chiamati più volte fino a quando non viene restituito SEC_E_OK.</span><span class="sxs-lookup"><span data-stu-id="d4c55-149">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="d4c55-150">SspiReinitAsyncContext è stato fornito per semplificare l'utilizzo e per semplificare le prestazioni in questo caso.</span><span class="sxs-lookup"><span data-stu-id="d4c55-150">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="d4c55-151">Le asserzioni vengono usate per evidenziare ciò che ci si aspetterebbe in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d4c55-151">Asserts are used to highlight what we would expect in the case of success.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d4c55-152">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d4c55-152">See Also</span></span>

[<span data-ttu-id="d4c55-153">intestazione SSPI. h</span><span class="sxs-lookup"><span data-stu-id="d4c55-153">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="d4c55-154">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="d4c55-154">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="d4c55-155">Strutture SSPI</span><span class="sxs-lookup"><span data-stu-id="d4c55-155">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


