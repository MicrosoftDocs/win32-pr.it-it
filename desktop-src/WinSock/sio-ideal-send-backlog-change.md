---
description: Il codice di controllo notifica a un'applicazione quando viene modificato il valore di backlog di invio ideale per la connessione.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: Codice di controllo SIO_IDEAL_SEND_BACKLOG_CHANGE
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755071"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="1a1c8-103">Codice di controllo SIO_IDEAL_SEND_BACKLOG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="1a1c8-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1a1c8-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a1c8-104">Description</span></span>

<span data-ttu-id="1a1c8-105">Il codice di controllo delle **\_ modifiche del backlog di invio ideale per sio \_ Invia \_ \_** una notifica all'applicazione quando viene modificato il valore di backlog di invio ideale per la connessione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="1a1c8-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="1a1c8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a1c8-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1a1c8-108">s</span><span class="sxs-lookup"><span data-stu-id="1a1c8-108">s</span></span>

<span data-ttu-id="1a1c8-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1a1c8-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="1a1c8-110">dwIoControlCode</span></span>

<span data-ttu-id="1a1c8-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-111">The control code for the operation.</span></span>
<span data-ttu-id="1a1c8-112">Usare **la \_ \_ modifica del \_ backlog \_ di invio ideale di sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1a1c8-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="1a1c8-113">lpvInBuffer</span></span>

<span data-ttu-id="1a1c8-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="1a1c8-115">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="1a1c8-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="1a1c8-116">cbInBuffer</span></span>

<span data-ttu-id="1a1c8-117">Dimensione, in byte, del buffer di input. Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1a1c8-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1a1c8-118">lpvOutBuffer</span></span>

<span data-ttu-id="1a1c8-119">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="1a1c8-120">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1a1c8-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1a1c8-121">cbOutBuffer</span></span>

<span data-ttu-id="1a1c8-122">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="1a1c8-123">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1a1c8-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="1a1c8-124">lpcbBytesReturned</span></span>

<span data-ttu-id="1a1c8-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="1a1c8-126">Il parametro restituito punta a un valore **DWORD** pari a zero per questa operazione, poiché non è presente alcun output.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1a1c8-127">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="1a1c8-127">lpvOverlapped</span></span>

<span data-ttu-id="1a1c8-128">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1a1c8-129">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1a1c8-130">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="1a1c8-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1a1c8-131">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1a1c8-132">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1a1c8-133">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1a1c8-134">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1a1c8-134">lpCompletionRoutine</span></span>

<span data-ttu-id="1a1c8-135">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1a1c8-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1a1c8-136">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="1a1c8-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1a1c8-137">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="1a1c8-137">lpThreadId</span></span>

<span data-ttu-id="1a1c8-138">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="1a1c8-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1a1c8-139">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1a1c8-140">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1a1c8-141">lpErrno</span><span class="sxs-lookup"><span data-stu-id="1a1c8-141">lpErrno</span></span>

<span data-ttu-id="1a1c8-142">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-142">A pointer to the error code.</span></span>

<span data-ttu-id="1a1c8-143">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a1c8-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a1c8-144">Return value</span></span>

<span data-ttu-id="1a1c8-145">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1a1c8-146">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1a1c8-147">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1a1c8-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1a1c8-148">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="1a1c8-148">Error code</span></span> | <span data-ttu-id="1a1c8-149">Significato</span><span class="sxs-lookup"><span data-stu-id="1a1c8-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="1a1c8-150">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1a1c8-151">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1a1c8-152">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1a1c8-153">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="1a1c8-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-154">**WSAEFAULT**</span></span> | <span data-ttu-id="1a1c8-155">Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1a1c8-156">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1a1c8-157">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1a1c8-158">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-158">**WSAEINTR**</span></span> | <span data-ttu-id="1a1c8-159">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1a1c8-160">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-160">**WSAEINVAL**</span></span> | <span data-ttu-id="1a1c8-161">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="1a1c8-162">Questo errore viene restituito se il parametro *cbOutBuffer* è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="1a1c8-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="1a1c8-164">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="1a1c8-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="1a1c8-166">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="1a1c8-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="1a1c8-168">Il socket *s* non è connesso.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="1a1c8-169">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1a1c8-170">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="1a1c8-171">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1a1c8-172">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="1a1c8-173">Questo errore viene restituito se la **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non è supportata dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="1a1c8-174">Questo errore viene restituito anche quando viene eseguito un tentativo di usare il comando di **modifica del backlog di invio della \_ soluzione sio ideale \_ \_ \_** su un socket di datagramma.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1a1c8-175">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a1c8-175">Remarks</span></span>

