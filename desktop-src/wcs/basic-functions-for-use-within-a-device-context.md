---
title: Funzioni di base da usare all'interno di un contesto di dispositivo
description: Le funzioni WCS seguenti offrono funzionalità di mapping dei colori di base all'interno di contesti di dispositivo. Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con un sovraccarico ridotto e un intervento minimo dell'utente.
ms.assetid: 199fac5e-daba-4aa3-a631-bb1eb2270b2e
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), contesti di dispositivo
- WCS (sistema di colori Windows), contesti di dispositivo
- Gestione colori immagine, contesti di dispositivo
- gestione dei colori, contesti di dispositivo
- colori, contesti di dispositivo
- Riferimento a WCS, contesti di dispositivo
- informazioni di riferimento per WCS, contesti di dispositivo
- contesti di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde99ed077af108ddc20c73f86e17bedfe1d4a8c
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320188"
---
# <a name="basic-functions-for-use-within-a-device-context"></a><span data-ttu-id="b5c51-119">Funzioni di base da usare all'interno di un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="b5c51-119">Basic Functions for Use Within a Device Context</span></span>

<span data-ttu-id="b5c51-120">Le funzioni WCS seguenti offrono funzionalità di [mapping dei colori](c.md) di base all'interno di contesti di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-120">The following WCS functions deliver basic [color mapping](c.md) capabilities within device contexts.</span></span> <span data-ttu-id="b5c51-121">Sono utili per tutte le applicazioni che devono implementare la gestione dei colori con un sovraccarico ridotto e un intervento minimo dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b5c51-121">They are useful to all applications that need to implement color management with low overhead and minimal user intervention.</span></span>



| <span data-ttu-id="b5c51-122">Funzione</span><span class="sxs-lookup"><span data-stu-id="b5c51-122">Function</span></span>                                                           | <span data-ttu-id="b5c51-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5c51-123">Description</span></span>                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b5c51-124">**CheckColorsInGamut**</span><span class="sxs-lookup"><span data-stu-id="b5c51-124">**CheckColorsInGamut**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-checkcolorsingamut)                   | <span data-ttu-id="b5c51-125">Controlla se i colori specificati si trovano nel gamut del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-125">Checks if given colors are in a device's gamut.</span></span>                                                                                                     |
| [<span data-ttu-id="b5c51-126">**ColorCorrectPalette**</span><span class="sxs-lookup"><span data-stu-id="b5c51-126">**ColorCorrectPalette**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colorcorrectpalette)                 | <span data-ttu-id="b5c51-127">Corregge le voci in una tavolozza per un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-127">Corrects the entries in a palette for a device context.</span></span>                                                                                             |
| [<span data-ttu-id="b5c51-128">**ColorMatchToTarget**</span><span class="sxs-lookup"><span data-stu-id="b5c51-128">**ColorMatchToTarget**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-colormatchtotarget)                   | <span data-ttu-id="b5c51-129">Esegue il mapping dei colori a scopo di anteprima.</span><span class="sxs-lookup"><span data-stu-id="b5c51-129">Performs color mapping for preview purposes.</span></span>                                                                                                        |
| [<span data-ttu-id="b5c51-130">**CreateColorSpace**</span><span class="sxs-lookup"><span data-stu-id="b5c51-130">**CreateColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createcolorspacea)                       | <span data-ttu-id="b5c51-131">Crea uno spazio colore.</span><span class="sxs-lookup"><span data-stu-id="b5c51-131">Creates a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="b5c51-132">**DeleteColorSpace**</span><span class="sxs-lookup"><span data-stu-id="b5c51-132">**DeleteColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-deletecolorspace)                       | <span data-ttu-id="b5c51-133">Elimina uno spazio colore.</span><span class="sxs-lookup"><span data-stu-id="b5c51-133">Deletes a color space.</span></span>                                                                                                                              |
| [<span data-ttu-id="b5c51-134">**EnumICMProfiles**</span><span class="sxs-lookup"><span data-stu-id="b5c51-134">**EnumICMProfiles**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa)                         | <span data-ttu-id="b5c51-135">Enumera i profili dei colori di output disponibili per un determinato contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-135">Enumerates output color profiles available for a given device context.</span></span>                                                                              |
| [<span data-ttu-id="b5c51-136">**EnumICMProfilesProcCallback**</span><span class="sxs-lookup"><span data-stu-id="b5c51-136">**EnumICMProfilesProcCallback**</span></span>](/windows/desktop/api/Wingdi/) | <span data-ttu-id="b5c51-137">Funzione di callback definita dall'applicazione per [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span><span class="sxs-lookup"><span data-stu-id="b5c51-137">Application-defined callback function for [**EnumICMProfiles**](/windows/desktop/api/Wingdi/nf-wingdi-enumicmprofilesa).</span></span> <span data-ttu-id="b5c51-138">Il nome di questa funzione viene definito anche dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5c51-138">The name of this function is also defined by the application.</span></span> |
| [<span data-ttu-id="b5c51-139">**GetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="b5c51-139">**GetColorSpace**</span></span>](/windows/win32/api/wingdi/nf-wingdi-getcolorspace) | <span data-ttu-id="b5c51-140">Ottiene lo spazio del colore di input corrente in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-140">Gets the current input color space in a device context.</span></span> |
| [<span data-ttu-id="b5c51-141">**GetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="b5c51-141">**GetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-geticmprofilea)                             | <span data-ttu-id="b5c51-142">Ottiene il profilo del colore di output corrente di un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-142">Gets the current output color profile of a device context.</span></span>                                                                                          |
| [<span data-ttu-id="b5c51-143">**GetLogColorSpace**</span><span class="sxs-lookup"><span data-stu-id="b5c51-143">**GetLogColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getlogcolorspacea)                       | <span data-ttu-id="b5c51-144">Ottiene la struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) di un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-144">Gets the [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) structure of a device context.</span></span>                                                                      |
| [<span data-ttu-id="b5c51-145">**SetColorSpace**</span><span class="sxs-lookup"><span data-stu-id="b5c51-145">**SetColorSpace**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setcolorspace)                             | <span data-ttu-id="b5c51-146">Imposta lo spazio colore di input di un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-146">Sets a device context's input color space.</span></span>                                                                                                          |
| [<span data-ttu-id="b5c51-147">**SetICMMode**</span><span class="sxs-lookup"><span data-stu-id="b5c51-147">**SetICMMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)                                   | <span data-ttu-id="b5c51-148">Attiva o disattiva la gestione dei colori in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5c51-148">Turns color management on or off in a device context.</span></span>                                                                                               |
| [<span data-ttu-id="b5c51-149">**SetICMProfile**</span><span class="sxs-lookup"><span data-stu-id="b5c51-149">**SetICMProfile**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-seticmprofilea)                             | <span data-ttu-id="b5c51-150">Imposta il profilo del colore di output per un contesto di dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="b5c51-150">Sets the output color profile for a given device context.</span></span>                                                                                           |
| [<span data-ttu-id="b5c51-151">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="b5c51-151">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)               | <span data-ttu-id="b5c51-152">Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="b5c51-152">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                      |



 

 

 




