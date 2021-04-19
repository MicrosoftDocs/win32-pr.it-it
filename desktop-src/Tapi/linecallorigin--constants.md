---
description: Le \_ costanti LINECALLORIGIN descrivono l'origine di una chiamata.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Costanti LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326615"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="97134-103">\_Costanti LINECALLORIGIN</span><span class="sxs-lookup"><span data-stu-id="97134-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="97134-104">Le **costanti \_ LINECALLORIGIN** descrivono l'origine di una chiamata.</span><span class="sxs-lookup"><span data-stu-id="97134-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="97134-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_conferenza LINECALLORIGIN**</span><span class="sxs-lookup"><span data-stu-id="97134-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-106">L'handle di chiamata è per una chiamata di conferenza, ovvero è la connessione dell'applicazione al Bridge di conferenza nel Commuter.</span><span class="sxs-lookup"><span data-stu-id="97134-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ esterno**</span><span class="sxs-lookup"><span data-stu-id="97134-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-108">La chiamata ha avuto origine come una chiamata in ingresso su una riga esterna.</span><span class="sxs-lookup"><span data-stu-id="97134-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN in \_ ingresso**</span><span class="sxs-lookup"><span data-stu-id="97134-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-110">La chiamata ha avuto origine come chiamata in ingresso, ma il provider di servizi non è in grado di determinare se proviene da un'altra stazione nello stesso Commuter o da una riga esterna.</span><span class="sxs-lookup"><span data-stu-id="97134-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="97134-111">I provider di servizi possono usare questa costante solo quando è stata negoziata la versione 1,4 o successiva di TAPI.</span><span class="sxs-lookup"><span data-stu-id="97134-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="97134-112">In caso contrario, il provider di servizi può sostituire LINECALLORIGIN \_ undisp.</span><span class="sxs-lookup"><span data-stu-id="97134-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**</span><span class="sxs-lookup"><span data-stu-id="97134-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-114">La chiamata ha avuto origine come chiamata in ingresso in una stazione interna allo stesso ambiente di cambio.</span><span class="sxs-lookup"><span data-stu-id="97134-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN in \_ uscita**</span><span class="sxs-lookup"><span data-stu-id="97134-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-116">La chiamata ha avuto origine da questa stazione come chiamata in uscita.</span><span class="sxs-lookup"><span data-stu-id="97134-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="97134-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-118">L'origine della chiamata non è disponibile e non verrà mai conosciuta per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="97134-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97134-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="97134-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97134-120">L'origine della chiamata è attualmente sconosciuta, ma potrebbe essere nota in seguito.</span><span class="sxs-lookup"><span data-stu-id="97134-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97134-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="97134-121">Remarks</span></span>

<span data-ttu-id="97134-122">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="97134-122">No extensibility.</span></span> <span data-ttu-id="97134-123">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="97134-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="97134-124">L'origine di una chiamata viene archiviata nel membro **dwOrigin** della struttura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) della chiamata.</span><span class="sxs-lookup"><span data-stu-id="97134-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="97134-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97134-125">Requirements</span></span>



| <span data-ttu-id="97134-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="97134-126">Requirement</span></span> | <span data-ttu-id="97134-127">Valore</span><span class="sxs-lookup"><span data-stu-id="97134-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97134-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="97134-128">TAPI version</span></span><br/> | <span data-ttu-id="97134-129">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="97134-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97134-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97134-130">Header</span></span><br/>       | <dl> <span data-ttu-id="97134-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97134-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




