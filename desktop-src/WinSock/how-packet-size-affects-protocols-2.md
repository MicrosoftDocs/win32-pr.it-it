---
description: I problemi relativi alle dimensioni dei pacchetti multimediali descritti nell'argomento relativo alle dimensioni dei pacchetti multimediali influiscono sui diversi \_ protocolli IPX PF in modo diverso.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Impatto delle dimensioni del pacchetto sui protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343506"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="87145-103">Impatto delle dimensioni del pacchetto sui protocolli</span><span class="sxs-lookup"><span data-stu-id="87145-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="87145-104">I problemi relativi alle dimensioni dei pacchetti multimediali descritti nell'argomento [relativo alle dimensioni dei pacchetti multimediali](about-media-packet-size-2.md)influiscono sui diversi \_ protocolli IPX PF in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="87145-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="87145-105">Una strategia comune per la gestione di diversi vincoli di dimensioni del router e dei supporti consiste nell'usare le dimensioni massime dei supporti quando il numero di rete della stazione remota corrisponde alla stazione locale ed eseguire il fallback alla dimensione minima del pacchetto in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="87145-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="87145-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87145-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87145-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="87145-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="87145-108">Fornisce un servizio datagramma; ogni datagramma deve risiedere entro la dimensione massima del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87145-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="87145-109">Winsock imposta la dimensione massima del pacchetto del datagramma sulle dimensioni del pacchetto multimediale locale meno l'intestazione IPX.</span><span class="sxs-lookup"><span data-stu-id="87145-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="87145-110">Tenere presente, tuttavia, che se il pacchetto viene indirizzato, è possibile che si verifichino restrizioni del router in Route.</span><span class="sxs-lookup"><span data-stu-id="87145-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="87145-111">Assicurarsi che l'applicazione sia in grado di eseguire il fallback a datagrammi a 546 byte.</span><span class="sxs-lookup"><span data-stu-id="87145-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="87145-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>\_SPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="87145-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="87145-113">Fornisce servizi per pacchetti di flusso e sequenziato.</span><span class="sxs-lookup"><span data-stu-id="87145-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="87145-114">Winsock IPX/SPX consente ai flussi di dati e ai messaggi di estendersi su più pacchetti, pertanto le dimensioni dei pacchetti non limitano la quantità di dati gestiti da [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) e [**ricezione**](/windows/desktop/api/winsock/nf-winsock-recv).</span><span class="sxs-lookup"><span data-stu-id="87145-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="87145-115">Tuttavia, le dimensioni dei supporti sottostanti devono essere impostate correttamente oppure il primo pacchetto di grandi dimensioni sarà non recapitabile e la connessione verrà reimpostata.</span><span class="sxs-lookup"><span data-stu-id="87145-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="87145-116">Se la stazione di destinazione si trova nella rete locale, Winsock imposta le dimensioni del pacchetto sulle dimensioni del pacchetto multimediale.</span><span class="sxs-lookup"><span data-stu-id="87145-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="87145-117">In caso contrario, il valore predefinito è 512 byte.</span><span class="sxs-lookup"><span data-stu-id="87145-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="87145-118">Queste dimensioni possono essere modificate immediatamente dopo la [**connessione**](/windows/desktop/api/Winsock2/nf-winsock2-connect) o l' [**accettazione**](/windows/desktop/api/Winsock2/nf-winsock2-accept) tramite [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="87145-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="87145-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>\_SPXII NSPROTO</span><span class="sxs-lookup"><span data-stu-id="87145-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="87145-120">SPXII offre una negoziazione di pacchetti Internet di grandi dimensioni per mantenere le dimensioni più adatte per i pacchetti e non richiede l'intervento del programmatore.</span><span class="sxs-lookup"><span data-stu-id="87145-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="87145-121">Tuttavia, se la stazione remota non supporta SPXII e negozia fino a SPX standard, le \_ regole SPX NSPROTO sono attive.</span><span class="sxs-lookup"><span data-stu-id="87145-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="87145-122">Protocollo</span><span class="sxs-lookup"><span data-stu-id="87145-122">Protocol</span></span>     | <span data-ttu-id="87145-123">File multimediali</span><span class="sxs-lookup"><span data-stu-id="87145-123">Media</span></span>      | <span data-ttu-id="87145-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="87145-124">Type</span></span>        | <span data-ttu-id="87145-125">Dimensioni del pacchetto di dati</span><span class="sxs-lookup"><span data-stu-id="87145-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="87145-126">NSPROTO \_ IPX</span><span class="sxs-lookup"><span data-stu-id="87145-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="87145-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="87145-127">Ethernet</span></span>   | <span data-ttu-id="87145-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="87145-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="87145-129">802.3</span><span class="sxs-lookup"><span data-stu-id="87145-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="87145-130">802.2</span><span class="sxs-lookup"><span data-stu-id="87145-130">802.2</span></span>       | <span data-ttu-id="87145-131">1466</span><span class="sxs-lookup"><span data-stu-id="87145-131">1466</span></span>             |
|              |            | <span data-ttu-id="87145-132">SNAP</span><span class="sxs-lookup"><span data-stu-id="87145-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="87145-133">Token ring</span><span class="sxs-lookup"><span data-stu-id="87145-133">Token Ring</span></span> | <span data-ttu-id="87145-134">4 megabit</span><span class="sxs-lookup"><span data-stu-id="87145-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="87145-135">16 megabit</span><span class="sxs-lookup"><span data-stu-id="87145-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="87145-136">\_SPX NSPROTO</span><span class="sxs-lookup"><span data-stu-id="87145-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="87145-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="87145-137">Ethernet</span></span>   | <span data-ttu-id="87145-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="87145-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="87145-139">802.3</span><span class="sxs-lookup"><span data-stu-id="87145-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="87145-140">802.2</span><span class="sxs-lookup"><span data-stu-id="87145-140">802.2</span></span>       | <span data-ttu-id="87145-141">1454</span><span class="sxs-lookup"><span data-stu-id="87145-141">1454</span></span>             |
|              |            | <span data-ttu-id="87145-142">SNAP</span><span class="sxs-lookup"><span data-stu-id="87145-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="87145-143">Token ring</span><span class="sxs-lookup"><span data-stu-id="87145-143">Token Ring</span></span> | <span data-ttu-id="87145-144">4 megabit</span><span class="sxs-lookup"><span data-stu-id="87145-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="87145-145">16 megabit</span><span class="sxs-lookup"><span data-stu-id="87145-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



