---
description: Restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo utilizzati da un socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Opzione socket SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755058"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="a7195-103">\_ \_ Opzione socket stato BSP</span><span class="sxs-lookup"><span data-stu-id="a7195-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="a7195-104">L'opzione **so \_ BSP \_ state** socket restituisce l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket.</span><span class="sxs-lookup"><span data-stu-id="a7195-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="a7195-105">Per eseguire questa operazione, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="a7195-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="a7195-106">Valore dell'opzione socket</span><span class="sxs-lookup"><span data-stu-id="a7195-106">Socket option value</span></span>

<span data-ttu-id="a7195-107">La costante che rappresenta questa opzione socket è 0x1009.</span><span class="sxs-lookup"><span data-stu-id="a7195-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7195-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7195-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="a7195-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7195-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7195-110">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7195-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7195-111">Descrittore che identifica il socket.</span><span class="sxs-lookup"><span data-stu-id="a7195-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="a7195-112">*livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a7195-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7195-113">Livello in corrispondenza del quale è definita l'opzione.</span><span class="sxs-lookup"><span data-stu-id="a7195-113">The level at which the option is defined.</span></span> <span data-ttu-id="a7195-114">Usare **il \_ socket Sol** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a7195-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a7195-115">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7195-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7195-116">Opzione socket per la quale deve essere recuperato il valore.</span><span class="sxs-lookup"><span data-stu-id="a7195-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="a7195-117">Usare **così \_ \_ lo stato BSP** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="a7195-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a7195-118">*optVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a7195-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7195-119">Puntatore al buffer in cui deve essere restituito il valore per l'opzione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a7195-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="a7195-120">Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di una struttura [**di \_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="a7195-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a7195-121">*optlen* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a7195-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7195-122">Puntatore alla dimensione, in byte, del buffer *optVal* .</span><span class="sxs-lookup"><span data-stu-id="a7195-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="a7195-123">Questa dimensione deve essere maggiore o uguale alla dimensione di una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="a7195-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7195-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7195-124">Return value</span></span>

<span data-ttu-id="a7195-125">Se l'operazione viene completata correttamente, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="a7195-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="a7195-126">Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a7195-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="a7195-127">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="a7195-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="a7195-128">Significato</span><span class="sxs-lookup"><span data-stu-id="a7195-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7195-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="a7195-130">Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="a7195-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="a7195-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="a7195-132">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a7195-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="a7195-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="a7195-134">Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="a7195-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="a7195-135">Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di una struttura [**di \_ informazioni di CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="a7195-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="a7195-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="a7195-137">È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="a7195-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="a7195-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="a7195-139">Il parametro *Level* è sconosciuto o non valido.</span><span class="sxs-lookup"><span data-stu-id="a7195-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="a7195-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="a7195-141">L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.</span><span class="sxs-lookup"><span data-stu-id="a7195-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="a7195-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="a7195-143">Il descrittore non è un socket.</span><span class="sxs-lookup"><span data-stu-id="a7195-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a7195-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7195-144">Remarks</span></span>

<span data-ttu-id="a7195-145">La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **\_ \_ dello stato BSP** , recupera l'indirizzo locale, la porta locale, l'indirizzo remoto, la porta remota, il tipo di socket e il protocollo usati da un socket.</span><span class="sxs-lookup"><span data-stu-id="a7195-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="a7195-146">L'opzione per il socket di **\_ \_ stato BSP** è compatibile con i socket IPv6 o IPv4 (le famiglie di indirizzi **AF \_ INET6** e **AF \_ inet** ).</span><span class="sxs-lookup"><span data-stu-id="a7195-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="a7195-147">Se la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito positivo, le informazioni vengono restituite in una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) nel buffer a cui punta il parametro *optVal* .</span><span class="sxs-lookup"><span data-stu-id="a7195-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="a7195-148">Il numero intero a cui punta *optlen* deve contenere originariamente la dimensione del buffer. al ritorno, verrà impostato sulla lunghezza, in byte, del valore restituito nel parametro *optVal* .</span><span class="sxs-lookup"><span data-stu-id="a7195-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="a7195-149">I membri **iSocketType** e **iProtocol** nella struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita vengono compilati per il descrittore di socket nel parametro *s* .</span><span class="sxs-lookup"><span data-stu-id="a7195-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="a7195-150">Se il socket è in uno stato connesso o associato, il membro **LocalAddr** della struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita verrà impostato su una struttura [sockaddr](sockaddr-2.md) che rappresenta l'indirizzo e la porta locali.</span><span class="sxs-lookup"><span data-stu-id="a7195-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="a7195-151">Se il socket è in uno stato connesso, il membro **IndirizzoRemoto** della struttura di **\_ informazioni CSADDR** restituita verrà impostato su una struttura SOCKADDR che rappresenta l'indirizzo remoto e la porta.</span><span class="sxs-lookup"><span data-stu-id="a7195-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="a7195-152">Se il socket non si trova in uno stato connesso o associato, il membro **LocalAddr** della struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita viene restituito con un puntatore **null** nel membro **lpSockaddr** e il membro **iSockaddrLength** è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a7195-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="a7195-153">Se il socket non è in uno stato associato, il membro **IndirizzoRemoto** della struttura di **\_ informazioni CSADDR** restituita viene restituito con un **puntatore null** nel membro **lpSockaddr** e il membro **iSockaddrLength** impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a7195-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="a7195-154">Se la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ha esito negativo, i parametri *optVal* e *optlen* vengono lasciati invariati e il parametro *optVal* non punta a una struttura di [**\_ informazioni CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) restituita.</span><span class="sxs-lookup"><span data-stu-id="a7195-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="a7195-155">Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="a7195-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7195-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7195-156">Requirements</span></span>



| <span data-ttu-id="a7195-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7195-157">Requirement</span></span> | <span data-ttu-id="a7195-158">Valore</span><span class="sxs-lookup"><span data-stu-id="a7195-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7195-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7195-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a7195-160">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7195-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7195-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a7195-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a7195-162">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7195-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7195-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7195-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7195-164"><dt>Ws2def. h (include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7195-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7195-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7195-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7195-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="a7195-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="a7195-167">**\_informazioni CSADDR**</span><span class="sxs-lookup"><span data-stu-id="a7195-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="a7195-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="a7195-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
