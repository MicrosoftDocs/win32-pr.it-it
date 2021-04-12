---
title: Contesti asincroni
description: Panoramica dei contesti asincroni e dell'intestazione SSPI asincrona.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347296"
---
# <a name="asynchronous-contexts"></a><span data-ttu-id="f12ef-103">Contesti asincroni</span><span class="sxs-lookup"><span data-stu-id="f12ef-103">Asynchronous Contexts</span></span>

<span data-ttu-id="f12ef-104">I contesti di sicurezza SSPI asincroni consentono ai chiamanti di procedere senza bloccare e ricevere notifiche al termine della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f12ef-104">Asynchronous SSPI security contexts allow callers to proceed without blocking and receive notifications once the call completes.</span></span> <span data-ttu-id="f12ef-105">I contesti asincroni sono attualmente supportati solo per i client e i server TLS in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="f12ef-105">Asynchronous contexts are currently only supported for kernel-mode TLS clients and servers.</span></span> <span data-ttu-id="f12ef-106">Le seguenti funzioni SSPI asincrone operano su contesti di sicurezza asincroni:</span><span class="sxs-lookup"><span data-stu-id="f12ef-106">The following asynchronous SSPI functions operate on asynchronous security contexts:</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="f12ef-107">Tipi di gestione del contesto asincrono</span><span class="sxs-lookup"><span data-stu-id="f12ef-107">Async context management types</span></span>

| <span data-ttu-id="f12ef-108">Nome oggetto</span><span class="sxs-lookup"><span data-stu-id="f12ef-108">Object Name</span></span> | <span data-ttu-id="f12ef-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12ef-109">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="f12ef-110">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="f12ef-110">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="f12ef-111">Callback utilizzato per notificare il completamento di una chiamata SSPI asincrona.</span><span class="sxs-lookup"><span data-stu-id="f12ef-111">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="f12ef-112">Funzioni di gestione del contesto asincrono</span><span class="sxs-lookup"><span data-stu-id="f12ef-112">Async context management functions</span></span>

| <span data-ttu-id="f12ef-113">Nome API</span><span class="sxs-lookup"><span data-stu-id="f12ef-113">API Name</span></span> | <span data-ttu-id="f12ef-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12ef-114">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="f12ef-115">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="f12ef-115">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="f12ef-116">Crea un'istanza di SspiAsyncContext che viene utilizzata per tenere traccia della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="f12ef-116">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="f12ef-117">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="f12ef-117">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="f12ef-118">Contrassegna un contesto asincrono per il riutilizzo.</span><span class="sxs-lookup"><span data-stu-id="f12ef-118">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="f12ef-119">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="f12ef-119">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="f12ef-120">Registra un callback che riceve una notifica sul completamento della chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="f12ef-120">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="f12ef-121">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="f12ef-121">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="f12ef-122">Determina se un contesto asincrono specificato richiede una notifica al completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f12ef-122">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="f12ef-123">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="f12ef-123">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="f12ef-124">Ottiene lo stato corrente di una chiamata asincrona associata al contesto fornito.</span><span class="sxs-lookup"><span data-stu-id="f12ef-124">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="f12ef-125">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="f12ef-125">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="f12ef-126">Libera un contesto creato nella chiamata alla funzione SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="f12ef-126">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="f12ef-127">Funzioni SSPI asincrone</span><span class="sxs-lookup"><span data-stu-id="f12ef-127">Async SSPI functions</span></span>

<span data-ttu-id="f12ef-128">Le funzioni seguenti accettano un contesto asincrono, oltre a tutti gli stessi parametri della relativa controparte sincrona.</span><span class="sxs-lookup"><span data-stu-id="f12ef-128">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="f12ef-129">Nome API</span><span class="sxs-lookup"><span data-stu-id="f12ef-129">API Name</span></span> | <span data-ttu-id="f12ef-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f12ef-130">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="f12ef-131">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="f12ef-131">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="f12ef-132">Acquisisce in modo asincrono un handle per le credenziali preesistenti di un'entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f12ef-132">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="f12ef-133">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="f12ef-133">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="f12ef-134">Consente al componente server di un'applicazione di trasporto di stabilire in modo asincrono un contesto di sicurezza tra il server e un client remoto.</span><span class="sxs-lookup"><span data-stu-id="f12ef-134">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="f12ef-135">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="f12ef-135">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="f12ef-136">Inizializza un contesto di sicurezza asincrono.</span><span class="sxs-lookup"><span data-stu-id="f12ef-136">Initializes an async security context.</span></span> |
| [<span data-ttu-id="f12ef-137">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="f12ef-137">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="f12ef-138">Elimina le strutture di dati locali associate al contesto di sicurezza specificato avviato da una chiamata precedente alla funzione SspiInitializeSecurityContextAsync o SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="f12ef-138">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="f12ef-139">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="f12ef-139">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="f12ef-140">Libera un handle di credenziale.</span><span class="sxs-lookup"><span data-stu-id="f12ef-140">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="f12ef-141">Esempio di API</span><span class="sxs-lookup"><span data-stu-id="f12ef-141">API Sample</span></span>

<span data-ttu-id="f12ef-142">Un tipico flusso di chiamate funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="f12ef-142">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="f12ef-143">Creare il contesto SspiAsyncContext per tenere traccia della chiamata mediante [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="f12ef-143">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="f12ef-144">Registrare un [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) per il contesto</span><span class="sxs-lookup"><span data-stu-id="f12ef-144">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="f12ef-145">Eseguire la chiamata asincrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="f12ef-145">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="f12ef-146">Su callback recuperare il risultato usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="f12ef-146">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="f12ef-147">Eliminare SspiAsyncContext usando [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="f12ef-147">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="f12ef-148">Se si riutilizza il contesto con [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), tornare al passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="f12ef-148">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="f12ef-149">Nell'esempio seguente viene illustrata una chiamata di SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="f12ef-149">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="f12ef-150">L'esempio attende il completamento della chiamata e recupera il risultato.</span><span class="sxs-lookup"><span data-stu-id="f12ef-150">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="f12ef-151">In un handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync vengono chiamati più volte fino a quando non viene restituito SEC_E_OK.</span><span class="sxs-lookup"><span data-stu-id="f12ef-151">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="f12ef-152">SspiReinitAsyncContext è stato fornito per semplificare l'utilizzo e per semplificare le prestazioni in questo caso.</span><span class="sxs-lookup"><span data-stu-id="f12ef-152">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="f12ef-153">Le asserzioni vengono usate per evidenziare ciò che ci si aspetterebbe in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f12ef-153">Asserts are used to highlight what we would expect in the case of success.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="f12ef-154">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f12ef-154">See Also</span></span>

[<span data-ttu-id="f12ef-155">intestazione SSPI. h</span><span class="sxs-lookup"><span data-stu-id="f12ef-155">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="f12ef-156">Funzioni SSPI</span><span class="sxs-lookup"><span data-stu-id="f12ef-156">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="f12ef-157">Strutture SSPI</span><span class="sxs-lookup"><span data-stu-id="f12ef-157">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


