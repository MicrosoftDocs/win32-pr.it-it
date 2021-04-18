---
description: Il codice di controllo Configura un socket TCP per una latenza più bassa e operazioni più veloci sull'interfaccia di loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: Codice di controllo SIO_LOOPBACK_FAST_PATH
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315780"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="2d799-103">Codice di controllo SIO_LOOPBACK_FAST_PATH</span><span class="sxs-lookup"><span data-stu-id="2d799-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2d799-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d799-104">Description</span></span>

<span data-ttu-id="2d799-105">Il codice di controllo del **\_ \_ \_ percorso rapido del loopback sio** configura un socket TCP per una latenza più bassa e operazioni più veloci sull'interfaccia di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="2d799-106">**Importante**  Il **\_ \_ \_ percorso veloce del loopback sio** è deprecato e non è consigliabile usarlo nel codice.</span><span class="sxs-lookup"><span data-stu-id="2d799-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="2d799-107">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d799-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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

## <a name="parameters"></a><span data-ttu-id="2d799-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d799-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2d799-109">s</span><span class="sxs-lookup"><span data-stu-id="2d799-109">s</span></span>

<span data-ttu-id="2d799-110">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2d799-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="2d799-111">dwIoControlCode</span></span>

<span data-ttu-id="2d799-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-112">The control code for the operation.</span></span>
<span data-ttu-id="2d799-113">USA **il \_ \_ \_ percorso veloce di loopback di sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2d799-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="2d799-114">lpvInBuffer</span></span>

<span data-ttu-id="2d799-115">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="2d799-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="2d799-116">Questo parametro contiene un puntatore a un valore booleano che indica se il socket deve essere configurato per le operazioni di loopback veloce.</span><span class="sxs-lookup"><span data-stu-id="2d799-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2d799-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="2d799-117">cbInBuffer</span></span>

<span data-ttu-id="2d799-118">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="2d799-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2d799-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2d799-119">lpvOutBuffer</span></span>

<span data-ttu-id="2d799-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2d799-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2d799-121">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2d799-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="2d799-122">cbOutBuffer</span></span>

<span data-ttu-id="2d799-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2d799-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="2d799-124">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="2d799-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2d799-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="2d799-125">lpcbBytesReturned</span></span>

<span data-ttu-id="2d799-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2d799-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="2d799-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="2d799-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="2d799-128">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="2d799-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="2d799-129">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2d799-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="2d799-130">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2d799-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="2d799-131">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2d799-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="2d799-132">lpvOverlapped</span></span>

<span data-ttu-id="2d799-133">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="2d799-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2d799-134">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="2d799-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2d799-135">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="2d799-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2d799-136">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="2d799-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2d799-137">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2d799-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2d799-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2d799-139">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="2d799-139">lpCompletionRoutine</span></span>

<span data-ttu-id="2d799-140">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2d799-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2d799-141">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="2d799-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2d799-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="2d799-142">lpThreadId</span></span>

<span data-ttu-id="2d799-143">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="2d799-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2d799-144">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="2d799-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2d799-145">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="2d799-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2d799-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="2d799-146">lpErrno</span></span>

<span data-ttu-id="2d799-147">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="2d799-147">A pointer to the error code.</span></span>

<span data-ttu-id="2d799-148">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="2d799-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d799-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d799-149">Return value</span></span>

