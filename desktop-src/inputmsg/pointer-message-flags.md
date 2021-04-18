---
title: Flag messaggi puntatore
description: Valori utilizzati in diverse macro del puntatore (vedere macro).
ms.assetid: C3AF232C-A68E-48DA-A8D3-4ECE6F19317A
topic_type:
- apiref
api_name:
- POINTER_MESSAGE_FLAG_NEW
- POINTER_MESSAGE_FLAG_INRANGE
- POINTER_MESSAGE_FLAG_INCONTACT
- POINTER_MESSAGE_FLAG_FIRSTBUTTON
- POINTER_MESSAGE_FLAG_SECONDBUTTON
- POINTER_MESSAGE_FLAG_THIRDBUTTON
- POINTER_MESSAGE_FLAG_FOURTHBUTTON
- POINTER_MESSAGE_FLAG_FIFTHBUTTON
- POINTER_MESSAGE_FLAG_PRIMARY
- POINTER_MESSAGE_FLAG_CONFIDENCE
- POINTER_MESSAGE_FLAG_CANCELED
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 853566dc6db7cfafed6a73b9a1ba3032001f02cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302078"
---
# <a name="pointer-message-flags"></a><span data-ttu-id="e84be-103">Flag messaggi puntatore</span><span class="sxs-lookup"><span data-stu-id="e84be-103">Pointer Message Flags</span></span>

<span data-ttu-id="e84be-104">Valori utilizzati in diverse macro del puntatore (vedere [macro](macros.md)).</span><span class="sxs-lookup"><span data-stu-id="e84be-104">Values that are used in various pointer macros (see [Macros](macros.md)).</span></span>

<dl> <dt>

<span data-ttu-id="e84be-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="e84be-105"><span id="POINTER_MESSAGE_FLAG_NEW"></span><span id="pointer_message_flag_new"></span>**POINTER_MESSAGE_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e84be-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e84be-107">Indica l'arrivo di un nuovo puntatore.</span><span class="sxs-lookup"><span data-stu-id="e84be-107">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="e84be-108"><span id="POINTER_MESSAGE_FLAG_INRANGE"></span><span id="pointer_message_flag_inrange"></span>**POINTER_MESSAGE_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e84be-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e84be-110">Indica che il puntatore continua a esistere.</span><span class="sxs-lookup"><span data-stu-id="e84be-110">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="e84be-111">Quando questo flag non è impostato, indica che il puntatore ha un intervallo di rilevamento sinistro.</span><span class="sxs-lookup"><span data-stu-id="e84be-111">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="e84be-112">Questo flag non viene in genere impostato solo quando un puntatore del mouse lascia un intervallo di rilevamento (**POINTER_FLAG_UPDATE** è impostato) o quando un puntatore in contatto con una superficie della finestra lascia un intervallo di rilevamento (**POINTER_FLAG_UP** è impostato).</span><span class="sxs-lookup"><span data-stu-id="e84be-112">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="e84be-113"><span id="POINTER_MESSAGE_FLAG_INCONTACT"></span><span id="pointer_message_flag_incontact"></span>**POINTER_MESSAGE_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e84be-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e84be-115">Indica che il puntatore è in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="e84be-115">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="e84be-116">Quando questo flag non è impostato, indica un puntatore al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-116">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e84be-117"><span id="POINTER_MESSAGE_FLAG_FIRSTBUTTON"></span><span id="pointer_message_flag_firstbutton"></span>**POINTER_MESSAGE_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-118">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e84be-118">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e84be-119">Indica un'azione primaria, analoga a un pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-119">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="e84be-120">Questo flag è impostato in un puntatore tocco quando è in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="e84be-120">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="e84be-121">Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="e84be-121">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="e84be-122">Questo flag è impostato su un puntatore del mouse quando il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="e84be-122">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e84be-123"><span id="POINTER_MESSAGE_FLAG_SECONDBUTTON"></span><span id="pointer_message_flag_secondbutton"></span>**POINTER_MESSAGE_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-124">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e84be-124">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e84be-125">Indica un'azione secondaria, analoga a un pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-125">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="e84be-126">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-126">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-127">Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.</span><span class="sxs-lookup"><span data-stu-id="e84be-127">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="e84be-128">Questo flag è impostato da un puntatore del mouse quando il pulsante destro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="e84be-128">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e84be-129"><span id="POINTER_MESSAGE_FLAG_THIRDBUTTON"></span><span id="pointer_message_flag_thirdbutton"></span>**POINTER_MESSAGE_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-130">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e84be-130">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e84be-131">Analogo al pulsante della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-131">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="e84be-132">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-132">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-133">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-133">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-134">Questo flag è impostato da un puntatore del mouse quando il pulsante della rotellina del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e84be-134">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e84be-135"><span id="POINTER_MESSAGE_FLAG_FOURTHBUTTON"></span><span id="pointer_message_flag_fourthbutton"></span>**POINTER_MESSAGE_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-136">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e84be-136">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="e84be-137">Analogo a un primo pulsante del mouse esteso (XButton1).</span><span class="sxs-lookup"><span data-stu-id="e84be-137">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="e84be-138">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-138">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-139">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-139">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-140">Questo flag è impostato da un puntatore del mouse quando il primo pulsante del mouse esteso (XBUTTON1) è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e84be-140">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e84be-141"><span id="POINTER_MESSAGE_FLAG_FIFTHBUTTON"></span><span id="pointer_message_flag_fifthbutton"></span>**POINTER_MESSAGE_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-142">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e84be-142">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="e84be-143">Analogo a un secondo pulsante del mouse esteso (XButton2).</span><span class="sxs-lookup"><span data-stu-id="e84be-143">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="e84be-144">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-144">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-145">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e84be-145">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e84be-146">Questo flag è impostato da un puntatore del mouse quando il secondo pulsante del mouse esteso (XBUTTON2) è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e84be-146">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="e84be-147"><span id="POINTER_MESSAGE_FLAG_PRIMARY"></span><span id="pointer_message_flag_primary"></span>**POINTER_MESSAGE_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-148">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e84be-148">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e84be-149">Indica che il puntatore è stato designato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e84be-149">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="e84be-150">Un puntatore primario è un puntatore singolo che può eseguire azioni oltre a quelle disponibili per i puntatori non primari.</span><span class="sxs-lookup"><span data-stu-id="e84be-150">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="e84be-151">Ad esempio, quando un puntatore primario mette in contatto con una superficie della finestra, può fornire alla finestra la possibilità di attivare inviando una WM_POINTERACTIVATE messaggio.</span><span class="sxs-lookup"><span data-stu-id="e84be-151">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a WM_POINTERACTIVATE message.</span></span>

