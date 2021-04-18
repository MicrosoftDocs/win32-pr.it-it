---
description: Il codice di controllo consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: Codice di controllo SIO_RCVALL
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306903"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="1e369-103">Codice di controllo SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="1e369-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1e369-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e369-104">Description</span></span>
<span data-ttu-id="1e369-105">Il codice di controllo **sio \_ RCVALL** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="1e369-106">Per eseguire questa operazione, chiamare la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="1e369-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="1e369-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e369-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1e369-108">s</span><span class="sxs-lookup"><span data-stu-id="1e369-108">s</span></span>

<span data-ttu-id="1e369-109">Descrittore che identifica un socket.</span><span class="sxs-lookup"><span data-stu-id="1e369-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1e369-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="1e369-110">dwIoControlCode</span></span>

<span data-ttu-id="1e369-111">Codice di controllo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-111">The control code for the operation.</span></span>
<span data-ttu-id="1e369-112">Usare **sio \_ RCVALL** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1e369-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="1e369-113">lpvInBuffer</span></span>

<span data-ttu-id="1e369-114">Puntatore al buffer di input che deve contenere il valore dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="1e369-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="1e369-115">I valori possibili per l'opzione IOCTL **\_ RCVALL di sio** sono specificati nell'enumerazione **RCVALL_VALUE** definita nel file di intestazione *MSTCPIP. h* .</span><span class="sxs-lookup"><span data-stu-id="1e369-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="1e369-116">I valori possibili per **sio \_ RCVALL** sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e369-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="1e369-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1e369-117">Value</span></span> | <span data-ttu-id="1e369-118">Significato</span><span class="sxs-lookup"><span data-stu-id="1e369-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="1e369-119">**RCVALL \_ disattivato**</span><span class="sxs-lookup"><span data-stu-id="1e369-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="1e369-120">Disabilitare questa opzione in modo che un socket non riceva tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="1e369-121">**RCVALL \_**</span><span class="sxs-lookup"><span data-stu-id="1e369-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="1e369-122">Abilitare questa opzione per consentire a un socket di ricevere tutti i pacchetti IPv4 o IPv6 che passano attraverso un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="1e369-123">Questa opzione Abilita la modalità promiscua sulla scheda di interfaccia di rete (NIC) se la scheda di interfaccia di rete supporta la modalità promiscua.</span><span class="sxs-lookup"><span data-stu-id="1e369-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="1e369-124">In un segmento LAN con un hub di rete, una scheda di interfaccia di rete che supporta la modalità promiscua acquisisce tutto il traffico IPv4 o IPv6 sulla LAN, incluso il traffico tra altri computer nello stesso segmento LAN.</span><span class="sxs-lookup"><span data-stu-id="1e369-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="1e369-125">Tutti i pacchetti acquisiti (IPv4 o IPv6, a seconda del socket) verranno recapitati al socket non elaborato.</span><span class="sxs-lookup"><span data-stu-id="1e369-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="1e369-126">Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="1e369-127">Netmon usa la stessa modalità per l'interfaccia di rete, ma non usa questa opzione per acquisire il traffico.</span><span class="sxs-lookup"><span data-stu-id="1e369-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="1e369-128">**\_SOCKETLEVELONLY RCVALL**</span><span class="sxs-lookup"><span data-stu-id="1e369-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="1e369-129">Questa funzionalità non è attualmente implementata, pertanto l'impostazione di questa opzione non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1e369-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="1e369-130">**\_IPLEVEL RCVALL**</span><span class="sxs-lookup"><span data-stu-id="1e369-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="1e369-131">Abilitare questa opzione per consentire a un socket IPv4 o IPv6 di ricevere tutti i pacchetti a livello IP che passano attraverso un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="1e369-132">Questa opzione non Abilita la modalità promiscua nella scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="1e369-133">Questa opzione influiscono solo sull'elaborazione dei pacchetti a livello IP.</span><span class="sxs-lookup"><span data-stu-id="1e369-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="1e369-134">La scheda di interfaccia di rete riceve ancora solo i pacchetti indirizzati agli indirizzi unicast e multicast configurati.</span><span class="sxs-lookup"><span data-stu-id="1e369-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="1e369-135">Tuttavia, un socket con questa opzione abilitata riceverà non solo i pacchetti diretti a indirizzi IP specifici, ma riceverà tutti i pacchetti IPv4 o IPv6 ricevuti dalla scheda di interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="1e369-136">Questa opzione non consente di acquisire altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) ricevuti sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="1e369-137">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="1e369-137">cbInBuffer</span></span>

