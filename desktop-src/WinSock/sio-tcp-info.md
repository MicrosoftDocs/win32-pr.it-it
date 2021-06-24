---
description: Il codice di controllo recupera Transmission Control Protocol statistiche (TCP) per un socket specificato.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO codice di controllo
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f6076440f117ed287ad544c308e574454f33e2b7
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587794"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="ad468-103">SIO_TCP_INFO codice di controllo</span><span class="sxs-lookup"><span data-stu-id="ad468-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="ad468-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad468-104">Description</span></span>

<span data-ttu-id="ad468-105">Il **codice di controllo \_ SIO TCP \_ INFO** recupera le statistiche Transmission Control Protocol (TCP) per un socket specificato.</span><span class="sxs-lookup"><span data-stu-id="ad468-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="ad468-106">Per eseguire questa operazione, chiamare la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad468-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="ad468-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad468-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="ad468-108">s</span><span class="sxs-lookup"><span data-stu-id="ad468-108">s</span></span>

<span data-ttu-id="ad468-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="ad468-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="ad468-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="ad468-110">dwIoControlCode</span></span>

<span data-ttu-id="ad468-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ad468-111">The control code for the operation.</span></span>
<span data-ttu-id="ad468-112">Usare **SIO \_ TCP \_ INFO** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="ad468-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="ad468-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad468-113">lpvInBuffer</span></span>

<span data-ttu-id="ad468-114">Puntatore al buffer di input.</span><span class="sxs-lookup"><span data-stu-id="ad468-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="ad468-115">Questo parametro contiene un puntatore a **un valore DWORD** che specifica la versione del codice di controllo **SIO TCP \_ \_ INFO** in uso.</span><span class="sxs-lookup"><span data-stu-id="ad468-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="ad468-116">Specificare 0 per [usare](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)TCP_INFO_v0 .</span><span class="sxs-lookup"><span data-stu-id="ad468-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="ad468-117">Specificare 1 per [usare](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)TCP_INFO_v1 , che fornisce più campi.</span><span class="sxs-lookup"><span data-stu-id="ad468-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which provides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="ad468-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="ad468-118">cbInBuffer</span></span>

<span data-ttu-id="ad468-119">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="ad468-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="ad468-120">Questo parametro deve essere la dimensione del **tipo di dati DWORD.**</span><span class="sxs-lookup"><span data-stu-id="ad468-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="ad468-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad468-121">lpvOutBuffer</span></span>

<span data-ttu-id="ad468-122">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="ad468-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="ad468-123">In caso di esito positivo, questo parametro contiene un puntatore a [**una TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) contenente le statistiche TCP per il socket specificato.</span><span class="sxs-lookup"><span data-stu-id="ad468-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="ad468-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="ad468-124">cbOutBuffer</span></span>

<span data-ttu-id="ad468-125">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="ad468-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="ad468-126">Questo parametro deve avere almeno le dimensioni della [**struttura**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) TCP_INFO_v0.</span><span class="sxs-lookup"><span data-stu-id="ad468-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="ad468-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="ad468-127">lpcbBytesReturned</span></span>

<span data-ttu-id="ad468-128">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="ad468-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="ad468-129">Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) restituisce [**WSAEINVAL**](windows-sockets-error-codes-2.md)e il parametro *lpcbBytesReturned* punta a un valore **DWORD** pari a zero.</span><span class="sxs-lookup"><span data-stu-id="ad468-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="ad468-130">Se *lpOverlapped* è **NULL,** il **valore DWORD** a cui punta il *parametro lpcbBytesReturned* restituito in una chiamata riuscita non può essere zero.</span><span class="sxs-lookup"><span data-stu-id="ad468-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="ad468-131">Se il *parametro lpOverlapped* non è **NULL** per i socket sovrapposti, le operazioni che non possono essere completate immediatamente verranno avviate e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="ad468-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="ad468-132">Il **valore DWORD** a cui punta il *parametro lpcbBytesReturned* restituito può essere zero perché le dimensioni dei dati archiviati non possono essere determinate fino al completamento dell'operazione sovrapposta.</span><span class="sxs-lookup"><span data-stu-id="ad468-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="ad468-133">Lo stato di completamento finale può essere recuperato quando viene segnalato il metodo di completamento appropriato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ad468-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="ad468-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="ad468-134">lpvOverlapped</span></span>