<span data-ttu-id="e84be-152">Il puntatore primario viene identificato da tutte le interazioni utente correnti nel sistema (mouse, tocco, penna e così via).</span><span class="sxs-lookup"><span data-stu-id="e84be-152">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="e84be-153">Di conseguenza, il puntatore primario potrebbe non essere associato all'app.</span><span class="sxs-lookup"><span data-stu-id="e84be-153">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="e84be-154">Il primo contatto in un'interazione multitocco viene impostato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e84be-154">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="e84be-155">Una volta identificato un puntatore primario, è necessario rimuovere tutti i contatti prima che un nuovo contatto possa essere identificato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e84be-155">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="e84be-156">Per le app che non elaborano l'input del puntatore, solo gli eventi del puntatore primario vengono promossi agli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-156">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="e84be-157"><span id="POINTER_MESSAGE_FLAG_CONFIDENCE"></span><span id="pointer_message_flag_confidence"></span>**POINTER_MESSAGE_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-158">0x00000400</span><span class="sxs-lookup"><span data-stu-id="e84be-158">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="e84be-159">Un suggerimento dal dispositivo di origine indica se il puntatore rappresenta un'interazione intenzionale o accidentale, che è particolarmente rilevante per PT_TOUCH puntatori in cui un'interazione accidentale (ad esempio con il Palm della mano) può attivare l'input.</span><span class="sxs-lookup"><span data-stu-id="e84be-159">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="e84be-160">La presenza di questo flag indica che il dispositivo di origine ha una sicurezza elevata che questo input fa parte di un'interazione prevista.</span><span class="sxs-lookup"><span data-stu-id="e84be-160">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e84be-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="e84be-161"><span id="POINTER_MESSAGE_FLAG_CANCELED"></span><span id="pointer_message_flag_canceled"></span>**POINTER_MESSAGE_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e84be-162">0x00000800</span><span class="sxs-lookup"><span data-stu-id="e84be-162">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="e84be-163">Indica che il puntatore viene ripartito in modo anomalo, ad esempio quando il sistema riceve un input non valido per il puntatore o quando un dispositivo con puntatori attivi viene ripartito in modo improvviso.</span><span class="sxs-lookup"><span data-stu-id="e84be-163">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="e84be-164">Se l'applicazione che riceve l'input è in una posizione a tale scopo, deve considerare l'interazione come non completata e invertire gli effetti del puntatore interessato.</span><span class="sxs-lookup"><span data-stu-id="e84be-164">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e84be-165">Commenti</span><span class="sxs-lookup"><span data-stu-id="e84be-165">Remarks</span></span>

<span data-ttu-id="e84be-166">XBUTTON1 e XBUTTON2 sono pulsanti aggiuntivi usati in molti dispositivi mouse.</span><span class="sxs-lookup"><span data-stu-id="e84be-166">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="e84be-167">Restituiscono gli stessi dati dei pulsanti del mouse standard.</span><span class="sxs-lookup"><span data-stu-id="e84be-167">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="e84be-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e84be-168">Requirements</span></span>



| <span data-ttu-id="e84be-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="e84be-169">Requirement</span></span> | <span data-ttu-id="e84be-170">Valore</span><span class="sxs-lookup"><span data-stu-id="e84be-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e84be-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84be-171">Minimum supported client</span></span><br/> | <span data-ttu-id="e84be-172">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e84be-172">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e84be-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e84be-173">Minimum supported server</span></span><br/> | <span data-ttu-id="e84be-174">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e84be-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e84be-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e84be-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="e84be-176"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e84be-176"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e84be-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e84be-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e84be-178">Costanti</span><span class="sxs-lookup"><span data-stu-id="e84be-178">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e84be-179">Macro</span><span class="sxs-lookup"><span data-stu-id="e84be-179">Macros</span></span>](macros.md)
</dt> </dl>

 

 





