---
description: Il codice di controllo esegue una query sulle impostazioni di trasporto in un socket.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: Codice di controllo SIO_QUERY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880449"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="75d44-103">Codice di controllo SIO_QUERY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="75d44-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="75d44-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75d44-104">Description</span></span>

<span data-ttu-id="75d44-105">Il codice di controllo dell' **\_ \_ \_ impostazione del trasporto query sio** esegue una query sulle impostazioni di trasporto in un socket.</span><span class="sxs-lookup"><span data-stu-id="75d44-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="75d44-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="75d44-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="75d44-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="75d44-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="75d44-108">s</span><span class="sxs-lookup"><span data-stu-id="75d44-108">s</span></span>

<span data-ttu-id="75d44-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="75d44-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="75d44-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="75d44-110">dwIoControlCode</span></span>

<span data-ttu-id="75d44-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="75d44-111">The control code for the operation.</span></span>
<span data-ttu-id="75d44-112">Usare **l' \_ \_ \_ impostazione del trasporto di query sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="75d44-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="75d44-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="75d44-113">lpvInBuffer</span></span>

<span data-ttu-id="75d44-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="75d44-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="75d44-115">Questo parametro contiene un puntatore a una struttura in cui il primo membro della struttura è una struttura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) che determina l'impostazione di trasporto sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="75d44-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="75d44-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="75d44-116">cbInBuffer</span></span>

<span data-ttu-id="75d44-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="75d44-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="75d44-118">Questo parametro dipende dall'impostazione di trasporto sottoposta a query.</span><span class="sxs-lookup"><span data-stu-id="75d44-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="75d44-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="75d44-119">lpvOutBuffer</span></span>

<span data-ttu-id="75d44-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="75d44-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="75d44-121">Questo parametro dipende dall'impostazione di trasporto sottoposta a query se i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**.</span><span class="sxs-lookup"><span data-stu-id="75d44-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="75d44-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="75d44-122">cbOutBuffer</span></span>

<span data-ttu-id="75d44-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="75d44-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="75d44-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="75d44-124">lpcbBytesReturned</span></span>

<span data-ttu-id="75d44-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="75d44-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="75d44-126">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="75d44-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="75d44-127">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="75d44-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="75d44-128">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="75d44-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="75d44-129">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="75d44-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="75d44-130">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="75d44-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="75d44-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="75d44-131">lpvOverlapped</span></span>

<span data-ttu-id="75d44-132">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="75d44-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="75d44-133">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="75d44-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="75d44-134">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="75d44-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="75d44-135">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="75d44-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="75d44-136">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="75d44-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="75d44-137">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="75d44-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="75d44-138">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="75d44-138">lpCompletionRoutine</span></span>

<span data-ttu-id="75d44-139">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="75d44-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="75d44-140">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="75d44-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="75d44-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="75d44-141">lpThreadId</span></span>

<span data-ttu-id="75d44-142">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="75d44-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="75d44-143">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="75d44-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="75d44-144">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="75d44-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="75d44-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="75d44-145">lpErrno</span></span>

<span data-ttu-id="75d44-146">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="75d44-146">A pointer to the error code.</span></span>

<span data-ttu-id="75d44-147">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="75d44-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="75d44-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="75d44-148">Return value</span></span>

