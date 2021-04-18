---
description: È progettato per consentire a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket in ascolto.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Opzione socket SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315777"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="8e720-103">\_ \_ Opzione socket Accept condizionale</span><span class="sxs-lookup"><span data-stu-id="8e720-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="8e720-104">L'opzione del socket **\_ \_ Accept condizionale** è progettata per consentire a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket di ascolto.</span><span class="sxs-lookup"><span data-stu-id="8e720-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="8e720-105">Valore dell'opzione socket</span><span class="sxs-lookup"><span data-stu-id="8e720-105">Socket option value</span></span>

<span data-ttu-id="8e720-106">La costante che rappresenta questa opzione socket è 0x3002.</span><span class="sxs-lookup"><span data-stu-id="8e720-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e720-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e720-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="8e720-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e720-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e720-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e720-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e720-110">Descrittore che identifica il socket.</span><span class="sxs-lookup"><span data-stu-id="8e720-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="8e720-111">*livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8e720-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e720-112">Livello in corrispondenza del quale è definita l'opzione.</span><span class="sxs-lookup"><span data-stu-id="8e720-112">The level at which the option is defined.</span></span> <span data-ttu-id="8e720-113">Usare **il \_ socket Sol** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8e720-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8e720-114">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e720-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e720-115">Opzione socket per la quale deve essere impostato il valore.</span><span class="sxs-lookup"><span data-stu-id="8e720-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="8e720-116">Usare **così \_ l' \_ accettazione condizionale** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="8e720-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="8e720-117">*optVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e720-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e720-118">Puntatore al buffer che contiene il valore per l'opzione da impostare.</span><span class="sxs-lookup"><span data-stu-id="8e720-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="8e720-119">Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8e720-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="8e720-120">Questo valore viene considerato come un valore booleano con 0 usato per indicare **false** (disabilitato) e un valore diverso da zero per indicare **true** (abilitato).</span><span class="sxs-lookup"><span data-stu-id="8e720-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="8e720-121">*optlen* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8e720-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e720-122">Puntatore alla dimensione, in byte, del buffer *optVal* .</span><span class="sxs-lookup"><span data-stu-id="8e720-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="8e720-123">Questa dimensione deve essere maggiore o uguale alla dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8e720-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e720-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e720-124">Return value</span></span>

<span data-ttu-id="8e720-125">Se l'operazione viene completata correttamente, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="8e720-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="8e720-126">Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8e720-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="8e720-127">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="8e720-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="8e720-128">Significato</span><span class="sxs-lookup"><span data-stu-id="8e720-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8e720-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="8e720-130">Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="8e720-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="8e720-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8e720-132">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8e720-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="8e720-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8e720-134">Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="8e720-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="8e720-135">Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="8e720-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="8e720-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8e720-137">È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="8e720-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="8e720-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="8e720-139">Il parametro *Level* è sconosciuto o non valido.</span><span class="sxs-lookup"><span data-stu-id="8e720-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="8e720-140">Questo errore viene restituito anche se il socket si trova già in uno stato di attesa.</span><span class="sxs-lookup"><span data-stu-id="8e720-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="8e720-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="8e720-142">L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.</span><span class="sxs-lookup"><span data-stu-id="8e720-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="8e720-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="8e720-144">Il descrittore non è un socket.</span><span class="sxs-lookup"><span data-stu-id="8e720-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="8e720-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e720-145">Remarks</span></span>

