---
title: Close-Session
description: Usare il pacchetto Close-Session per indicare al server BITS che il caricamento del file è stato completato e terminare la sessione.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- BIT Close-Session
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857129"
---
# <a name="close-session"></a><span data-ttu-id="cbfbd-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="cbfbd-104">Close-Session</span></span>

<span data-ttu-id="cbfbd-105">Usare il pacchetto di **chiusura sessione** per indicare al server BITS che il caricamento del file è stato completato e terminare la sessione.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="cbfbd-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="cbfbd-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="cbfbd-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS</span><span class="sxs-lookup"><span data-stu-id="cbfbd-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="cbfbd-108">Verbo specifico di BITS che identifica il pacchetto nel server BITS.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="cbfbd-109">Sostituire Remote-URL con l'URI assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="cbfbd-110">In genere, sostituire Remote-URL con il nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="cbfbd-111">Per considerazioni sul bilanciamento del carico di rete, vedere l'intestazione BITS-host-ID nel pacchetto di [**creazione della sessione**](create-session.md) .</span><span class="sxs-lookup"><span data-stu-id="cbfbd-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="cbfbd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="cbfbd-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="cbfbd-113">Identifica il pacchetto della richiesta come pacchetto di Close-Session.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="cbfbd-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BIT-session-ID</span><span class="sxs-lookup"><span data-stu-id="cbfbd-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="cbfbd-115">GUID di stringa che identifica la sessione al server.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="cbfbd-116">Sostituire {GUID} con l'identificatore di sessione restituito dal server nell' [**ACK per**](ack-for-create-session.md) il pacchetto di risposta per la creazione della sessione.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbfbd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cbfbd-117">Remarks</span></span>

<span data-ttu-id="cbfbd-118">Il server BITS rilascia tutte le risorse ed Elimina tutti i file temporanei al momento della ricezione del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="cbfbd-119">Per i processi di caricamento-risposta, è necessario scaricare la risposta prima di inviare la **sessione di chiusura**.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="cbfbd-120">In caso contrario, la risposta viene persa.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="cbfbd-121">Se si invia questo pacchetto prima di caricare tutti i frammenti, il file di caricamento viene eliminato. non è possibile caricare un file parziale.</span><span class="sxs-lookup"><span data-stu-id="cbfbd-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbfbd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbfbd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbfbd-123">**ACK per chiusura sessione**</span><span class="sxs-lookup"><span data-stu-id="cbfbd-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="cbfbd-124">**Annulla-sessione**</span><span class="sxs-lookup"><span data-stu-id="cbfbd-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="cbfbd-125">**Creazione sessione**</span><span class="sxs-lookup"><span data-stu-id="cbfbd-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




