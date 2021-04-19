---
description: Il codice di controllo rilascia una prenotazione di runtime per un blocco di porte TCP o UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: Codice di controllo SIO_RELEASE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309925"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="bc606-103">Codice di controllo SIO_RELEASE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="bc606-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="bc606-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bc606-104">Description</span></span>

<span data-ttu-id="bc606-105">Il codice di controllo della **\_ prenotazione della \_ porta \_ di rilascio sio** rilascia una prenotazione di runtime per un blocco di porte TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="bc606-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="bc606-106">La prenotazione di runtime da rilasciare deve essere stata ottenuta dal processo di emissione usando il comando IOCTL [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) .</span><span class="sxs-lookup"><span data-stu-id="bc606-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="bc606-107">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="bc606-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="bc606-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc606-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="bc606-109">s</span><span class="sxs-lookup"><span data-stu-id="bc606-109">s</span></span>

<span data-ttu-id="bc606-110">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="bc606-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="bc606-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="bc606-111">dwIoControlCode</span></span>

<span data-ttu-id="bc606-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-112">The control code for the operation.</span></span>
<span data-ttu-id="bc606-113">Usare **la \_ \_ \_ prenotazione della porta di rilascio sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="bc606-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="bc606-114">lpvInBuffer</span></span>

<span data-ttu-id="bc606-115">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="bc606-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="bc606-116">Questo parametro contiene un puntatore a una struttura di [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) con il token per la prenotazione della porta TCP o UDP da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="bc606-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="bc606-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="bc606-117">cbInBuffer</span></span>

<span data-ttu-id="bc606-118">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="bc606-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="bc606-119">Questo parametro deve essere almeno pari alla dimensione della struttura [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .</span><span class="sxs-lookup"><span data-stu-id="bc606-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="bc606-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="bc606-120">lpvOutBuffer</span></span>

<span data-ttu-id="bc606-121">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="bc606-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="bc606-122">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="bc606-123">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="bc606-123">cbOutBuffer</span></span>

<span data-ttu-id="bc606-124">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="bc606-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="bc606-125">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="bc606-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="bc606-126">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="bc606-126">lpcbBytesReturned</span></span>

<span data-ttu-id="bc606-127">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="bc606-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="bc606-128">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="bc606-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="bc606-129">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="bc606-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="bc606-130">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bc606-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="bc606-131">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bc606-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="bc606-132">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="bc606-133">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="bc606-133">lpvOverlapped</span></span>

<span data-ttu-id="bc606-134">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="bc606-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bc606-135">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="bc606-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="bc606-136">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="bc606-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="bc606-137">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="bc606-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bc606-138">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="bc606-139">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="bc606-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="bc606-140">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="bc606-140">lpCompletionRoutine</span></span>

<span data-ttu-id="bc606-141">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="bc606-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="bc606-142">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="bc606-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="bc606-143">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="bc606-143">lpThreadId</span></span>

<span data-ttu-id="bc606-144">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="bc606-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="bc606-145">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="bc606-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="bc606-146">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="bc606-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="bc606-147">lpErrno</span><span class="sxs-lookup"><span data-stu-id="bc606-147">lpErrno</span></span>

<span data-ttu-id="bc606-148">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="bc606-148">A pointer to the error code.</span></span>

<span data-ttu-id="bc606-149">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="bc606-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="bc606-150">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc606-150">Return value</span></span>

<span data-ttu-id="bc606-151">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="bc606-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="bc606-152">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="bc606-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="bc606-153">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="bc606-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="bc606-154">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="bc606-154">Error code</span></span> | <span data-ttu-id="bc606-155">Significato</span><span class="sxs-lookup"><span data-stu-id="bc606-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="bc606-156">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="bc606-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="bc606-157">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="bc606-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="bc606-158">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bc606-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="bc606-159">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="bc606-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="bc606-160">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="bc606-161">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="bc606-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="bc606-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="bc606-162">**WSAEFAULT**</span></span> | <span data-ttu-id="bc606-163">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="bc606-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="bc606-164">Questo errore viene restituito dal parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="bc606-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="bc606-165">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="bc606-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="bc606-166">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="bc606-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="bc606-167">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="bc606-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="bc606-168">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="bc606-168">**WSAEINTR**</span></span> | <span data-ttu-id="bc606-169">Un'operazione di blocco è stata interrotta da una chiamata a **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="bc606-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="bc606-170">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="bc606-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="bc606-171">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="bc606-171">**WSAEINVAL**</span></span> | <span data-ttu-id="bc606-172">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="bc606-172">An invalid argument was supplied.</span></span> <span data-ttu-id="bc606-173">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="bc606-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="bc606-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="bc606-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="bc606-175">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="bc606-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="bc606-176">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bc606-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="bc606-177">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="bc606-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="bc606-178">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="bc606-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="bc606-179">Questo errore viene restituito se il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="bc606-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="bc606-180">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="bc606-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="bc606-181">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="bc606-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="bc606-182">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bc606-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="bc606-183">Questo errore viene restituito anche se il provider di trasporto non supporta la **\_ prenotazione della \_ porta \_ di rilascio sio** .</span><span class="sxs-lookup"><span data-stu-id="bc606-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="bc606-184">Questo errore viene restituito anche quando viene eseguito un tentativo di usare l'IOCTL di **\_ prenotazione della \_ porta \_ di rilascio sio** su un socket diverso da UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="bc606-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="bc606-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc606-185">Remarks</span></span>