<span data-ttu-id="2d799-150">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="2d799-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2d799-151">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="2d799-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2d799-152">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="2d799-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2d799-153">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="2d799-153">Error code</span></span> | <span data-ttu-id="2d799-154">Significato</span><span class="sxs-lookup"><span data-stu-id="2d799-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="2d799-155">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="2d799-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2d799-156">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="2d799-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="2d799-157">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="2d799-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2d799-158">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="2d799-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2d799-159">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2d799-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="2d799-160">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando **\_ IOCTL di scaricamento sio** .</span><span class="sxs-lookup"><span data-stu-id="2d799-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="2d799-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="2d799-161">**WSAEACCES**</span></span> | <span data-ttu-id="2d799-162">È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="2d799-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="2d799-163">Questo errore viene restituito in diverse condizioni per le prenotazioni di porte permanenti che includono quanto segue: l'utente non dispone dei privilegi amministrativi richiesti nel computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="2d799-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="2d799-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2d799-164">**WSAEFAULT**</span></span> | <span data-ttu-id="2d799-165">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="2d799-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="2d799-166">Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="2d799-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2d799-167">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="2d799-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2d799-168">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="2d799-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="2d799-169">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="2d799-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2d799-170">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="2d799-170">**WSAEINTR**</span></span> | <span data-ttu-id="2d799-171">Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="2d799-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="2d799-172">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="2d799-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2d799-173">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="2d799-173">**WSAEINVAL**</span></span> | <span data-ttu-id="2d799-174">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="2d799-174">An invalid argument was supplied.</span></span> <span data-ttu-id="2d799-175">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="2d799-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="2d799-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2d799-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="2d799-177">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="2d799-178">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="2d799-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="2d799-179">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="2d799-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2d799-180">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="2d799-181">Questo errore viene restituito se il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="2d799-182">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="2d799-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2d799-183">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="2d799-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="2d799-184">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="2d799-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="2d799-185">Questo errore viene restituito anche se l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** non è supportato dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="2d799-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2d799-186">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d799-186">Remarks</span></span>

