---
description: Le \_ costanti del flag di bit LINEOFFERINGMODE (versioni TAPI 1,4 e successive) descrivono i diversi sottostati di una chiamata a un'offerta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Costanti LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331259"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="e3ae4-103">\_Costanti LINEOFFERINGMODE</span><span class="sxs-lookup"><span data-stu-id="e3ae4-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="e3ae4-104">Le costanti del flag di bit **LINEOFFERINGMODE \_** (versioni TAPI 1,4 e successive) descrivono i diversi sottostati di una chiamata a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="e3ae4-105">Una modalità è disponibile come stato della chiamata all'applicazione dopo lo stato di chiamata trdansitions all'offerta e all'interno del messaggio di [**riga \_ CALLSTATE**](line-callstate.md) che indica che la chiamata è nell' \_ offerta LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="e3ae4-106">Questi valori vengono usati quando la chiamata si trova su un indirizzo condiviso (con bridging) con altre stazioni (vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi di chiave elettronica.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="e3ae4-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="e3ae4-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ae4-108">Indica che la chiamata sta inviando avvisi alla stazione corrente (sarà accompagnata da messaggi di chiamata LINEDEVSTATE \_ ) e, se un'applicazione è configurata in modo da rispondere automaticamente, questa operazione può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="e3ae4-109">Se la modalità di stato della chiamata è pari a ZERO, è necessario che l'applicazione presupponga che il valore sia attivo (che corrisponderebbe alla situazione di un indirizzo non con bridging).</span><span class="sxs-lookup"><span data-stu-id="e3ae4-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="e3ae4-110">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="e3ae4-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3ae4-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INattivo**</span><span class="sxs-lookup"><span data-stu-id="e3ae4-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3ae4-112">Indica che la chiamata viene offerta in più di una stazione, ma che la stazione corrente non sta inviando avvisi (ad esempio, potrebbe trattarsi di una stazione di supervisore in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); il software nella stazione impostata per la risposta automatica dovrebbe preferibilmente non rispondere alla chiamata, perché questo dovrebbe essere la prerogativa della stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="e3ae4-113">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="e3ae4-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3ae4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3ae4-114">Remarks</span></span>

<span data-ttu-id="e3ae4-115">Non estendibile.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-115">Not extensible.</span></span> <span data-ttu-id="e3ae4-116">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="e3ae4-117">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questi \_ valori LINEOFFERINGMODE se non sono supportati nella versione negoziata.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="e3ae4-118">Per le applicazioni che non sono consapevoli di LINEOFFERINGMODE \_ , probabilmente si presuppone che una chiamata nell' \_ offerta LINECALLSTATE sia in LINEOFFERINGMODE \_ Active.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="e3ae4-119">I \_ valori inattivi di LINEOFFERINGMODE Active e LINEOFFERINGMODE \_ vengono usati quando la chiamata si trova in un indirizzo condiviso con altre stazioni (Bridged; vedere [ \_ costanti LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente sistemi a chiave elettronica.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="e3ae4-120">Se la modalità di stato della chiamata dell'offerta è "attiva", significa che la chiamata sta inviando avvisi alla stazione corrente (sarà accompagnata da messaggi di LINEDEVSTATE \_ squillanti) e se un'applicazione è configurata in modo da rispondere automaticamente, questa operazione può essere eseguita.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="e3ae4-121">Se la modalità di stato della chiamata è "inattiva", la chiamata viene offerta in più di una stazione, ma la stazione corrente non sta inviando avvisi (ad esempio, potrebbe trattarsi di una stazione di supervisore in cui lo stato dell'offerta è consultivo, ad esempio lampeggiando una luce); il software nella stazione impostata per la risposta automatica dovrebbe preferibilmente non rispondere alla chiamata, perché questo dovrebbe essere la prerogativa della stazione primaria (avviso), ma è possibile usare [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) per connettere la chiamata.</span><span class="sxs-lookup"><span data-stu-id="e3ae4-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="e3ae4-122">Se la modalità di stato della chiamata è pari a ZERO, è necessario che l'applicazione presupponga che il valore sia attivo (che corrisponderebbe alla situazione di un indirizzo non con bridging).</span><span class="sxs-lookup"><span data-stu-id="e3ae4-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3ae4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3ae4-123">Requirements</span></span>



| <span data-ttu-id="e3ae4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3ae4-124">Requirement</span></span> | <span data-ttu-id="e3ae4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="e3ae4-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3ae4-126">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e3ae4-126">TAPI version</span></span><br/> | <span data-ttu-id="e3ae4-127">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e3ae4-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e3ae4-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3ae4-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e3ae4-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ae4-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




