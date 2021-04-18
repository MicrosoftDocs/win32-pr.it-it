---
description: Il codice di controllo imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione del servizio di reindirizzamento.
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: Codice di controllo SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315778"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="fb100-103">Codice di controllo SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS</span><span class="sxs-lookup"><span data-stu-id="fb100-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="fb100-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb100-104">Description</span></span>

<span data-ttu-id="fb100-105">Il codice di controllo dei **record di reindirizzamento della connessione di sio \_ set \_ WFP \_ \_ \_** imposta il record di reindirizzamento sul nuovo socket TCP usato per la connessione alla destinazione finale per l'uso da parte di un servizio di reindirizzamento della piattaforma filtro Windows (WFP).</span><span class="sxs-lookup"><span data-stu-id="fb100-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="fb100-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="fb100-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="fb100-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb100-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="fb100-108">s</span><span class="sxs-lookup"><span data-stu-id="fb100-108">s</span></span>

<span data-ttu-id="fb100-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="fb100-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="fb100-110">dwIoControlCode</span></span>

<span data-ttu-id="fb100-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-111">The control code for the operation.</span></span>
<span data-ttu-id="fb100-112">Usare i **record di reindirizzamento della connessione di sio \_ set \_ WFP \_ \_ \_** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="fb100-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="fb100-113">lpvInBuffer</span></span>

<span data-ttu-id="fb100-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="fb100-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="fb100-115">Questo parametro contiene un puntatore al record di reindirizzamento di WFP associato al socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="fb100-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="fb100-116">cbInBuffer</span></span>

<span data-ttu-id="fb100-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="fb100-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="fb100-118">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="fb100-118">lpvOutBuffer</span></span>

<span data-ttu-id="fb100-119">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fb100-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="fb100-120">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="fb100-121">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="fb100-121">cbOutBuffer</span></span>

<span data-ttu-id="fb100-122">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fb100-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="fb100-123">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="fb100-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="fb100-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="fb100-124">lpcbBytesReturned</span></span>

<span data-ttu-id="fb100-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="fb100-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="fb100-126">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="fb100-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="fb100-127">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="fb100-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="fb100-128">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="fb100-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="fb100-129">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fb100-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="fb100-130">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="fb100-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="fb100-131">lpvOverlapped</span></span>

<span data-ttu-id="fb100-132">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="fb100-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fb100-133">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fb100-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="fb100-134">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="fb100-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="fb100-135">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="fb100-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fb100-136">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="fb100-137">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="fb100-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="fb100-138">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="fb100-138">lpCompletionRoutine</span></span>

<span data-ttu-id="fb100-139">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="fb100-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="fb100-140">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="fb100-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="fb100-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="fb100-141">lpThreadId</span></span>

<span data-ttu-id="fb100-142">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="fb100-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="fb100-143">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="fb100-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="fb100-144">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="fb100-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="fb100-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="fb100-145">lpErrno</span></span>

<span data-ttu-id="fb100-146">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="fb100-146">A pointer to the error code.</span></span>

<span data-ttu-id="fb100-147">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="fb100-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb100-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb100-148">Return value</span></span>

<span data-ttu-id="fb100-149">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="fb100-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="fb100-150">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="fb100-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="fb100-151">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="fb100-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="fb100-152">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="fb100-152">Error code</span></span> | <span data-ttu-id="fb100-153">Significato</span><span class="sxs-lookup"><span data-stu-id="fb100-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="fb100-154">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="fb100-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="fb100-155">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="fb100-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="fb100-156">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="fb100-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="fb100-157">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="fb100-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="fb100-158">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="fb100-159">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="fb100-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="fb100-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="fb100-160">**WSAEACCES**</span></span> | <span data-ttu-id="fb100-161">È stato effettuato un tentativo di accesso a un socket in modo non consentito dalle autorizzazioni di accesso.</span><span class="sxs-lookup"><span data-stu-id="fb100-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="fb100-162">Questo errore viene restituito in diverse condizioni che includono quanto segue: l'utente non dispone dei privilegi amministrativi necessari sul computer locale o l'applicazione non è in esecuzione in una shell avanzata come amministratore predefinito ( `RunAs administrator` ).</span><span class="sxs-lookup"><span data-stu-id="fb100-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="fb100-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fb100-163">**WSAEFAULT**</span></span> | <span data-ttu-id="fb100-164">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="fb100-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="fb100-165">Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="fb100-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="fb100-166">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="fb100-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="fb100-167">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="fb100-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="fb100-168">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="fb100-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="fb100-169">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="fb100-169">**WSAEINTR**</span></span> | <span data-ttu-id="fb100-170">Un'operazione di blocco è stata interrotta da una chiamata a **WSACancelBlockingCall**.</span><span class="sxs-lookup"><span data-stu-id="fb100-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="fb100-171">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="fb100-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="fb100-172">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="fb100-172">**WSAEINVAL**</span></span> | <span data-ttu-id="fb100-173">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="fb100-173">An invalid argument was supplied.</span></span> <span data-ttu-id="fb100-174">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="fb100-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="fb100-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="fb100-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="fb100-176">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="fb100-177">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fb100-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="fb100-178">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="fb100-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="fb100-179">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="fb100-180">Questo errore viene restituito se il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="fb100-181">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="fb100-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="fb100-182">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="fb100-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="fb100-183">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="fb100-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="fb100-184">Questo errore viene restituito anche se il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** non è supportato dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="fb100-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fb100-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="fb100-185">Remarks</span></span>

