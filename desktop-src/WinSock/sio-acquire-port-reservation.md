---
description: Il codice di controllo acquisisce una prenotazione di runtime per un blocco di porte TCP o UDP.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: Codice di controllo SIO_ACQUIRE_PORT_RESERVATION
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310429"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="b0909-103">Codice di controllo SIO_ACQUIRE_PORT_RESERVATION</span><span class="sxs-lookup"><span data-stu-id="b0909-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="b0909-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0909-104">Description</span></span>

<span data-ttu-id="b0909-105">Il codice di controllo della **\_ prenotazione della \_ porta \_ di acquisizione sio** acquisisce una prenotazione di runtime per un blocco di porte TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="b0909-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="b0909-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="b0909-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="b0909-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0909-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b0909-108">s</span><span class="sxs-lookup"><span data-stu-id="b0909-108">s</span></span>

<span data-ttu-id="b0909-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="b0909-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b0909-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="b0909-110">dwIoControlCode</span></span>

<span data-ttu-id="b0909-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-111">The control code for the operation.</span></span>
<span data-ttu-id="b0909-112">Usare **la \_ \_ \_ prenotazione della porta di acquisizione sio**  per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b0909-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="b0909-113">lpvInBuffer</span></span>

<span data-ttu-id="b0909-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="b0909-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b0909-115">Questo parametro contiene un puntatore a una struttura di [**\_ \_ intervallo di porte inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) che specifica il numero del punto iniziale e il numero di porte da riservare.</span><span class="sxs-lookup"><span data-stu-id="b0909-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b0909-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="b0909-116">cbInBuffer</span></span>

