---
description: Il codice di controllo applica una o più impostazioni di trasporto a un socket.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: Codice di controllo SIO_APPLY_TRANSPORT_SETTING
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309933"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="a8dd5-103">Codice di controllo SIO_APPLY_TRANSPORT_SETTING</span><span class="sxs-lookup"><span data-stu-id="a8dd5-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="a8dd5-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8dd5-104">Description</span></span>

<span data-ttu-id="a8dd5-105">Il codice di controllo **sio \_ Applica \_ trasporto \_** applica una o più impostazioni di trasporto a un socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="a8dd5-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="a8dd5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8dd5-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a8dd5-108">s</span><span class="sxs-lookup"><span data-stu-id="a8dd5-108">s</span></span>

<span data-ttu-id="a8dd5-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a8dd5-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a8dd5-110">dwIoControlCode</span></span>

<span data-ttu-id="a8dd5-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-111">The control code for the operation.</span></span>
<span data-ttu-id="a8dd5-112">Usare **l' \_ \_ \_ impostazione applica trasporto sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a8dd5-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="a8dd5-113">lpvInBuffer</span></span>

<span data-ttu-id="a8dd5-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="a8dd5-115">Questo parametro contiene un puntatore a una struttura in cui il primo membro della struttura è una struttura [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) che determina quale impostazione di trasporto viene applicata.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a8dd5-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="a8dd5-116">cbInBuffer</span></span>

<span data-ttu-id="a8dd5-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="a8dd5-118">Questo parametro dipende dall'impostazione di trasporto applicata.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a8dd5-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a8dd5-119">lpvOutBuffer</span></span>

<span data-ttu-id="a8dd5-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="a8dd5-121">Questo parametro dipende dall'impostazione di trasporto applicata.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a8dd5-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="a8dd5-122">cbOutBuffer</span></span>

<span data-ttu-id="a8dd5-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a8dd5-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="a8dd5-124">lpcbBytesReturned</span></span>

<span data-ttu-id="a8dd5-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a8dd5-126">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *LpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a8dd5-127">Se *lpOverlapped* è **null**, il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito per una chiamata con esito positivo non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a8dd5-128">Se il parametro *lpOverlapped* non è **null** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a8dd5-129">Il valore **DWORD** a cui fa riferimento il parametro *lpcbBytesReturned* restituito può essere zero perché non è possibile determinare la dimensione dei dati archiviati finché l'operazione sovrapposta non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a8dd5-130">Lo stato di completamento finale può essere recuperato quando il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a8dd5-131">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="a8dd5-131">lpvOverlapped</span></span>

<span data-ttu-id="a8dd5-132">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a8dd5-133">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a8dd5-134">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a8dd5-135">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a8dd5-136">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a8dd5-137">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a8dd5-138">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a8dd5-138">lpCompletionRoutine</span></span>

<span data-ttu-id="a8dd5-139">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a8dd5-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a8dd5-140">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a8dd5-141">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="a8dd5-141">lpThreadId</span></span>

<span data-ttu-id="a8dd5-142">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="a8dd5-143">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="a8dd5-144">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a8dd5-145">lpErrno</span><span class="sxs-lookup"><span data-stu-id="a8dd5-145">lpErrno</span></span>

<span data-ttu-id="a8dd5-146">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-146">A pointer to the error code.</span></span>

<span data-ttu-id="a8dd5-147">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8dd5-148">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a8dd5-148">Return value</span></span>

