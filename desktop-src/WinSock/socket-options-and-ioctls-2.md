---
description: Nella tabella seguente sono riepilogate alcune delle opzioni del socket per Windows Sockets 2.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opzioni socket e IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315766"
---
# <a name="socket-options-and-ioctls"></a><span data-ttu-id="b6628-103">Opzioni socket e IOCTL</span><span class="sxs-lookup"><span data-stu-id="b6628-103">Socket Options and IOCTLs</span></span>

<span data-ttu-id="b6628-104">Nella tabella seguente sono riepilogate alcune delle opzioni del socket per Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="b6628-104">Some of the socket options for Windows Sockets 2 are summarized in the following table.</span></span> <span data-ttu-id="b6628-105">Informazioni più dettagliate sono disponibili nella sezione 4 in [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) e/o [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b6628-105">More detailed information is provided in section 4 under [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) and/or [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)).</span></span> <span data-ttu-id="b6628-106">Sono disponibili altre nuove opzioni di socket specifiche del protocollo, che è possibile trovare nell'allegato Protocol-Specific.</span><span class="sxs-lookup"><span data-stu-id="b6628-106">There are other new protocol-specific socket options which can be found in the Protocol-Specific Annex.</span></span> <span data-ttu-id="b6628-107">Un elenco completo delle [**Opzioni di socket**](socket-options.md) per Windows Sockets è disponibile nella Guida di riferimento a Winsock.</span><span class="sxs-lookup"><span data-stu-id="b6628-107">A complete list of [**Socket Options**](socket-options.md) for Windows Sockets are available in the Winsock reference.</span></span>

<span data-ttu-id="b6628-108">Per un riepilogo di alcune delle IOCTL di Winsock, vedere [Riepilogo dei codici operativi IOCTL del socket](summary-of-socket-ioctl-opcodes-2.md).</span><span class="sxs-lookup"><span data-stu-id="b6628-108">For a a summary of some of the Winsock Ioctls, see [Summary of Socket Ioctl Opcodes](summary-of-socket-ioctl-opcodes-2.md).</span></span> <span data-ttu-id="b6628-109">Un elenco completo di [**IOCTL Winsock**](winsock-ioctls.md) è disponibile nella Guida di riferimento a Winsock.</span><span class="sxs-lookup"><span data-stu-id="b6628-109">A complete list of [**Winsock IOCTLs**](winsock-ioctls.md) are available in the Winsock reference.</span></span>

## <a name="summary-of-common-socket-options"></a><span data-ttu-id="b6628-110">Riepilogo delle opzioni dei socket comuni</span><span class="sxs-lookup"><span data-stu-id="b6628-110">Summary of Common Socket Options</span></span>

<span data-ttu-id="b6628-111">Un provider di servizi Winsock deve riconoscere tutte queste opzioni e (per [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) restituire valori plausibili per ogni.</span><span class="sxs-lookup"><span data-stu-id="b6628-111">A Winsock service provider must recognize all of these options, and (for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) return plausible values for each.</span></span> <span data-ttu-id="b6628-112">Il valore predefinito per ogni opzione è illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b6628-112">The default value for each option is shown in the following table.</span></span>

<span data-ttu-id="b6628-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b6628-113">Value</span></span>

<span data-ttu-id="b6628-114">Type</span><span class="sxs-lookup"><span data-stu-id="b6628-114">Type</span></span>

<span data-ttu-id="b6628-115">Significato</span><span class="sxs-lookup"><span data-stu-id="b6628-115">Meaning</span></span>

<span data-ttu-id="b6628-116">Predefinito</span><span class="sxs-lookup"><span data-stu-id="b6628-116">Default</span></span>

<span data-ttu-id="b6628-117">Nota</span><span class="sxs-lookup"><span data-stu-id="b6628-117">Note</span></span>

<span data-ttu-id="b6628-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN</span><span class="sxs-lookup"><span data-stu-id="b6628-118"><span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>SO\_ACCEPTCONN</span></span>

<span data-ttu-id="b6628-119">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-119">BOOL</span></span>

<span data-ttu-id="b6628-120">Il socket è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="b6628-120">Socket is listening.</span></span>

<span data-ttu-id="b6628-121">FALSE a meno che non sia stato eseguito un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b6628-121">FALSE unless a [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) has been performed.</span></span>

<span data-ttu-id="b6628-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_trasmissione</span><span class="sxs-lookup"><span data-stu-id="b6628-122"><span id="SO_BROADCAST"></span><span id="so_broadcast"></span>SO\_BROADCAST</span></span>

<span data-ttu-id="b6628-123">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-123">BOOL</span></span>

<span data-ttu-id="b6628-124">Il socket è configurato per la trasmissione e la ricezione di messaggi broadcast.</span><span class="sxs-lookup"><span data-stu-id="b6628-124">Socket is configured for the transmission and receipt of broadcast messages.</span></span>

<span data-ttu-id="b6628-125">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-125">FALSE</span></span>

<span data-ttu-id="b6628-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>\_debug</span><span class="sxs-lookup"><span data-stu-id="b6628-126"><span id="SO_DEBUG"></span><span id="so_debug"></span>SO\_DEBUG</span></span>

<span data-ttu-id="b6628-127">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-127">BOOL</span></span>

<span data-ttu-id="b6628-128">Il debug è abilitato.</span><span class="sxs-lookup"><span data-stu-id="b6628-128">Debugging is enabled.</span></span>

<span data-ttu-id="b6628-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-129">FALSE</span></span>

<span data-ttu-id="b6628-130">i</span><span class="sxs-lookup"><span data-stu-id="b6628-130">(i)</span></span>

<span data-ttu-id="b6628-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER</span><span class="sxs-lookup"><span data-stu-id="b6628-131"><span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>SO\_DONTLINGER</span></span>

<span data-ttu-id="b6628-132">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-132">BOOL</span></span>

<span data-ttu-id="b6628-133">Se true, l' \_ opzione so Linger è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="b6628-133">If true, the SO\_LINGER option is disabled.</span></span>

<span data-ttu-id="b6628-134">true</span><span class="sxs-lookup"><span data-stu-id="b6628-134">TRUE</span></span>

<span data-ttu-id="b6628-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="b6628-135"><span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>SO\_DONTROUTE</span></span>

<span data-ttu-id="b6628-136">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-136">BOOL</span></span>

<span data-ttu-id="b6628-137">Il routing è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="b6628-137">Routing is disabled.</span></span> <span data-ttu-id="b6628-138">Ha esito positivo, ma viene ignorato nei \_ socket inet AF; non riesce nei \_ socket INET6 AF con [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="b6628-138">Succeeds but is ignored on AF\_INET sockets; fails on AF\_INET6 sockets with [WSAENOPROTOOPT](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="b6628-139">Non supportato nei socket ATM (genera un errore).</span><span class="sxs-lookup"><span data-stu-id="b6628-139">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="b6628-140">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-140">FALSE</span></span>

<span data-ttu-id="b6628-141">i</span><span class="sxs-lookup"><span data-stu-id="b6628-141">(i)</span></span>

<span data-ttu-id="b6628-142"><span id="SO_ERROR"></span><span id="so_error"></span>\_errore</span><span class="sxs-lookup"><span data-stu-id="b6628-142"><span id="SO_ERROR"></span><span id="so_error"></span>SO\_ERROR</span></span>

<span data-ttu-id="b6628-143">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-143">int</span></span>

<span data-ttu-id="b6628-144">Recupera lo stato di errore e Cancella.</span><span class="sxs-lookup"><span data-stu-id="b6628-144">Retrieves error status and clear.</span></span>

<span data-ttu-id="b6628-145">0</span><span class="sxs-lookup"><span data-stu-id="b6628-145">0</span></span>

<span data-ttu-id="b6628-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_ID gruppo \_</span><span class="sxs-lookup"><span data-stu-id="b6628-146"><span id="SO_GROUP_ID"></span><span id="so_group_id"></span>SO\_GROUP\_ID</span></span>

<span data-ttu-id="b6628-147">GROUP</span><span class="sxs-lookup"><span data-stu-id="b6628-147">GROUP</span></span>

<span data-ttu-id="b6628-148">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b6628-148">Reserved.</span></span>

<span data-ttu-id="b6628-149">NULL</span><span class="sxs-lookup"><span data-stu-id="b6628-149">NULL</span></span>

<span data-ttu-id="b6628-150">Solo Get</span><span class="sxs-lookup"><span data-stu-id="b6628-150">Get only</span></span>

<span data-ttu-id="b6628-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>QUINDI \_ , \_ Priorità gruppo</span><span class="sxs-lookup"><span data-stu-id="b6628-151"><span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>SO\_GROUP\_PRIORITY</span></span>

<span data-ttu-id="b6628-152">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-152">int</span></span>

<span data-ttu-id="b6628-153">Riservato.</span><span class="sxs-lookup"><span data-stu-id="b6628-153">Reserved.</span></span>

<span data-ttu-id="b6628-154">0</span><span class="sxs-lookup"><span data-stu-id="b6628-154">0</span></span>

[<span data-ttu-id="b6628-155">**QUINDI \_ KeepAlive**</span><span class="sxs-lookup"><span data-stu-id="b6628-155">**SO\_KEEPALIVE**</span></span>](so-keepalive.md)

<span data-ttu-id="b6628-156">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-156">BOOL</span></span>

<span data-ttu-id="b6628-157">È in corso l'invio di KeepAlive.</span><span class="sxs-lookup"><span data-stu-id="b6628-157">Keepalives are being sent.</span></span> <span data-ttu-id="b6628-158">Non supportato nei socket ATM (genera un errore).</span><span class="sxs-lookup"><span data-stu-id="b6628-158">Not supported on ATM sockets (results in an error).</span></span>

<span data-ttu-id="b6628-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-159">FALSE</span></span>

<span data-ttu-id="b6628-160">i</span><span class="sxs-lookup"><span data-stu-id="b6628-160">(i)</span></span>

<span data-ttu-id="b6628-161"><span id="SO_LINGER"></span><span id="so_linger"></span>QUINDI, \_ indugio</span><span class="sxs-lookup"><span data-stu-id="b6628-161"><span id="SO_LINGER"></span><span id="so_linger"></span>SO\_LINGER</span></span>

<span data-ttu-id="b6628-162">Struttura Linger</span><span class="sxs-lookup"><span data-stu-id="b6628-162">Structure linger</span></span>

<span data-ttu-id="b6628-163">Restituisce le opzioni Linger correnti.</span><span class="sxs-lookup"><span data-stu-id="b6628-163">Returns the current linger options.</span></span>

<span data-ttu-id="b6628-164">l \_ OnOff è 0</span><span class="sxs-lookup"><span data-stu-id="b6628-164">l\_onoff is 0</span></span>

<span data-ttu-id="b6628-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_dimensioni massime \_ messaggio \_</span><span class="sxs-lookup"><span data-stu-id="b6628-165"><span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>SO\_MAX\_MSG\_SIZE</span></span>

<span data-ttu-id="b6628-166">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-166">int</span></span>

<span data-ttu-id="b6628-167">Dimensioni massime in uscita di un messaggio per i tipi di socket del messaggio.</span><span class="sxs-lookup"><span data-stu-id="b6628-167">Maximum outbound size of a message for message socket types.</span></span> <span data-ttu-id="b6628-168">Non è previsto alcun provisioning per determinare la dimensione massima del messaggio in ingresso.</span><span class="sxs-lookup"><span data-stu-id="b6628-168">There is no provision to determine the maximum inbound message size.</span></span> <span data-ttu-id="b6628-169">Non ha significato per i socket orientati al flusso.</span><span class="sxs-lookup"><span data-stu-id="b6628-169">Has no meaning for stream-oriented sockets.</span></span>

<span data-ttu-id="b6628-170">Dipendente dall'implementazione</span><span class="sxs-lookup"><span data-stu-id="b6628-170">Implementation dependent</span></span>

<span data-ttu-id="b6628-171">Solo Get</span><span class="sxs-lookup"><span data-stu-id="b6628-171">Get only</span></span>

<span data-ttu-id="b6628-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE</span><span class="sxs-lookup"><span data-stu-id="b6628-172"><span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>SO\_OOBINLINE</span></span>

<span data-ttu-id="b6628-173">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-173">BOOL</span></span>

<span data-ttu-id="b6628-174">I dati di OOB vengono ricevuti nel flusso di dati normale.</span><span class="sxs-lookup"><span data-stu-id="b6628-174">OOB data is being received in the normal data stream.</span></span>

<span data-ttu-id="b6628-175">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-175">FALSE</span></span>

<span data-ttu-id="b6628-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_protocollo \_ INFOW</span><span class="sxs-lookup"><span data-stu-id="b6628-176"><span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>SO\_PROTOCOL\_INFOW</span></span>

<span data-ttu-id="b6628-177">[ **\_ informazioni WSAPROTOCOL** struttura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span><span class="sxs-lookup"><span data-stu-id="b6628-177">structure [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)</span></span>

<span data-ttu-id="b6628-178">Descrizione delle informazioni sul protocollo associate al socket.</span><span class="sxs-lookup"><span data-stu-id="b6628-178">Description of protocol information for the protocol that is bound to this socket.</span></span>

<span data-ttu-id="b6628-179">Dipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="b6628-179">Protocol dependent</span></span>

<span data-ttu-id="b6628-180">Solo Get</span><span class="sxs-lookup"><span data-stu-id="b6628-180">Get only</span></span>

<span data-ttu-id="b6628-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF</span><span class="sxs-lookup"><span data-stu-id="b6628-181"><span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>SO\_RCVBUF</span></span>

<span data-ttu-id="b6628-182">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-182">int</span></span>

<span data-ttu-id="b6628-183">Spazio totale del buffer per socket riservato per le ricevute.</span><span class="sxs-lookup"><span data-stu-id="b6628-183">The total per-socket buffer space reserved for receives.</span></span> <span data-ttu-id="b6628-184">Questa operazione non è correlata \_ alla \_ \_ dimensione massima dei messaggi e non corrisponde necessariamente alle dimensioni della finestra di ricezione TCP.</span><span class="sxs-lookup"><span data-stu-id="b6628-184">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of the TCP receive window.</span></span>

<span data-ttu-id="b6628-185">Dipendente dall'implementazione</span><span class="sxs-lookup"><span data-stu-id="b6628-185">Implementation dependent</span></span>

<span data-ttu-id="b6628-186">i</span><span class="sxs-lookup"><span data-stu-id="b6628-186">(i)</span></span>

<span data-ttu-id="b6628-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="b6628-187"><span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>SO\_REUSEADDR</span></span>

<span data-ttu-id="b6628-188">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-188">BOOL</span></span>

<span data-ttu-id="b6628-189">L'indirizzo a cui è associato il socket può essere usato da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="b6628-189">The address to which this socket is bound can be used by others.</span></span> <span data-ttu-id="b6628-190">Non applicabile nei socket ATM.</span><span class="sxs-lookup"><span data-stu-id="b6628-190">Not applicable on ATM sockets.</span></span>

<span data-ttu-id="b6628-191">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6628-191">FALSE</span></span>

<span data-ttu-id="b6628-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_sndbuf</span><span class="sxs-lookup"><span data-stu-id="b6628-192"><span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>SO\_SNDBUF</span></span>

<span data-ttu-id="b6628-193">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-193">int</span></span>

<span data-ttu-id="b6628-194">Spazio totale del buffer per socket riservato per gli invii.</span><span class="sxs-lookup"><span data-stu-id="b6628-194">The total per-socket buffer space reserved for sends.</span></span> <span data-ttu-id="b6628-195">Questa operazione non è correlata \_ alla \_ \_ dimensione massima dei messaggi e non corrisponde necessariamente alle dimensioni di una finestra di trasmissione TCP.</span><span class="sxs-lookup"><span data-stu-id="b6628-195">This is unrelated to SO\_MAX\_MSG\_SIZE and does not necessarily correspond to the size of a TCP send window.</span></span>

<span data-ttu-id="b6628-196">Dipendente dall'implementazione</span><span class="sxs-lookup"><span data-stu-id="b6628-196">Implementation dependent</span></span>

<span data-ttu-id="b6628-197">i</span><span class="sxs-lookup"><span data-stu-id="b6628-197">(i)</span></span>

<span data-ttu-id="b6628-198"><span id="SO_TYPE"></span><span id="so_type"></span>QUINDI, \_ digitare</span><span class="sxs-lookup"><span data-stu-id="b6628-198"><span id="SO_TYPE"></span><span id="so_type"></span>SO\_TYPE</span></span>

<span data-ttu-id="b6628-199">INT</span><span class="sxs-lookup"><span data-stu-id="b6628-199">int</span></span>

<span data-ttu-id="b6628-200">Tipo di socket (ad esempio, il flusso di SOCK \_ ).</span><span class="sxs-lookup"><span data-stu-id="b6628-200">The type of the socket (for example, SOCK\_STREAM).</span></span>

<span data-ttu-id="b6628-201">Creato tramite socket.</span><span class="sxs-lookup"><span data-stu-id="b6628-201">As created through socket.</span></span>

<span data-ttu-id="b6628-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>configurazione di PVD \_</span><span class="sxs-lookup"><span data-stu-id="b6628-202"><span id="PVD_CONFIG"></span><span id="pvd_config"></span>PVD\_CONFIG</span></span>

<span data-ttu-id="b6628-203">caratteri lontani \*</span><span class="sxs-lookup"><span data-stu-id="b6628-203">char FAR \*</span></span>

<span data-ttu-id="b6628-204">Oggetto struttura di dati opaco contenente le informazioni di configurazione del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="b6628-204">An opaque data structure object containing configuration information of the service provider.</span></span>

<span data-ttu-id="b6628-205">Dipendente dall'implementazione</span><span class="sxs-lookup"><span data-stu-id="b6628-205">Implementation dependent</span></span>

<span data-ttu-id="b6628-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>NoDelay TCP \_</span><span class="sxs-lookup"><span data-stu-id="b6628-206"><span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP\_NODELAY</span></span>

<span data-ttu-id="b6628-207">BOOL</span><span class="sxs-lookup"><span data-stu-id="b6628-207">BOOL</span></span>

<span data-ttu-id="b6628-208">Disabilita l'algoritmo Nagle di unione dei pacchetti in invio.</span><span class="sxs-lookup"><span data-stu-id="b6628-208">Disables the Nagle algorithm for send coalescing.</span></span>

<span data-ttu-id="b6628-209">Dipendente dall'implementazione</span><span class="sxs-lookup"><span data-stu-id="b6628-209">Implementation dependent</span></span>

<span data-ttu-id="b6628-210">(i) un provider di servizi può ignorare l'opzione in modo invisibile all'utente in [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) e restituire un valore costante per [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), oppure può accettare un valore per **WSPSetSockOpt** e restituire il valore corrispondente in **WSPGetSockOpt** senza usare il valore in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="b6628-210">(i) A service provider may silently ignore this option on [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) and return a constant value for [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), or it may accept a value for **WSPSetSockOpt** and return the corresponding value in **WSPGetSockOpt** without using the value in any way.</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="b6628-211">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b6628-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6628-212">**Opzioni socket**</span><span class="sxs-lookup"><span data-stu-id="b6628-212">**Socket Options**</span></span>](socket-options.md)
</dt> <dt>

[<span data-ttu-id="b6628-213">**\_Opzioni Socket socket Sol**</span><span class="sxs-lookup"><span data-stu-id="b6628-213">**SOL\_SOCKET Socket Options**</span></span>](sol-socket-socket-options.md)
</dt> <dt>

[<span data-ttu-id="b6628-214">**\_Opzioni socket TCP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="b6628-214">**IPPROTO\_TCP Socket Options**</span></span>](ipproto-tcp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="b6628-215">**\_Opzioni socket UDP IPPROTO**</span><span class="sxs-lookup"><span data-stu-id="b6628-215">**IPPROTO\_UDP Socket Options**</span></span>](ipproto-udp-socket-options.md)
</dt> <dt>

[<span data-ttu-id="b6628-216">**IOCTL Winsock**</span><span class="sxs-lookup"><span data-stu-id="b6628-216">**Winsock IOCTLs**</span></span>](winsock-ioctls.md)
</dt> </dl>

 

 
