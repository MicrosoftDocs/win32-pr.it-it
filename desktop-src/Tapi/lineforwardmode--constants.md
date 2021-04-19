---
description: Le \_ costanti del flag di bit LINEFORWARDMODE descrivono le condizioni in base alle quali è possibile inviare le chiamate a un indirizzo.
ms.assetid: 8cc053bd-1056-42be-b48a-d2312c456893
title: Costanti LINEFORWARDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33702be12afaef5d1194ca5c0d288bd967a93e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333548"
---
# <a name="lineforwardmode_-constants"></a><span data-ttu-id="1a461-103">\_Costanti LINEFORWARDMODE</span><span class="sxs-lookup"><span data-stu-id="1a461-103">LINEFORWARDMODE\_ Constants</span></span>

<span data-ttu-id="1a461-104">Le costanti del flag di bit **LINEFORWARDMODE \_** descrivono le condizioni in base alle quali è possibile inviare le chiamate a un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="1a461-104">The **LINEFORWARDMODE\_** bit-flag constants describe the conditions under which calls to an address can be forwarded.</span></span>

<dl> <dt>

<span data-ttu-id="1a461-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="1a461-105"><span id="LINEFORWARDMODE_BUSY"></span><span id="lineforwardmode_busy"></span>**LINEFORWARDMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-106">Fare in modo che tutte le chiamate siano occupate, indipendentemente dall'origine.</span><span class="sxs-lookup"><span data-stu-id="1a461-106">Forward all calls on busy, irrespective of their origin.</span></span> <span data-ttu-id="1a461-107">Usare questo valore quando si esegue l'inoltri per le chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-107">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**\_BUSYEXTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-108"><span id="LINEFORWARDMODE_BUSYEXTERNAL"></span><span id="lineforwardmode_busyexternal"></span>**LINEFORWARDMODE\_BUSYEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-109">Inviare tutte le chiamate esterne in occupato.</span><span class="sxs-lookup"><span data-stu-id="1a461-109">Forward all external calls on busy.</span></span> <span data-ttu-id="1a461-110">Usare questo valore quando si esegue l'invio di chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-110">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**\_BUSYINTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-111"><span id="LINEFORWARDMODE_BUSYINTERNAL"></span><span id="lineforwardmode_busyinternal"></span>**LINEFORWARDMODE\_BUSYINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-112">Invia tutte le chiamate interne in occupato.</span><span class="sxs-lookup"><span data-stu-id="1a461-112">Forward all internal calls on busy.</span></span> <span data-ttu-id="1a461-113">Usare questo valore quando si esegue l'invio di chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-113">Use this value when forwarding for internal and external calls on busy and on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**\_BUSYNA LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-114"><span id="LINEFORWARDMODE_BUSYNA"></span><span id="lineforwardmode_busyna"></span>**LINEFORWARDMODE\_BUSYNA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-115">Invia tutte le chiamate su occupato/nessuna risposta, indipendentemente dall'origine.</span><span class="sxs-lookup"><span data-stu-id="1a461-115">Forward all calls on busy/no answer, irrespective of their origin.</span></span> <span data-ttu-id="1a461-116">Usare questo valore quando si esegue l'inoltri per le chiamate interne ed esterne in occupato e non è possibile controllare separatamente la risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-116">Use this value when forwarding for internal and external calls on busy and on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**\_BUSYNAEXTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-117"><span id="LINEFORWARDMODE_BUSYNAEXTERNAL"></span><span id="lineforwardmode_busynaexternal"></span>**LINEFORWARDMODE\_BUSYNAEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-118">Invia tutte le chiamate esterne su occupato/nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-118">Forward all external calls on busy/no answer.</span></span> <span data-ttu-id="1a461-119">Usare questo valore quando l'invio delle chiamate su occupato e su nessuna risposta non può essere controllato separatamente per le chiamate interne.</span><span class="sxs-lookup"><span data-stu-id="1a461-119">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**\_BUSYNAINTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-120"><span id="LINEFORWARDMODE_BUSYNAINTERNAL"></span><span id="lineforwardmode_busynainternal"></span>**LINEFORWARDMODE\_BUSYNAINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-121">Invia tutte le chiamate interne su occupato/nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-121">Forward all internal calls on busy/no answer.</span></span> <span data-ttu-id="1a461-122">Usare questo valore quando l'invio delle chiamate su occupato e su nessuna risposta non può essere controllato separatamente per le chiamate interne.</span><span class="sxs-lookup"><span data-stu-id="1a461-122">Use this value when call forwarding on busy and on no answer cannot be controlled separately for internal calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**\_BUSYNASPECIFIC LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-123"><span id="LINEFORWARDMODE_BUSYNASPECIFIC"></span><span id="lineforwardmode_busynaspecific"></span>**LINEFORWARDMODE\_BUSYNASPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-124">Avanti su occupato/nessuna risposta a tutte le chiamate originate a un indirizzo specificato (l'invio di chiamate selettive).</span><span class="sxs-lookup"><span data-stu-id="1a461-124">Forward on busy/no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**\_BUSYSPECIFIC LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-125"><span id="LINEFORWARDMODE_BUSYSPECIFIC"></span><span id="lineforwardmode_busyspecific"></span>**LINEFORWARDMODE\_BUSYSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-126">In avanti, tutte le chiamate originate a un indirizzo specificato (invio di chiamate selettivo).</span><span class="sxs-lookup"><span data-stu-id="1a461-126">Forward on busy all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**\_NOANSW LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-127"><span id="LINEFORWARDMODE_NOANSW"></span><span id="lineforwardmode_noansw"></span>**LINEFORWARDMODE\_NOANSW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-128">Inviare tutte le chiamate senza risposta, indipendentemente dall'origine.</span><span class="sxs-lookup"><span data-stu-id="1a461-128">Forward all calls on no answer, irrespective of their origin.</span></span> <span data-ttu-id="1a461-129">Utilizzare questo valore quando non è possibile controllare separatamente la chiamata di invio per chiamate interne ed esterne in nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-129">Use this value when call forwarding for internal and external calls on no answer cannot be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**\_NOANSWEXTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-130"><span id="LINEFORWARDMODE_NOANSWEXTERNAL"></span><span id="lineforwardmode_noanswexternal"></span>**LINEFORWARDMODE\_NOANSWEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-131">Invia tutte le chiamate esterne senza risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-131">Forward all external calls on no answer.</span></span> <span data-ttu-id="1a461-132">Usare questo valore quando l'invio di chiamate interne ed esterne in nessuna risposta può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-132">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**\_NOANSWINTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-133"><span id="LINEFORWARDMODE_NOANSWINTERNAL"></span><span id="lineforwardmode_noanswinternal"></span>**LINEFORWARDMODE\_NOANSWINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-134">Invia tutte le chiamate interne senza risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-134">Forward all internal calls on no answer.</span></span> <span data-ttu-id="1a461-135">Usare questo valore quando l'invio di chiamate interne ed esterne in nessuna risposta può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-135">Use this value when forwarding for internal and external calls on no answer can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**\_NOANSWSPECIFIC LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-136"><span id="LINEFORWARDMODE_NOANSWSPECIFIC"></span><span id="lineforwardmode_noanswspecific"></span>**LINEFORWARDMODE\_NOANSWSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-137">Avanti su nessuna risposta, tutte le chiamate originate a un indirizzo specificato (l'invio di chiamate selettivo).</span><span class="sxs-lookup"><span data-stu-id="1a461-137">Forward on no answer all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="1a461-138"><span id="LINEFORWARDMODE_UNAVAIL"></span><span id="lineforwardmode_unavail"></span>**LINEFORWARDMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-139">Le chiamate vengono eseguite, ma le condizioni in cui si verificherà l'invio non sono note e non saranno mai note dal provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="1a461-139">Calls are forwarded, but the conditions under which forwarding will occur are not known, and will never be known by the service provider.</span></span> <span data-ttu-id="1a461-140">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="1a461-140">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE \_ UNcond**</span><span class="sxs-lookup"><span data-stu-id="1a461-141"><span id="LINEFORWARDMODE_UNCOND"></span><span id="lineforwardmode_uncond"></span>**LINEFORWARDMODE\_UNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-142">Inviare tutte le chiamate in modo incondizionato, indipendentemente dall'origine.</span><span class="sxs-lookup"><span data-stu-id="1a461-142">Forward all calls unconditionally, irrespective of their origin.</span></span> <span data-ttu-id="1a461-143">Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne non può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-143">Use this value when unconditional forwarding for internal and external calls cannot be controlled separately.</span></span> <span data-ttu-id="1a461-144">L'invio non condizionale esegue l'override in base alle condizioni di disponibilità e/o nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-144">Unconditional forwarding overrides forwarding on busy and/or no answer conditions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**\_UNCONDEXTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-145"><span id="LINEFORWARDMODE_UNCONDEXTERNAL"></span><span id="lineforwardmode_uncondexternal"></span>**LINEFORWARDMODE\_UNCONDEXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-146">Inviare tutte le chiamate esterne in modo incondizionato.</span><span class="sxs-lookup"><span data-stu-id="1a461-146">Forward all external calls unconditionally.</span></span> <span data-ttu-id="1a461-147">Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-147">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**\_UNCONDINTERNAL LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-148"><span id="LINEFORWARDMODE_UNCONDINTERNAL"></span><span id="lineforwardmode_uncondinternal"></span>**LINEFORWARDMODE\_UNCONDINTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-149">Invia tutte le chiamate interne in modo incondizionato.</span><span class="sxs-lookup"><span data-stu-id="1a461-149">Forward all internal calls unconditionally.</span></span> <span data-ttu-id="1a461-150">Utilizzare questo valore quando l'invio non condizionale per le chiamate interne ed esterne può essere controllato separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-150">Use this value when unconditional forwarding for internal and external calls can be controlled separately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**\_UNCONDSPECIFIC LINEFORWARDMODE**</span><span class="sxs-lookup"><span data-stu-id="1a461-151"><span id="LINEFORWARDMODE_UNCONDSPECIFIC"></span><span id="lineforwardmode_uncondspecific"></span>**LINEFORWARDMODE\_UNCONDSPECIFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-152">Inviare in modo non condizionale tutte le chiamate originate in corrispondenza di un indirizzo specificato, ovvero l'invio di una chiamata selettiva.</span><span class="sxs-lookup"><span data-stu-id="1a461-152">Unconditionally forward all calls that originated at a specified address (selective call forwarding).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1a461-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="1a461-153"><span id="LINEFORWARDMODE_UNKNOWN"></span><span id="lineforwardmode_unknown"></span>**LINEFORWARDMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1a461-154">Le chiamate vengono eseguite, ma in questo momento non sono note le condizioni in cui si verificherà l'invio.</span><span class="sxs-lookup"><span data-stu-id="1a461-154">Calls are forwarded, but the conditions under which forwarding will occur are not known at this time.</span></span> <span data-ttu-id="1a461-155">È possibile che le condizioni possano diventare note in un momento successivo.</span><span class="sxs-lookup"><span data-stu-id="1a461-155">It is possible that the conditions may become known at a future time.</span></span> <span data-ttu-id="1a461-156">(Versioni TAPI 1,4 e successive)</span><span class="sxs-lookup"><span data-stu-id="1a461-156">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a461-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a461-157">Remarks</span></span>

<span data-ttu-id="1a461-158">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="1a461-158">No extensibility.</span></span> <span data-ttu-id="1a461-159">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="1a461-159">All 32 bits are reserved.</span></span>

<span data-ttu-id="1a461-160">I flag di bit definiti da LINEFORWARDMODE \_ non sono ortogonali.</span><span class="sxs-lookup"><span data-stu-id="1a461-160">The bit flags defined by LINEFORWARDMODE\_ are not orthogonal.</span></span> <span data-ttu-id="1a461-161">L'invio non condizionale ignora eventuali condizioni specifiche, ad esempio occupato o nessuna risposta.</span><span class="sxs-lookup"><span data-stu-id="1a461-161">Unconditional forwarding ignores any specific condition such as busy or no answer.</span></span> <span data-ttu-id="1a461-162">Se l'invio non condizionale non è attivo, l'invio su occupato e su nessuna risposta può essere controllato separatamente o non separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-162">If unconditional forwarding is not in effect, then forwarding on busy and on no answer can be controlled separately or not separately.</span></span> <span data-ttu-id="1a461-163">Se controllato separatamente, i \_ flag LINEFORWARDMODE occupato e LINEFORWARDMODE \_ NOANSW possono essere usati separatamente.</span><span class="sxs-lookup"><span data-stu-id="1a461-163">If controlled separately, the LINEFORWARDMODE\_BUSY and LINEFORWARDMODE\_NOANSW flags can be used separately.</span></span> <span data-ttu-id="1a461-164">Se non è controllato separatamente, \_ è necessario usare il flag LINEFORWARDMODE BUSYNA.</span><span class="sxs-lookup"><span data-stu-id="1a461-164">If not controlled separately, the flag LINEFORWARDMODE\_BUSYNA must be used.</span></span> <span data-ttu-id="1a461-165">Analogamente, se l'invio di chiamate interne ed esterne può essere controllato separatamente, \_ \_ è possibile usare separatamente i flag esterni LINEFORWARDMODE interni e LINEFORWARDMODE; in caso contrario, viene usata la combinazione.</span><span class="sxs-lookup"><span data-stu-id="1a461-165">Similarly, if forwarding of internal and external calls can be controlled separately, then LINEFORWARDMODE\_INTERNAL and LINEFORWARDMODE\_EXTERNAL flags can be used separately; otherwise the combination is used.</span></span>

<span data-ttu-id="1a461-166">Le funzionalità degli indirizzi indicano quali modalità di invio sono disponibili per ogni indirizzo assegnato a una riga.</span><span class="sxs-lookup"><span data-stu-id="1a461-166">Address capabilities indicate which forwarding modes are available for each address assigned to a line.</span></span> <span data-ttu-id="1a461-167">Un'applicazione può usare [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) per impostare le condizioni di invio al passaggio.</span><span class="sxs-lookup"><span data-stu-id="1a461-167">An application can use [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) to set forwarding conditions at the switch.</span></span>

<span data-ttu-id="1a461-168">Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questi \_ valori LINEFORWARDMODE se la versione negoziata non li supporta.</span><span class="sxs-lookup"><span data-stu-id="1a461-168">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEFORWARDMODE\_ values if the negotiated version does not support them.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a461-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a461-169">Requirements</span></span>



| <span data-ttu-id="1a461-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a461-170">Requirement</span></span> | <span data-ttu-id="1a461-171">Valore</span><span class="sxs-lookup"><span data-stu-id="1a461-171">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1a461-172">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="1a461-172">TAPI version</span></span><br/> | <span data-ttu-id="1a461-173">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="1a461-173">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="1a461-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a461-174">Header</span></span><br/>       | <dl> <span data-ttu-id="1a461-175"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a461-175"><dt>Tapi.h</dt></span></span> </dl> |



 

 




