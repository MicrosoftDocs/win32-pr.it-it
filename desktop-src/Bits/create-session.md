---
title: Create-Session
description: Usare il pacchetto Create-Session per richiedere una sessione di caricamento con il server BITS.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- BIT Create-Session
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471859"
---
# <a name="create-session"></a><span data-ttu-id="8703e-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="8703e-104">Create-Session</span></span>

<span data-ttu-id="8703e-105">Usare il pacchetto di **creazione sessione** per richiedere una sessione di caricamento con il server BITS.</span><span class="sxs-lookup"><span data-stu-id="8703e-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="8703e-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="8703e-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="8703e-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS</span><span class="sxs-lookup"><span data-stu-id="8703e-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="8703e-108">Verbo specifico di BITS che identifica il pacchetto nel server BITS.</span><span class="sxs-lookup"><span data-stu-id="8703e-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="8703e-109">Sostituire Remote-URL con l'URI assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="8703e-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="8703e-110">In genere, sostituire Remote-URL con il nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="8703e-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="8703e-111">Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID.</span><span class="sxs-lookup"><span data-stu-id="8703e-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="8703e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="8703e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="8703e-113">Identifica il pacchetto della richiesta come pacchetto di Create-Session.</span><span class="sxs-lookup"><span data-stu-id="8703e-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="8703e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span><span class="sxs-lookup"><span data-stu-id="8703e-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="8703e-115">Elenco delimitato da spazi dei protocolli supportati dal client.</span><span class="sxs-lookup"><span data-stu-id="8703e-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="8703e-116">Usare i GUID di stringa per identificare i protocolli.</span><span class="sxs-lookup"><span data-stu-id="8703e-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="8703e-117">Specificare l'elenco in ordine di preferenza, dal più o meno preferibile.</span><span class="sxs-lookup"><span data-stu-id="8703e-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="8703e-118">La tabella seguente elenca il protocollo supportato dal client BITS.</span><span class="sxs-lookup"><span data-stu-id="8703e-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="8703e-119">Sostituisci {guid1}... {guidn} con uno o più GUID di stringa dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="8703e-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="8703e-120">Protocollo</span><span class="sxs-lookup"><span data-stu-id="8703e-120">Protocol</span></span>                                          | <span data-ttu-id="8703e-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8703e-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="8703e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span><span class="sxs-lookup"><span data-stu-id="8703e-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="8703e-123">Protocollo di caricamento BITS 1,5</span><span class="sxs-lookup"><span data-stu-id="8703e-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8703e-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="8703e-124">Remarks</span></span>

<span data-ttu-id="8703e-125">È necessario inviare un pacchetto [**ping**](ping.md) per stabilire una connessione HTTP prima di inviare il pacchetto di Create-Session.</span><span class="sxs-lookup"><span data-stu-id="8703e-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="8703e-126">Il pacchetto di Create-Session può inoltre stabilire la connessione. Tuttavia, il pacchetto di Create-Session è meno efficiente.</span><span class="sxs-lookup"><span data-stu-id="8703e-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="8703e-127">Il server seleziona il protocollo che si vuole usare dall'elenco fornito dal client nell'intestazione BITS-Supported-Protocols.</span><span class="sxs-lookup"><span data-stu-id="8703e-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="8703e-128">Il server restituisce il protocollo selezionato nell'intestazione BITS-Protocol del ACK per il pacchetto di risposta di [**creazione-sessione**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8703e-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="8703e-129">Il client prevede che il server restituisca un ACK per il pacchetto di risposta [**di creazione sessione**](ack-for-create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="8703e-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="8703e-130">Se il server è stato in grado di stabilire una sessione, il client usa il pacchetto di richiesta del [**frammento**](fragment.md) per inviare gli intervalli del file al server.</span><span class="sxs-lookup"><span data-stu-id="8703e-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="8703e-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8703e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8703e-132">**ACK per create-Session**</span><span class="sxs-lookup"><span data-stu-id="8703e-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="8703e-133">**Frammento**</span><span class="sxs-lookup"><span data-stu-id="8703e-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="8703e-134">**Ping**</span><span class="sxs-lookup"><span data-stu-id="8703e-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





