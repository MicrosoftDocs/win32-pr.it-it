---
description: È progettato per consentire a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Opzione socket SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315776"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="5f2ce-103">\_Opzione socket KeepAlive</span><span class="sxs-lookup"><span data-stu-id="5f2ce-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="5f2ce-104">L'opzione per il socket **\_ KeepAlive** è progettata per consentire a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="5f2ce-105">Per eseguire una query sullo stato di questa opzione socket, chiamare la funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="5f2ce-106">Per impostare questa opzione, chiamare la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) con i parametri seguenti.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="5f2ce-107">Valore dell'opzione socket</span><span class="sxs-lookup"><span data-stu-id="5f2ce-107">Socket option value</span></span>

<span data-ttu-id="5f2ce-108">La costante che rappresenta questa opzione socket è 0x0008.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f2ce-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f2ce-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="5f2ce-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f2ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f2ce-111">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ce-112">Descrittore che identifica il socket.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="5f2ce-113">*livello* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ce-114">Livello in corrispondenza del quale è definita l'opzione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-114">The level at which the option is defined.</span></span> <span data-ttu-id="5f2ce-115">Usare **il \_ socket Sol** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f2ce-116">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ce-117">Opzione socket per la quale deve essere impostato il valore.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="5f2ce-118">Usare **così \_ KeepAlive** per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="5f2ce-119">*optVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ce-120">Puntatore al buffer che contiene il valore per l'opzione da impostare.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="5f2ce-121">Questo parametro deve puntare a un buffer uguale o maggiore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="5f2ce-122">Questo valore viene considerato come un valore booleano con 0 usato per indicare **false** (disabilitato) e un valore diverso da zero per indicare **true** (abilitato).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="5f2ce-123">*optlen* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5f2ce-124">Puntatore alla dimensione, in byte, del buffer *optVal* .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="5f2ce-125">Questa dimensione deve essere maggiore o uguale alla dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f2ce-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f2ce-126">Return value</span></span>

