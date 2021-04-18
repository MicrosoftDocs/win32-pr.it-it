---
title: Ping
description: Usare il pacchetto ping per stabilire una connessione e negoziare la sicurezza con il server.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- BIT ping
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299269"
---
# <a name="ping"></a><span data-ttu-id="65256-104">Ping</span><span class="sxs-lookup"><span data-stu-id="65256-104">Ping</span></span>

<span data-ttu-id="65256-105">Usare il pacchetto **ping** per stabilire una connessione e negoziare la sicurezza con il server.</span><span class="sxs-lookup"><span data-stu-id="65256-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="65256-106">Intestazioni</span><span class="sxs-lookup"><span data-stu-id="65256-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="65256-107"><span id="BITS_POST"></span><span id="bits_post"></span>\_post BITS</span><span class="sxs-lookup"><span data-stu-id="65256-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="65256-108">Verbo specifico di BITS che identifica il pacchetto nel server BITS.</span><span class="sxs-lookup"><span data-stu-id="65256-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="65256-109">Sostituire Remote-URL con l'URI assoluto o relativo.</span><span class="sxs-lookup"><span data-stu-id="65256-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="65256-110">In genere, sostituire Remote-URL con il nome file remoto del processo.</span><span class="sxs-lookup"><span data-stu-id="65256-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="65256-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-tipo-pacchetto</span><span class="sxs-lookup"><span data-stu-id="65256-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="65256-112">Identifica il pacchetto di richiesta come un pacchetto ping.</span><span class="sxs-lookup"><span data-stu-id="65256-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65256-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="65256-113">Remarks</span></span>

<span data-ttu-id="65256-114">Il pacchetto **ping** è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="65256-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="65256-115">Anziché inviare un pacchetto **ping** , è possibile usare il pacchetto [**create-Session**](create-session.md) per stabilire una connessione e negoziare la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="65256-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="65256-116">Tuttavia, è più efficiente usare il pacchetto **ping** a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="65256-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="65256-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65256-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65256-118">**ACK per ping**</span><span class="sxs-lookup"><span data-stu-id="65256-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="65256-119">**Creazione sessione**</span><span class="sxs-lookup"><span data-stu-id="65256-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




