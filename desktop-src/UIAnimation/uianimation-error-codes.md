---
title: Codici di errore dell'animazione Windows (Winerror. h)
description: Se si verifica un errore, l'animazione di Windows restituisce un codice come valore HRESULT. In questa sezione viene fornito un elenco di codici di errore specifici dell'animazione Windows. Per un elenco di codici di errore COM generali, vedere codici di errore COM.
ms.assetid: 38f15d61-d415-4c7d-b454-5144fc7c9b1e
topic_type:
- apiref
api_name:
- UI_E_CREATE_FAILED
- UI_E_SHUTDOWN_CALLED
- UI_E_ILLEGAL_REENTRANCY
- UI_E_OBJECT_SEALED
- UI_E_VALUE_NOT_SET
- UI_E_VALUE_NOT_DETERMINED
- UI_E_INVALID_OUTPUT
- UI_E_BOOLEAN_EXPECTED
- UI_E_DIFFERENT_OWNER
- UI_E_AMBIGUOUS_MATCH
- UI_E_FP_OVERFLOW
- UI_E_WRONG_THREAD
- UI_E_STORYBOARD_ACTIVE
- UI_E_STORYBOARD_NOT_PLAYING
- UI_E_START_KEYFRAME_AFTER_END
- UI_E_END_KEYFRAME_NOT_DETERMINED
- UI_E_LOOPS_OVERLAP
- UI_E_TRANSITION_ALREADY_USED
- UI_E_TRANSITION_NOT_IN_STORYBOARD
- UI_E_TRANSITION_ECLIPSED
- UI_E_TIME_BEFORE_LAST_UPDATE
- UI_E_TIMER_CLIENT_ALREADY_CONNECTED
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb7c63066690b15ec8fad8ef5b9f74ed5cf2fbc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301500"
---
# <a name="windows-animation-error-codes"></a><span data-ttu-id="533e6-105">Codici di errore dell'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="533e6-105">Windows Animation Error Codes</span></span>

