---
description: Il codice di controllo esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: Codice di controllo SIO_QUERY_RSS_PROCESSOR_INFO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966673"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="21e7c-103">Codice di controllo SIO_QUERY_RSS_PROCESSOR_INFO</span><span class="sxs-lookup"><span data-stu-id="21e7c-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="21e7c-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21e7c-104">Description</span></span>

<span data-ttu-id="21e7c-105">Il codice di controllo delle **\_ \_ \_ \_ informazioni del processore RSS della query sio** esegue una query sull'associazione tra un socket e un core del processore RSS e un nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="21e7c-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="21e7c-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="21e7c-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="21e7c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21e7c-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="21e7c-108">s</span><span class="sxs-lookup"><span data-stu-id="21e7c-108">s</span></span>

<span data-ttu-id="21e7c-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="21e7c-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="21e7c-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="21e7c-110">dwIoControlCode</span></span>

<span data-ttu-id="21e7c-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-111">The control code for the operation.</span></span>
<span data-ttu-id="21e7c-112">Usare **le \_ \_ informazioni sul \_ processore \_ RSS della query sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="21e7c-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="21e7c-113">lpvInBuffer</span></span>

<span data-ttu-id="21e7c-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="21e7c-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="21e7c-115">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="21e7c-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="21e7c-116">cbInBuffer</span></span>

<span data-ttu-id="21e7c-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="21e7c-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="21e7c-118">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="21e7c-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="21e7c-119">lpvOutBuffer</span></span>

<span data-ttu-id="21e7c-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="21e7c-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="21e7c-121">Questo parametro deve puntare a una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="21e7c-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="21e7c-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="21e7c-122">cbOutBuffer</span></span>

<span data-ttu-id="21e7c-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="21e7c-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="21e7c-124">Questo parametro deve essere almeno pari alla dimensione di una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="21e7c-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="21e7c-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="21e7c-125">lpcbBytesReturned</span></span>

<span data-ttu-id="21e7c-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="21e7c-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="21e7c-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore *DWORD* pari a zero.</span><span class="sxs-lookup"><span data-stu-id="21e7c-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="21e7c-128">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="21e7c-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="21e7c-129">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="21e7c-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="21e7c-130">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="21e7c-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="21e7c-131">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="21e7c-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="21e7c-132">lpvOverlapped</span></span>

<span data-ttu-id="21e7c-133">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="21e7c-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="21e7c-134">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="21e7c-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="21e7c-135">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="21e7c-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="21e7c-136">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="21e7c-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="21e7c-137">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="21e7c-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="21e7c-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="21e7c-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="21e7c-139">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="21e7c-139">lpCompletionRoutine</span></span>

<span data-ttu-id="21e7c-140">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="21e7c-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="21e7c-141">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="21e7c-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="21e7c-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="21e7c-142">lpThreadId</span></span>

<span data-ttu-id="21e7c-143">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="21e7c-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="21e7c-144">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="21e7c-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="21e7c-145">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="21e7c-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="21e7c-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="21e7c-146">lpErrno</span></span>

<span data-ttu-id="21e7c-147">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="21e7c-147">A pointer to the error code.</span></span>

<span data-ttu-id="21e7c-148">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="21e7c-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="21e7c-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21e7c-149">Return value</span></span>

<span data-ttu-id="21e7c-150">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="21e7c-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="21e7c-151">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="21e7c-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="21e7c-152">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="21e7c-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="21e7c-153">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="21e7c-153">Error code</span></span> | <span data-ttu-id="21e7c-154">Significato</span><span class="sxs-lookup"><span data-stu-id="21e7c-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="21e7c-155">**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="21e7c-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="21e7c-156">L'area dati passata a una chiamata di sistema è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="21e7c-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="21e7c-157">Questo errore viene restituito se il buffer a cui punta il parametro *lpvOutBuffer* con una dimensione del buffer passata nel parametro *cbOutBuffer* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="21e7c-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="21e7c-158">La dimensione del buffer richiesta verrà restituita nel parametro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="21e7c-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="21e7c-159">Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di una struttura [**di \_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="21e7c-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="21e7c-160">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="21e7c-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="21e7c-161">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="21e7c-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="21e7c-162">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="21e7c-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="21e7c-163">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** .</span><span class="sxs-lookup"><span data-stu-id="21e7c-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="21e7c-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="21e7c-164">**WSAEFAULT**</span></span> | <span data-ttu-id="21e7c-165">Il parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="21e7c-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="21e7c-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="21e7c-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="21e7c-167">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="21e7c-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="21e7c-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="21e7c-168">**WSAEINTR**</span></span> | <span data-ttu-id="21e7c-169">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="21e7c-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="21e7c-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="21e7c-170">**WSAEINVAL**</span></span> | <span data-ttu-id="21e7c-171">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="21e7c-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="21e7c-172">Questo errore viene restituito se il parametro *cbOutBuffer* è minore della dimensione di una struttura [**di \_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) .</span><span class="sxs-lookup"><span data-stu-id="21e7c-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="21e7c-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="21e7c-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="21e7c-174">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="21e7c-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="21e7c-175">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="21e7c-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="21e7c-176">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="21e7c-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="21e7c-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="21e7c-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="21e7c-178">Il socket *s* non è connesso.</span><span class="sxs-lookup"><span data-stu-id="21e7c-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="21e7c-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="21e7c-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="21e7c-180">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="21e7c-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="21e7c-181">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="21e7c-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="21e7c-182">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="21e7c-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="21e7c-183">Questo errore viene restituito se le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** non sono supportate dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="21e7c-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="21e7c-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="21e7c-184">Remarks</span></span>

<span data-ttu-id="21e7c-185">Le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** sono supportate in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="21e7c-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="21e7c-186">Le **\_ informazioni sul \_ \_ processore RSS \_ della query sio** vengono usate per determinare l'associazione tra un socket e un core del processore RSS e un nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="21e7c-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="21e7c-187">Questo IOCTL restituisce una struttura di [**\_ \_ affinità del processore di socket**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) che contiene il [**\_ numero del processore**](/windows/desktop/api/winnt/ns-winnt-processor_number) e l'ID del nodo NUMA.</span><span class="sxs-lookup"><span data-stu-id="21e7c-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="21e7c-188">La struttura [**del \_ numero di processore**](/windows/desktop/api/winnt/ns-winnt-processor_number) restituito contiene un numero di gruppo e un numero di processore relativo all'interno del gruppo.</span><span class="sxs-lookup"><span data-stu-id="21e7c-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="21e7c-189">Se il socket è un socket UDP, è necessario che il socket sia connesso per il corretto funzionamento del comando IOCTL per le **\_ \_ \_ \_ informazioni sul processore RSS della query sio** .</span><span class="sxs-lookup"><span data-stu-id="21e7c-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="21e7c-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21e7c-190">See also</span></span>

[<span data-ttu-id="21e7c-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="21e7c-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="21e7c-192">**presa**</span><span class="sxs-lookup"><span data-stu-id="21e7c-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="21e7c-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="21e7c-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="21e7c-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="21e7c-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="21e7c-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="21e7c-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="21e7c-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="21e7c-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="21e7c-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="21e7c-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="21e7c-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="21e7c-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="21e7c-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="21e7c-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
