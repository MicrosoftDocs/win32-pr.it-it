---
description: Il codice di controllo ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: Codice di controllo SIO_ADDRESS_LIST_QUERY
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315788"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="dd387-103">Codice di controllo SIO_ADDRESS_LIST_QUERY</span><span class="sxs-lookup"><span data-stu-id="dd387-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="dd387-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd387-104">Description</span></span>

<span data-ttu-id="dd387-105">Il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.</span><span class="sxs-lookup"><span data-stu-id="dd387-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="dd387-106">L'elenco di indirizzi varia in base alla famiglia di indirizzi e alcuni indirizzi sono esclusi dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="dd387-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="dd387-107">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="dd387-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="dd387-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dd387-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="dd387-109">s</span><span class="sxs-lookup"><span data-stu-id="dd387-109">s</span></span>

<span data-ttu-id="dd387-110">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="dd387-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="dd387-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="dd387-111">dwIoControlCode</span></span>

<span data-ttu-id="dd387-112">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd387-112">The control code for the operation.</span></span>
<span data-ttu-id="dd387-113">Usare **la \_ \_ \_ query dell'elenco di indirizzi sio** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="dd387-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="dd387-114">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="dd387-114">lpvInBuffer</span></span>

<span data-ttu-id="dd387-115">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="dd387-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="dd387-116">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="dd387-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="dd387-117">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="dd387-117">cbInBuffer</span></span>

<span data-ttu-id="dd387-118">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="dd387-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="dd387-119">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="dd387-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="dd387-120">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dd387-120">lpvOutBuffer</span></span>

<span data-ttu-id="dd387-121">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="dd387-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="dd387-122">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="dd387-122">cbOutBuffer</span></span>

<span data-ttu-id="dd387-123">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="dd387-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="dd387-124">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="dd387-124">lpcbBytesReturned</span></span>

<span data-ttu-id="dd387-125">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="dd387-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="dd387-126">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="dd387-126">lpvOverlapped</span></span>

<span data-ttu-id="dd387-127">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="dd387-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dd387-128">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="dd387-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="dd387-129">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="dd387-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="dd387-130">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="dd387-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dd387-131">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="dd387-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="dd387-132">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="dd387-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="dd387-133">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="dd387-133">lpCompletionRoutine</span></span>

<span data-ttu-id="dd387-134">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="dd387-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="dd387-135">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="dd387-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="dd387-136">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="dd387-136">lpThreadId</span></span>

<span data-ttu-id="dd387-137">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="dd387-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="dd387-138">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="dd387-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="dd387-139">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dd387-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="dd387-140">lpErrno</span><span class="sxs-lookup"><span data-stu-id="dd387-140">lpErrno</span></span>

<span data-ttu-id="dd387-141">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="dd387-141">A pointer to the error code.</span></span>

<span data-ttu-id="dd387-142">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="dd387-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd387-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dd387-143">Return value</span></span>

<span data-ttu-id="dd387-144">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="dd387-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="dd387-145">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="dd387-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="dd387-146">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="dd387-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="dd387-147">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="dd387-147">Error code</span></span> | <span data-ttu-id="dd387-148">Significato</span><span class="sxs-lookup"><span data-stu-id="dd387-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="dd387-149">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="dd387-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="dd387-150">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="dd387-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="dd387-151">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="dd387-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="dd387-152">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **\_ Flush sio** .</span><span class="sxs-lookup"><span data-stu-id="dd387-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="dd387-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="dd387-153">**WSAEFAULT**</span></span> | <span data-ttu-id="dd387-154">Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="dd387-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="dd387-155">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="dd387-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="dd387-156">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="dd387-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="dd387-157">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="dd387-157">**WSAEINTR**</span></span> | <span data-ttu-id="dd387-158">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="dd387-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="dd387-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="dd387-159">**WSAEINVAL**</span></span> | <span data-ttu-id="dd387-160">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="dd387-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="dd387-161">Questo errore viene restituito se il parametro *cbInBuffer* non è impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="dd387-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="dd387-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="dd387-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="dd387-163">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dd387-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="dd387-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="dd387-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="dd387-165">Non è disponibile spazio nel buffer.</span><span class="sxs-lookup"><span data-stu-id="dd387-165">No buffer space available.</span></span> |
| <span data-ttu-id="dd387-166">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="dd387-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="dd387-167">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="dd387-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="dd387-168">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="dd387-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="dd387-169">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="dd387-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="dd387-170">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="dd387-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="dd387-171">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="dd387-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="dd387-172">Questo errore viene restituito se la **\_ query dell' \_ elenco \_ di indirizzi sio** non è supportata dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="dd387-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="dd387-173">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd387-173">Remarks</span></span>