<span data-ttu-id="533e6-106">Se si verifica un errore, l'animazione di Windows restituisce un codice come valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="533e6-106">If an error occurs, Windows Animation returns a code as an **HRESULT** value.</span></span> <span data-ttu-id="533e6-107">In questa sezione viene fornito un elenco di codici di errore specifici dell'animazione Windows.</span><span class="sxs-lookup"><span data-stu-id="533e6-107">This section provides a list of error codes specific to Windows Animation.</span></span> <span data-ttu-id="533e6-108">Per un elenco di codici di errore COM generali, vedere [codici di errore com](/windows/desktop/com/com-error-codes).</span><span class="sxs-lookup"><span data-stu-id="533e6-108">For a list of general COM error codes, see [COM Error Codes](/windows/desktop/com/com-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="533e6-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**creazione dell'interfaccia utente \_ E \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="533e6-109"><span id="UI_E_CREATE_FAILED"></span><span id="ui_e_create_failed"></span>**UI\_E\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-110">0x802A0001</span><span class="sxs-lookup"><span data-stu-id="533e6-110">0x802A0001</span></span>
</dt> <dt>



<span data-ttu-id="533e6-111">Impossibile creare l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="533e6-111">The object could not be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**interfaccia utente \_ E \_ chiusura \_ chiamata**</span><span class="sxs-lookup"><span data-stu-id="533e6-112"><span id="UI_E_SHUTDOWN_CALLED"></span><span id="ui_e_shutdown_called"></span>**UI\_E\_SHUTDOWN\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-113">0x802A0002</span><span class="sxs-lookup"><span data-stu-id="533e6-113">0x802A0002</span></span>
</dt> <dt>



<span data-ttu-id="533e6-114">Il metodo [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) è stato chiamato sul gestore delle animazioni, causando l'arresto di gestione animazioni e tutte le variabili di animazione e gli storyboard creati per essere rilasciati.</span><span class="sxs-lookup"><span data-stu-id="533e6-114">The [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown) method has been called on the animation manager, causing the animation manager to shut down and all the animation variables and storyboards it created to be released.</span></span>

> [!Note]  
> <span data-ttu-id="533e6-115">Non è possibile chiamare metodi su alcun oggetto di animazione dopo l' [**arresto**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span><span class="sxs-lookup"><span data-stu-id="533e6-115">No methods can be called on any animation object after [**Shutdown**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-shutdown).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**interfaccia utente E rientranza non \_ \_ valida \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-116"><span id="UI_E_ILLEGAL_REENTRANCY"></span><span id="ui_e_illegal_reentrancy"></span>**UI\_E\_ILLEGAL\_REENTRANCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-117">0x802A0003</span><span class="sxs-lookup"><span data-stu-id="533e6-117">0x802A0003</span></span>
</dt> <dt>



<span data-ttu-id="533e6-118">Questo metodo non può essere chiamato durante questo tipo di callback.</span><span class="sxs-lookup"><span data-stu-id="533e6-118">This method cannot be called during this type of callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**interfaccia utente \_ E \_ oggetto \_ sealed**</span><span class="sxs-lookup"><span data-stu-id="533e6-119"><span id="UI_E_OBJECT_SEALED"></span><span id="ui_e_object_sealed"></span>**UI\_E\_OBJECT\_SEALED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-120">0x802A0004</span><span class="sxs-lookup"><span data-stu-id="533e6-120">0x802A0004</span></span>
</dt> <dt>



<span data-ttu-id="533e6-121">Questo oggetto è stato sealed, quindi questa modifica non è più consentita.</span><span class="sxs-lookup"><span data-stu-id="533e6-121">This object has been sealed, so this change is no longer allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**valore dell'interfaccia utente \_ E \_ \_ non \_ impostato**</span><span class="sxs-lookup"><span data-stu-id="533e6-122"><span id="UI_E_VALUE_NOT_SET"></span><span id="ui_e_value_not_set"></span>**UI\_E\_VALUE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-123">0x802A0005</span><span class="sxs-lookup"><span data-stu-id="533e6-123">0x802A0005</span></span>
</dt> <dt>



<span data-ttu-id="533e6-124">Il valore richiesto non è mai stato impostato e pertanto non può essere recuperato.</span><span class="sxs-lookup"><span data-stu-id="533e6-124">The requested value has never been set, and therefore cannot be retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**valore dell'interfaccia utente \_ E \_ \_ non \_ determinato**</span><span class="sxs-lookup"><span data-stu-id="533e6-125"><span id="UI_E_VALUE_NOT_DETERMINED"></span><span id="ui_e_value_not_determined"></span>**UI\_E\_VALUE\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-126">0x802A0006</span><span class="sxs-lookup"><span data-stu-id="533e6-126">0x802A0006</span></span>
</dt> <dt>



<span data-ttu-id="533e6-127">Impossibile determinare il valore richiesto.</span><span class="sxs-lookup"><span data-stu-id="533e6-127">The requested value cannot be determined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**OUTPUT dell'interfaccia utente \_ E \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-128"><span id="UI_E_INVALID_OUTPUT"></span><span id="ui_e_invalid_output"></span>**UI\_E\_INVALID\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-129">0x802A0007</span><span class="sxs-lookup"><span data-stu-id="533e6-129">0x802A0007</span></span>
</dt> <dt>



<span data-ttu-id="533e6-130">Un callback ha restituito un parametro di output non valido.</span><span class="sxs-lookup"><span data-stu-id="533e6-130">A callback returned an invalid output parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**prevista l'interfaccia utente \_ E un \_ valore booleano \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-131"><span id="UI_E_BOOLEAN_EXPECTED"></span><span id="ui_e_boolean_expected"></span>**UI\_E\_BOOLEAN\_EXPECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-132">0x802A0008</span><span class="sxs-lookup"><span data-stu-id="533e6-132">0x802A0008</span></span>
</dt> <dt>



<span data-ttu-id="533e6-133">Un callback ha restituito un codice di esito positivo diverso da S \_ OK o s \_ false.</span><span class="sxs-lookup"><span data-stu-id="533e6-133">A callback returned a success code other than S\_OK or S\_FALSE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**interfaccia \_ utente \_ E \_ proprietario diverso**</span><span class="sxs-lookup"><span data-stu-id="533e6-134"><span id="UI_E_DIFFERENT_OWNER"></span><span id="ui_e_different_owner"></span>**UI\_E\_DIFFERENT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-135">0x802A0009</span><span class="sxs-lookup"><span data-stu-id="533e6-135">0x802A0009</span></span>
</dt> <dt>



<span data-ttu-id="533e6-136">Un parametro che deve essere di proprietà di questo oggetto è di proprietà di un oggetto diverso.</span><span class="sxs-lookup"><span data-stu-id="533e6-136">A parameter that should be owned by this object is owned by a different object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**interfaccia \_ utente \_ E \_ corrispondenza ambigua**</span><span class="sxs-lookup"><span data-stu-id="533e6-137"><span id="UI_E_AMBIGUOUS_MATCH"></span><span id="ui_e_ambiguous_match"></span>**UI\_E\_AMBIGUOUS\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-138">0x802A000A</span><span class="sxs-lookup"><span data-stu-id="533e6-138">0x802A000A</span></span>
</dt> <dt>



<span data-ttu-id="533e6-139">Più di un elemento corrisponde ai criteri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="533e6-139">More than one item matched the search criteria.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**OVERFLOW dell'interfaccia utente \_ E \_ FP \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-140"><span id="UI_E_FP_OVERFLOW"></span><span id="ui_e_fp_overflow"></span>**UI\_E\_FP\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-141">0x802A000B</span><span class="sxs-lookup"><span data-stu-id="533e6-141">0x802A000B</span></span>
</dt> <dt>



<span data-ttu-id="533e6-142">Si è verificato un overflow a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="533e6-142">A floating-point overflow occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**\_thread UI E \_ errato \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-143"><span id="UI_E_WRONG_THREAD"></span><span id="ui_e_wrong_thread"></span>**UI\_E\_WRONG\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-144">0x802A000C</span><span class="sxs-lookup"><span data-stu-id="533e6-144">0x802A000C</span></span>
</dt> <dt>



<span data-ttu-id="533e6-145">Questo metodo può essere chiamato solo dal thread che ha creato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="533e6-145">This method can only be called from the thread that created the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**interfaccia utente \_ E \_ Storyboard \_ attivi**</span><span class="sxs-lookup"><span data-stu-id="533e6-146"><span id="UI_E_STORYBOARD_ACTIVE"></span><span id="ui_e_storyboard_active"></span>**UI\_E\_STORYBOARD\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-147">0x802A0101</span><span class="sxs-lookup"><span data-stu-id="533e6-147">0x802A0101</span></span>
</dt> <dt>



<span data-ttu-id="533e6-148">Lo storyboard è attualmente nella pianificazione.</span><span class="sxs-lookup"><span data-stu-id="533e6-148">The storyboard is currently in the schedule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**STORYBOARD dell'interfaccia utente \_ E \_ non in \_ \_ esecuzione**</span><span class="sxs-lookup"><span data-stu-id="533e6-149"><span id="UI_E_STORYBOARD_NOT_PLAYING"></span><span id="ui_e_storyboard_not_playing"></span>**UI\_E\_STORYBOARD\_NOT\_PLAYING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-150">0x802A0102</span><span class="sxs-lookup"><span data-stu-id="533e6-150">0x802A0102</span></span>
</dt> <dt>



<span data-ttu-id="533e6-151">Lo storyboard non viene riprodotto.</span><span class="sxs-lookup"><span data-stu-id="533e6-151">The storyboard is not playing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**interfaccia utente \_ E \_ inizio \_ fotogramma chiave \_ dopo la \_ fine**</span><span class="sxs-lookup"><span data-stu-id="533e6-152"><span id="UI_E_START_KEYFRAME_AFTER_END"></span><span id="ui_e_start_keyframe_after_end"></span>**UI\_E\_START\_KEYFRAME\_AFTER\_END**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-153">0x802A0103</span><span class="sxs-lookup"><span data-stu-id="533e6-153">0x802A0103</span></span>
</dt> <dt>



<span data-ttu-id="533e6-154">Il fotogramma chiave iniziale potrebbe verificarsi dopo il fotogramma chiave End.</span><span class="sxs-lookup"><span data-stu-id="533e6-154">The start keyframe might occur after the end keyframe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**fotogramma chiave dell'interfaccia utente \_ E \_ fine \_ \_ non \_ determinato**</span><span class="sxs-lookup"><span data-stu-id="533e6-155"><span id="UI_E_END_KEYFRAME_NOT_DETERMINED"></span><span id="ui_e_end_keyframe_not_determined"></span>**UI\_E\_END\_KEYFRAME\_NOT\_DETERMINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-156">0x802A0104</span><span class="sxs-lookup"><span data-stu-id="533e6-156">0x802A0104</span></span>
</dt> <dt>



<span data-ttu-id="533e6-157">Potrebbe non essere possibile determinare l'ora di fine del fotogramma chiave quando viene raggiunto il fotogramma chiave di avvio.</span><span class="sxs-lookup"><span data-stu-id="533e6-157">It might not be possible to determine the end keyframe time when the start keyframe is reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**\_sovrapposizione di \_ cicli dell'interfaccia utente \_**</span><span class="sxs-lookup"><span data-stu-id="533e6-158"><span id="UI_E_LOOPS_OVERLAP"></span><span id="ui_e_loops_overlap"></span>**UI\_E\_LOOPS\_OVERLAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-159">0x802A0105</span><span class="sxs-lookup"><span data-stu-id="533e6-159">0x802A0105</span></span>
</dt> <dt>



<span data-ttu-id="533e6-160">Due parti ripetute di uno storyboard potrebbero sovrapporsi.</span><span class="sxs-lookup"><span data-stu-id="533e6-160">Two repeated portions of a storyboard might overlap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**transizione interfaccia utente \_ E \_ già in \_ \_ uso**</span><span class="sxs-lookup"><span data-stu-id="533e6-161"><span id="UI_E_TRANSITION_ALREADY_USED"></span><span id="ui_e_transition_already_used"></span>**UI\_E\_TRANSITION\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-162">0x802A0106</span><span class="sxs-lookup"><span data-stu-id="533e6-162">0x802A0106</span></span>
</dt> <dt>



<span data-ttu-id="533e6-163">La transizione è già stata aggiunta a uno storyboard diverso oppure è stata aggiunta a uno storyboard che ha terminato la riproduzione ed è stata rilasciata.</span><span class="sxs-lookup"><span data-stu-id="533e6-163">The transition has already been added to a different storyboard or has been added to a storyboard that has finished playing and been released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**transizione dell'interfaccia utente \_ E \_ \_ non \_ nello \_ storyboard**</span><span class="sxs-lookup"><span data-stu-id="533e6-164"><span id="UI_E_TRANSITION_NOT_IN_STORYBOARD"></span><span id="ui_e_transition_not_in_storyboard"></span>**UI\_E\_TRANSITION\_NOT\_IN\_STORYBOARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-165">0x802A0107</span><span class="sxs-lookup"><span data-stu-id="533e6-165">0x802A0107</span></span>
</dt> <dt>



<span data-ttu-id="533e6-166">La transizione non è stata aggiunta ad alcun Storyboard.</span><span class="sxs-lookup"><span data-stu-id="533e6-166">The transition has not been added to any storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**transizione dell'interfaccia utente \_ E \_ \_ eclissata**</span><span class="sxs-lookup"><span data-stu-id="533e6-167"><span id="UI_E_TRANSITION_ECLIPSED"></span><span id="ui_e_transition_eclipsed"></span>**UI\_E\_TRANSITION\_ECLIPSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-168">0x802A0108</span><span class="sxs-lookup"><span data-stu-id="533e6-168">0x802A0108</span></span>
</dt> <dt>



<span data-ttu-id="533e6-169">La transizione potrebbe eclissare l'inizio di un'altra transizione nello storyboard.</span><span class="sxs-lookup"><span data-stu-id="533e6-169">The transition might eclipse the beginning of another transition in the storyboard.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**interfaccia utente \_ E \_ tempo prima dell' \_ \_ ultimo \_ aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="533e6-170"><span id="UI_E_TIME_BEFORE_LAST_UPDATE"></span><span id="ui_e_time_before_last_update"></span>**UI\_E\_TIME\_BEFORE\_LAST\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-171">0x802A0109</span><span class="sxs-lookup"><span data-stu-id="533e6-171">0x802A0109</span></span>
</dt> <dt>



<span data-ttu-id="533e6-172">L'ora specificata è precedente all'ora passata all'ultimo aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="533e6-172">The specified time is earlier than the time passed to the last update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="533e6-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**\_client timer interfaccia utente E \_ \_ \_ già \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="533e6-173"><span id="UI_E_TIMER_CLIENT_ALREADY_CONNECTED"></span><span id="ui_e_timer_client_already_connected"></span>**UI\_E\_TIMER\_CLIENT\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533e6-174">0x802A010A</span><span class="sxs-lookup"><span data-stu-id="533e6-174">0x802A010A</span></span>
</dt> <dt>



<span data-ttu-id="533e6-175">Questo client è già connesso a un timer.</span><span class="sxs-lookup"><span data-stu-id="533e6-175">This client is already connected to a timer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="533e6-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="533e6-176">Requirements</span></span>



| <span data-ttu-id="533e6-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="533e6-177">Requirement</span></span> | <span data-ttu-id="533e6-178">Valore</span><span class="sxs-lookup"><span data-stu-id="533e6-178">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="533e6-179">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533e6-179">Minimum supported client</span></span><br/> | <span data-ttu-id="533e6-180">Windows 7, Windows Vista e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="533e6-180">Windows 7, Windows Vista and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="533e6-181">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533e6-181">Minimum supported server</span></span><br/> | <span data-ttu-id="533e6-182">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="533e6-182">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="533e6-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="533e6-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="533e6-184"><dt>Winerror. h</dt></span><span class="sxs-lookup"><span data-stu-id="533e6-184"><dt>Winerror.h</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="533e6-185">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="533e6-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533e6-186">Informazioni di riferimento sull'animazione Windows</span><span class="sxs-lookup"><span data-stu-id="533e6-186">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

