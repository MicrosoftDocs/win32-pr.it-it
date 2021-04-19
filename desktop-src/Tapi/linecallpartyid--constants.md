---
description: Le \_ costanti del flag di bit LINECALLPARTYID descrivono la natura delle informazioni disponibili sulle entità coinvolte in una chiamata.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Costanti LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332896"
---
# <a name="linecallpartyid_-constants"></a><span data-ttu-id="72759-103">\_Costanti LINECALLPARTYID</span><span class="sxs-lookup"><span data-stu-id="72759-103">LINECALLPARTYID\_ Constants</span></span>

<span data-ttu-id="72759-104">Le costanti del flag di bit **LINECALLPARTYID \_** descrivono la natura delle informazioni disponibili sulle entità coinvolte in una chiamata.</span><span class="sxs-lookup"><span data-stu-id="72759-104">The **LINECALLPARTYID\_** bit-flag constants describe the nature of the information available about the parties involved in a call.</span></span>

<dl> <dt>

<span data-ttu-id="72759-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**\_Indirizzo LINECALLPARTYID**</span><span class="sxs-lookup"><span data-stu-id="72759-105"><span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**LINECALLPARTYID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-106">Le informazioni sull'identificatore dell'entità sono costituite dall'indirizzo dell'entità nel formato di indirizzo canonico o nel formato di indirizzo di composizione.</span><span class="sxs-lookup"><span data-stu-id="72759-106">Party identifier information consists of the party's address in either canonical address format or dialable address format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloccati**</span><span class="sxs-lookup"><span data-stu-id="72759-107"><span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-108">Le informazioni sull'identificatore dell'entità non sono disponibili perché sono state bloccate dalla parte remota.</span><span class="sxs-lookup"><span data-stu-id="72759-108">Party identifier information is not available because it has been blocked by the remote party.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**\_nome LINECALLPARTYID**</span><span class="sxs-lookup"><span data-stu-id="72759-109"><span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**LINECALLPARTYID\_NAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-110">Le informazioni sull'identificatore dell'entità sono costituite dal nome dell'entità, ad esempio da una directory mantenuta all'interno dell'opzione.</span><span class="sxs-lookup"><span data-stu-id="72759-110">Party identifier information consists of the party's name (as, for example, from a directory kept inside the switch).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**\_OUTOFAREA LINECALLPARTYID**</span><span class="sxs-lookup"><span data-stu-id="72759-111"><span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID\_OUTOFAREA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-112">Le informazioni relative all'ID chiamante per la chiamata non sono disponibili perché la rete non viene propagata.</span><span class="sxs-lookup"><span data-stu-id="72759-112">Caller ID information for the call is not available because it is not propagated all the way by the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parziale**</span><span class="sxs-lookup"><span data-stu-id="72759-113"><span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-114">Le informazioni sull'identificatore dell'entità sono valide ma sono limitate solo a informazioni parziali.</span><span class="sxs-lookup"><span data-stu-id="72759-114">Party identifier information is valid but it is limited to partial information only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="72759-115"><span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-116">Le informazioni sull'identificatore dell'entità non sono disponibili e non saranno disponibili in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="72759-116">Party identifier information is not available and will not become available later.</span></span> <span data-ttu-id="72759-117">Le informazioni potrebbero non essere disponibili per motivi non specificati.</span><span class="sxs-lookup"><span data-stu-id="72759-117">Information may be unavailable for unspecified reasons.</span></span> <span data-ttu-id="72759-118">Ad esempio, le informazioni non sono state recapitate dalla rete, ma sono state ignorate dal provider di servizi e così via.</span><span class="sxs-lookup"><span data-stu-id="72759-118">For example, the information was not delivered by the network, it was ignored by the service provider, and so forth.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="72759-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="72759-119"><span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="72759-120">Le informazioni sull'identificatore dell'entità sono attualmente sconosciute, ma possono essere note successivamente.</span><span class="sxs-lookup"><span data-stu-id="72759-120">Party identifier information is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72759-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="72759-121">Remarks</span></span>

<span data-ttu-id="72759-122">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="72759-122">No extensibility.</span></span> <span data-ttu-id="72759-123">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="72759-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="72759-124">Per ognuna delle entità possibili coinvolte in una chiamata, le **costanti \_ LINECALLPARTYID** descrivono come vengono formattate le informazioni sull'identificatore dell'entità.</span><span class="sxs-lookup"><span data-stu-id="72759-124">For each of the possible parties involved in a call, the **LINECALLPARTYID\_** constants describe how the party identifier information is formatted.</span></span> <span data-ttu-id="72759-125">Queste informazioni vengono fornite nella struttura dei dati [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="72759-125">This information is supplied in the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="72759-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72759-126">Requirements</span></span>



| <span data-ttu-id="72759-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="72759-127">Requirement</span></span> | <span data-ttu-id="72759-128">Valore</span><span class="sxs-lookup"><span data-stu-id="72759-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="72759-129">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="72759-129">TAPI version</span></span><br/> | <span data-ttu-id="72759-130">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="72759-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="72759-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72759-131">Header</span></span><br/>       | <dl> <span data-ttu-id="72759-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="72759-132"><dt>Tapi.h</dt></span></span> </dl> |



 

 




