---
description: Codice di controllo che configura i parametri del timeout di ritrasmissione iniziale (RTO) in un socket.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: Codice di controllo SIO_TCP_INITIAL_RTO
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/09/2020
ms.locfileid: "104474582"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="5137d-103">Codice di controllo SIO_TCP_INITIAL_RTO</span><span class="sxs-lookup"><span data-stu-id="5137d-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="5137d-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5137d-104">Description</span></span>

<span data-ttu-id="5137d-105">Il codice di controllo **SIO_TCP_INITIAL_RTO** configura i parametri del timeout di ritrasmissione iniziale (RTO) in un socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="5137d-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="5137d-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="5137d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5137d-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="5137d-108">s</span><span class="sxs-lookup"><span data-stu-id="5137d-108">s</span></span>

<span data-ttu-id="5137d-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="5137d-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="5137d-110">dwIoControlCode</span></span>

<span data-ttu-id="5137d-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-111">The control code for the operation.</span></span>
<span data-ttu-id="5137d-112">Usare **SIO_TCP_INITIAL_RTO** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="5137d-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="5137d-113">lpvInBuffer</span></span>

<span data-ttu-id="5137d-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="5137d-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="5137d-115">Questo parametro contiene un puntatore al [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associato al socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="5137d-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="5137d-116">cbInBuffer</span></span>

<span data-ttu-id="5137d-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="5137d-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="5137d-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5137d-118">lpvOutBuffer</span></span>

<span data-ttu-id="5137d-119">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="5137d-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="5137d-120">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="5137d-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="5137d-121">cbOutBuffer</span></span>

<span data-ttu-id="5137d-122">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="5137d-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="5137d-123">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="5137d-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="5137d-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="5137d-124">lpcbBytesReturned</span></span>

<span data-ttu-id="5137d-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="5137d-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="5137d-126">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="5137d-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="5137d-127">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="5137d-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="5137d-128">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="5137d-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="5137d-129">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5137d-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="5137d-130">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="5137d-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="5137d-131">lpvOverlapped</span></span>

<span data-ttu-id="5137d-132">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="5137d-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5137d-133">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5137d-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="5137d-134">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="5137d-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="5137d-135">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="5137d-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="5137d-136">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="5137d-137">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="5137d-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="5137d-138">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="5137d-138">lpCompletionRoutine</span></span>

<span data-ttu-id="5137d-139">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="5137d-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="5137d-140">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="5137d-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="5137d-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="5137d-141">lpThreadId</span></span>

<span data-ttu-id="5137d-142">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="5137d-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="5137d-143">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="5137d-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="5137d-144">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5137d-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="5137d-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="5137d-145">lpErrno</span></span>

<span data-ttu-id="5137d-146">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="5137d-146">A pointer to the error code.</span></span>

<span data-ttu-id="5137d-147">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="5137d-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="5137d-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5137d-148">Return value</span></span>

<span data-ttu-id="5137d-149">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5137d-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="5137d-150">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="5137d-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="5137d-151">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5137d-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="5137d-152">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="5137d-152">Error code</span></span> | <span data-ttu-id="5137d-153">Significato</span><span class="sxs-lookup"><span data-stu-id="5137d-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="5137d-154">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="5137d-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="5137d-155">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="5137d-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="5137d-156">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="5137d-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="5137d-157">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="5137d-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="5137d-158">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5137d-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="5137d-159">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL di **\_ scaricamento sio** .</span><span class="sxs-lookup"><span data-stu-id="5137d-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="5137d-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="5137d-160">**WSAEACCES**</span></span> | <span data-ttu-id="5137d-161">È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="5137d-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="5137d-162">Questo errore viene restituito in diverse condizioni che includono quanto segue: l'utente non dispone dei privilegi amministrativi necessari sul computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="5137d-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="5137d-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5137d-163">**WSAEFAULT**</span></span> | <span data-ttu-id="5137d-164">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="5137d-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="5137d-165">Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="5137d-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="5137d-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="5137d-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="5137d-167">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="5137d-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="5137d-168">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="5137d-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="5137d-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="5137d-169">**WSAEINTR**</span></span> | <span data-ttu-id="5137d-170">Un'operazione di blocco è stata interrotta da una chiamata a *WSACancelBlockingCall*.</span><span class="sxs-lookup"><span data-stu-id="5137d-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="5137d-171">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="5137d-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="5137d-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="5137d-172">**WSAEINVAL**</span></span> | <span data-ttu-id="5137d-173">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="5137d-173">An invalid argument was supplied.</span></span> <span data-ttu-id="5137d-174">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="5137d-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="5137d-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="5137d-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="5137d-176">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="5137d-177">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5137d-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="5137d-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="5137d-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="5137d-179">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="5137d-180">Questo errore viene restituito se il descrittore s non è un socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="5137d-181">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="5137d-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="5137d-182">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="5137d-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="5137d-183">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5137d-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="5137d-184">Questo errore viene restituito anche se il **SIO_TCP_INITIAL_RTO** IOCTL non è supportato dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="5137d-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="5137d-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="5137d-185">Remarks</span></span>

<span data-ttu-id="5137d-186">Un'applicazione può utilizzare il **SIO_TCP_INITIAL_RTO** IOCTL per controllare le caratteristiche di ritrasmissione iniziali (SYN/SYN + ACK) di un socket TCP, se necessario.</span><span class="sxs-lookup"><span data-stu-id="5137d-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="5137d-187">Un'applicazione, se si utilizza questa opzione, deve fornire valori appropriati prima di avviare un tentativo di connessione TCP sul socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="5137d-188">Il [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL consente a un'applicazione di configurare il timeout di ritrasmissione (SYN) iniziale (RTO) utilizzato dal socket.</span><span class="sxs-lookup"><span data-stu-id="5137d-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="5137d-189">Un puntatore a una struttura [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) passata nel parametro *lpvInBuffer* consente a un'applicazione di configurare il tempo di round trip iniziale (RTT) usato per calcolare il timeout di ritrasmissione.</span><span class="sxs-lookup"><span data-stu-id="5137d-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="5137d-190">L'applicazione può inoltre configurare il numero di ritrasmissioni che verranno tentate prima che il tentativo di connessione non riesca.</span><span class="sxs-lookup"><span data-stu-id="5137d-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="5137d-191">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5137d-191">See also</span></span>

[<span data-ttu-id="5137d-192">presa</span><span class="sxs-lookup"><span data-stu-id="5137d-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="5137d-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="5137d-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="5137d-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="5137d-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="5137d-195">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="5137d-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="5137d-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="5137d-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="5137d-197">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="5137d-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="5137d-198">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="5137d-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="5137d-199">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="5137d-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