<span data-ttu-id="dd387-174">La **\_ \_ \_ query elenco indirizzi sio** è supportata in Windows 2000 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dd387-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="dd387-175">Il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** ottiene un elenco degli indirizzi di trasporto locali della famiglia di protocolli del socket a cui l'applicazione può eseguire il binding.</span><span class="sxs-lookup"><span data-stu-id="dd387-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="dd387-176">L'elenco di indirizzi varia in base alla famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="dd387-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="dd387-177">Per la \_ famiglia di indirizzi AF INET6, vengono restituiti tutti gli indirizzi tranne i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd387-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="dd387-178">Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati (DAD) non è IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="dd387-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="dd387-179">Qualsiasi indirizzo IP con un livello di ambito inferiore a ScopeLevelSubnet su un'interfaccia in cui il tipo di interfaccia è **se \_ digitare \_ \_ loopback software**.</span><span class="sxs-lookup"><span data-stu-id="dd387-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="dd387-180">Questo significa che gli indirizzi locali di collegamento (FE80: \*) e loopback (:: 1) sulle interfacce di se il tipo di **\_ \_ \_ loopback software** sono esclusi, ma non se questi indirizzi si trovano su un'interfaccia con un tipo diverso.</span><span class="sxs-lookup"><span data-stu-id="dd387-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="dd387-181">Per la famiglia di indirizzi **AF \_ inet** , vengono restituiti tutti gli indirizzi tranne i seguenti:</span><span class="sxs-lookup"><span data-stu-id="dd387-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="dd387-182">Qualsiasi indirizzo IP in cui lo stato di rilevamento degli indirizzi duplicati (DAD) non è IpDadStatePreferred.</span><span class="sxs-lookup"><span data-stu-id="dd387-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="dd387-183">Qualsiasi indirizzo IP in un'interfaccia in cui il tipo di interfaccia è **se il \_ tipo di \_ \_ loopback** e il collegamento del software sono locali.</span><span class="sxs-lookup"><span data-stu-id="dd387-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="dd387-184">Questo significa che gli indirizzi locali rispetto al collegamento (169,254.*) e loopback (127.*) sulle interfacce di se il tipo di **\_ \_ \_ loopback software** è escluso, ma non se questi indirizzi si trovano su un'interfaccia con un tipo diverso.</span><span class="sxs-lookup"><span data-stu-id="dd387-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="dd387-185">Per ulteriori informazioni sullo stato di DAD, vedere la documentazione dell'helper IP sull' [**enumerazione \_ \_ dello stato IP DAD**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) e la struttura degli [**\_ \_ \_ indirizzi unicast dell'adapter IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e la documentazione MIB sulla struttura di [**\_ \_ riga MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .</span><span class="sxs-lookup"><span data-stu-id="dd387-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="dd387-186">Per ulteriori informazioni sul tipo di interfaccia, vedere la documentazione dell'helper IP sulla struttura degli [**\_ \_ indirizzi IP dell'adapter**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e la funzione [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e la documentazione MIB in [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) struttura.</span><span class="sxs-lookup"><span data-stu-id="dd387-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="dd387-187">Per ulteriori informazioni sul livello di ambito, vedere la documentazione dell'helper IP sulla struttura [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e l'enumerazione [**a \_ livello di ambito**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .</span><span class="sxs-lookup"><span data-stu-id="dd387-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="dd387-188">L'elenco restituito nel buffer di output a cui fa riferimento il parametro *lpvOutBuffer* è nel formato di una struttura dell' [**elenco di \_ indirizzi \_ del socket**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .</span><span class="sxs-lookup"><span data-stu-id="dd387-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="dd387-189">Se il buffer di output specificato nel parametro *lpvOutBuffer* non è sufficientemente grande da contenere l'elenco indirizzi, viene restituito un **\_ errore socket** come risultato di questo IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [WSAEFAULT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="dd387-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="dd387-190">La dimensione richiesta, in byte, per il buffer di output viene restituita nel parametro *lpcbBytesReturned* in questo caso.</span><span class="sxs-lookup"><span data-stu-id="dd387-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="dd387-191">Si noti che il codice di errore [WSAEFAULT](windows-sockets-error-codes-2.md) viene restituito anche se il parametro *lpvInBuffer*, *lpvOutBuffer* o *lpcbBytesReturned* non è completamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="dd387-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="dd387-192">La **\_ query di \_ elenco \_ indirizzi sio** viene in genere chiamata in modo sincrono con il parametro *lpvOverlapped* impostato su **null**, perché l'elenco di indirizzi viene restituito immediatamente.</span><span class="sxs-lookup"><span data-stu-id="dd387-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="dd387-193">**Nota**  Negli ambienti plug-n-Play di Windows gli indirizzi possono essere aggiunti e rimossi dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="dd387-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="dd387-194">Pertanto, le applicazioni non possono basarsi sulle informazioni restituite dalla **\_ query dell' \_ elenco \_ di indirizzi sio** per essere persistenti.</span><span class="sxs-lookup"><span data-stu-id="dd387-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="dd387-195">Le applicazioni possono registrarsi per le notifiche di modifica degli indirizzi tramite l' **\_ elenco indirizzi sio \_ \_ modificare** IOCTL, che fornisce la notifica tramite l'evento di **\_ \_ \_ modifica elenco indirizzi** I/o sovrapposto o FD.</span><span class="sxs-lookup"><span data-stu-id="dd387-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="dd387-196">La sequenza di azioni seguente può essere utilizzata per garantire che l'applicazione disponga sempre di informazioni sull'elenco di indirizzi correnti:</span><span class="sxs-lookup"><span data-stu-id="dd387-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="dd387-197">Rilasciare l' **\_ elenco indirizzi \_ sio \_ modificare** IOCTL</span><span class="sxs-lookup"><span data-stu-id="dd387-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="dd387-198">Eseguire la **\_ query dell' \_ elenco \_ di indirizzi sio**</span><span class="sxs-lookup"><span data-stu-id="dd387-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="dd387-199">Ogni volta che l' **\_ elenco di indirizzi sio \_ \_ modifica** la chiamata IOCTL, informa l'applicazione di una modifica dell'elenco di indirizzi (tramite i/o sovrapposti o segnalando l'evento di modifica dell' **\_ \_ elenco \_ di indirizzi FD** ), l'intera sequenza di azioni deve essere ripetuta.</span><span class="sxs-lookup"><span data-stu-id="dd387-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="dd387-200">In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è stata modificata e il codice di controllo della **\_ query dell' \_ elenco \_ di indirizzi sio** è definito nel file di intestazione *Ws2def. h* .</span><span class="sxs-lookup"><span data-stu-id="dd387-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="dd387-201">Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="dd387-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd387-202">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dd387-202">See also</span></span>

[<span data-ttu-id="dd387-203">**GetAdaptersAddresses**</span><span class="sxs-lookup"><span data-stu-id="dd387-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="dd387-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="dd387-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="dd387-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="dd387-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="dd387-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="dd387-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="dd387-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="dd387-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="dd387-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="dd387-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="dd387-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="dd387-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="dd387-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="dd387-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="dd387-211">**presa**</span><span class="sxs-lookup"><span data-stu-id="dd387-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="dd387-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="dd387-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="dd387-213">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="dd387-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="dd387-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="dd387-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="dd387-215">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="dd387-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="dd387-216">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="dd387-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="dd387-217">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="dd387-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
