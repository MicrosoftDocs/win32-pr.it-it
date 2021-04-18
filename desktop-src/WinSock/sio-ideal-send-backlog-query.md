---
description: Il codice di controllo Recupera il valore del backlog di invio ideale per la connessione sottostante.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: Codice di controllo SIO_IDEAL_SEND_BACKLOG_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315781"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="6e301-103">Codice di controllo SIO_IDEAL_SEND_BACKLOG_QUERY</span><span class="sxs-lookup"><span data-stu-id="6e301-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="6e301-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e301-104">Description</span></span>

<span data-ttu-id="6e301-105">Il codice di controllo della **\_ query del \_ \_ backlog \_ di invio ideale per sio** Recupera il valore di backlog di invio ideale per la connessione sottostante.</span><span class="sxs-lookup"><span data-stu-id="6e301-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="6e301-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e301-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="6e301-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e301-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="6e301-108">s</span><span class="sxs-lookup"><span data-stu-id="6e301-108">s</span></span>

<span data-ttu-id="6e301-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="6e301-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="6e301-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="6e301-110">dwIoControlCode</span></span>

<span data-ttu-id="6e301-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-111">The control code for the operation.</span></span>
<span data-ttu-id="6e301-112">Usare **la \_ \_ query del \_ backlog \_ di invio ideale di sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="6e301-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="6e301-113">lpvInBuffer</span></span>

<span data-ttu-id="6e301-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="6e301-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="6e301-115">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="6e301-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="6e301-116">cbInBuffer</span></span>

<span data-ttu-id="6e301-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="6e301-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="6e301-118">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="6e301-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="6e301-119">lpvOutBuffer</span></span>

<span data-ttu-id="6e301-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="6e301-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="6e301-121">Questo parametro deve puntare a un tipo di dati **ULONG** se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="6e301-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="6e301-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="6e301-122">cbOutBuffer</span></span>

<span data-ttu-id="6e301-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="6e301-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="6e301-124">Questo parametro deve essere almeno la dimensione di un tipo di dati **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="6e301-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="6e301-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="6e301-125">lpcbBytesReturned</span></span>

<span data-ttu-id="6e301-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="6e301-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="6e301-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="6e301-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="6e301-128">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="6e301-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="6e301-129">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6e301-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="6e301-130">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6e301-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="6e301-131">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="6e301-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="6e301-132">lpvOverlapped</span></span>

<span data-ttu-id="6e301-133">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="6e301-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="6e301-134">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="6e301-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="6e301-135">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="6e301-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="6e301-136">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="6e301-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="6e301-137">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6e301-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="6e301-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="6e301-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="6e301-139">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="6e301-139">lpCompletionRoutine</span></span>

<span data-ttu-id="6e301-140">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="6e301-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="6e301-141">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="6e301-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="6e301-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="6e301-142">lpThreadId</span></span>

<span data-ttu-id="6e301-143">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="6e301-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="6e301-144">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="6e301-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="6e301-145">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="6e301-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="6e301-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="6e301-146">lpErrno</span></span>

<span data-ttu-id="6e301-147">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="6e301-147">A pointer to the error code.</span></span>

<span data-ttu-id="6e301-148">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="6e301-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e301-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e301-149">Return value</span></span>

<span data-ttu-id="6e301-150">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="6e301-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="6e301-151">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="6e301-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="6e301-152">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="6e301-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="6e301-153">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="6e301-153">Error code</span></span> | <span data-ttu-id="6e301-154">Significato</span><span class="sxs-lookup"><span data-stu-id="6e301-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="6e301-155">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="6e301-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="6e301-156">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="6e301-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="6e301-157">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="6e301-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="6e301-158">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** .</span><span class="sxs-lookup"><span data-stu-id="6e301-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="6e301-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6e301-159">**WSAEFAULT**</span></span> | <span data-ttu-id="6e301-160">Il parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="6e301-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="6e301-161">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="6e301-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="6e301-162">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="6e301-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="6e301-163">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="6e301-163">**WSAEINTR**</span></span> | <span data-ttu-id="6e301-164">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="6e301-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="6e301-165">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="6e301-165">**WSAEINVAL**</span></span> | <span data-ttu-id="6e301-166">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="6e301-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="6e301-167">Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di un tipo di dati **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="6e301-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="6e301-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="6e301-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="6e301-169">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6e301-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="6e301-170">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="6e301-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="6e301-171">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="6e301-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="6e301-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="6e301-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="6e301-173">Il Socket s non è connesso.</span><span class="sxs-lookup"><span data-stu-id="6e301-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="6e301-174">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="6e301-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="6e301-175">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="6e301-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="6e301-176">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="6e301-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="6e301-177">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6e301-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="6e301-178">Questo errore viene restituito se la **\_ query di \_ \_ backlog di \_ invio ideale di sio** non è supportata dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="6e301-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="6e301-179">Questo errore viene restituito anche quando viene eseguito un tentativo di usare la **\_ query di \_ \_ backlog \_ di invio ideale di sio** per un socket di datagramma.</span><span class="sxs-lookup"><span data-stu-id="6e301-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="6e301-180">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e301-180">Remarks</span></span>

