---
description: Il codice di controllo Recupera il contesto di reindirizzamento per un record di reindirizzamento utilizzato da un servizio di reindirizzamento della piattaforma filtro Windows.
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: Codice di controllo SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129127"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="53519-103">Codice di controllo SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="53519-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="53519-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53519-104">Description</span></span>

<span data-ttu-id="53519-105">Il codice di controllo del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** Recupera il contesto di reindirizzamento per un record di reindirizzamento usato da un servizio di reindirizzamento della piattaforma filtro Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="53519-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="53519-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="53519-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure 
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="53519-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="53519-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="53519-108">s</span><span class="sxs-lookup"><span data-stu-id="53519-108">s</span></span>

<span data-ttu-id="53519-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="53519-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="53519-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="53519-110">dwIoControlCode</span></span>

<span data-ttu-id="53519-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-111">The control code for the operation.</span></span>
<span data-ttu-id="53519-112">Usare **il \_ \_ contesto di \_ \_ Reindirizzamento della \_ connessione WFP per la query sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="53519-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="53519-113">lpvInBuffer</span></span>

<span data-ttu-id="53519-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="53519-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="53519-115">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="53519-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="53519-116">cbInBuffer</span></span>

<span data-ttu-id="53519-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="53519-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="53519-118">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="53519-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="53519-119">lpvOutBuffer</span></span>

<span data-ttu-id="53519-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="53519-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="53519-121">Questo parametro deve puntare a un tipo di dati **ULONG** se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="53519-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="53519-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="53519-122">cbOutBuffer</span></span>

<span data-ttu-id="53519-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="53519-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="53519-124">Questo parametro deve essere almeno la dimensione di un tipo di dati **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="53519-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="53519-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="53519-125">lpcbBytesReturned</span></span>

<span data-ttu-id="53519-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="53519-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="53519-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="53519-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="53519-128">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="53519-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="53519-129">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="53519-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="53519-130">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="53519-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="53519-131">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="53519-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="53519-132">lpvOverlapped</span></span>

<span data-ttu-id="53519-133">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="53519-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="53519-134">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="53519-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="53519-135">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="53519-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="53519-136">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="53519-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="53519-137">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53519-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="53519-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="53519-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="53519-139">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="53519-139">lpCompletionRoutine</span></span>

<span data-ttu-id="53519-140">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="53519-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="53519-141">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="53519-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="53519-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="53519-142">lpThreadId</span></span>

<span data-ttu-id="53519-143">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="53519-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="53519-144">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="53519-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="53519-145">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="53519-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="53519-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="53519-146">lpErrno</span></span>

<span data-ttu-id="53519-147">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="53519-147">A pointer to the error code.</span></span>

<span data-ttu-id="53519-148">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="53519-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="53519-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53519-149">Return value</span></span>

<span data-ttu-id="53519-150">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="53519-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="53519-151">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="53519-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="53519-152">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="53519-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="53519-153">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="53519-153">Error code</span></span> | <span data-ttu-id="53519-154">Significato</span><span class="sxs-lookup"><span data-stu-id="53519-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="53519-155">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="53519-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="53519-156">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="53519-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="53519-157">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="53519-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="53519-158">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL SIO_FLUSH.</span><span class="sxs-lookup"><span data-stu-id="53519-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="53519-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="53519-159">**WSAEFAULT**</span></span> | <span data-ttu-id="53519-160">Il parametro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="53519-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="53519-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="53519-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="53519-162">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="53519-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="53519-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="53519-163">**WSAEINTR**</span></span> | <span data-ttu-id="53519-164">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="53519-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="53519-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="53519-165">**WSAEINVAL**</span></span> | <span data-ttu-id="53519-166">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="53519-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="53519-167">Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di un tipo di dati **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="53519-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="53519-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="53519-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="53519-169">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53519-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="53519-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="53519-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="53519-171">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="53519-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="53519-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="53519-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="53519-173">Il socket *s* non è connesso.</span><span class="sxs-lookup"><span data-stu-id="53519-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="53519-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="53519-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="53519-175">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="53519-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="53519-176">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="53519-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="53519-177">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="53519-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="53519-178">Questo errore viene restituito se il **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione** per la query di sio non è supportato dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="53519-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="53519-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="53519-179">Remarks</span></span>