<span data-ttu-id="1e369-138">Dimensione, in byte, del buffer di input.</span><span class="sxs-lookup"><span data-stu-id="1e369-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="1e369-139">Questo parametro deve essere uguale o maggiore della dimensione del **RCVALL_VALUE** valore di enumerazione a cui punta il parametro *lpvInBuffer* .</span><span class="sxs-lookup"><span data-stu-id="1e369-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1e369-140">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1e369-140">lpvOutBuffer</span></span>

<span data-ttu-id="1e369-141">Puntatore al buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1e369-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="1e369-142">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1e369-143">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="1e369-143">cbOutBuffer</span></span>

<span data-ttu-id="1e369-144">Dimensione, in byte, del buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1e369-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="1e369-145">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1e369-146">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="1e369-146">lpcbBytesReturned</span></span>

<span data-ttu-id="1e369-147">Puntatore a una variabile che riceve le dimensioni, in byte, dei dati archiviati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="1e369-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="1e369-148">Questo parametro non è utilizzato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1e369-149">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="1e369-149">lpvOverlapped</span></span>

<span data-ttu-id="1e369-150">Puntatore a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .</span><span class="sxs-lookup"><span data-stu-id="1e369-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1e369-151">Se il socket *s* è stato creato senza l'attributo Overlapped, il parametro *lpOverlapped* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="1e369-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1e369-152">Se *s* è stato aperto con l'attributo Overlapped e il parametro *LpOverlapped* non è **null**, l'operazione viene eseguita come operazione sovrapposta (asincrona).</span><span class="sxs-lookup"><span data-stu-id="1e369-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1e369-153">In questo caso, il parametro *lpOverlapped* deve puntare a una struttura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) valida.</span><span class="sxs-lookup"><span data-stu-id="1e369-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1e369-154">Per le operazioni sovrapposte, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce immediatamente un risultato e il metodo di completamento appropriato viene segnalato al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1e369-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1e369-155">In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="1e369-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1e369-156">Il lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1e369-156">lpCompletionRoutine</span></span>

<span data-ttu-id="1e369-157">Tipo: \_ in_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1e369-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1e369-158">Puntatore alla routine di completamento chiamata quando l'operazione è stata completata (ignorata per i socket non sovrapposti).</span><span class="sxs-lookup"><span data-stu-id="1e369-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1e369-159">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="1e369-159">lpThreadId</span></span>

