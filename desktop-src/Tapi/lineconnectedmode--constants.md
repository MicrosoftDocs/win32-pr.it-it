---
description: Le \_ costanti del flag di bit LINECONNECTEDMODE descrivono i diversi sottostati di una chiamata connessa.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Costanti LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328905"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="6a55b-103">\_Costanti LINECONNECTEDMODE</span><span class="sxs-lookup"><span data-stu-id="6a55b-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="6a55b-104">Le costanti del flag di bit **LINECONNECTEDMODE \_** descrivono i diversi sottostati di una chiamata connessa.</span><span class="sxs-lookup"><span data-stu-id="6a55b-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="6a55b-105">Una modalità è disponibile come stato della chiamata all'applicazione dopo che lo stato della chiamata passa a connesso e all'interno del \_ messaggio di riga CALLSTATE che indica che la chiamata si trova in LINECALLSTATE \_ connesso.</span><span class="sxs-lookup"><span data-stu-id="6a55b-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="6a55b-106">Questi valori vengono usati quando la chiamata si trova su un indirizzo condiviso (con bridging) con altre stazioni (per altre informazioni, vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi di chiave elettronica.</span><span class="sxs-lookup"><span data-stu-id="6a55b-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="6a55b-107">Le **\_ costanti LINECONNECTEDMODE** presentano i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="6a55b-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="6a55b-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="6a55b-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a55b-109">Indica che la chiamata è connessa alla stazione corrente (la stazione corrente è un partecipante alla chiamata).</span><span class="sxs-lookup"><span data-stu-id="6a55b-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="6a55b-110">Se la modalità di stato della chiamata è pari a 0 (zero), l'applicazione deve presupporre che il valore sia "Active" (che corrisponderebbe alla situazione di un indirizzo non con bridging).</span><span class="sxs-lookup"><span data-stu-id="6a55b-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="6a55b-111">La modalità può passare tra ACTIVE e inactive durante una chiamata se l'utente si unisce e lascia la chiamata attraverso un'azione manuale.</span><span class="sxs-lookup"><span data-stu-id="6a55b-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="6a55b-112">In una situazione di questo tipo, un'operazione [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) potrebbe non eliminare effettivamente la chiamata o inserirla in attesa, perché lo stato di altre stazioni della chiamata può governare, ad esempio il tentativo di "mantenere" una chiamata quando le altre stazioni non sono possibili. al contrario, la chiamata può essere modificata in modalità inattiva se rimane connessa in altre stazioni.</span><span class="sxs-lookup"><span data-stu-id="6a55b-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a55b-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**\_ACTIVEHELD LINECONNECTEDMODE**</span><span class="sxs-lookup"><span data-stu-id="6a55b-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a55b-114">Indica che la stazione è un partecipante attivo nella chiamata, ma che la parte remota ha effettuato la chiamata in attesa (l'altra parte considera la chiamata nello stato onHolding).</span><span class="sxs-lookup"><span data-stu-id="6a55b-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="6a55b-115">In genere, tali informazioni sono disponibili solo quando entrambi gli endpoint della chiamata rientrano nello stesso dominio di cambio.</span><span class="sxs-lookup"><span data-stu-id="6a55b-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="6a55b-116">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6a55b-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="6a55b-117">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="6a55b-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a55b-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confermato**</span><span class="sxs-lookup"><span data-stu-id="6a55b-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a55b-119">Indica che il provider di servizi ha ricevuto una notifica affermativa che la chiamata è entrata nello stato connesso, ad esempio tramite la supervisione della risposta o meccanismi simili.</span><span class="sxs-lookup"><span data-stu-id="6a55b-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="6a55b-120">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6a55b-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="6a55b-121">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="6a55b-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a55b-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INattivo**</span><span class="sxs-lookup"><span data-stu-id="6a55b-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a55b-123">Indica che la chiamata è attiva in una o più stazioni, ma la stazione corrente non è un partecipante alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="6a55b-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="6a55b-124">Se la modalità di stato della chiamata è pari a ZERO, l'applicazione deve presupporre che il valore sia "Active", ovvero la situazione in un indirizzo non con Bridge.</span><span class="sxs-lookup"><span data-stu-id="6a55b-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="6a55b-125">Una chiamata nello stato inattivo può essere unita in join con [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="6a55b-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="6a55b-126">Molte operazioni valide nelle chiamate nello stato connesso possono essere impossibili in modalità inattiva, ad esempio il monitoraggio di toni e cifre, perché la stazione non partecipa effettivamente alla chiamata; il monitoraggio viene in genere sospeso (anche se non annullato) mentre la chiamata è in modalità inattiva.</span><span class="sxs-lookup"><span data-stu-id="6a55b-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6a55b-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**\_INACTIVEHELD LINECONNECTEDMODE**</span><span class="sxs-lookup"><span data-stu-id="6a55b-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6a55b-128">Indica che la stazione non è un partecipante attivo nella chiamata e che la parte remota ha effettuato la chiamata in attesa.</span><span class="sxs-lookup"><span data-stu-id="6a55b-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="6a55b-129">Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6a55b-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="6a55b-130">(Versioni TAPI 2,0 e successive)</span><span class="sxs-lookup"><span data-stu-id="6a55b-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a55b-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a55b-131">Remarks</span></span>

<span data-ttu-id="6a55b-132">Non estendibile.</span><span class="sxs-lookup"><span data-stu-id="6a55b-132">Not extensible.</span></span> <span data-ttu-id="6a55b-133">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="6a55b-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="6a55b-134">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare i \_ valori LINECONNECTEDMODE non supportati nella versione negoziata.</span><span class="sxs-lookup"><span data-stu-id="6a55b-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="6a55b-135">Per le applicazioni che non sono consapevoli di LINECONNECTEDMODE \_ , probabilmente si presuppone che una chiamata in LINECALLSTATE \_ connessa si trovi in LINECONNECTEDMODE \_ Active.</span><span class="sxs-lookup"><span data-stu-id="6a55b-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="6a55b-136">I \_ valori inattivi di LINECONNECTEDMODE Active e LINECONNECTEDMODE \_ vengono usati quando la chiamata si trova in un indirizzo condiviso con altre stazioni (Bridged; vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi a chiave elettronica.</span><span class="sxs-lookup"><span data-stu-id="6a55b-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="6a55b-137">Se la modalità di stato della chiamata connessa è "attiva", significa che la chiamata è connessa alla stazione corrente (la stazione corrente è un partecipante alla chiamata).</span><span class="sxs-lookup"><span data-stu-id="6a55b-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="6a55b-138">Se la modalità di stato della chiamata è "inattiva", la chiamata è attiva in una o più stazioni, ma la stazione corrente non è un partecipante alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="6a55b-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="6a55b-139">Se la modalità di stato della chiamata è pari a ZERO, l'applicazione deve presupporre che il valore sia "Active", ovvero la situazione in un indirizzo non con Bridge.</span><span class="sxs-lookup"><span data-stu-id="6a55b-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="6a55b-140">La modalità può passare tra ACTIVE e inactive durante una chiamata se l'utente si unisce e lascia la chiamata attraverso un'azione manuale.</span><span class="sxs-lookup"><span data-stu-id="6a55b-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="6a55b-141">In una situazione di questo tipo, un'operazione [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) potrebbe non eliminare effettivamente la chiamata o inserirla in attesa, perché lo stato di altre stazioni della chiamata può governare (ad esempio, il tentativo di "tenere" una chiamata quando altre stazioni partecipano non sarà possibile); al contrario, la chiamata può essere semplicemente modificata in modalità inattiva se rimane connessa in altre stazioni.</span><span class="sxs-lookup"><span data-stu-id="6a55b-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="6a55b-142">È possibile unire in join una chiamata nello stato inattivo usando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="6a55b-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="6a55b-143">Molte operazioni valide nelle chiamate nello stato connesso possono essere impossibili in modalità inattiva, ad esempio il monitoraggio di toni e cifre, perché la stazione non partecipa effettivamente alla chiamata; il monitoraggio viene in genere sospeso (anche se non annullato) mentre la chiamata è in modalità inattiva.</span><span class="sxs-lookup"><span data-stu-id="6a55b-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a55b-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a55b-144">Requirements</span></span>



| <span data-ttu-id="6a55b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a55b-145">Requirement</span></span> | <span data-ttu-id="6a55b-146">Valore</span><span class="sxs-lookup"><span data-stu-id="6a55b-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6a55b-147">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="6a55b-147">TAPI version</span></span><br/> | <span data-ttu-id="6a55b-148">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="6a55b-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6a55b-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a55b-149">Header</span></span><br/>       | <dl> <span data-ttu-id="6a55b-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a55b-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a55b-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a55b-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a55b-152">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="6a55b-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="6a55b-153">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="6a55b-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="6a55b-154">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="6a55b-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




