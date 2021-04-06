---
title: Flag puntatore
description: Valori che possono essere visualizzati nel campo pointerFlags della struttura POINTER_INFO.
ms.assetid: CC3F8E21-F4FF-495C-922E-A3708D3F2093
topic_type:
- apiref
api_name:
- POINTER_FLAG_NONE
- POINTER_FLAG_NEW
- POINTER_FLAG_INRANGE
- POINTER_FLAG_INCONTACT
- POINTER_FLAG_FIRSTBUTTON
- POINTER_FLAG_SECONDBUTTON
- POINTER_FLAG_THIRDBUTTON
- POINTER_FLAG_FOURTHBUTTON
- POINTER_FLAG_FIFTHBUTTON
- POINTER_FLAG_PRIMARY
- POINTER_FLAG_CONFIDENCE
- POINTER_FLAG_CANCELED
- POINTER_FLAG_DOWN
- POINTER_FLAG_UPDATE
- POINTER_FLAG_UP
- POINTER_FLAG_WHEEL
- POINTER_FLAG_HWHEEL
- POINTER_FLAG_CAPTURECHANGED
- POINTER_FLAG_HASTRANSFORM
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 21a4191aa09bcb0cb9fda1a4c9bc011d978e203a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742330"
---
# <a name="pointer-flags"></a><span data-ttu-id="e2765-103">Flag puntatore</span><span class="sxs-lookup"><span data-stu-id="e2765-103">Pointer Flags</span></span>