<span data-ttu-id="ad468-135">Puntatore a una [**struttura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)</span><span class="sxs-lookup"><span data-stu-id="ad468-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad468-136">Se socket *s è* stato creato senza l'attributo sovrapposto, il *parametro lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="ad468-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="ad468-137">Se *s è* stato aperto con l'attributo sovrapposto e il parametro *lpOverlapped* non è **NULL,** l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="ad468-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="ad468-138">In questo caso, *il parametro lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="ad468-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="ad468-139">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente e il metodo di completamento appropriato viene segnalato al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ad468-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="ad468-140">In caso contrario, la funzione non restituisce finché l'operazione non è stata completata o non si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ad468-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="ad468-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="ad468-141">lpCompletionRoutine</span></span>

<span data-ttu-id="ad468-142">Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="ad468-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="ad468-143">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="ad468-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="ad468-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="ad468-144">lpThreadId</span></span>

<span data-ttu-id="ad468-145">Puntatore a una [**struttura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere utilizzata dal provider in una chiamata successiva a [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)</span><span class="sxs-lookup"><span data-stu-id="ad468-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="ad468-146">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore allo stesso) fino a quando non viene restituita [**la funzione WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)</span><span class="sxs-lookup"><span data-stu-id="ad468-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="ad468-147">**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**</span><span class="sxs-lookup"><span data-stu-id="ad468-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="ad468-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="ad468-148">lpErrno</span></span>

<span data-ttu-id="ad468-149">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ad468-149">A pointer to the error code.</span></span>

<span data-ttu-id="ad468-150">**Nota**  Questo parametro si applica solo alla **funzione WSPIoctl.**</span><span class="sxs-lookup"><span data-stu-id="ad468-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="ad468-151">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad468-151">Return value</span></span>

<span data-ttu-id="ad468-152">Se l'operazione viene completata correttamente, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="ad468-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="ad468-153">Se l'operazione ha esito negativo o è in sospeso, la [**funzione WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce **SOCKET \_ ERROR**.</span><span class="sxs-lookup"><span data-stu-id="ad468-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="ad468-154">Per ottenere informazioni estese sugli errori, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="ad468-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="ad468-155">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="ad468-155">Error code</span></span> | <span data-ttu-id="ad468-156">Significato</span><span class="sxs-lookup"><span data-stu-id="ad468-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="ad468-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="ad468-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="ad468-158">Il puntatore al buffer di input **era NULL** o la dimensione specificata del buffer di input non era corretta.</span><span class="sxs-lookup"><span data-stu-id="ad468-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="ad468-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="ad468-159">**WSAEINVAL**</span></span> | <span data-ttu-id="ad468-160">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="ad468-160">An invalid argument was supplied.</span></span> <span data-ttu-id="ad468-161">Questo errore viene restituito se il *parametro dwIoControlCode* non è un comando valido o se un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="ad468-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="ad468-162">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad468-162">Remarks</span></span>

<span data-ttu-id="ad468-163">A differenza del recupero di statistiche TCP con la [**funzione GetPerTcpConnectionEStats,**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) il recupero delle statistiche TCP con questo codice di controllo non richiede che il codice utente carichi, archivi e filtri la tabella di connessione TCP e non richieda privilegi elevati per l'uso.</span><span class="sxs-lookup"><span data-stu-id="ad468-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="ad468-164">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ad468-164">See also</span></span>

[<span data-ttu-id="ad468-165">Socket</span><span class="sxs-lookup"><span data-stu-id="ad468-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="ad468-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="ad468-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="ad468-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="ad468-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="ad468-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="ad468-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="ad468-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="ad468-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="ad468-170">**Wsaioctl**</span><span class="sxs-lookup"><span data-stu-id="ad468-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="ad468-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="ad468-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="ad468-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="ad468-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="ad468-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="ad468-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