<span data-ttu-id="a8dd5-149">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a8dd5-150">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a8dd5-151">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a8dd5-152">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="a8dd5-152">Error code</span></span> | <span data-ttu-id="a8dd5-153">Significato</span><span class="sxs-lookup"><span data-stu-id="a8dd5-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="a8dd5-154">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a8dd5-155">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="a8dd5-156">Questo valore viene restituito se un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a8dd5-157">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a8dd5-158">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="a8dd5-159">Questo errore viene restituito se un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL di **\_ scaricamento sio** .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="a8dd5-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-160">**WSAEFAULT**</span></span> | <span data-ttu-id="a8dd5-161">Il sistema ha rilevato un indirizzo puntatore non valido durante il tentativo di usare un argomento puntatore in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="a8dd5-162">Questo errore viene restituito dal parametro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a8dd5-163">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a8dd5-164">È in corso un'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="a8dd5-165">Questo errore viene restituito se la funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a8dd5-166">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-166">**WSAEINTR**</span></span> | <span data-ttu-id="a8dd5-167">Un'operazione di blocco è stata interrotta da una chiamata a [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="a8dd5-168">Questo errore viene restituito se un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a8dd5-169">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-169">**WSAEINVAL**</span></span> | <span data-ttu-id="a8dd5-170">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-170">An invalid argument was supplied.</span></span> <span data-ttu-id="a8dd5-171">Questo errore viene restituito se il parametro *dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile o se il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="a8dd5-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="a8dd5-173">Rete inattiva rilevata durante l'operazione del socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="a8dd5-174">Questo errore viene restituito se il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="a8dd5-175">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a8dd5-176">Si è tentato di eseguire un'operazione su un elemento che non è un socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="a8dd5-177">Questo errore viene restituito se il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a8dd5-178">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a8dd5-179">L'operazione tentata non è supportata per il tipo di oggetto a cui si fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="a8dd5-180">Questo errore viene restituito se il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="a8dd5-181">Questo errore viene restituito anche se l' **\_ impostazione applica \_ trasporto \_** IOCTL non è supportata dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a8dd5-182">Questo errore viene restituito anche quando viene eseguito un tentativo di usare l' **\_ impostazione del \_ trasporto \_ IOCTL Apply** per un socket diverso da UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a8dd5-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="a8dd5-183">Remarks</span></span>

<span data-ttu-id="a8dd5-184">L' **\_ \_ \_ impostazione sio applica trasporto** IOCTL è supportata in windows 8 e Windows Server 2012 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="a8dd5-185">L' **\_ \_ \_ impostazione sio applica trasporto** IOCTL è un IOCTL generico usato per applicare le impostazioni di trasporto al socket.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="a8dd5-186">L'impostazione di trasporto da applicare è basata sul [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="a8dd5-187">A partire da Windows 8 e Windows Server 2012, il sistema definisce la funzionalità **REAL_TIME_NOTIFICATION_CAPABILITY** su un socket TCP.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="a8dd5-188">A partire da Windows 10 e Windows Server 2016, viene definito anche il **\_ \_ contesto associato NAMERES** .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="a8dd5-189">Per ulteriori informazioni, vedere [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) e [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="a8dd5-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="a8dd5-190">Se il [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passato nel parametro lpvInBuffer ha il membro GUID impostato sulla **funzionalità di \_ \_ notifica in \_ tempo reale**, si tratta di una richiesta per applicare le impostazioni di notifica in tempo reale per il socket TCP usato con [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) per ricevere notifiche di rete in background in un'app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="a8dd5-191">Il parametro *lpvInBuffer* deve puntare a una struttura **REAL_TIME_NOTIFICATION_SETTING_INPUT** .</span><span class="sxs-lookup"><span data-stu-id="a8dd5-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="a8dd5-192">Il parametro *lpvOutBuffer* non è usato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="a8dd5-193">Questa impostazione del trasporto si applica solo ai socket TCP.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="a8dd5-194">Questa impostazione del trasporto fornisce un modo per WinInet o servizi di rete simili per contrassegnare un socket TCP specificato come [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) abilitato.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="a8dd5-195">Windows contrassegnerà il socket TCP corrispondente e configurerà le impostazioni hardware e software appropriate quando viene chiamata questa opzione.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="a8dd5-196">Un'applicazione Windows Store non chiamerà direttamente questo IOCTL.</span><span class="sxs-lookup"><span data-stu-id="a8dd5-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8dd5-197">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a8dd5-197">See also</span></span>

[<span data-ttu-id="a8dd5-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="a8dd5-199">presa</span><span class="sxs-lookup"><span data-stu-id="a8dd5-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a8dd5-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="a8dd5-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="a8dd5-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="a8dd5-203">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a8dd5-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a8dd5-205">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a8dd5-206">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a8dd5-207">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="a8dd5-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