<span data-ttu-id="fb100-186">Il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** è supportato in Windows 8 e Windows Server 2012 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb100-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="fb100-187">Il WFP consente di accedere al percorso di elaborazione dei pacchetti TCP/IP, in cui è possibile esaminare o modificare i pacchetti in uscita e in ingresso prima di consentire l'ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="fb100-188">Toccando il percorso di elaborazione TCP/IP, i fornitori di software indipendenti (ISV) possono creare più facilmente firewall, software antivirus, software di diagnostica e altri tipi di applicazioni e servizi.</span><span class="sxs-lookup"><span data-stu-id="fb100-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="fb100-189">PAM fornisce componenti in modalità utente e kernel, in modo che gli ISV di terze parti possano partecipare alle decisioni di filtro che avvengono a diversi livelli nello stack di protocolli TCP/IP e in tutto il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fb100-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="fb100-190">La funzionalità di reindirizzamento della connessione WFP consente a un driver del kernel di callout di WFP di reindirizzare una connessione localmente a un processo in modalità utente, di eseguire l'ispezione dei contenuti in modalità utente e inoltrare il contenuto ispezionato utilizzando una connessione diversa alla destinazione originale.</span><span class="sxs-lookup"><span data-stu-id="fb100-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="fb100-191">I **\_ record di reindirizzamento della connessione del set di \_ \_ \_ \_ dati di sio** e di molti altri IOCTL correlati sono componenti in modalità utente utilizzati per consentire a più applicazioni proxy di connessione basate su WFP di ispezionare lo stesso flusso di traffico in modo cooperativo.</span><span class="sxs-lookup"><span data-stu-id="fb100-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="fb100-192">Ogni agente di ispezione può verificare in modo sicuro il traffico di rete che è già stato ispezionato da un altro agente di ispezione.</span><span class="sxs-lookup"><span data-stu-id="fb100-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="fb100-193">Con la presenza di più proxy (sviluppati da ISV diversi, ad esempio) la connessione utilizzata da un proxy per comunicare con la destinazione finale può a sua volta essere reindirizzata da un secondo proxy e la nuova connessione potrebbe essere reindirizzata dal proxy originale.</span><span class="sxs-lookup"><span data-stu-id="fb100-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="fb100-194">Senza il rilevamento della connessione, la connessione originale potrebbe non raggiungere mai la destinazione finale poiché rimane bloccata in un ciclo del proxy infinito.</span><span class="sxs-lookup"><span data-stu-id="fb100-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="fb100-195">Il **\_ set di \_ dati di \_ \_ Reindirizzamento \_ della connessione di sio set WFP** viene usato per fornire il rilevamento delle connessioni con proxy sulle connessioni socket reindirizzate.</span><span class="sxs-lookup"><span data-stu-id="fb100-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="fb100-196">Questa funzionalità WFP facilita il rilevamento dei record di reindirizzamento dal reindirizzamento iniziale di una connessione alla connessione finale alla destinazione.</span><span class="sxs-lookup"><span data-stu-id="fb100-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="fb100-197">Il [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL viene usato da un servizio di reindirizzamento basato su WFP per recuperare il record di reindirizzamento dalla connessione del pacchetto TCP/IP accettata, ad esempio il socket connesso per un socket TCP o un socket UDP, ad esempio, reindirizzato al relativo callout in modalità kernel registrato nei livelli di  **\_ \_ Reindirizzamento di ale Connect** in un driver in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="fb100-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="fb100-198">Il [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL recupera il contesto di reindirizzamento per un record di reindirizzamento, che viene usato.</span><span class="sxs-lookup"><span data-stu-id="fb100-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="fb100-199">Il contesto di reindirizzamento è facoltativo e viene usato se lo stato del reindirizzamento corrente di una connessione è che la connessione è stata reindirizzata dal servizio di reindirizzamento chiamante oppure la connessione è stata reindirizzata in precedenza dal servizio di reindirizzamento chiamante, ma in seguito reindirizzato da un servizio di reindirizzamento diverso. Il servizio di reindirizzamento trasferisce il record di reindirizzamento recuperato al socket TCP usato per eseguire il proxy del contenuto originale usando il **set di dati di \_ Reindirizzamento della connessione sio set \_ WFP \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="fb100-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="fb100-200">Non è necessario che l'applicazione che chiama il **set di dati di reindirizzamento della connessione del set di \_ \_ \_ \_ \_ dati** per il comando IOCTL contenga il BLOB contenente il record di Reindirizzamento da impostare.</span><span class="sxs-lookup"><span data-stu-id="fb100-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="fb100-201">Si tratta di un BLOB opaco di dati che l'applicazione deve passare nuovamente al nuovo socket.</span><span class="sxs-lookup"><span data-stu-id="fb100-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="fb100-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb100-202">See also</span></span>

[<span data-ttu-id="fb100-203">**Opzioni di IPPROTO_IP socket**</span><span class="sxs-lookup"><span data-stu-id="fb100-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="fb100-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="fb100-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="fb100-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="fb100-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="fb100-206">**presa**</span><span class="sxs-lookup"><span data-stu-id="fb100-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="fb100-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="fb100-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="fb100-208">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="fb100-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="fb100-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="fb100-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="fb100-210">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="fb100-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="fb100-211">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="fb100-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="fb100-212">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="fb100-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
