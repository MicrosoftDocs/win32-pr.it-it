---
description: Le \_ costanti LINEAGENTSESSIONSTATE descrivono diversi Stati della sessione di Agent.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Costanti LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327784"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="d8908-103">\_Costanti LINEAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="d8908-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="d8908-104">Le **\_ costanti LINEAGENTSESSIONSTATE** descrivono diversi Stati della sessione di Agent.</span><span class="sxs-lookup"><span data-stu-id="d8908-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="d8908-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**\_BUSYONCALL LINEAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="d8908-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-106">L'agente è occupato a gestire una chiamata.</span><span class="sxs-lookup"><span data-stu-id="d8908-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8908-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**\_BUSYWRAPUP LINEAGENTSESSIONSTATE**</span><span class="sxs-lookup"><span data-stu-id="d8908-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-108">L'agente occupa la gestione del completamento della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d8908-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8908-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ terminato**</span><span class="sxs-lookup"><span data-stu-id="d8908-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-110">La sessione dell'agente è terminata.</span><span class="sxs-lookup"><span data-stu-id="d8908-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8908-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ NObattistrada**</span><span class="sxs-lookup"><span data-stu-id="d8908-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-112">L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa).</span><span class="sxs-lookup"><span data-stu-id="d8908-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="d8908-113">Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.</span><span class="sxs-lookup"><span data-stu-id="d8908-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8908-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="d8908-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-115">L'agente è pronto per accettare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="d8908-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8908-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ rilasciato**</span><span class="sxs-lookup"><span data-stu-id="d8908-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d8908-117">La sessione dell'agente è stata rilasciata.</span><span class="sxs-lookup"><span data-stu-id="d8908-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8908-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8908-118">Requirements</span></span>



| <span data-ttu-id="d8908-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8908-119">Requirement</span></span> | <span data-ttu-id="d8908-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d8908-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d8908-121">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="d8908-121">TAPI version</span></span><br/> | <span data-ttu-id="d8908-122">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="d8908-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="d8908-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8908-123">Header</span></span><br/>       | <dl> <span data-ttu-id="d8908-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8908-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