<span data-ttu-id="1a1c8-176">Il IOCTL ideale per la **\_ modifica del \_ \_ backlog \_ di invio** è supportato in Windows Server 2008, Windows Vista con Service Pack 1 (SP1) e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="1a1c8-177">Quando si inviano dati tramite una connessione TCP mediante Windows Sockets, è importante garantire una quantità sufficiente di dati in attesa (inviati ma non ancora riconosciuti) in TCP per ottenere la massima velocità effettiva.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="1a1c8-178">Il valore ideale per la quantità di dati in attesa di ottenere la migliore velocità effettiva per la connessione TCP è denominato dimensione del backlog di invio ideale.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="1a1c8-179">Il valore ISB è una funzione del prodotto di ritardo della larghezza di banda della connessione TCP e della finestra di ricezione annunciata del ricevitore (e parzialmente la quantità di congestione nella rete).</span><span class="sxs-lookup"><span data-stu-id="1a1c8-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="1a1c8-180">Il valore ISB per connessione è disponibile nell'implementazione del protocollo TCP in Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="1a1c8-181">La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** può essere usata da un'applicazione per ricevere una notifica quando il valore di ISB cambia in modo dinamico per una connessione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="1a1c8-182">In Windows Server 2008, Windows Vista con SP1 e versioni successive del sistema operativo, la modifica del **\_ backlog di \_ INVIO \_ del \_ backlog ideale di sio** e la [**query del \_ \_ backlog di invio \_ \_ ideale di sio**](sio-ideal-send-backlog-query.md) sono supportate nei socket orientati al flusso che si trovano in uno stato connesso.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="1a1c8-183">L'intervallo per il valore ISB per una connessione TCP può teoricamente variare da 0 a un massimo di 16 megabyte.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="1a1c8-184">Vedere la pagina di riferimento per la [**\_ query di \_ \_ backlog \_ di invio ideale per sio**](sio-ideal-send-backlog-query.md) per l'uso tipico del meccanismo ISB per ottenere una migliore velocità effettiva su connessioni di prodotti con ritardo della larghezza di banda elevata.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="1a1c8-185">La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** è consentita solo su un socket di flusso che si trova nello stato connesso.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="1a1c8-186">In caso contrario, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** avrà esito negativo con **WSAENOTCONN**.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="1a1c8-187">La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non utilizza buffer di input o di output e in sospeso né blocca fino a quando non viene apportata una modifica all'ISB nella connessione sottostante.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="1a1c8-188">Quando questo comando IOCTL viene completato, un'applicazione Winsock può usare l'IOCTL [**\_ query di \_ \_ backlog \_ di invio ideale di sio**](sio-ideal-send-backlog-query.md) per recuperare il nuovo valore ISB sulla connessione.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="1a1c8-189">La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** non supporta la modalità non di blocco.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="1a1c8-190">Un'applicazione è autorizzata a eseguire questo IOCTL su un socket non bloccante, ma il IOCTL verrà semplicemente bloccato o sospeso fino a quando il valore di ISB non cambia.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="1a1c8-191">Se entrambi i parametri *lpOverlapped* e *il lpCompletionRoutine* sono null, il socket in questa funzione verrà considerato come un socket non sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="1a1c8-192">Per un socket non sovrapposto, i parametri *lpOverlapped* e *il lpCompletionRoutine* vengono ignorati, ad eccezione del fatto che la funzione può essere bloccata se socket *s* è in modalità di blocco.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="1a1c8-193">Se il socket *s* è in modalità non di blocco, questa funzione verrà comunque bloccata poiché questo particolare IOCTL non supporta la modalità non di blocco.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="1a1c8-194">Per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="1a1c8-195">Qualsiasi IOCTL può bloccarsi per un periodo illimitato, a seconda dell'implementazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="1a1c8-196">Se l'applicazione non è in grado di tollerare il blocco in una chiamata di funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** , si consiglia di eseguire l'i/O sovrapposto per le IOCTL che sono particolarmente probabilmente bloccate.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="1a1c8-197">La **\_ modifica del \_ \_ backlog di \_ invio della soluzione sio ideale** fornisce una notifica e dovrebbe bloccarsi o essere sospesa fino a quando il valore di ISB non cambia.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="1a1c8-198">Quindi, in genere verrebbe chiamato in modo asincrono con il parametro *lpOverlapped* impostato su una struttura WSAOVERLAPPED valida.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="1a1c8-199">La **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** può avere esito negativo con l'operazione **WSAEINTR** o **WSA \_ \_ interrotta** nei casi seguenti:</span><span class="sxs-lookup"><span data-stu-id="1a1c8-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="1a1c8-200">La connessione TCP viene normalmente disconnessa nella direzione di invio.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="1a1c8-201">Questo problema può verificarsi in seguito a una chiamata alla funzione Shutdown con il parametro how impostato su **SD \_ Send**, una chiamata alla funzione **DisconnectEx** o una chiamata alla funzione **TransmitFile** o **TransmitPackets** con il parametro *dwFlags* impostato su **tf \_ Disconnect** o **tf \_ riuso**.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="1a1c8-202">La connessione TCP è stata reimpostata o interrotta.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="1a1c8-203">L'applicazione rilascia un comando IOCTL di **\_ invio della \_ \_ \_ modifica del backlog ideale** quando è già presente una richiesta di notifica in sospeso.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="1a1c8-204">È consentita solo la richiesta di **\_ modifica del \_ backlog di invio \_ \_ ideale** di 1 1 in sospeso alla volta.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="1a1c8-205">La richiesta viene annullata dal gestore di I/O.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="1a1c8-206">Il socket è chiuso.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-206">The socket is closed.</span></span>

<span data-ttu-id="1a1c8-207">Due funzioni wrapper inline per tali IOCTL sono definite nel file di intestazione *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="1a1c8-208">Si consiglia di usare queste funzioni inline invece di usare la modifica del **\_ backlog di \_ INVIO \_ \_** e la [**\_ \_ \_ \_ query**](sio-ideal-send-backlog-query.md) di backlog di invio ideale per Sio, direttamente.</span><span class="sxs-lookup"><span data-stu-id="1a1c8-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="1a1c8-209">La funzione wrapper inline per la **\_ modifica del \_ \_ backlog di \_ invio ideale di sio** è la funzione **idealsendbacklognotify** .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="1a1c8-210">La funzione wrapper inline per la [**\_ query di \_ \_ backlog di \_ invio ideale di sio**](sio-ideal-send-backlog-query.md) è la funzione **idealsendbacklogquery** .</span><span class="sxs-lookup"><span data-stu-id="1a1c8-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a1c8-211">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a1c8-211">See also</span></span>

[<span data-ttu-id="1a1c8-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="1a1c8-213">**presa**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1a1c8-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="1a1c8-215">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1a1c8-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1a1c8-217">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1a1c8-218">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1a1c8-219">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="1a1c8-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