<span data-ttu-id="6e301-181">La **\_ query del \_ \_ backlog di \_ invio ideale di sio** è supportata in Windows Server 2008, Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e301-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="6e301-182">Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="6e301-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="6e301-183">Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale.</span><span class="sxs-lookup"><span data-stu-id="6e301-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="6e301-184">Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).</span><span class="sxs-lookup"><span data-stu-id="6e301-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="6e301-185">Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6e301-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="6e301-186">La **\_ query del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per ricevere una notifica quando il valore di ISB cambia in modo dinamico per una connessione.</span><span class="sxs-lookup"><span data-stu-id="6e301-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="6e301-187">In Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo, la modifica del [**\_ backlog di \_ INVIO \_ del \_ backlog ideale di sio**](sio-ideal-send-backlog-change.md) e la **query del \_ \_ backlog di invio \_ \_ ideale di sio** sono supportate nei socket orientati al flusso che si trovano in uno stato connesso.</span><span class="sxs-lookup"><span data-stu-id="6e301-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="6e301-188">L'intervallo per il valore ISB per una connessione TCP può teoricamente variare da 0 a un massimo di 16 megabyte.</span><span class="sxs-lookup"><span data-stu-id="6e301-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="6e301-189">L'utilizzo tipico della [**modifica del \_ \_ backlog di \_ INVIO \_ ideale di sio**](sio-ideal-send-backlog-change.md) e della **\_ \_ \_ \_ query di backlog di invio ideale di sio** è basato sul metodo Send usato dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="6e301-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="6e301-190">Vengono illustrati due casi comuni.</span><span class="sxs-lookup"><span data-stu-id="6e301-190">Two common cases are discussed.</span></span>

