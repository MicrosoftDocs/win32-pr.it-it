---
title: Errori mciSendString
description: Errori mciSendString
ms.assetid: 286102bd-fcf3-425b-9adc-e0ca2d62e453
keywords:
- Valori restituiti MCIERR, errori mciSendString
- riferimenti multimediali, errori di mciSendString
- informazioni di riferimento per gli errori mciSendString e multimediali
- Interfaccia di controllo multimediale (MCI), errori di mciSendString
- MCI (interfaccia di controllo multimediale), errori di mciSendString
- informazioni di riferimento per MCI, errori di mciSendString
- Riferimento a MCI, errori di mciSendString
- Interfaccia di controllo multimediale (MCI), errori
- MCI (interfaccia di controllo multimediale), errori
- informazioni di riferimento per MCI, errori
- Riferimento a MCI, errori
- errori mciSendString
- mciSendString (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063db1986d3bff2416ad17886afb3b6281e20165
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872445"
---
# <a name="mcisendstring-errors"></a><span data-ttu-id="f5891-116">Errori mciSendString</span><span class="sxs-lookup"><span data-stu-id="f5891-116">mciSendString Errors</span></span>

<span data-ttu-id="f5891-117">Gli errori seguenti vengono restituiti dalla funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) ma non da [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="f5891-117">The following errors are returned by the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function but not by [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)):</span></span>



| <span data-ttu-id="f5891-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5891-118">Value</span></span>                             | <span data-ttu-id="f5891-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f5891-119">Meaning</span></span>                                           |
|-----------------------------------|---------------------------------------------------|
| <span data-ttu-id="f5891-120">costante MCIERR non \_ valida \_</span><span class="sxs-lookup"><span data-stu-id="f5891-120">MCIERR\_BAD\_CONSTANT</span></span>             | <span data-ttu-id="f5891-121">Il valore specificato per un parametro è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5891-121">The value specified for a parameter is unknown.</span></span>   |
| <span data-ttu-id="f5891-122">MCIERR \_ integer non valido \_</span><span class="sxs-lookup"><span data-stu-id="f5891-122">MCIERR\_BAD\_INTEGER</span></span>              | <span data-ttu-id="f5891-123">Numero intero nel comando non valido o mancante.</span><span class="sxs-lookup"><span data-stu-id="f5891-123">An integer in the command was invalid or missing.</span></span> |
| <span data-ttu-id="f5891-124">\_flag duplicati MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="f5891-124">MCIERR\_DUPLICATE\_FLAGS</span></span>          | <span data-ttu-id="f5891-125">Un flag o un valore è stato specificato due volte.</span><span class="sxs-lookup"><span data-stu-id="f5891-125">A flag or value was specified twice.</span></span>              |
| <span data-ttu-id="f5891-126">MCIERR \_ \_ stringa di comando mancante \_</span><span class="sxs-lookup"><span data-stu-id="f5891-126">MCIERR\_MISSING\_COMMAND\_STRING</span></span>  | <span data-ttu-id="f5891-127">Non è stato specificato alcun comando.</span><span class="sxs-lookup"><span data-stu-id="f5891-127">No command was specified.</span></span>                         |
| <span data-ttu-id="f5891-128">MCIERR \_ \_ nome dispositivo \_ mancante</span><span class="sxs-lookup"><span data-stu-id="f5891-128">MCIERR\_MISSING\_DEVICE\_NAME</span></span>     | <span data-ttu-id="f5891-129">Non è stato specificato alcun nome dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5891-129">No device name was specified.</span></span>                     |
| <span data-ttu-id="f5891-130">MCIERR \_ \_ argomento stringa \_ mancante</span><span class="sxs-lookup"><span data-stu-id="f5891-130">MCIERR\_MISSING\_STRING\_ARGUMENT</span></span> | <span data-ttu-id="f5891-131">Nel comando manca un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="f5891-131">A string value was missing from the command.</span></span>      |
| <span data-ttu-id="f5891-132">MCIERR \_ nuovo \_ richiede \_ alias</span><span class="sxs-lookup"><span data-stu-id="f5891-132">MCIERR\_NEW\_REQUIRES\_ALIAS</span></span>      | <span data-ttu-id="f5891-133">È necessario usare un alias con il nome del dispositivo "nuovo".</span><span class="sxs-lookup"><span data-stu-id="f5891-133">An alias must be used with the "new" device name.</span></span> |
| <span data-ttu-id="f5891-134">MCIERR \_ Nessuna \_ \_ virgoletta di chiusura</span><span class="sxs-lookup"><span data-stu-id="f5891-134">MCIERR\_NO\_CLOSING\_QUOTE</span></span>        | <span data-ttu-id="f5891-135">Virgolette di chiusura mancanti.</span><span class="sxs-lookup"><span data-stu-id="f5891-135">A closing quotation mark is missing.</span></span>              |
| <span data-ttu-id="f5891-136">\_notifica MCIERR \_ per \_ \_ apertura automatica</span><span class="sxs-lookup"><span data-stu-id="f5891-136">MCIERR\_NOTIFY\_ON\_AUTO\_OPEN</span></span>    | <span data-ttu-id="f5891-137">Il flag di notifica non è valido con l'apertura automatica.</span><span class="sxs-lookup"><span data-stu-id="f5891-137">The "notify" flag is illegal with auto-open.</span></span>      |
| <span data-ttu-id="f5891-138">\_overflow param \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="f5891-138">MCIERR\_PARAM\_OVERFLOW</span></span>           | <span data-ttu-id="f5891-139">Lunghezza della stringa di output insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f5891-139">The output string was not long enough.</span></span>            |
| <span data-ttu-id="f5891-140">\_interno del parser MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="f5891-140">MCIERR\_PARSER\_INTERNAL</span></span>          | <span data-ttu-id="f5891-141">Si è verificato un errore interno del parser.</span><span class="sxs-lookup"><span data-stu-id="f5891-141">An internal parser error occurred.</span></span>                |
| <span data-ttu-id="f5891-142">\_parola chiave non riconosciuta MCIERR \_</span><span class="sxs-lookup"><span data-stu-id="f5891-142">MCIERR\_UNRECOGNIZED\_KEYWORD</span></span>     | <span data-ttu-id="f5891-143">È stato specificato un parametro di comando sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5891-143">An unknown command parameter was specified.</span></span>       |



 

 

 