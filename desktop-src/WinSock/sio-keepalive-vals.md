---
description: Il codice di controllo Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: Codice di controllo SIO_KEEPALIVE_VALS
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131019"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="32ed7-103">Codice di controllo SIO_KEEPALIVE_VALS</span><span class="sxs-lookup"><span data-stu-id="32ed7-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="32ed7-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32ed7-104">Description</span></span>

<span data-ttu-id="32ed7-105">Il codice di controllo **sio \_ KeepAlive \_ Vals** Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP.</span><span class="sxs-lookup"><span data-stu-id="32ed7-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="32ed7-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="32ed7-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="32ed7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="32ed7-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="32ed7-108">s</span><span class="sxs-lookup"><span data-stu-id="32ed7-108">s</span></span>

<span data-ttu-id="32ed7-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="32ed7-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="32ed7-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="32ed7-110">dwIoControlCode</span></span>

<span data-ttu-id="32ed7-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="32ed7-111">The control code for the operation.</span></span>
<span data-ttu-id="32ed7-112">Per questa operazione, usare **sio \_ KeepAlive \_** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="32ed7-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="32ed7-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="32ed7-113">lpvInBuffer</span></span>

<span data-ttu-id="32ed7-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="32ed7-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="32ed7-115">Questo parametro deve puntare a una struttura **TCP \_ KeepAlive** .</span><span class="sxs-lookup"><span data-stu-id="32ed7-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="32ed7-116">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="32ed7-116">cbInBuffer</span></span>

<span data-ttu-id="32ed7-117">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="32ed7-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="32ed7-118">Questo parametro deve essere uguale o maggiore della dimensione della struttura **TCP \_ KeepAlive** a cui punta il parametro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="32ed7-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="32ed7-119">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="32ed7-119">lpvOutBuffer</span></span>

<span data-ttu-id="32ed7-120">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="32ed7-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="32ed7-121">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="32ed7-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="32ed7-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="32ed7-122">cbOutBuffer</span></span>

<span data-ttu-id="32ed7-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="32ed7-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="32ed7-124">Questo parametro deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="32ed7-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="32ed7-125">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="32ed7-125">lpcbBytesReturned</span></span>

<span data-ttu-id="32ed7-126">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="32ed7-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="32ed7-127">Il parametro restituito punta a un valore **DWORD** pari a zero per questa operazione, poiché non è presente alcun output.</span><span class="sxs-lookup"><span data-stu-id="32ed7-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="32ed7-128">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="32ed7-128">lpvOverlapped</span></span>

<span data-ttu-id="32ed7-129">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="32ed7-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="32ed7-130">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="32ed7-131">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="32ed7-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="32ed7-132">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="32ed7-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="32ed7-133">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="32ed7-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="32ed7-134">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="32ed7-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="32ed7-135">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="32ed7-135">lpCompletionRoutine</span></span>

<span data-ttu-id="32ed7-136">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="32ed7-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="32ed7-137">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="32ed7-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="32ed7-138">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="32ed7-138">lpThreadId</span></span>

<span data-ttu-id="32ed7-139">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="32ed7-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="32ed7-140">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="32ed7-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="32ed7-141">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="32ed7-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="32ed7-142">lpErrno</span><span class="sxs-lookup"><span data-stu-id="32ed7-142">lpErrno</span></span>

<span data-ttu-id="32ed7-143">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="32ed7-143">A pointer to the error code.</span></span>

<span data-ttu-id="32ed7-144">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="32ed7-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="32ed7-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32ed7-145">Return value</span></span>

<span data-ttu-id="32ed7-146">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="32ed7-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="32ed7-147">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="32ed7-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="32ed7-148">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="32ed7-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="32ed7-149">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="32ed7-149">Error code</span></span> | <span data-ttu-id="32ed7-150">Significato</span><span class="sxs-lookup"><span data-stu-id="32ed7-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="32ed7-151">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="32ed7-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="32ed7-152">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="32ed7-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="32ed7-153">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="32ed7-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="32ed7-154">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando **IOCTL SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="32ed7-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="32ed7-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="32ed7-155">**WSAEFAULT**</span></span> | <span data-ttu-id="32ed7-156">Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="32ed7-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="32ed7-157">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="32ed7-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="32ed7-158">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="32ed7-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="32ed7-159">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="32ed7-159">**WSAEINTR**</span></span> | <span data-ttu-id="32ed7-160">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="32ed7-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="32ed7-161">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="32ed7-161">**WSAEINVAL**</span></span> | <span data-ttu-id="32ed7-162">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="32ed7-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="32ed7-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="32ed7-164">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="32ed7-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="32ed7-165">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="32ed7-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="32ed7-166">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="32ed7-167">Questo errore viene restituito per un socket di datagramma.</span><span class="sxs-lookup"><span data-stu-id="32ed7-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="32ed7-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="32ed7-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="32ed7-169">Il descrittore s non è un socket.</span><span class="sxs-lookup"><span data-stu-id="32ed7-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="32ed7-170">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="32ed7-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="32ed7-171">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="32ed7-172">Questo errore viene restituito se il provider di trasporto non supporta il IOCTL di **sio \_ KeepAlive \_** .</span><span class="sxs-lookup"><span data-stu-id="32ed7-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="32ed7-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="32ed7-173">Remarks</span></span>