<span data-ttu-id="6e301-191">Le applicazioni che eseguono una richiesta di invio bloccante o non bloccante alla volta in genere si basano sul buffer di invio interno da Winsock per ottenere una velocità effettiva decente.</span><span class="sxs-lookup"><span data-stu-id="6e301-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="6e301-192">Il limite del buffer di invio per una determinata connessione è controllato dall'opzione socket **\_ sndbuf** .</span><span class="sxs-lookup"><span data-stu-id="6e301-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="6e301-193">Per il metodo Send bloccante e non bloccante, il limite del buffer di invio determina la quantità di dati mantenuti in attesa in TCP.</span><span class="sxs-lookup"><span data-stu-id="6e301-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="6e301-194">Se il valore ISB per la connessione è superiore al limite del buffer di invio, la velocità effettiva consentita per la connessione non è ottimale.</span><span class="sxs-lookup"><span data-stu-id="6e301-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="6e301-195">Per ottenere una velocità effettiva migliore, le applicazioni possono impostare il limite del buffer di invio in base al risultato della query ISB, in quanto si verificano notifiche di modifica ISB sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="6e301-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="6e301-196">Per le applicazioni che utilizzano il metodo di invio sovrapposto con più richieste di invio in attesa, la quantità di dati mantenuti in attesa in TCP è determinata dal limite del buffer di invio in Winsock e dalla quantità totale di dati contenuti nelle richieste di invio sovrapposte in attesa.</span><span class="sxs-lookup"><span data-stu-id="6e301-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="6e301-197">In questo caso, le applicazioni devono usare il valore ISB per determinare il numero di richieste di invio in attesa da tenere e le dimensioni dei dati per ogni richiesta di invio.</span><span class="sxs-lookup"><span data-stu-id="6e301-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="6e301-198">Idealmente, l'applicazione deve provare a tenere soddisfatta l'equazione seguente:</span><span class="sxs-lookup"><span data-stu-id="6e301-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="6e301-199">Si noti che l'utilizzo delle IOCTL ISB sui socket TCP nel modo precedente può comportare un aumento dell'utilizzo della memoria in Exchange per una maggiore velocità effettiva nelle connessioni con un prodotto con ritardo della larghezza di banda elevato.</span><span class="sxs-lookup"><span data-stu-id="6e301-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="6e301-200">L'implementazione TCP in Windows limiterà i valori ISB secondo le necessità in base all'utilizzo complessivo della memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="6e301-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="6e301-201">La **\_ query di \_ \_ backlog di \_ invio ideale di sio** è consentita solo su un socket del flusso che si trova nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="6e301-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="6e301-202">In caso contrario, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** avrà esito negativo con **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="6e301-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="6e301-203">Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="6e301-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="6e301-204">Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.</span><span class="sxs-lookup"><span data-stu-id="6e301-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="6e301-205">La **\_ query del \_ \_ backlog di \_ invio ideale per sio** non può essere bloccata in modo da essere normalmente chiamata in modo sincrono con i parametri *lpOverlapped* e *il lpCompletionRoutine* impostati su **null**.</span><span class="sxs-lookup"><span data-stu-id="6e301-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="6e301-206">La **\_ query del \_ \_ backlog di \_ invio ideale di sio** può avere esito negativo con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="6e301-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="6e301-207">La connessione TCP viene normalmente disconnessa nella direzione di invio.</span><span class="sxs-lookup"><span data-stu-id="6e301-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="6e301-208">Questo problema può verificarsi in seguito a una chiamata alla funzione Shutdown con il parametro how impostato su **SD \_ Send**, una chiamata alla funzione **DisconnectEx** o una chiamata alla funzione **TransmitFile** o **TransmitPackets** con il parametro *dwFlags* impostato su **tf \_ Disconnect** o **tf \_ riuso**.</span><span class="sxs-lookup"><span data-stu-id="6e301-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="6e301-209">La connessione TCP è stata reimpostata o interrotta.</span><span class="sxs-lookup"><span data-stu-id="6e301-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="6e301-210">La richiesta viene annullata dal gestore di I/O.</span><span class="sxs-lookup"><span data-stu-id="6e301-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="6e301-211">Due funzioni wrapper inline per tali IOCTL sono definite nel file di intestazione *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="6e301-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="6e301-212">Si consiglia di usare queste funzioni inline invece di usare la modifica del [**\_ backlog di \_ INVIO \_ \_**](sio-ideal-send-backlog-change.md) e la **\_ \_ \_ \_ query** di backlog di invio ideale per Sio, direttamente.</span><span class="sxs-lookup"><span data-stu-id="6e301-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="6e301-213">La funzione wrapper inline per la [**\_ modifica del \_ \_ backlog di \_ invio ideale di sio**](sio-ideal-send-backlog-change.md) è la funzione **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="6e301-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="6e301-214">La funzione wrapper inline per la **\_ query di \_ \_ backlog di \_ invio ideale di sio** è la funzione **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="6e301-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="6e301-215">Il buffer di invio dinamico per TCP è stato aggiunto in Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6e301-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="6e301-216">Per impostazione predefinita, il buffer di invio dinamico per TCP è abilitato, a meno che un'applicazione non imposti l'opzione **\_ sndbuf** socket sul socket di flusso.</span><span class="sxs-lookup"><span data-stu-id="6e301-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="6e301-217">L'utilizzo di netsh è il metodo consigliato per eseguire query o impostare il buffer di invio dinamico per TCP.</span><span class="sxs-lookup"><span data-stu-id="6e301-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="6e301-218">Il valore corrente per il buffer di invio dinamico per TCP può essere recuperato con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="6e301-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="6e301-219">Il buffer di invio dinamico per TCP può essere disabilitato usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="6e301-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="6e301-220">Il buffer di invio dinamico per TCP può essere abilitato usando il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="6e301-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="6e301-221">Sebbene sia sconsigliato, il buffer di invio dinamico può essere disabilitato da un'applicazione impostando il valore del registro di sistema seguente su zero:</span><span class="sxs-lookup"><span data-stu-id="6e301-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="6e301-222">Quando si modifica il valore del buffer di invio dinamico utilizzando NetSh.exe o modificando il valore del registro di sistema, è necessario riavviare il computer per rendere effettive le modifiche.</span><span class="sxs-lookup"><span data-stu-id="6e301-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="6e301-223">Con il buffering di invio dinamico in Windows 7 e Windows Server 2008 R2, l'uso [**della \_ modifica del backlog di invio del \_ \_ \_ backlog ideale**](sio-ideal-send-backlog-change.md) di SIO e della **query del \_ \_ \_ backlog \_ di invio ideale di sio** è necessario solo in circostanze particolari.</span><span class="sxs-lookup"><span data-stu-id="6e301-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e301-224">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e301-224">See also</span></span>

[<span data-ttu-id="6e301-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="6e301-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="6e301-226">**presa**</span><span class="sxs-lookup"><span data-stu-id="6e301-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="6e301-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="6e301-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="6e301-228">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="6e301-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="6e301-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="6e301-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="6e301-230">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="6e301-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="6e301-231">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="6e301-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="6e301-232">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="6e301-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
