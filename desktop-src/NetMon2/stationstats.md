---
description: La struttura STATIONSTATS fornisce statistiche su una specifica stazione descritta dall'acquisizione corrente.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Struttura STATIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049826"
---
# <a name="stationstats-structure"></a><span data-ttu-id="e7a59-103">Struttura STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="e7a59-103">STATIONSTATS structure</span></span>

<span data-ttu-id="e7a59-104">La struttura **STATIONSTATS** fornisce statistiche su una specifica [*stazione*](s.md) descritta dall'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e7a59-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7a59-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7a59-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="e7a59-106">Members</span><span class="sxs-lookup"><span data-stu-id="e7a59-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e7a59-107">**NextStationStats**</span><span class="sxs-lookup"><span data-stu-id="e7a59-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-108">Indice della stazione successiva registrata nella matrice di strutture **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="e7a59-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-109">**SessionPartnerList**</span><span class="sxs-lookup"><span data-stu-id="e7a59-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-110">Indice dell'elenco di partner di stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-111">**Flag**</span><span class="sxs-lookup"><span data-stu-id="e7a59-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-112">Questo membro è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e7a59-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-113">**StationAddress**</span><span class="sxs-lookup"><span data-stu-id="e7a59-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-114">Indirizzo MAC della stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-115">**Pad**</span><span class="sxs-lookup"><span data-stu-id="e7a59-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-116">Allineamento **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e7a59-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-117">**TotalPacketsReceived**</span><span class="sxs-lookup"><span data-stu-id="e7a59-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-118">Numero totale di pacchetti inviati alla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-119">**TotalDirectedPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="e7a59-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-120">Numero totale di pacchetti diretti inviati dalla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-121">**TotalBroadcastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="e7a59-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-122">Numero totale di pacchetti diretti da broadcast (indirizzo MAC FF FF FF FF FF) inviati dalla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-123">**TotalMulticastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="e7a59-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-124">Numero totale di pacchetti multicast (bit del gruppo impostati nell'indirizzo di destinazione) inviati dalla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="e7a59-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-126">Numero totale di byte inviati alla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="e7a59-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="e7a59-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="e7a59-128">Numero totale di byte inviati dalla stazione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7a59-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7a59-129">Remarks</span></span>

<span data-ttu-id="e7a59-130">Network Monitor archivia le informazioni sulla sessione e sulla stazione in due matrici associate.</span><span class="sxs-lookup"><span data-stu-id="e7a59-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="e7a59-131">i cui elementi sono rispettivamente [SESSIONSTATS](sessionstats.md) e **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="e7a59-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="e7a59-132">I membri di queste strutture possono essere utilizzati per spostarsi tra di essi.</span><span class="sxs-lookup"><span data-stu-id="e7a59-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="e7a59-133">Ad esempio, per passare alla stazione successiva, usare **NextStationStats**.</span><span class="sxs-lookup"><span data-stu-id="e7a59-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="e7a59-134">Per passare all'elenco partner di sessione nella matrice SESSIONSTATS, usare l'indice fornito in **SessionPartnerList**.</span><span class="sxs-lookup"><span data-stu-id="e7a59-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="e7a59-135">La matrice **STATIONSTATS** contiene un elemento per ogni stazione utilizzata durante l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="e7a59-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="e7a59-136">L'algoritmo Network Monitor USA per aggiungere elementi a questa matrice si basa sul modo più efficiente per registrare le informazioni mentre è in corso l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="e7a59-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="e7a59-137">Di conseguenza, la stazione successiva non è sempre l'elemento successivo nella matrice.</span><span class="sxs-lookup"><span data-stu-id="e7a59-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7a59-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7a59-138">Requirements</span></span>



| <span data-ttu-id="e7a59-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a59-139">Requirement</span></span> | <span data-ttu-id="e7a59-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a59-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a59-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7a59-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e7a59-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7a59-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e7a59-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e7a59-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e7a59-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e7a59-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e7a59-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7a59-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7a59-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a59-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7a59-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7a59-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7a59-148">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="e7a59-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="e7a59-149">IRTC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="e7a59-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="e7a59-150">IStats:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="e7a59-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