<span data-ttu-id="53519-180">Il **contesto IOCTL di \_ \_ \_ \_ Reindirizzamento della \_ connessione di query sio** è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53519-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="53519-181">Il WFP consente di accedere al percorso di elaborazione dei pacchetti TCP/IP, in cui è possibile esaminare o modificare i pacchetti in uscita e in ingresso prima di consentire l'ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="53519-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="53519-182">Toccando il percorso di elaborazione TCP/IP, i fornitori di software indipendenti (ISV) possono creare più facilmente firewall, software antivirus, software di diagnostica e altri tipi di applicazioni e servizi.</span><span class="sxs-lookup"><span data-stu-id="53519-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="53519-183">PAM fornisce componenti in modalità utente e kernel, in modo che gli ISV di terze parti possano partecipare alle decisioni di filtro che avvengono a diversi livelli nello stack di protocolli TCP/IP e in tutto il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53519-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="53519-184">La funzionalità di reindirizzamento della connessione WFP consente a un driver del kernel di callout di WFP di reindirizzare una connessione localmente a un processo in modalità utente, di eseguire l'ispezione dei contenuti in modalità utente e inoltrare il contenuto ispezionato utilizzando una connessione diversa alla destinazione originale.</span><span class="sxs-lookup"><span data-stu-id="53519-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="53519-185">La **\_ query sio \_ \_ contesto di \_ Reindirizzamento \_ della connessione WFP** e molti altri IOCTL correlati sono componenti in modalità utente utilizzati per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.</span><span class="sxs-lookup"><span data-stu-id="53519-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="53519-186">Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.</span><span class="sxs-lookup"><span data-stu-id="53519-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="53519-187">Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.</span><span class="sxs-lookup"><span data-stu-id="53519-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="53519-188">Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="53519-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="53519-189">L'IOCTL del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione della query sio** viene usato per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.</span><span class="sxs-lookup"><span data-stu-id="53519-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="53519-190">Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.</span><span class="sxs-lookup"><span data-stu-id="53519-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="53519-191">Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.</span><span class="sxs-lookup"><span data-stu-id="53519-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="53519-192">Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="53519-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="53519-193">L'IOCTL del **\_ contesto di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** viene usato per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate.</span><span class="sxs-lookup"><span data-stu-id="53519-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="53519-194">Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="53519-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="53519-195">I **\_ record di \_ \_ \_ Reindirizzamento \_ della connessione per la query sio** vengono usati da un servizio di reindirizzamento basato su WFP per recuperare il record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata (ad esempio, il socket connesso per un socket TCP o un socket UDP) reindirizzato al relativo callout in modalità kernel registrato in **ale Connect livelli di \_ \_ Reindirizzamento** in un driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="53519-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="53519-196">Il **\_ \_ \_ \_ \_ contesto** di reindirizzamento della connessione per la query sio viene usato da un servizio di reindirizzamento basato su WFP per recuperare il contesto di reindirizzamento per un record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata (ad esempio, il socket connesso per un socket TCP o un socket UDP) reindirizzato a esso dal callout complementare registrato a **ALE_CONNECT_REDIRECT** livelli.</span><span class="sxs-lookup"><span data-stu-id="53519-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="53519-197">Il contesto di reindirizzamento è facoltativo e viene usato se lo stato del reindirizzamento corrente di una connessione è che la connessione è stata reindirizzata dal servizio di reindirizzamento chiamante oppure la connessione è stata reindirizzata in precedenza dal servizio di reindirizzamento chiamante, ma in seguito reindirizzato da un servizio di reindirizzamento diverso.</span><span class="sxs-lookup"><span data-stu-id="53519-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="53519-198">Il servizio di reindirizzamento trasferisce il record di reindirizzamento recuperato al socket TCP usato per eseguire il proxy del contenuto originale usando il **set di dati di \_ Reindirizzamento della connessione sio set \_ WFP \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="53519-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="53519-199">Poiché il contesto di reindirizzamento di WFP è un BLOB di dati a lunghezza variabile impostato dal servizio di reindirizzamento, il chiamante può fornire un buffer di output di grandi dimensioni (ad esempio, un buffer 1K a cui punta il parametro *lpvOutBuffer* ) oppure può passare come dimensione del buffer di output nel parametro *cbOutBuffer* di 0 per eseguire una query sulle dimensioni del buffer necessarie per memorizzare il BLOB restituito.</span><span class="sxs-lookup"><span data-stu-id="53519-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="53519-200">Se la dimensione del buffer di output non è sufficiente per contenere i dati, le funzioni [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituiranno un **errore di \_ \_ buffer insufficiente** e le dimensioni del buffer richieste verranno restituite nel valore a cui punta il parametro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="53519-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="53519-201">L'applicazione che chiama **la \_ query sio \_ WF \ P_CONNECTION \_ reindirizza i \_ record** IOCTL non deve comprendere il BLOB contenente i record di reindirizzamento recuperati.</span><span class="sxs-lookup"><span data-stu-id="53519-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="53519-202">Si tratta di un BLOB opaco di dati che l'applicazione deve recuperare e passare nuovamente al nuovo socket.</span><span class="sxs-lookup"><span data-stu-id="53519-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="53519-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53519-203">See also</span></span>

[<span data-ttu-id="53519-204">**Opzioni di IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="53519-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="53519-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="53519-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="53519-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="53519-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="53519-207">**presa**</span><span class="sxs-lookup"><span data-stu-id="53519-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="53519-208">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="53519-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="53519-209">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="53519-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="53519-210">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="53519-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="53519-211">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="53519-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="53519-212">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="53519-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="53519-213">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="53519-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