<span data-ttu-id="bc606-186">L'IOCTL di **\_ prenotazione della \_ porta \_ di rilascio sio** è supportato in Windows Vista e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bc606-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="bc606-187">Le applicazioni e i servizi che devono riservare le porte rientrano in due categorie.</span><span class="sxs-lookup"><span data-stu-id="bc606-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="bc606-188">La prima categoria include i componenti che richiedono una determinata porta come parte dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="bc606-189">Tali componenti preferiscono in genere specificare la porta richiesta al momento dell'installazione, ad esempio in un manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="bc606-190">La seconda categoria include i componenti che richiedono qualsiasi porta o blocco di porte disponibile in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bc606-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="bc606-191">Queste due categorie corrispondono a richieste di prenotazione di porta specifiche e con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="bc606-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="bc606-192">Richieste di prenotazione specifiche possono essere permanenti o Runtime, mentre le richieste di prenotazione di porta con caratteri jolly sono supportate solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bc606-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="bc606-193">Il [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL viene usato per richiedere una prenotazione di runtime per un blocco di porte TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="bc606-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="bc606-194">Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni vengano utilizzate dal processo sul cui socket è stata concessa la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="bc606-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="bc606-195">Le prenotazioni di porte di runtime durano solo fino a quando la durata del socket in cui è stato chiamato il comando IOCTL [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) .</span><span class="sxs-lookup"><span data-stu-id="bc606-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="bc606-196">Al contrario, le prenotazioni di porte permanenti create utilizzando la funzione [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.</span><span class="sxs-lookup"><span data-stu-id="bc606-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="bc606-197">Per rilasciare una prenotazione di runtime per un blocco di porte TCP o UDP, viene usata la **\_ prenotazione della \_ porta \_ di rilascio sio** .</span><span class="sxs-lookup"><span data-stu-id="bc606-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="bc606-198">Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**, il socket in questa funzione verrà considerato come un socket non sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="bc606-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="bc606-199">Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.</span><span class="sxs-lookup"><span data-stu-id="bc606-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="bc606-200">Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.</span><span class="sxs-lookup"><span data-stu-id="bc606-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="bc606-201">Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="bc606-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="bc606-202">Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="bc606-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="bc606-203">Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.</span><span class="sxs-lookup"><span data-stu-id="bc606-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="bc606-204">La **\_ prenotazione della \_ porta \_ di rilascio sio** può avere esito negativo con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bc606-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="bc606-205">La richiesta viene annullata dal gestore di I/O.</span><span class="sxs-lookup"><span data-stu-id="bc606-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="bc606-206">Il socket è chiuso.</span><span class="sxs-lookup"><span data-stu-id="bc606-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="bc606-207">Esempio</span><span class="sxs-lookup"><span data-stu-id="bc606-207">Examples</span></span>

<span data-ttu-id="bc606-208">Nell'esempio seguente viene acquisita una prenotazione della porta di runtime, quindi viene rilasciata la prenotazione della porta di Runtime.</span><span class="sxs-lookup"><span data-stu-id="bc606-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="bc606-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc606-209">See also</span></span>

[<span data-ttu-id="bc606-210">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="bc606-211">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="bc606-212">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="bc606-213">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="bc606-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="bc606-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="bc606-215">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="bc606-216">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="bc606-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="bc606-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="bc606-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="bc606-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="bc606-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="bc606-219">presa</span><span class="sxs-lookup"><span data-stu-id="bc606-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="bc606-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="bc606-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="bc606-221">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="bc606-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="bc606-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="bc606-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="bc606-223">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="bc606-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="bc606-224">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="bc606-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="bc606-225">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="bc606-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