<span data-ttu-id="1e369-160">Puntatore a una struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) che deve essere usata dal provider in una chiamata successiva a [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span><span class="sxs-lookup"><span data-stu-id="1e369-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1e369-161">Il provider deve archiviare la struttura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a cui si fa riferimento (non il puntatore alla stessa) finché non viene restituito il risultato della funzione [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) .</span><span class="sxs-lookup"><span data-stu-id="1e369-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1e369-162">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1e369-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1e369-163">lpErrno</span><span class="sxs-lookup"><span data-stu-id="1e369-163">lpErrno</span></span>

<span data-ttu-id="1e369-164">Puntatore al codice di errore.</span><span class="sxs-lookup"><span data-stu-id="1e369-164">A pointer to the error code.</span></span>

<span data-ttu-id="1e369-165">**Nota**  Questo parametro è valido solo per la funzione **WSPIoctl** .</span><span class="sxs-lookup"><span data-stu-id="1e369-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1e369-166">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e369-166">Return value</span></span>

<span data-ttu-id="1e369-167">Se l'operazione viene completata correttamente, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="1e369-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1e369-168">Se l'operazione ha esito negativo o è in sospeso, la funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** restituisce un **\_ errore socket**.</span><span class="sxs-lookup"><span data-stu-id="1e369-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1e369-169">Per ottenere informazioni estese sull'errore, chiamare [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1e369-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1e369-170">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="1e369-170">Error code</span></span> | <span data-ttu-id="1e369-171">Significato</span><span class="sxs-lookup"><span data-stu-id="1e369-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="1e369-172">**\_io WSA \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="1e369-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1e369-173">Un'operazione sovrapposta è stata avviata correttamente e il completamento verrà indicato in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="1e369-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1e369-174">**\_operazione WSA \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="1e369-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1e369-175">Un'operazione sovrapposta è stata annullata a causa della chiusura del socket o dell'esecuzione del comando IOCTL **SIO_FLUSH** .</span><span class="sxs-lookup"><span data-stu-id="1e369-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="1e369-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1e369-176">**WSAEFAULT**</span></span> | <span data-ttu-id="1e369-177">Il parametro *lpOverlapped* o *il lpCompletionRoutine* non è interamente contenuto in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="1e369-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1e369-178">**WSAEINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="1e369-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1e369-179">La funzione viene richiamata quando è in corso un callback.</span><span class="sxs-lookup"><span data-stu-id="1e369-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1e369-180">**WSAEINTR**</span><span class="sxs-lookup"><span data-stu-id="1e369-180">**WSAEINTR**</span></span> | <span data-ttu-id="1e369-181">Un'operazione di blocco è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="1e369-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1e369-182">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="1e369-182">**WSAEINVAL**</span></span> | <span data-ttu-id="1e369-183">Il parametro *dwIoControlCode* non è un comando valido oppure un parametro di input specificato non è accettabile oppure il comando non è applicabile al tipo di socket specificato.</span><span class="sxs-lookup"><span data-stu-id="1e369-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="1e369-184">Questo errore viene restituito anche se il parametro *cbInBuffer* è minore di `sizeof(UCHAR)` o il parametro *lpvInBuffer* punta a un valore che non è un valore di enumerazione **RCVALL_VALUE** .</span><span class="sxs-lookup"><span data-stu-id="1e369-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="1e369-185">Questo errore può essere restituito anche se non è possibile trovare l'interfaccia di rete associata al socket.</span><span class="sxs-lookup"><span data-stu-id="1e369-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="1e369-186">Questo problema può verificarsi se l'interfaccia di rete associata al socket viene eliminata o rimossa (ad esempio, un dispositivo di rete USB Remove PCMCIA o USB).</span><span class="sxs-lookup"><span data-stu-id="1e369-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="1e369-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1e369-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="1e369-188">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1e369-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="1e369-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="1e369-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="1e369-190">Non è disponibile spazio nel buffer.</span><span class="sxs-lookup"><span data-stu-id="1e369-190">No buffer space available.</span></span> |
| <span data-ttu-id="1e369-191">**WSAENOPROTOOPT**</span><span class="sxs-lookup"><span data-stu-id="1e369-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="1e369-192">L'opzione socket non è supportata nel protocollo specificato.</span><span class="sxs-lookup"><span data-stu-id="1e369-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="1e369-193">**WSAENOTSOCK**</span><span class="sxs-lookup"><span data-stu-id="1e369-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1e369-194">Il descrittore *s* non è un socket.</span><span class="sxs-lookup"><span data-stu-id="1e369-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="1e369-195">**ILWSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="1e369-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1e369-196">Il comando IOCTL specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="1e369-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="1e369-197">Questo errore viene restituito se l' **IOCTL \_ RCVALL di sio** non è supportato dal provider di trasporto.</span><span class="sxs-lookup"><span data-stu-id="1e369-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1e369-198">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e369-198">Remarks</span></span>

<span data-ttu-id="1e369-199">L' **IOCTL \_ RCVALL sio** è supportato in Windows 2000 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1e369-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="1e369-200">L' **IOCTL \_ RCVALL di sio** consente a un socket di ricevere tutti i pacchetti IPv4 o IPv6 in un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="1e369-201">L'handle del socket passato alla funzione [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) o **WSPIoctl** deve essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e369-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="1e369-202">Un socket IPv4 creato con la famiglia di indirizzi impostata su AF_INET, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IP.</span><span class="sxs-lookup"><span data-stu-id="1e369-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="1e369-203">Socket IPv6 creato con la famiglia di indirizzi impostata su AF_INET6, il tipo di socket impostato su SOCK_RAW e il protocollo impostato su IPPROTO_IPV6.</span><span class="sxs-lookup"><span data-stu-id="1e369-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="1e369-204">Per ulteriori informazioni sui socket non elaborati, vedere [**TCP/IP raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="1e369-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="1e369-205">Il socket deve anche essere associato a un'interfaccia IPv4 o IPv6 locale esplicita, il che significa che non è possibile eseguire l'associazione a **inaddr \_ any** o **in6addr \_ any**.</span><span class="sxs-lookup"><span data-stu-id="1e369-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="1e369-206">Una volta che il socket è stato associato e l'IOCTL viene completato correttamente, le chiamate alle funzioni [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) o [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv) restituiscono datagrammi IPv4 che passano attraverso l'interfaccia IPv4 specificata o restituiscono datagrammi IPv6 passando attraverso l'interfaccia IPv6 specificata.</span><span class="sxs-lookup"><span data-stu-id="1e369-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="1e369-207">Si noti che è necessario fornire un buffer sufficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="1e369-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="1e369-208">Impostando questo IOCTL, i pacchetti IPv4 o IPv6 vengono acquisiti solo su una determinata interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="1e369-209">Questo IOCTL non acquisisce altri pacchetti (ad esempio, i pacchetti ARP, IPX e NetBEUI) nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="1e369-210">Un socket associato a una specifica interfaccia locale con l' **IOCTL \_ RCVALL di sio** riceverà solo i pacchetti che passano attraverso tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="1e369-211">Non riceverà i pacchetti ricevuti su un'altra interfaccia e verrà inoltrato a un'altra interfaccia diversa da quella associata al socket **sio \_ RCVALL** .</span><span class="sxs-lookup"><span data-stu-id="1e369-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="1e369-212">In Windows Server 2008 e versioni precedenti, l'impostazione IOCTL **\_ RCVALL di sio** non acquisisce i pacchetti locali inviati da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="1e369-213">Sono stati inclusi i pacchetti ricevuti su un'altra interfaccia ed è stata inoltrata l'interfaccia di rete specificata per l'IOCTL **\_ RCVALL sio** .</span><span class="sxs-lookup"><span data-stu-id="1e369-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="1e369-214">In Windows 7 e Windows Server 2008 R2 questa operazione è stata modificata in modo da acquisire anche i pacchetti locali inviati da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="1e369-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="1e369-215">Sono inclusi i pacchetti ricevuti su un'altra interfaccia e quindi l'interfaccia di rete associata al socket con IOCTL **\_ RCVALL di sio** .</span><span class="sxs-lookup"><span data-stu-id="1e369-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="1e369-216">Per impostare questo IOCTL è necessario disporre dei privilegi di amministratore nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="1e369-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="1e369-217">Questa funzionalità viene talvolta definita modalità promiscua.</span><span class="sxs-lookup"><span data-stu-id="1e369-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="1e369-218">Qualsiasi modifica diretta rispetto all'applicazione di questa opzione su un'interfaccia e quindi a un'altra interfaccia con una singola chiamata che usa questo IOCTL non è supportata.</span><span class="sxs-lookup"><span data-stu-id="1e369-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="1e369-219">Un'applicazione deve innanzitutto utilizzare questo IOCTL per disattivare il comportamento sulla prima interfaccia e quindi utilizzare questo IOCTL per abilitare il comportamento su una nuova interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1e369-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e369-220">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e369-220">See also</span></span>

[<span data-ttu-id="1e369-221">**presa**</span><span class="sxs-lookup"><span data-stu-id="1e369-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1e369-222">**Socket TCP/IP raw**</span><span class="sxs-lookup"><span data-stu-id="1e369-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="1e369-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1e369-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="1e369-224">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="1e369-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1e369-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="1e369-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1e369-226">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="1e369-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1e369-227">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="1e369-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1e369-228">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="1e369-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