<span data-ttu-id="e2765-104">Valori che possono essere visualizzati nel campo **pointerFlags** della struttura [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="e2765-104">Values that can appear in the **pointerFlags** field of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="e2765-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="e2765-105"><span id="POINTER_FLAG_NONE"></span><span id="pointer_flag_none"></span>**POINTER_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e2765-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-107">Predefinito</span><span class="sxs-lookup"><span data-stu-id="e2765-107">Default</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span><span class="sxs-lookup"><span data-stu-id="e2765-108"><span id="POINTER_FLAG_NEW"></span><span id="pointer_flag_new"></span>**POINTER_FLAG_NEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e2765-109">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="e2765-110">Indica l'arrivo di un nuovo puntatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-110">Indicates the arrival of a new pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span><span class="sxs-lookup"><span data-stu-id="e2765-111"><span id="POINTER_FLAG_INRANGE"></span><span id="pointer_flag_inrange"></span>**POINTER_FLAG_INRANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-112">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e2765-112">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="e2765-113">Indica che il puntatore continua a esistere.</span><span class="sxs-lookup"><span data-stu-id="e2765-113">Indicates that this pointer continues to exist.</span></span> <span data-ttu-id="e2765-114">Quando questo flag non è impostato, indica che il puntatore ha un intervallo di rilevamento sinistro.</span><span class="sxs-lookup"><span data-stu-id="e2765-114">When this flag is not set, it indicates the pointer has left detection range.</span></span>

<span data-ttu-id="e2765-115">Questo flag non viene in genere impostato solo quando un puntatore del mouse lascia un intervallo di rilevamento (**POINTER_FLAG_UPDATE** è impostato) o quando un puntatore in contatto con una superficie della finestra lascia un intervallo di rilevamento (**POINTER_FLAG_UP** è impostato).</span><span class="sxs-lookup"><span data-stu-id="e2765-115">This flag is typically not set only when a hovering pointer leaves detection range (**POINTER_FLAG_UPDATE** is set) or when a pointer in contact with a window surface leaves detection range (**POINTER_FLAG_UP** is set).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span><span class="sxs-lookup"><span data-stu-id="e2765-116"><span id="POINTER_FLAG_INCONTACT"></span><span id="pointer_flag_incontact"></span>**POINTER_FLAG_INCONTACT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-117">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e2765-117">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="e2765-118">Indica che il puntatore è in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-118">Indicates that this pointer is in contact with the digitizer surface.</span></span> <span data-ttu-id="e2765-119">Quando questo flag non è impostato, indica un puntatore al passaggio del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-119">When this flag is not set, it indicates a hovering pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2765-120"><span id="POINTER_FLAG_FIRSTBUTTON"></span><span id="pointer_flag_firstbutton"></span>**POINTER_FLAG_FIRSTBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-121">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e2765-121">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="e2765-122">Indica un'azione primaria, analoga a un pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-122">Indicates a primary action, analogous to a left mouse button down.</span></span>

<span data-ttu-id="e2765-123">Questo flag è impostato in un puntatore tocco quando è in contatto con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-123">A touch pointer has this flag set when it is in contact with the digitizer surface.</span></span>

<span data-ttu-id="e2765-124">Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore senza pulsanti premuti.</span><span class="sxs-lookup"><span data-stu-id="e2765-124">A pen pointer has this flag set when it is in contact with the digitizer surface with no buttons pressed.</span></span>

<span data-ttu-id="e2765-125">Questo flag è impostato su un puntatore del mouse quando il pulsante sinistro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="e2765-125">A mouse pointer has this flag set when the left mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2765-126"><span id="POINTER_FLAG_SECONDBUTTON"></span><span id="pointer_flag_secondbutton"></span>**POINTER_FLAG_SECONDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-127">0x00000020</span><span class="sxs-lookup"><span data-stu-id="e2765-127">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="e2765-128">Indica un'azione secondaria, analoga a un pulsante destro del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-128">Indicates a secondary action, analogous to a right mouse button down.</span></span>

<span data-ttu-id="e2765-129">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-129">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-130">Questo flag è impostato in un puntatore di penna quando è in contatto con la superficie del digitalizzatore con il pulsante della penna premuto.</span><span class="sxs-lookup"><span data-stu-id="e2765-130">A pen pointer has this flag set when it is in contact with the digitizer surface with the pen barrel button pressed.</span></span>

<span data-ttu-id="e2765-131">Questo flag è impostato da un puntatore del mouse quando il pulsante destro del mouse è premuto.</span><span class="sxs-lookup"><span data-stu-id="e2765-131">A mouse pointer has this flag set when the right mouse button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2765-132"><span id="POINTER_FLAG_THIRDBUTTON"></span><span id="pointer_flag_thirdbutton"></span>**POINTER_FLAG_THIRDBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-133">0x00000040</span><span class="sxs-lookup"><span data-stu-id="e2765-133">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="e2765-134">Analogo al pulsante della rotellina del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-134">Analogous to a mouse wheel button down.</span></span>

<span data-ttu-id="e2765-135">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-135">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-136">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-136">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-137">Questo flag è impostato da un puntatore del mouse quando il pulsante della rotellina del mouse è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e2765-137">A mouse pointer has this flag set when the mouse wheel button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2765-138"><span id="POINTER_FLAG_FOURTHBUTTON"></span><span id="pointer_flag_fourthbutton"></span>**POINTER_FLAG_FOURTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-139">0x00000080</span><span class="sxs-lookup"><span data-stu-id="e2765-139">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="e2765-140">Analogo a un primo pulsante del mouse esteso (XButton1).</span><span class="sxs-lookup"><span data-stu-id="e2765-140">Analogous to a first extended mouse (XButton1) button down.</span></span>

<span data-ttu-id="e2765-141">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-141">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-142">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-142">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-143">Questo flag è impostato da un puntatore del mouse quando il primo pulsante del mouse esteso (XBUTTON1) è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e2765-143">A mouse pointer has this flag set when the first extended mouse (XBUTTON1) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span><span class="sxs-lookup"><span data-stu-id="e2765-144"><span id="POINTER_FLAG_FIFTHBUTTON"></span><span id="pointer_flag_fifthbutton"></span>**POINTER_FLAG_FIFTHBUTTON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-145">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e2765-145">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="e2765-146">Analogo a un secondo pulsante del mouse esteso (XButton2).</span><span class="sxs-lookup"><span data-stu-id="e2765-146">Analogous to a second extended mouse (XButton2) button down.</span></span>

<span data-ttu-id="e2765-147">Un puntatore tocco non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-147">A touch pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-148">Un puntatore penna non utilizza questo flag.</span><span class="sxs-lookup"><span data-stu-id="e2765-148">A pen pointer does not use this flag.</span></span>

<span data-ttu-id="e2765-149">Questo flag è impostato da un puntatore del mouse quando il secondo pulsante del mouse esteso (XBUTTON2) è inattivo.</span><span class="sxs-lookup"><span data-stu-id="e2765-149">A mouse pointer has this flag set when the second extended mouse (XBUTTON2) button is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span><span class="sxs-lookup"><span data-stu-id="e2765-150"><span id="POINTER_FLAG_PRIMARY"></span><span id="pointer_flag_primary"></span>**POINTER_FLAG_PRIMARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-151">0x00002000</span><span class="sxs-lookup"><span data-stu-id="e2765-151">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-152">Indica che il puntatore è stato designato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e2765-152">Indicates that this pointer has been designated as the primary pointer.</span></span> <span data-ttu-id="e2765-153">Un puntatore primario è un puntatore singolo che può eseguire azioni oltre a quelle disponibili per i puntatori non primari.</span><span class="sxs-lookup"><span data-stu-id="e2765-153">A primary pointer is a single pointer that can perform actions beyond those available to non-primary pointers.</span></span> <span data-ttu-id="e2765-154">Ad esempio, quando un puntatore primario mette in contatto con una superficie della finestra, può fornire alla finestra la possibilità di attivare inviando una [**WM_POINTERACTIVATE**](wm-pointeractivate.md) messaggio.</span><span class="sxs-lookup"><span data-stu-id="e2765-154">For example, when a primary pointer makes contact with a window s surface, it may provide the window an opportunity to activate by sending it a [**WM_POINTERACTIVATE**](wm-pointeractivate.md) message.</span></span>

<span data-ttu-id="e2765-155">Il puntatore primario viene identificato da tutte le interazioni utente correnti nel sistema (mouse, tocco, penna e così via).</span><span class="sxs-lookup"><span data-stu-id="e2765-155">The primary pointer is identified from all current user interactions on the system (mouse, touch, pen, and so on).</span></span> <span data-ttu-id="e2765-156">Di conseguenza, il puntatore primario potrebbe non essere associato all'app.</span><span class="sxs-lookup"><span data-stu-id="e2765-156">As such, the primary pointer might not be associated with your app.</span></span> <span data-ttu-id="e2765-157">Il primo contatto in un'interazione multitocco viene impostato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e2765-157">The first contact in a multi-touch interaction is set as the primary pointer.</span></span> <span data-ttu-id="e2765-158">Una volta identificato un puntatore primario, è necessario rimuovere tutti i contatti prima che un nuovo contatto possa essere identificato come puntatore primario.</span><span class="sxs-lookup"><span data-stu-id="e2765-158">Once a primary pointer is identified, all contacts must be lifted before a new contact can be identified as a primary pointer.</span></span> <span data-ttu-id="e2765-159">Per le app che non elaborano l'input del puntatore, solo gli eventi del puntatore primario vengono promossi agli eventi del mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-159">For apps that don't process pointer input, only the primary pointer's events are promoted to mouse events.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span><span class="sxs-lookup"><span data-stu-id="e2765-160"><span id="POINTER_FLAG_CONFIDENCE"></span><span id="pointer_flag_confidence"></span>**POINTER_FLAG_CONFIDENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-161">0x000004000</span><span class="sxs-lookup"><span data-stu-id="e2765-161">0x000004000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-162">Un suggerimento dal dispositivo di origine indica se il puntatore rappresenta un'interazione intenzionale o accidentale, che è particolarmente rilevante per PT_TOUCH puntatori in cui un'interazione accidentale (ad esempio con il Palm della mano) può attivare l'input.</span><span class="sxs-lookup"><span data-stu-id="e2765-162">Confidence is a suggestion from the source device about whether the pointer represents an intended or accidental interaction, which is especially relevant for PT_TOUCH pointers where an accidental interaction (such as with the palm of the hand) can trigger input.</span></span> <span data-ttu-id="e2765-163">La presenza di questo flag indica che il dispositivo di origine ha una sicurezza elevata che questo input fa parte di un'interazione prevista.</span><span class="sxs-lookup"><span data-stu-id="e2765-163">The presence of this flag indicates that the source device has high confidence that this input is part of an intended interaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span><span class="sxs-lookup"><span data-stu-id="e2765-164"><span id="POINTER_FLAG_CANCELED"></span><span id="pointer_flag_canceled"></span>**POINTER_FLAG_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-165">0x000008000</span><span class="sxs-lookup"><span data-stu-id="e2765-165">0x000008000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-166">Indica che il puntatore viene ripartito in modo anomalo, ad esempio quando il sistema riceve un input non valido per il puntatore o quando un dispositivo con puntatori attivi viene ripartito in modo improvviso.</span><span class="sxs-lookup"><span data-stu-id="e2765-166">Indicates that the pointer is departing in an abnormal manner, such as when the system receives invalid input for the pointer or when a device with active pointers departs abruptly.</span></span> <span data-ttu-id="e2765-167">Se l'applicazione che riceve l'input è in una posizione a tale scopo, deve considerare l'interazione come non completata e invertire gli effetti del puntatore interessato.</span><span class="sxs-lookup"><span data-stu-id="e2765-167">If the application receiving the input is in a position to do so, it should treat the interaction as not completed and reverse any effects of the concerned pointer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span><span class="sxs-lookup"><span data-stu-id="e2765-168"><span id="POINTER_FLAG_DOWN"></span><span id="pointer_flag_down"></span>**POINTER_FLAG_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-169">0x00010000</span><span class="sxs-lookup"><span data-stu-id="e2765-169">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-170">Indica che il puntatore è passato a uno stato inattivo; ovvero è stato contattato con la superficie del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-170">Indicates that this pointer transitioned to a down state; that is, it made contact with the digitizer surface.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span><span class="sxs-lookup"><span data-stu-id="e2765-171"><span id="POINTER_FLAG_UPDATE"></span><span id="pointer_flag_update"></span>**POINTER_FLAG_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-172">0x00020000</span><span class="sxs-lookup"><span data-stu-id="e2765-172">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-173">Indica che si tratta di un semplice aggiornamento che non include le modifiche dello stato del puntatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-173">Indicates that this is a simple update that does not include pointer state changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span><span class="sxs-lookup"><span data-stu-id="e2765-174"><span id="POINTER_FLAG_UP"></span><span id="pointer_flag_up"></span>**POINTER_FLAG_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-175">0x00040000</span><span class="sxs-lookup"><span data-stu-id="e2765-175">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-176">Indica che il puntatore è passato a uno stato attivo; ovvero il contatto con la superficie del digitalizzatore è terminato.</span><span class="sxs-lookup"><span data-stu-id="e2765-176">Indicates that this pointer transitioned to an up state; that is, contact with the digitizer surface ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span><span class="sxs-lookup"><span data-stu-id="e2765-177"><span id="POINTER_FLAG_WHEEL"></span><span id="pointer_flag_wheel"></span>**POINTER_FLAG_WHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-178">0x00080000</span><span class="sxs-lookup"><span data-stu-id="e2765-178">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-179">Indica l'input associato a una rotellina del puntatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-179">Indicates input associated with a pointer wheel.</span></span> <span data-ttu-id="e2765-180">Per i puntatori del mouse, equivale all'azione della rotellina di scorrimento del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e2765-180">For mouse pointers, this is equivalent to the action of the mouse scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span><span class="sxs-lookup"><span data-stu-id="e2765-181"><span id="POINTER_FLAG_HWHEEL"></span><span id="pointer_flag_hwheel"></span>**POINTER_FLAG_HWHEEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-182">0x00100000</span><span class="sxs-lookup"><span data-stu-id="e2765-182">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-183">Indica l'input associato a una rotellina h del puntatore.</span><span class="sxs-lookup"><span data-stu-id="e2765-183">Indicates input associated with a pointer h-wheel.</span></span> <span data-ttu-id="e2765-184">Per i puntatori del mouse, equivale all'azione della rotellina di scorrimento orizzontale del mouse ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span><span class="sxs-lookup"><span data-stu-id="e2765-184">For mouse pointers, this is equivalent to the action of the mouse horizontal scroll wheel ([**WM_MOUSEHWHEEL**](../inputdev/wm-mousehwheel.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span><span class="sxs-lookup"><span data-stu-id="e2765-185"><span id="POINTER_FLAG_CAPTURECHANGED"></span><span id="pointer_flag_capturechanged"></span>**POINTER_FLAG_CAPTURECHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-186">0x00200000</span><span class="sxs-lookup"><span data-stu-id="e2765-186">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-187">Indica che il puntatore è stato acquisito da (associato a) un altro elemento e l'elemento originale ha perso l'acquisizione (vedere [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span><span class="sxs-lookup"><span data-stu-id="e2765-187">Indicates that this pointer was captured by (associated with) another element and the original element has lost capture (see [**WM_POINTERCAPTURECHANGED**](wm-pointercapturechanged.md)).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e2765-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span><span class="sxs-lookup"><span data-stu-id="e2765-188"><span id="POINTER_FLAG_HASTRANSFORM"></span><span id="pointer_flag_hastransform"></span>**POINTER_FLAG_HASTRANSFORM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2765-189">0x00400000</span><span class="sxs-lookup"><span data-stu-id="e2765-189">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="e2765-190">Indica che a questo puntatore è associata una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="e2765-190">Indicates that this pointer has an associated transform.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2765-191">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2765-191">Remarks</span></span>

<span data-ttu-id="e2765-192">XBUTTON1 e XBUTTON2 sono pulsanti aggiuntivi usati in molti dispositivi mouse.</span><span class="sxs-lookup"><span data-stu-id="e2765-192">XBUTTON1 and XBUTTON2 are additional buttons used on many mouse devices.</span></span> <span data-ttu-id="e2765-193">Restituiscono gli stessi dati dei pulsanti del mouse standard.</span><span class="sxs-lookup"><span data-stu-id="e2765-193">They return the same data as standard mouse buttons.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2765-194">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2765-194">Requirements</span></span>



| <span data-ttu-id="e2765-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2765-195">Requirement</span></span> | <span data-ttu-id="e2765-196">Valore</span><span class="sxs-lookup"><span data-stu-id="e2765-196">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2765-197">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2765-197">Minimum supported client</span></span><br/> | <span data-ttu-id="e2765-198">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2765-198">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e2765-199">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2765-199">Minimum supported server</span></span><br/> | <span data-ttu-id="e2765-200">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2765-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e2765-201">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2765-201">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2765-202"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2765-202"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2765-203">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2765-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2765-204">Costanti</span><span class="sxs-lookup"><span data-stu-id="e2765-204">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="e2765-205">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="e2765-205">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> <dt>

[<span data-ttu-id="e2765-206">**POINTER_BUTTON_CHANGE_TYPE**</span><span class="sxs-lookup"><span data-stu-id="e2765-206">**POINTER_BUTTON_CHANGE_TYPE**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