<span data-ttu-id="32ed7-174">Il IOCTL di **sio \_ KeepAlive \_ Vals** è supportato in Windows 2000 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="32ed7-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="32ed7-175">Il codice di controllo **sio \_ KeepAlive \_ Vals** Abilita o Disabilita l'impostazione per connessione dell'opzione keep-alive TCP che specifica il timeout e l'intervallo keep-alive TCP utilizzati per i pacchetti keep-alive TCP.</span><span class="sxs-lookup"><span data-stu-id="32ed7-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="32ed7-176">Per ulteriori informazioni sull'opzione Keep-Alive, vedere la sezione 4.2.3.6 in requisiti per gli host Internet-livelli di comunicazione specificati in RFC 1122 disponibili sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="32ed7-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="32ed7-177">Questa risorsa può essere disponibile solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="32ed7-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="32ed7-178">Il parametro *lpvInBuffer* deve puntare a una struttura **TCP \_ KeepAlive** definita nel file di intestazione *MSTCPIP. h* .</span><span class="sxs-lookup"><span data-stu-id="32ed7-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="32ed7-179">Questa struttura viene definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="32ed7-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="32ed7-180">Il valore specificato nel membro **OnOff** determina se il keep-alive TCP è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="32ed7-181">Se il membro **OnOff** è impostato su un valore diverso da zero, viene abilitato TCP Keep-Alive e vengono utilizzati gli altri membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="32ed7-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="32ed7-182">Il membro **KeepAliveTime** specifica il timeout, in millisecondi, senza alcuna attività fino a quando non viene inviato il primo pacchetto keep-alive.</span><span class="sxs-lookup"><span data-stu-id="32ed7-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="32ed7-183">Il membro **keepAliveInterval** specifica l'intervallo in millisecondi tra l'invio di pacchetti keep-alive successivi in caso di ricezione di un riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="32ed7-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="32ed7-184">L'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , che corrisponde a una delle [**Opzioni di SOL_SOCKET Socket**](/windows/desktop/winsock/sol-socket-socket-options), può essere usata anche per abilitare o disabilitare il keep-alive TCP in una connessione, nonché per eseguire query sullo stato corrente di questa opzione.</span><span class="sxs-lookup"><span data-stu-id="32ed7-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="32ed7-185">Per eseguire una query sul fatto che il keep-alive TCP sia abilitato in un socket, è possibile chiamare la funzione getsockopt con l'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="32ed7-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="32ed7-186">Per abilitare o disabilitare il keep-alive TCP, è possibile chiamare la funzione **setsockopt** con l'opzione [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) .</span><span class="sxs-lookup"><span data-stu-id="32ed7-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="32ed7-187">Se il keep-alive TCP è abilitato con [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive, a meno che tali valori non siano stati modificati usando **sio \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="32ed7-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="32ed7-188">Il valore predefinito a livello di sistema del timeout keep-alive è controllabile tramite l'impostazione del registro di sistema [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) che accetta un valore in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32ed7-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="32ed7-189">Se la chiave non è impostata, il timeout keep-alive predefinito è 2 ore.</span><span class="sxs-lookup"><span data-stu-id="32ed7-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="32ed7-190">Il valore predefinito a livello di sistema dell'intervallo keep-alive è controllabile tramite l'impostazione del registro di sistema [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) che accetta un valore in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="32ed7-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="32ed7-191">Se la chiave non è impostata, l'intervallo keep-alive predefinito è di 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="32ed7-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="32ed7-192">In Windows Vista e versioni successive, il numero di probe Keep-Alive (ritrasmissioni dati) è impostato su 10 e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="32ed7-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="32ed7-193">In Windows Server 2003, Windows XP e Windows 2000, l'impostazione predefinita per numero di probe Keep-Alive è 5.</span><span class="sxs-lookup"><span data-stu-id="32ed7-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="32ed7-194">Il numero di probe Keep-Alive è controllabile tramite le impostazioni del registro di sistema **TcpMaxDataRetransmissions** e [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="32ed7-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="32ed7-195">Il numero di probe Keep-Alive è impostato sul valore più elevato tra i due valori della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="32ed7-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="32ed7-196">Se questo numero è 0, i probe Keep-Alive non verranno inviati.</span><span class="sxs-lookup"><span data-stu-id="32ed7-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="32ed7-197">Se questo numero è superiore a 255, viene impostato su 255.</span><span class="sxs-lookup"><span data-stu-id="32ed7-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="32ed7-198">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32ed7-198">See also</span></span>

<span data-ttu-id="32ed7-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="32ed7-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="32ed7-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="32ed7-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="32ed7-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="32ed7-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="32ed7-202">presa</span><span class="sxs-lookup"><span data-stu-id="32ed7-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="32ed7-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="32ed7-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="32ed7-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="32ed7-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="32ed7-205">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="32ed7-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="32ed7-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="32ed7-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="32ed7-207">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="32ed7-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="32ed7-208">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="32ed7-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="32ed7-209">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="32ed7-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
