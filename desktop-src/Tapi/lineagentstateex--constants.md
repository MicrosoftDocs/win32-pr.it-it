---
description: Le \_ costanti LINEAGENTSTATEEX descrivono lo stato di un agente in un indirizzo.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Costanti LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332913"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="51f67-103">\_Costanti LINEAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="51f67-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="51f67-104">Le **\_ costanti LINEAGENTSTATEEX** descrivono lo stato di un agente in un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="51f67-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="51f67-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**\_BUSYACD LINEAGENTSTATEEX**</span><span class="sxs-lookup"><span data-stu-id="51f67-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-106">L'agente è occupato a gestire una chiamata instradata da una coda ACD.</span><span class="sxs-lookup"><span data-stu-id="51f67-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**\_BUSYINCOMING LINEAGENTSTATEEX**</span><span class="sxs-lookup"><span data-stu-id="51f67-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-108">L'agente è occupato a gestire una chiamata in ingresso che non è stata trasferita all'agente da una coda ACD in cui è connesso l'agente.</span><span class="sxs-lookup"><span data-stu-id="51f67-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**\_BUSYOUTGOING LINEAGENTSTATEEX**</span><span class="sxs-lookup"><span data-stu-id="51f67-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-110">L'agente è occupato a gestire una chiamata in uscita, ad esempio una instradata da una coda di composizione predittiva.</span><span class="sxs-lookup"><span data-stu-id="51f67-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ NObattistrada**</span><span class="sxs-lookup"><span data-stu-id="51f67-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-112">L'agente è connesso, ma è occupato da un'attività diversa da quella di una chiamata (ad esempio, in pausa).</span><span class="sxs-lookup"><span data-stu-id="51f67-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="51f67-113">Nessuna chiamata aggiuntiva deve essere indirizzata all'agente.</span><span class="sxs-lookup"><span data-stu-id="51f67-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="51f67-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-115">L'agente è pronto per accettare le chiamate.</span><span class="sxs-lookup"><span data-stu-id="51f67-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ rilasciato**</span><span class="sxs-lookup"><span data-stu-id="51f67-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-117">L'agente è stato rilasciato, probabilmente perché è stato disconnesso.</span><span class="sxs-lookup"><span data-stu-id="51f67-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="51f67-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="51f67-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="51f67-119">Lo stato dell'agente è attualmente sconosciuto, ma può diventare noto in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="51f67-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="51f67-120">Questo può essere uno stato di transizione quando una linea o un indirizzo viene aperto per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="51f67-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="51f67-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51f67-121">Requirements</span></span>



| <span data-ttu-id="51f67-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f67-122">Requirement</span></span> | <span data-ttu-id="51f67-123">Valore</span><span class="sxs-lookup"><span data-stu-id="51f67-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="51f67-124">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="51f67-124">TAPI version</span></span><br/> | <span data-ttu-id="51f67-125">Richiede TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="51f67-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="51f67-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51f67-126">Header</span></span><br/>       | <dl> <span data-ttu-id="51f67-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="51f67-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




