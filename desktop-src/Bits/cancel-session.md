---
title: Cancel-Session
description: Usare il pacchetto Cancel-Session per terminare la sessione di caricamento con il server BITS.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- BIT Cancel-Session
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299055"
---
# <a name="cancel-session"></a><span data-ttu-id="2096e-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="2096e-104">Cancel-Session</span></span>

<span data-ttu-id="2096e-105">Utilizzare il pacchetto **Annulla sessione** per terminare la sessione di caricamento con il server BITS.</span><span class="sxs-lookup"><span data-stu-id="2096e-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="2096e-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="2096e-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="2096e-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS</span><span class="sxs-lookup"><span data-stu-id="2096e-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="2096e-108">Verbo specifico di BITS che identifica il pacchetto nel server BITS.</span><span class="sxs-lookup"><span data-stu-id="2096e-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="2096e-109">Sostituire Remote-URL con l'URI assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="2096e-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="2096e-110">In genere, sostituire Remote-URL con il nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="2096e-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="2096e-111">Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID nel pacchetto di [**creazione della sessione**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="2096e-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="2096e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="2096e-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="2096e-113">Identifica il pacchetto della richiesta come pacchetto di Cancel-Session.</span><span class="sxs-lookup"><span data-stu-id="2096e-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="2096e-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="2096e-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="2096e-115">GUID di stringa che identifica la sessione al server.</span><span class="sxs-lookup"><span data-stu-id="2096e-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="2096e-116">Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="2096e-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2096e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2096e-117">Remarks</span></span>

<span data-ttu-id="2096e-118">Questo pacchetto Annulla un processo di caricamento se viene inviato prima dell'invio dell'ultimo frammento.</span><span class="sxs-lookup"><span data-stu-id="2096e-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="2096e-119">Cancel-Session non ha alcun effetto su un file il cui ultimo frammento è già stato inviato.</span><span class="sxs-lookup"><span data-stu-id="2096e-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="2096e-120">Quando il server BITS riceve l'ultimo frammento, scrive il file nella destinazione finale e, nel caso di upload-Reply, invia il file all'applicazione server.</span><span class="sxs-lookup"><span data-stu-id="2096e-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="2096e-121">Nel caso di caricamento-risposta, il pacchetto di Cancel-Session Annulla la parte di risposta di un processo di caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="2096e-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="2096e-122">Il server BITS rilascia tutte le risorse ed Elimina tutti i file temporanei al momento della ricezione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="2096e-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="2096e-123">Il client BITS Invia questo pacchetto quando l'utente annulla il processo.</span><span class="sxs-lookup"><span data-stu-id="2096e-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="2096e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2096e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2096e-125">**ACK per create-Session**</span><span class="sxs-lookup"><span data-stu-id="2096e-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="2096e-126">**Chiudi sessione**</span><span class="sxs-lookup"><span data-stu-id="2096e-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