<span data-ttu-id="5f2ce-127">Se l'operazione viene completata correttamente, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) restituisce zero.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="5f2ce-128">Se l'operazione ha esito negativo, viene restituito un valore di \_ errore socket e un codice di errore specifico può essere recuperato chiamando [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="5f2ce-129">Codice di errore</span><span class="sxs-lookup"><span data-stu-id="5f2ce-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="5f2ce-130">Significato</span><span class="sxs-lookup"><span data-stu-id="5f2ce-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f2ce-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="5f2ce-132">Prima di utilizzare questa funzione, è necessario che venga eseguita una chiamata [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="5f2ce-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="5f2ce-134">Il sottosistema di rete non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="5f2ce-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="5f2ce-136">Uno dei parametri *optVal* o *optlen* punta alla memoria che non si trova in una parte valida dello spazio degli indirizzi utente.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="5f2ce-137">Questo errore viene restituito anche se il valore a cui punta il parametro *optlen* è minore della dimensione di un valore **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="5f2ce-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="5f2ce-139">È in corso una chiamata di blocco di Windows Sockets 1,1 o il provider di servizi sta ancora elaborando una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="5f2ce-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="5f2ce-141">Il parametro *Level* è sconosciuto o non valido.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="5f2ce-142">In Windows Vista e versioni successive questo errore viene restituito anche se il socket si trovava in uno stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="5f2ce-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="5f2ce-144">L'opzione è sconosciuta o non supportata dalla famiglia di protocolli indicata.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="5f2ce-145">Questo errore viene restituito se il descrittore di socket passato al parametro *s* era per un socket di datagramma.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="5f2ce-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="5f2ce-147">Il descrittore non è un socket.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="5f2ce-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f2ce-148">Remarks</span></span>

<span data-ttu-id="5f2ce-149">La funzione [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) chiamata con l'opzione di socket **Keep- \_ Alive** consente a un'applicazione di recuperare lo stato corrente dell'opzione KeepAlive, anche se questa funzionalità non viene normalmente utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="5f2ce-150">Se un'applicazione deve abilitare i pacchetti KeepAlive in un socket, viene semplicemente chiamata la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) per abilitare l'opzione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="5f2ce-151">La funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) chiamata con l'opzione di socket **\_ Keep** -Alive consente a un'applicazione di abilitare i pacchetti Keep-Alive per una connessione socket.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="5f2ce-152">Per impostazione predefinita, l'opzione **\_ Keep-Alive** per un socket è disabilitata (impostata su **false**).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="5f2ce-153">Quando questa opzione socket è abilitata, lo stack TCP invia pacchetti keep-alive quando non sono stati ricevuti pacchetti di dati o di riconoscimento per la connessione entro un intervallo.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="5f2ce-154">Per ulteriori informazioni sull'opzione Keep-Alive, vedere la sezione 4.2.3.6 in *requisiti per gli host Internet-livelli di comunicazione* specificati in RFC 1122 disponibili sul [sito Web IETF](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="5f2ce-155">Questa risorsa può essere disponibile solo in inglese.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="5f2ce-156">Questa **opzione \_** è valida solo per i protocolli che supportano il concetto di Keep-Alive (protocolli orientati alla connessione).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="5f2ce-157">Per TCP, il timeout keep-alive predefinito è 2 ore e l'intervallo keep-alive è di 1 secondo.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="5f2ce-158">Il numero predefinito di probe Keep-Alive varia in base alla versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="5f2ce-159">Il codice di controllo di [**sio \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) può essere usato per abilitare o disabilitare Keep-Alive e modificare il timeout e l'intervallo per una singola connessione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="5f2ce-160">Se Keep-Alive è abilitato con **così \_ KeepAlive**, le impostazioni TCP predefinite vengono usate per il timeout e l'intervallo keep-alive, a meno che tali valori non siano stati modificati usando **sio \_ KeepAlive \_ Vals**.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="5f2ce-161">Il valore predefinito a livello di sistema del timeout keep-alive è controllabile tramite l'impostazione del registro di sistema [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) che accetta un valore in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="5f2ce-162">Il valore predefinito a livello di sistema dell'intervallo keep-alive è controllabile tramite l'impostazione del registro di sistema [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) che accetta un valore in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="5f2ce-163">In Windows Vista e versioni successive, il numero di probe Keep-Alive (ritrasmissioni dati) è impostato su 10 e non può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="5f2ce-164">In Windows Server 2003, Windows XP e Windows 2000, l'impostazione predefinita per numero di probe Keep-Alive è 5.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="5f2ce-165">Il numero di probe Keep-Alive è controllabile tramite le impostazioni del registro di sistema [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) e [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="5f2ce-166">Il numero di probe Keep-Alive è impostato sul valore più elevato tra i due valori della chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="5f2ce-167">Se questo numero è 0, i probe Keep-Alive non verranno inviati.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="5f2ce-168">Se questo numero è superiore a 255, viene impostato su 255.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="5f2ce-169">In Windows Vista e versioni successive, l'opzione di socket **\_ Keep-Alive** può essere impostata solo utilizzando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket è in uno stato noto, non è uno stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="5f2ce-170">Per TCP, l'opzione di socket **\_ Keep-Alive** deve essere impostata prima di chiamare la funzione Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)o [**con WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) o dopo il completamento della richiesta di connessione.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="5f2ce-171">Se la funzione Connect è stata chiamata in modo asincrono, è necessario attendere il completamento della connessione prima di tentare di impostare l'opzione del socket **\_ Keep-Alive** .</span><span class="sxs-lookup"><span data-stu-id="5f2ce-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="5f2ce-172">Se un'applicazione tenta di impostare l'opzione di socket **\_ Keep-Alive** quando una richiesta di connessione è ancora in corso, la funzione **setsockopt** avrà esito negativo e restituirà [WSAEINVAL](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="5f2ce-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="5f2ce-173">In Windows Server 2003, Windows XP e Windows 2000 è possibile impostare l'opzione di socket **\_ Keep-Alive** utilizzando la funzione [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) quando il socket è uno stato di transizione (una richiesta di connessione è ancora in corso) e uno stato noto.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="5f2ce-174">Si noti che il file di intestazione *Ws2def. h* viene incluso automaticamente in *Winsock2. h* e non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="5f2ce-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f2ce-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f2ce-175">Requirements</span></span>



| <span data-ttu-id="5f2ce-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f2ce-176">Requirement</span></span> | <span data-ttu-id="5f2ce-177">Valore</span><span class="sxs-lookup"><span data-stu-id="5f2ce-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f2ce-178">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f2ce-178">Minimum supported client</span></span><br/> | <span data-ttu-id="5f2ce-179">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5f2ce-180">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f2ce-180">Minimum supported server</span></span><br/> | <span data-ttu-id="5f2ce-181">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f2ce-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5f2ce-182">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f2ce-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f2ce-183"><dt>Ws2def. h (include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f2ce-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f2ce-184">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f2ce-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f2ce-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="5f2ce-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="5f2ce-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="5f2ce-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="5f2ce-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5f2ce-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="5f2ce-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5f2ce-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="5f2ce-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5f2ce-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="5f2ce-190">**presa**</span><span class="sxs-lookup"><span data-stu-id="5f2ce-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="5f2ce-191">[**KeepAlive di SIO \_ \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f2ce-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="5f2ce-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5f2ce-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="5f2ce-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="5f2ce-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
