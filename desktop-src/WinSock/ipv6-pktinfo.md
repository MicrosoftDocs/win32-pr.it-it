---
description: Consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione WSARecvMsg su un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Opzione socket IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306940"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="5ed0d-103">IPV6 \_ pktinfo socket-opzione</span><span class="sxs-lookup"><span data-stu-id="5ed0d-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="5ed0d-104">L' \_ opzione pktinfo socket IPv6 consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="5ed0d-105">Per eseguire una query sullo stato di questa opzione socket, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="5ed0d-106">Per impostare questa opzione, chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="5ed0d-107">Valore dell'opzione socket</span><span class="sxs-lookup"><span data-stu-id="5ed0d-107">Socket option value</span></span>

<span data-ttu-id="5ed0d-108">La costante che rappresenta l'opzione del socket è 19.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ed0d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ed0d-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="5ed0d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ed0d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ed0d-111">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed0d-112">Descrittore che identifica il socket.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="5ed0d-113">*livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed0d-114">Livello in corrispondenza del quale è definita l'opzione.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-114">The level at which the option is defined.</span></span> <span data-ttu-id="5ed0d-115">Usare **IPPROTO \_ IPv6** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ed0d-116">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed0d-117">Opzione socket per la quale ottenere o impostare il valore.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="5ed0d-118">Usare \_ pktinfo IPv6 per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5ed0d-119">*optVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed0d-120">Puntatore al buffer che contiene il valore per l'opzione da impostare.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="5ed0d-121">Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="5ed0d-122">Questo valore viene considerato come un valore booleano con 0 usato per indicare **false** (disabilitato) e un valore diverso da zero per indicare **true** (abilitato).</span><span class="sxs-lookup"><span data-stu-id="5ed0d-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="5ed0d-123">*optlen* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ed0d-124">Puntatore alla dimensione, in byte, del buffer *optVal* .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="5ed0d-125">Questa dimensione deve essere maggiore o uguale alla dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ed0d-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ed0d-126">Return value</span></span>

<span data-ttu-id="5ed0d-127">Se l'operazione viene completata correttamente, la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) o [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="5ed0d-128">Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5ed0d-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="5ed0d-129">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="5ed0d-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="5ed0d-130">Significato</span><span class="sxs-lookup"><span data-stu-id="5ed0d-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ed0d-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="5ed0d-132">Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="5ed0d-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="5ed0d-134">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="5ed0d-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="5ed0d-136">Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="5ed0d-137">Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="5ed0d-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="5ed0d-139">È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="5ed0d-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="5ed0d-141">Argomento fornito non valido.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-141">An invalid argument was supplied.</span></span> <span data-ttu-id="5ed0d-142">Questo errore viene restituito se il parametro *Level* è sconosciuto o non valido.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="5ed0d-143">In Windows Vista e versioni successive questo errore viene restituito anche se il socket si trovava in uno stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5ed0d-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="5ed0d-145">L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="5ed0d-146">Questo errore viene restituito se il parametro di *tipo* per il descrittore di socket passato al parametro *s* non è **Sock \_ DGRAM** o **Sock \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="5ed0d-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="5ed0d-148">Il descrittore non è un socket.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5ed0d-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ed0d-149">Remarks</span></span>

<span data-ttu-id="5ed0d-150">La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l' \_ opzione socket pktinfo IPv6 consente a un'applicazione di determinare se le informazioni sui pacchetti devono essere restituite dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)per un socket IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="5ed0d-151">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l' \_ opzione socket pktinfo IPv6 consente a un'applicazione di abilitare o disabilitare la restituzione di informazioni sui pacchetti mediante la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="5ed0d-152">Per \_ impostazione predefinita, l'opzione pktinfo IPv6 per un socket è disabilitata (impostata su **false**).</span><span class="sxs-lookup"><span data-stu-id="5ed0d-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="5ed0d-153">Quando questa opzione socket è abilitata in un socket IPv6 di **tipo Sock \_ DGRAM** o **Sock \_ RAW**, la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisce informazioni sui pacchetti nella struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) a cui punta il parametro *lpMsg* .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="5ed0d-154">Uno degli oggetti dati del controllo nella struttura **WSAMSG** restituita conterrà una [**struttura \_ pktinfo IN6**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilizzata per archiviare le informazioni relative all'indirizzo del pacchetto ricevuto.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="5ed0d-155">Per i datagrammi ricevuti dalla funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) su IPv6, il membro del **controllo** della struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) ricevuta conterrà una struttura [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) che contiene una struttura **WSACMSGHDR** .</span><span class="sxs-lookup"><span data-stu-id="5ed0d-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="5ed0d-156">Il membro del **\_ livello cmsg** di questa struttura **WSACMSGHDR** conterrà **IPPROTO \_ IPv6**, il membro di **\_ tipo cmsg** di questa struttura conterrà **IPv6 \_ pktinfo** e il membro **\_ dati cmsg** conterrebbe una struttura IN6 [**\_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilizzata per archiviare le informazioni sull'indirizzo del pacchetto IPv6 ricevute.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="5ed0d-157">L'indirizzo IPv6 nella struttura **\_ pktinfo di IN6** è l'indirizzo IPv6 dal quale è stato ricevuto il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="5ed0d-158">Per un socket di datagramma a doppio stack, se un'applicazione richiede che la funzione [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) restituisca informazioni sui pacchetti in una struttura [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) per datagrammi ricevuti su IPv4, l'opzione socket [IP \_ pktinfo](ip-pktinfo.md) deve essere impostata su true nel socket.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="5ed0d-159">Se solo l' \_ opzione pktinfo IPv6 è impostata su true nel socket, le informazioni sui pacchetti verranno fornite per i datagrammi ricevuti su IPv6, ma potrebbero non essere fornite per datagrammi ricevuti tramite IPv4.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="5ed0d-160">Si noti che il file di intestazione *Ws2ipdef. h* viene incluso automaticamente in *Ws2tcpip. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="5ed0d-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ed0d-161">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ed0d-161">Requirements</span></span>



| <span data-ttu-id="5ed0d-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ed0d-162">Requirement</span></span> | <span data-ttu-id="5ed0d-163">Valore</span><span class="sxs-lookup"><span data-stu-id="5ed0d-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ed0d-164">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed0d-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5ed0d-165">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="5ed0d-166">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ed0d-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5ed0d-167">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ed0d-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ed0d-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ed0d-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ed0d-169"><dt>Ws2ipdef. h (include Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ed0d-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ed0d-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ed0d-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ed0d-171">Socket dual stack</span><span class="sxs-lookup"><span data-stu-id="5ed0d-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="5ed0d-172">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="5ed0d-173">**\_pktinfo IN6**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="5ed0d-174">\_pktinfo IP</span><span class="sxs-lookup"><span data-stu-id="5ed0d-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="5ed0d-175">**\_Opzioni socket IPv6 IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="5ed0d-176">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="5ed0d-177">**presa**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="5ed0d-178">**WSAMSG**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="5ed0d-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span><span class="sxs-lookup"><span data-stu-id="5ed0d-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
