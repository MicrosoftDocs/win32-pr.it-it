---
description: La struttura SESSIONSTATS fornisce statistiche su una sessione.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Struttura SESSIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226963"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="6d71a-103">Struttura SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="6d71a-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="6d71a-104">La struttura **SESSIONSTATS** fornisce statistiche su una [*sessione*](s.md).</span><span class="sxs-lookup"><span data-stu-id="6d71a-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d71a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6d71a-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="6d71a-106">Members</span><span class="sxs-lookup"><span data-stu-id="6d71a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d71a-107">**NextSession**</span><span class="sxs-lookup"><span data-stu-id="6d71a-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="6d71a-108">Indice della sessione successiva del proprietario della stazione.</span><span class="sxs-lookup"><span data-stu-id="6d71a-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="6d71a-109">**StationOwner**</span><span class="sxs-lookup"><span data-stu-id="6d71a-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="6d71a-110">Indice di una stazione proprietaria all'interno della matrice di strutture [STATIONSTATS](stationstats.md) associata.</span><span class="sxs-lookup"><span data-stu-id="6d71a-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="6d71a-111">La stazione del proprietario è la stazione che ha avviato la sessione, ovvero la stazione che ha inviato i pacchetti della sessione.</span><span class="sxs-lookup"><span data-stu-id="6d71a-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="6d71a-112">**StationPartner**</span><span class="sxs-lookup"><span data-stu-id="6d71a-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="6d71a-113">Indice dell'altra stazione all'interno della matrice di strutture [STATIONSTATS](stationstats.md) associata.</span><span class="sxs-lookup"><span data-stu-id="6d71a-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="6d71a-114">La stazione partner è la stazione che ha ricevuto i pacchetti della sessione.</span><span class="sxs-lookup"><span data-stu-id="6d71a-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="6d71a-115">**Flag**</span><span class="sxs-lookup"><span data-stu-id="6d71a-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="6d71a-116">Questo membro è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="6d71a-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="6d71a-117">**TotalPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="6d71a-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="6d71a-118">Numero di pacchetti inviati nella sessione.</span><span class="sxs-lookup"><span data-stu-id="6d71a-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d71a-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6d71a-119">Remarks</span></span>

<span data-ttu-id="6d71a-120">Network Monitor archivia le informazioni sulla sessione e sulla stazione in due matrici associate, i cui elementi sono rispettivamente **SESSIONSTATS** e [STATIONSTATS](stationstats.md) .</span><span class="sxs-lookup"><span data-stu-id="6d71a-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="6d71a-121">I membri di queste strutture possono essere utilizzati per spostarsi tra di essi.</span><span class="sxs-lookup"><span data-stu-id="6d71a-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="6d71a-122">Ad esempio, per passare alla sessione successiva per un proprietario di stazione specifico, usare **NextSession**.</span><span class="sxs-lookup"><span data-stu-id="6d71a-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="6d71a-123">Per passare al proprietario e alla stazione partner della sessione nell'array STATIONSTATS, usare l'indice fornito in **StationOwner** e **StationPartner**.</span><span class="sxs-lookup"><span data-stu-id="6d71a-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="6d71a-124">La matrice SESSIONSTATS contiene un elemento per ogni sessione nell'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="6d71a-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="6d71a-125">L'algoritmo Network Monitor USA per aggiungere elementi alla matrice SESSIONSTATS si basa sulla registrazione efficiente delle informazioni mentre è in corso l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="6d71a-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="6d71a-126">Di conseguenza, la sessione successiva per una stazione proprietaria specifica non è sempre l'elemento successivo nella matrice.</span><span class="sxs-lookup"><span data-stu-id="6d71a-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d71a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6d71a-127">Requirements</span></span>



| <span data-ttu-id="6d71a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d71a-128">Requirement</span></span> | <span data-ttu-id="6d71a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6d71a-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6d71a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d71a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6d71a-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d71a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6d71a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6d71a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6d71a-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6d71a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6d71a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6d71a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d71a-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d71a-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d71a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6d71a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d71a-137">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="6d71a-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="6d71a-138">IRTC:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="6d71a-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="6d71a-139">IStats:: GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="6d71a-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