<span data-ttu-id="b0909-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="b0909-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="b0909-118">Questo parametro deve corrispondere alla dimensione della struttura [**dell' \_ \_ intervallo di porte inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) .</span><span class="sxs-lookup"><span data-stu-id="b0909-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b0909-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b0909-119">lpvOutBuffer</span></span>

<span data-ttu-id="b0909-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="b0909-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="b0909-121">In caso di esito positivo, questo parametro contiene un puntatore a una struttura dell' [**\_ istanza di \_ prenotazione \_ della porta inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="b0909-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b0909-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="b0909-122">cbOutBuffer</span></span>

<span data-ttu-id="b0909-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="b0909-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b0909-124">Questo parametro deve essere pari almeno alla dimensione della struttura [**dell' \_ \_ \_ istanza di prenotazione della porta inet**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="b0909-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b0909-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="b0909-125">lpcbBytesReturned</span></span>

<span data-ttu-id="b0909-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="b0909-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="b0909-127">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="b0909-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="b0909-128">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="b0909-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="b0909-129">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b0909-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="b0909-130">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b0909-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="b0909-131">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b0909-132">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="b0909-132">lpvOverlapped</span></span>

<span data-ttu-id="b0909-133">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="b0909-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b0909-134">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b0909-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b0909-135">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="b0909-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b0909-136">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="b0909-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b0909-137">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b0909-138">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="b0909-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b0909-139">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="b0909-139">lpCompletionRoutine</span></span>

<span data-ttu-id="b0909-140">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b0909-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b0909-141">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="b0909-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b0909-142">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="b0909-142">lpThreadId</span></span>

<span data-ttu-id="b0909-143">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a **WPUQueueApc**.</span><span class="sxs-lookup"><span data-stu-id="b0909-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="b0909-144">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione **WPUQueueApc** .</span><span class="sxs-lookup"><span data-stu-id="b0909-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="b0909-145">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b0909-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b0909-146">lpErrno</span><span class="sxs-lookup"><span data-stu-id="b0909-146">lpErrno</span></span>

<span data-ttu-id="b0909-147">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="b0909-147">A pointer to the error code.</span></span>

<span data-ttu-id="b0909-148">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="b0909-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0909-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0909-149">Return value</span></span>

<span data-ttu-id="b0909-150">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="b0909-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b0909-151">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="b0909-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b0909-152">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b0909-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b0909-153">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="b0909-153">Error code</span></span> | <span data-ttu-id="b0909-154">Significato</span><span class="sxs-lookup"><span data-stu-id="b0909-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="b0909-155">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="b0909-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b0909-156">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="b0909-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="b0909-157">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b0909-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b0909-158">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="b0909-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b0909-159">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="b0909-160">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL di **\_ scaricamento sio** .</span><span class="sxs-lookup"><span data-stu-id="b0909-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="b0909-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b0909-161">**WSAEFAULT**</span></span> | <span data-ttu-id="b0909-162">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="b0909-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="b0909-163">Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="b0909-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b0909-164">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="b0909-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b0909-165">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="b0909-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="b0909-166">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="b0909-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b0909-167">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="b0909-167">**WSAEINTR**</span></span> | <span data-ttu-id="b0909-168">Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="b0909-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="b0909-169">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="b0909-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b0909-170">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="b0909-170">**WSAEINVAL**</span></span> | <span data-ttu-id="b0909-171">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="b0909-171">An invalid argument was supplied.</span></span> <span data-ttu-id="b0909-172">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="b0909-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b0909-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b0909-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="b0909-174">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="b0909-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="b0909-175">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b0909-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="b0909-176">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="b0909-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b0909-177">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="b0909-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="b0909-178">Questo errore viene restituito se il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="b0909-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="b0909-179">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="b0909-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b0909-180">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="b0909-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="b0909-181">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b0909-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="b0909-182">Questo errore viene restituito anche se il provider di trasporto IOCTL per la **\_ prenotazione della \_ porta \_ di acquisizione sio** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b0909-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="b0909-183">Questo errore viene restituito anche quando un tentativo di usare l'IOCTL di **\_ prenotazione della \_ porta \_ di acquisizione sio** viene eseguito su un socket diverso da UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="b0909-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b0909-184">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0909-184">Remarks</span></span>

<span data-ttu-id="b0909-185">Il IOCTL di **\_ prenotazione della \_ porta \_ di acquisizione sio**  è supportato in Windows Vista e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b0909-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="b0909-186">Le applicazioni e i servizi che devono riservare le porte rientrano in due categorie.</span><span class="sxs-lookup"><span data-stu-id="b0909-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="b0909-187">La prima categoria include i componenti che richiedono una determinata porta come parte dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="b0909-188">Tali componenti preferiscono in genere specificare la porta richiesta al momento dell'installazione, ad esempio in un manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="b0909-189">La seconda categoria include i componenti che richiedono qualsiasi porta o blocco di porte disponibile in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b0909-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="b0909-190">Queste due categorie corrispondono a richieste di prenotazione di porta specifiche e con caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="b0909-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="b0909-191">Richieste di prenotazione specifiche possono essere permanenti o Runtime, mentre le richieste di prenotazione di porta con caratteri jolly sono supportate solo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b0909-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="b0909-192">Per richiedere una prenotazione di runtime per un blocco di porte TCP o UDP, viene usato il comando di **\_ prenotazione della \_ porta \_ di acquisizione sio**  .</span><span class="sxs-lookup"><span data-stu-id="b0909-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="b0909-193">Per le prenotazioni di porte di runtime, il pool di porte richiede che le prenotazioni vengano utilizzate dal processo sul cui socket è stata concessa la prenotazione.</span><span class="sxs-lookup"><span data-stu-id="b0909-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="b0909-194">Le prenotazioni di porte di runtime durano solo fino a quando la durata del socket in cui è stata chiamata la **\_ porta di acquisizione \_ \_ sio**  è stata chiamata.</span><span class="sxs-lookup"><span data-stu-id="b0909-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="b0909-195">Al contrario, le prenotazioni di porte permanenti create utilizzando la funzione [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) o [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) possono essere utilizzate da qualsiasi processo con la possibilità di ottenere prenotazioni permanenti.</span><span class="sxs-lookup"><span data-stu-id="b0909-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="b0909-196">Una volta ottenuta una prenotazione della porta TCP o UDP di runtime, un'applicazione può richiedere le assegnazioni delle porte dalla prenotazione della porta aprendo un socket TCP o UDP, quindi chiamando la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) specificando il IOCTL di [**prenotazione della \_ \_ porta \_ di associazione sio**](sio-associate-port-reservation.md) e passando il token di prenotazione prima di emettere una chiamata alla funzione di binding sul socket.</span><span class="sxs-lookup"><span data-stu-id="b0909-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="b0909-197">Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono **null**, il socket in questa funzione verrà considerato come un socket non sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="b0909-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="b0909-198">Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.</span><span class="sxs-lookup"><span data-stu-id="b0909-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="b0909-199">Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.</span><span class="sxs-lookup"><span data-stu-id="b0909-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="b0909-200">Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="b0909-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="b0909-201">Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="b0909-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="b0909-202">Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione WSAIoctl o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.</span><span class="sxs-lookup"><span data-stu-id="b0909-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="b0909-203">Il codice IOCTL per la **prenotazione della porta di \_ acquisizione \_ \_ sio**  può non riuscire con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b0909-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="b0909-204">La richiesta viene annullata dal gestore di I/O.</span><span class="sxs-lookup"><span data-stu-id="b0909-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="b0909-205">Il socket è chiuso.</span><span class="sxs-lookup"><span data-stu-id="b0909-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="b0909-206">Esempio</span><span class="sxs-lookup"><span data-stu-id="b0909-206">Examples</span></span>

<span data-ttu-id="b0909-207">Nell'esempio seguente viene acquisita una prenotazione della porta di runtime, viene quindi creato un socket e viene allocata una porta dalla prenotazione della porta di runtime per il socket, quindi viene chiuso il socket e il rilascia la prenotazione della porta di Runtime.</span><span class="sxs-lookup"><span data-stu-id="b0909-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="b0909-208">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0909-208">See also</span></span>

[<span data-ttu-id="b0909-209">**accettare**</span><span class="sxs-lookup"><span data-stu-id="b0909-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="b0909-210">**associare**</span><span class="sxs-lookup"><span data-stu-id="b0909-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="b0909-211">**CreatePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="b0909-212">**CreatePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="b0909-213">**DeletePersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="b0909-214">**DeletePersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="b0909-215">**\_intervallo di porte inet \_**</span><span class="sxs-lookup"><span data-stu-id="b0909-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="b0909-216">**\_ \_ istanza prenotazione porta \_ inet**</span><span class="sxs-lookup"><span data-stu-id="b0909-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="b0909-217">**LookupPersistentTcpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="b0909-218">**LookupPersistentUdpPortReservation**</span><span class="sxs-lookup"><span data-stu-id="b0909-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="b0909-219">**\_ \_ prenotazione porta di associazione sio \_**</span><span class="sxs-lookup"><span data-stu-id="b0909-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="b0909-220">**\_ \_ prenotazione porta versione \_ sio**</span><span class="sxs-lookup"><span data-stu-id="b0909-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="b0909-221">**presa**</span><span class="sxs-lookup"><span data-stu-id="b0909-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b0909-222">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="b0909-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="b0909-223">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="b0909-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b0909-224">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="b0909-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b0909-225">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="b0909-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b0909-226">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="b0909-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b0909-227">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="b0909-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