<span data-ttu-id="75d44-149">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="75d44-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="75d44-150">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="75d44-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="75d44-151">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="75d44-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="75d44-152">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="75d44-152">Error code</span></span> | <span data-ttu-id="75d44-153">Significato</span><span class="sxs-lookup"><span data-stu-id="75d44-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="75d44-154">**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="75d44-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="75d44-155">L'area dati passata a una chiamata di sistema è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="75d44-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="75d44-156">Questo errore viene restituito se il buffer a cui punta il parametro *lpvOutBuffer* con una dimensione del buffer passata nel parametro *cbOutBuffer* è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="75d44-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="75d44-157">La dimensione del buffer richiesta verrà restituita nel parametro *lpcbBytesReturned* .</span><span class="sxs-lookup"><span data-stu-id="75d44-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="75d44-158">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="75d44-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="75d44-159">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="75d44-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="75d44-160">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="75d44-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="75d44-161">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** .</span><span class="sxs-lookup"><span data-stu-id="75d44-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="75d44-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="75d44-162">**WSAEFAULT**</span></span> | <span data-ttu-id="75d44-163">Il parametro *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="75d44-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="75d44-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="75d44-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="75d44-165">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="75d44-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="75d44-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="75d44-166">**WSAEINTR**</span></span> | <span data-ttu-id="75d44-167">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="75d44-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="75d44-168">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="75d44-168">**WSAEINVAL**</span></span> | <span data-ttu-id="75d44-169">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="75d44-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="75d44-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="75d44-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="75d44-171">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="75d44-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="75d44-172">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="75d44-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="75d44-173">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="75d44-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="75d44-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="75d44-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="75d44-175">Il Socket s non è connesso.</span><span class="sxs-lookup"><span data-stu-id="75d44-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="75d44-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="75d44-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="75d44-177">Il descrittore s non è un socket.</span><span class="sxs-lookup"><span data-stu-id="75d44-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="75d44-178">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="75d44-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="75d44-179">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="75d44-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="75d44-180">Questo errore viene restituito se l' **\_ impostazione del \_ trasporto \_ di query sio** non è supportata dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="75d44-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="75d44-181">Commenti</span><span class="sxs-lookup"><span data-stu-id="75d44-181">Remarks</span></span>

<span data-ttu-id="75d44-182">L' **\_ impostazione del \_ trasporto \_ di query sio** è supportata in windows 8 e Windows Server 2012 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="75d44-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="75d44-183">L' **\_ impostazione del \_ trasporto \_ di query sio** è un IOCTL generico usato per eseguire query sulle impostazioni di trasporto in un socket.</span><span class="sxs-lookup"><span data-stu-id="75d44-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="75d44-184">L'impostazione di trasporto sottoposta a query è basata sul [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="75d44-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="75d44-185">L'unica impostazione del trasporto attualmente definita è per la funzionalità di **\_ notifica in tempo \_ \_ reale** in un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="75d44-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="75d44-186">Se il [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro *lpvInBuffer* ha il membro GUID impostato sulla **funzionalità di \_ \_ notifica in \_ tempo reale**, si tratta di una richiesta per eseguire una query sulle impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75d44-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="75d44-187">Il parametro *lpvInBuffer* deve puntare a una struttura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) .</span><span class="sxs-lookup"><span data-stu-id="75d44-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="75d44-188">Il parametro *lpvOutBuffer* deve puntare a una struttura di output di **impostazione della \_ \_ notifica in \_ \_ tempo reale** .</span><span class="sxs-lookup"><span data-stu-id="75d44-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="75d44-189">Questa impostazione del trasporto si applica solo ai socket TCP.</span><span class="sxs-lookup"><span data-stu-id="75d44-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="75d44-190">Questa impostazione di trasporto consente a WinInet o ai servizi di rete simili di eseguire query su un socket TCP specifico per determinare lo stato di [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) .</span><span class="sxs-lookup"><span data-stu-id="75d44-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="75d44-191">Un'applicazione Windows Store non chiamerà direttamente questo IOCTL.</span><span class="sxs-lookup"><span data-stu-id="75d44-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="75d44-192">Se la chiamata a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** ha esito positivo, questo IOCTL restituisce una struttura di **output dell'impostazione di \_ notifica in tempo \_ \_ \_ reale** con lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="75d44-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="75d44-193">L' **\_ impostazione del \_ trasporto \_ di query sio** consente a WinInet o ai servizi di rete simili di eseguire una query per lo stato delle impostazioni di trasporto per un socket TCP specificato per determinare se [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) è abilitato sul socket.</span><span class="sxs-lookup"><span data-stu-id="75d44-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="75d44-194">Un'applicazione Windows Store non chiamerà direttamente questo IOCTL.</span><span class="sxs-lookup"><span data-stu-id="75d44-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="75d44-195">Questo IOCTL si applica solo ai socket TCP.</span><span class="sxs-lookup"><span data-stu-id="75d44-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="75d44-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75d44-196">See also</span></span>

[<span data-ttu-id="75d44-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="75d44-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="75d44-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="75d44-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="75d44-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="75d44-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="75d44-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="75d44-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="75d44-201">presa</span><span class="sxs-lookup"><span data-stu-id="75d44-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="75d44-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="75d44-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="75d44-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="75d44-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="75d44-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="75d44-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="75d44-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="75d44-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="75d44-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="75d44-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="75d44-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="75d44-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