<span data-ttu-id="8e720-146">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione per il socket **\_ \_ Accept condizionale** consente a un'applicazione di decidere se accettare o meno una connessione in ingresso su un socket di ascolto.</span><span class="sxs-lookup"><span data-stu-id="8e720-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="8e720-147">Per impostazione predefinita, l'opzione Accept condizionale per un socket è disabilitata (impostata su **false**).</span><span class="sxs-lookup"><span data-stu-id="8e720-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="8e720-148">Quando questa opzione socket è abilitata, lo stack TCP non accetta automaticamente le connessioni.</span><span class="sxs-lookup"><span data-stu-id="8e720-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="8e720-149">Attende che l'applicazione indichi che accetta la connessione tramite il callback Accept condizionale registrato con la funzione [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) .</span><span class="sxs-lookup"><span data-stu-id="8e720-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="8e720-150">Una volta ricevuta una richiesta di connessione, Winsock richiama il callback Accept condizionale registrato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="8e720-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="8e720-151">Solo quando il callback Accept condizionale restituisce **CF \_ Accept** , Winsock notifica al trasporto di accettare completamente la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e720-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="8e720-152">Quando l'opzione per il socket **\_ \_ Accept condizionale** è impostata su Enabled (impostata su **true**), questo ha diversi effetti collaterali sul socket:</span><span class="sxs-lookup"><span data-stu-id="8e720-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="8e720-153">In questo modo vengono disabilitate le difese di protezione degli attacchi SYN predefinite dello stack TCP, perché l'applicazione sta assumendo la proprietà di accettare le connessioni.</span><span class="sxs-lookup"><span data-stu-id="8e720-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="8e720-154">In questo modo, il backlog di ascolto viene disabilitato perché non sono accettate connessioni per conto di un socket in ascolto.</span><span class="sxs-lookup"><span data-stu-id="8e720-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="8e720-155">Una connessione non viene mai completamente accettata finché l'applicazione non accetta completamente l'utilizzo del meccanismo di **\_ accettazione CF** .</span><span class="sxs-lookup"><span data-stu-id="8e720-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="8e720-156">Ciò significa anche che l'applicazione deve essere sempre in uno stato per gestire prontamente i callback Accept per accettare la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e720-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="8e720-157">Se l'applicazione è occupata da un'altra elaborazione, potrebbe verificarsi il timeout del lato client prima che l'applicazione accetti effettivamente la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e720-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="8e720-158">Questo comporta un'esperienza client scadente.</span><span class="sxs-lookup"><span data-stu-id="8e720-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="8e720-159">In genere, il motivo principale per cui le applicazioni utilizzano l'accettazione condizionale è quello di controllare la porta o l'indirizzo IP di origine utilizzato dal client che si connette, quindi decidere di accettare o rifiutare la connessione.</span><span class="sxs-lookup"><span data-stu-id="8e720-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="8e720-160">Tuttavia, è probabile che le prestazioni delle applicazioni siano migliori se l' \_ opzione di accettazione condizionale \_ non è abilitata e l'applicazione consente allo stack TCP e al backlog di ascolto di funzionare come previsto.</span><span class="sxs-lookup"><span data-stu-id="8e720-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="8e720-161">Quando l'applicazione gestisce la connessione accettata, se è da un indirizzo di origine IP o da una porta non corretta, l'applicazione può semplicemente chiudere il socket.</span><span class="sxs-lookup"><span data-stu-id="8e720-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="8e720-162">Lo svantaggio di sicurezza di questo comportamento è che ora il client è in grado di confermare che l'applicazione è in ascolto su un indirizzo IP e una porta poiché ha chiuso forzatamente la connessione accettata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="8e720-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="8e720-163">Tuttavia, gli svantaggi dell'abilitazione **dell' \_ \_ accettazione condizionale** sono in genere superiori a questa limitazione.</span><span class="sxs-lookup"><span data-stu-id="8e720-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="8e720-164">La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **\_ \_ Accept condizionale** consente a un'applicazione di recuperare lo stato corrente dell'opzione Accept condizionale, anche se questa funzionalità non viene normalmente utilizzata.</span><span class="sxs-lookup"><span data-stu-id="8e720-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="8e720-165">Se un'applicazione deve abilitare l'accettazione condizionale su un socket, viene semplicemente chiamata la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per abilitare l'opzione.</span><span class="sxs-lookup"><span data-stu-id="8e720-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="8e720-166">Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="8e720-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e720-167">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e720-167">Requirements</span></span>



| <span data-ttu-id="8e720-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e720-168">Requirement</span></span> | <span data-ttu-id="8e720-169">Valore</span><span class="sxs-lookup"><span data-stu-id="8e720-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e720-170">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e720-170">Minimum supported client</span></span><br/> | <span data-ttu-id="8e720-171">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e720-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8e720-172">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e720-172">Minimum supported server</span></span><br/> | <span data-ttu-id="8e720-173">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e720-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8e720-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e720-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e720-175"><dt>Ws2def. h (include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8e720-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e720-176">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8e720-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e720-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="8e720-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="8e720-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="8e720-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="8e720-179">**WSAAccept**</span><span class="sxs-lookup"><span data-stu-id="8e720-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




