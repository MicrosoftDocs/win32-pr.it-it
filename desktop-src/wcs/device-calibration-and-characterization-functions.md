---
title: Funzioni di calibratura e di caratterizzazione del dispositivo
description: Le funzioni seguenti sono utili per la scrittura di strumenti di calibratura e di caratterizzazione dei dispositivi necessari per installare e calibrare i dispositivi di visualizzazione dei colori, ad esempio monitoraggi e stampanti.
ms.assetid: e66115cc-b6a9-4df5-b774-38619881bdb0
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), calibrazione del dispositivo
- WCS (sistema di colori Windows), calibrazione del dispositivo
- Gestione colori immagine, calibrazione dispositivo
- gestione dei colori, calibrazione del dispositivo
- colori, calibrazione del dispositivo
- Riferimento a WCS, calibrazione del dispositivo
- informazioni di riferimento per WCS, calibrazione del dispositivo
- Sistema di colori Windows (WCS), caratterizzazione
- WCS (sistema di colori Windows), caratterizzazione
- Gestione colori immagine, caratterizzazione
- gestione dei colori, caratterizzazione
- colori, caratterizzazione
- Riferimento a WCS, caratterizzazione
- informazioni di riferimento su WCS, caratterizzazione
- calibrazione del dispositivo
- calibrazione
- caratterizzazione
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367bbc6385cc21c8dbff3a88bed685616fb3f29
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322035"
---
# <a name="device-calibration-and-characterization-functions"></a><span data-ttu-id="b0bf1-127">Funzioni di calibratura e di caratterizzazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b0bf1-127">Device Calibration and Characterization Functions</span></span>

<span data-ttu-id="b0bf1-128">Le funzioni seguenti sono utili per la scrittura di strumenti di calibratura e di caratterizzazione dei dispositivi necessari per installare e calibrare i dispositivi di visualizzazione dei colori, ad esempio monitoraggi e stampanti.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-128">The following functions are useful for writing device calibration and characterization tools needed for installing and calibrating color display devices such as monitors and printers.</span></span>