<span data-ttu-id="2d799-187">Un'applicazione può usare l'IOCTL del **\_ \_ \_ percorso rapido di loopback sio** per ridurre la latenza e migliorare le prestazioni delle operazioni di loopback su un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="2d799-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="2d799-188">Questo IOCTL richiede che lo stack TCP/IP usi un percorso veloce speciale per le operazioni di loopback in questo socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="2d799-189">Il **\_ \_ \_ percorso veloce del loopback sio** può essere usato solo con i socket TCP.</span><span class="sxs-lookup"><span data-stu-id="2d799-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="2d799-190">Questo IOCTL deve essere utilizzato su entrambi i lati della sessione di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="2d799-191">Il percorso veloce di loopback TCP è supportato tramite l'interfaccia di loopback IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="2d799-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="2d799-192">Il socket che prevede di avviare la richiesta di connessione deve applicare questo IOCTL prima di effettuare la richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="2d799-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="2d799-193">Quindi, il socket usato dalla funzione [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) per avviare la connessione deve applicare questo IOCTL per usare il percorso rapido per le operazioni di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="2d799-194">Il socket in ascolto della richiesta di connessione deve applicare questo IOCTL prima di accettare la connessione.</span><span class="sxs-lookup"><span data-stu-id="2d799-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="2d799-195">Quindi, il socket usato dalla funzione Listen deve applicare questo IOCTL, in modo che tutti i socket accettati usino il percorso rapido per il loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="2d799-196">Tutti i socket restituiti dalla funzione Listen e passati alla funzione [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)o [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) verranno contrassegnati per l'utilizzo del percorso rapido speciale per le operazioni di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="2d799-197">Una volta che un'applicazione stabilisce la connessione su un'interfaccia di loopback usando il percorso veloce, tutti i pacchetti per la durata della connessione devono usare il percorso veloce.</span><span class="sxs-lookup"><span data-stu-id="2d799-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="2d799-198">L'applicazione del **\_ \_ \_ percorso rapido di loopback sio** a un socket che verrà connesso a un percorso non di loopback non avrà alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="2d799-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="2d799-199">Questa ottimizzazione del loopback TCP genera pacchetti che passano attraverso il livello di trasporto (TL) anziché il loopback tradizionale attraverso il livello di rete.</span><span class="sxs-lookup"><span data-stu-id="2d799-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="2d799-200">Questa ottimizzazione migliora la latenza per i pacchetti di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="2d799-201">Quando un'applicazione opta per l'impostazione del livello di connessione per utilizzare il percorso veloce di loopback, tutti i pacchetti seguiranno il percorso di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="2d799-202">Per le comunicazioni loopback, la congestione e la riduzione dei pacchetti non sono previsti.</span><span class="sxs-lookup"><span data-stu-id="2d799-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="2d799-203">Il concetto di controllo della congestione e recapito affidabile in TCP non sarà necessario.</span><span class="sxs-lookup"><span data-stu-id="2d799-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="2d799-204">Questo, tuttavia, non è vero per il controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d799-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="2d799-205">Senza il controllo del flusso, il mittente può sovraccaricare il buffer di ricezione, causando un comportamento errato del loopback TCP.</span><span class="sxs-lookup"><span data-stu-id="2d799-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="2d799-206">Il controllo di flusso nel percorso di loopback ottimizzato per TCP viene mantenuto inserendo richieste di invio in una coda.</span><span class="sxs-lookup"><span data-stu-id="2d799-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="2d799-207">Quando il buffer di ricezione è pieno, lo stack TCP/IP garantisce che le trasmissioni non verranno completate fino a quando la coda non verrà gestita con il controllo di flusso.</span><span class="sxs-lookup"><span data-stu-id="2d799-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="2d799-208">Le connessioni loopback con percorso veloce TCP in presenza di un callout della piattaforma filtro Windows per i dati di connessione devono prendere il percorso lento non ottimizzato per il loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="2d799-209">Pertanto, i filtri WFP impediscano l'utilizzo di questo nuovo percorso veloce di loopback.</span><span class="sxs-lookup"><span data-stu-id="2d799-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="2d799-210">Quando è abilitato un filtro WFP, il sistema utilizzerà il percorso lento anche se è stato impostato l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** .</span><span class="sxs-lookup"><span data-stu-id="2d799-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="2d799-211">Ciò garantisce che le applicazioni in modalità utente dispongano della funzionalità di sicurezza WFP completa.</span><span class="sxs-lookup"><span data-stu-id="2d799-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="2d799-212">Per impostazione predefinita, il **\_ \_ \_ percorso rapido di loopback sio** è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2d799-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="2d799-213">Solo un subset delle opzioni del socket TCP/IP è supportato quando viene utilizzato l'IOCTL del **\_ \_ \_ percorso veloce del loopback sio** per abilitare il percorso veloce di loopback in un socket.</span><span class="sxs-lookup"><span data-stu-id="2d799-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="2d799-214">L'elenco delle opzioni supportate include quanto segue:</span><span class="sxs-lookup"><span data-stu-id="2d799-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="2d799-215">**\_TTL IP**</span><span class="sxs-lookup"><span data-stu-id="2d799-215">**IP\_TTL**</span></span>
* <span data-ttu-id="2d799-216">**\_unicast IP \_ se**</span><span class="sxs-lookup"><span data-stu-id="2d799-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="2d799-217">**\_Hop unicast \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="2d799-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="2d799-218">**\_Unicast IPv6 \_ se**</span><span class="sxs-lookup"><span data-stu-id="2d799-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="2d799-219">**\_V6ONLY IPv6**</span><span class="sxs-lookup"><span data-stu-id="2d799-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="2d799-220">**\_accettazione condizionale \_**</span><span class="sxs-lookup"><span data-stu-id="2d799-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="2d799-221">**\_EXCLUSIVEADDRUSE**</span><span class="sxs-lookup"><span data-stu-id="2d799-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="2d799-222">**\_ \_ scalabilità delle porte**</span><span class="sxs-lookup"><span data-stu-id="2d799-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="2d799-223">**\_RCVBUF**</span><span class="sxs-lookup"><span data-stu-id="2d799-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="2d799-224">**\_REUSEADDR**</span><span class="sxs-lookup"><span data-stu-id="2d799-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="2d799-225">**\_BSDURGENT TCP**</span><span class="sxs-lookup"><span data-stu-id="2d799-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="2d799-226">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d799-226">See also</span></span>

[<span data-ttu-id="2d799-227">**Opzioni di IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="2d799-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="2d799-228">**Opzioni di IPPROTO_IPV6 socket**</span><span class="sxs-lookup"><span data-stu-id="2d799-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="2d799-229">**Opzioni di IPPROTO_TCP socket**</span><span class="sxs-lookup"><span data-stu-id="2d799-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="2d799-230">**presa**</span><span class="sxs-lookup"><span data-stu-id="2d799-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2d799-231">**Opzioni di SOL_SOCKET Socket**</span><span class="sxs-lookup"><span data-stu-id="2d799-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="2d799-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="2d799-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="2d799-233">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="2d799-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2d799-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="2d799-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2d799-235">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="2d799-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2d799-236">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="2d799-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2d799-237">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="2d799-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