| <span data-ttu-id="b0bf1-129">Funzione</span><span class="sxs-lookup"><span data-stu-id="b0bf1-129">Function</span></span> | <span data-ttu-id="b0bf1-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0bf1-130">Description</span></span> |
|-|-|
| [<span data-ttu-id="b0bf1-131">**CloseColorProfile**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-131">**CloseColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-closecolorprofile) | <span data-ttu-id="b0bf1-132">Chiude un handle del profilo aperto.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-132">Closes an open profile handle.</span></span> |
| [<span data-ttu-id="b0bf1-133">**CreateDeviceLinkProfile**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-133">**CreateDeviceLinkProfile**</span></span>](/windows/win32/api/icm/nf-icm-createdevicelinkprofile) | <span data-ttu-id="b0bf1-134">Crea un *profilo di collegamento del dispositivo* ICC (International Color Consortium) da un set di profili colori, usando gli Intent specificati.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-134">Creates an International Color Consortium (ICC) *device link profile* from a set of color profiles, using the specified intents.</span></span> |
| [<span data-ttu-id="b0bf1-135">**GetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-135">**GetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelement) | <span data-ttu-id="b0bf1-136">Copia i dati da un elemento profilo con tag specificato di un profilo colori specificato in un buffer.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-136">Copies data from a specified tagged profile element of a specified color profile into a buffer.</span></span> |
| [<span data-ttu-id="b0bf1-137">**GetColorProfileElementTag**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-137">**GetColorProfileElementTag**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileelementtag) | <span data-ttu-id="b0bf1-138">Recupera il nome del tag specificato da *dwIndex* nella tabella dei tag di un profilo colori ICC (International Color Consortium) specificato, in cui *dwIndex* è un indice in base uno in tale tabella.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-138">Retrieves the tag name specified by *dwIndex* in the tag table of a given International Color Consortium (ICC) color profile, where *dwIndex* is a one-based index into that table.</span></span> |
| [<span data-ttu-id="b0bf1-139">**GetColorProfileFromHandle**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-139">**GetColorProfileFromHandle**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofilefromhandle)| <span data-ttu-id="b0bf1-140">Recupera il contenuto del profilo colori dato un handle a un profilo colori aperto.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-140">Retrieves the color profile contents given a handle to an open color profile.</span></span>     |
| [<span data-ttu-id="b0bf1-141">**GetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-141">**GetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-getcolorprofileheader) | <span data-ttu-id="b0bf1-142">Recupera o deriva la struttura di intestazione ICC da profilo colori ICC o dal profilo XML WCS.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-142">Retrieves or derives ICC header structure from either ICC color profile or WCS XML profile.</span></span> <span data-ttu-id="b0bf1-143">I driver e le applicazioni devono presupporre che restituisca **true** solo indica che viene restituita un'intestazione strutturata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-143">Drivers and applications should assume returning **TRUE** only indicates that a properly structured header is returned.</span></span> <span data-ttu-id="b0bf1-144">Ogni tag dovrà comunque essere convalidato in modo indipendente usando API ICM2 legacy o API XML Schema.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-144">Each tag will still need to be validated independently using either legacy ICM2 APIs or XML schema APIs.</span></span> |
| [<span data-ttu-id="b0bf1-145">**GetCountColorProfileElements**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-145">**GetCountColorProfileElements**</span></span>](/windows/win32/api/icm/nf-icm-getcountcolorprofileelements) | <span data-ttu-id="b0bf1-146">Recupera il numero di elementi contrassegnati in un profilo colori specificato.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-146">Retrieves the number of tagged elements in a given color profile.</span></span> |
| [<span data-ttu-id="b0bf1-147">**GetPS2ColorRenderingDictionary**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-147">**GetPS2ColorRenderingDictionary**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingdictionary) | <span data-ttu-id="b0bf1-148">Recupera il dizionario per il rendering del colore di livello 2 PostScript dal profilo colori ICC specificato.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-148">Retrieves the PostScript Level 2 color rendering dictionary from the specified ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-149">**GetPS2ColorRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-149">**GetPS2ColorRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorrenderingintent) | <span data-ttu-id="b0bf1-150">Recupera lo [scopo del rendering](r.md) dei colori a livello 2 del post-script da un profilo colori ICC.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-150">Retrieves the PostScript Level 2 color [rendering intent](r.md) from an ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-151">**GetPS2ColorSpaceArray**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-151">**GetPS2ColorSpaceArray**</span></span>](/windows/win32/api/icm/nf-icm-getps2colorspacearray) | <span data-ttu-id="b0bf1-152">Recupera la matrice di spazi dei [colori](c.md) di livello 2 PostScript da un profilo colori ICC.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-152">Retrieves the PostScript Level 2 [color space](c.md) array from an ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-153">**IsColorProfileTagPresent**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-153">**IsColorProfileTagPresent**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofiletagpresent) | <span data-ttu-id="b0bf1-154">Indica se nel profilo colori specificato è presente un tag ICC (International Color Consortium) specificato.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-154">Reports whether a specified International Color Consortium (ICC) tag is present in the specified color profile.</span></span> |
| [<span data-ttu-id="b0bf1-155">**IsColorProfileValid**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-155">**IsColorProfileValid**</span></span>](/windows/win32/api/icm/nf-icm-iscolorprofilevalid) | <span data-ttu-id="b0bf1-156">Consente di determinare se il profilo specificato è un profilo ICC (International Color Consortium) valido o un handle del profilo WCS (Windows Color System) valido che può essere utilizzato per la gestione dei colori.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-156">Allows you to determine whether the specified profile is a valid International Color Consortium (ICC) profile, or a valid Windows Color System (WCS) profile handle that can be used for color management.</span></span> |
| [<span data-ttu-id="b0bf1-157">**OpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-157">**OpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-opencolorprofilew) | <span data-ttu-id="b0bf1-158">Crea un handle per un profilo colori specificato.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-158">Creates a handle to a specified color profile.</span></span> <span data-ttu-id="b0bf1-159">L'handle può quindi essere utilizzato in altre funzioni di gestione dei profili.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-159">The handle can then be used in other profile management functions.</span></span> |
| [<span data-ttu-id="b0bf1-160">**SetColorProfileElement**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-160">**SetColorProfileElement**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelement) | <span data-ttu-id="b0bf1-161">Imposta i dati dell'elemento per un elemento del profilo con tag in un profilo colori ICC.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-161">Sets the element data for a tagged profile element in an ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-162">**SetColorProfileElementReference**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-162">**SetColorProfileElementReference**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementreference) | <span data-ttu-id="b0bf1-163">Crea in un profilo colori ICC specificato un nuovo tag che fa riferimento agli stessi dati di un tag esistente.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-163">Creates in a specified ICC color profile a new tag that references the same data as an existing tag.</span></span> |
| [<span data-ttu-id="b0bf1-164">**SetColorProfileElementSize**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-164">**SetColorProfileElementSize**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileelementsize) | <span data-ttu-id="b0bf1-165">Imposta la dimensione di un elemento con tag in un profilo colori ICC.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-165">Sets the size of a tagged element in an ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-166">**SetColorProfileHeader**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-166">**SetColorProfileHeader**</span></span>](/windows/win32/api/icm/nf-icm-setcolorprofileheader) | <span data-ttu-id="b0bf1-167">Imposta i dati dell'intestazione in un profilo colori ICC specificato.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-167">Sets the header data in a specified ICC color profile.</span></span> |
| [<span data-ttu-id="b0bf1-168">**WcsGetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-168">**WcsGetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetcalibrationmanagementstate) | <span data-ttu-id="b0bf1-169">Determina se è abilitata la gestione del sistema dello stato di calibrazione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-169">Determines whether system management of the display calibration state is enabled.</span></span> |
| [<span data-ttu-id="b0bf1-170">**WcsSetCalibrationManagementState**</span><span class="sxs-lookup"><span data-stu-id="b0bf1-170">**WcsSetCalibrationManagementState**</span></span>](/windows/win32/api/icm/nf-icm-wcssetcalibrationmanagementstate) | <span data-ttu-id="b0bf1-171">Determina se è abilitata la gestione del sistema dello stato di calibrazione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="b0bf1-171">Determines whether system management of the display calibration state is enabled.</span></span> |



 

 

 




