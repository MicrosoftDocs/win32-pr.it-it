---
title: Funzioni di gestione del profilo
description: Funzioni di gestione del profilo
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- Riferimento a WCS, profili
- informazioni di riferimento su WCS, profili
- gestione dei profili
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320206"
---
# <a name="profile-management-functions"></a><span data-ttu-id="c6f95-118">Funzioni di gestione del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-118">Profile Management Functions</span></span>

## <a name="profile-management-functions"></a><span data-ttu-id="c6f95-119">Funzioni di gestione del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-119">Profile Management Functions</span></span>

<span data-ttu-id="c6f95-120">Le funzioni API seguenti sono utili per la gestione dei profili.</span><span class="sxs-lookup"><span data-stu-id="c6f95-120">The following API functions are useful in profile management.</span></span>



| <span data-ttu-id="c6f95-121">Funzione</span><span class="sxs-lookup"><span data-stu-id="c6f95-121">Function</span></span>                                                                               | <span data-ttu-id="c6f95-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c6f95-122">Description</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c6f95-123">**AssociateColorProfileWithDeviceW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-123">**AssociateColorProfileWithDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | <span data-ttu-id="c6f95-124">Associa un profilo colori specificato a un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-124">Associates a specified color profile with a specified device.</span></span>                                                              |
| <span data-ttu-id="c6f95-125">[**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span><span class="sxs-lookup"><span data-stu-id="c6f95-125">[**CreateProfileFromLogColorSpaceW**]((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew)</span></span> | <span data-ttu-id="c6f95-126">Converte uno [spazio di colore](c.md) logico in un [profilo di dispositivo](d.md).</span><span class="sxs-lookup"><span data-stu-id="c6f95-126">Converts a logical [color space](c.md) to a [device profile](d.md).</span></span> |
| [<span data-ttu-id="c6f95-127">**DisassociateColorProfileFromDeviceW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-127">**DisassociateColorProfileFromDeviceW**</span></span>](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | <span data-ttu-id="c6f95-128">Annulla l'associazione di un profilo colori specificato a un dispositivo specificato in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-128">Disassociates a specified color profile with a specified device on a specified computer.</span></span> |
| [<span data-ttu-id="c6f95-129">**EnumColorProfilesW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-129">**EnumColorProfilesW**</span></span>](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | <span data-ttu-id="c6f95-130">Enumera tutti i profili che soddisfano i criteri di enumerazione specificati.</span><span class="sxs-lookup"><span data-stu-id="c6f95-130">Enumerates all the profiles satisfying the given enumeration criteria.</span></span> |
| [<span data-ttu-id="c6f95-131">**GetColorDirectoryW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-131">**GetColorDirectoryW**</span></span>](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | <span data-ttu-id="c6f95-132">Recupera il percorso della directory dei colori di Windows in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-132">Retrieves the path of the Windows COLOR directory on a specified machine.</span></span> |
| [<span data-ttu-id="c6f95-133">**GetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="c6f95-133">**GetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | <span data-ttu-id="c6f95-134">Ottiene la rampa gamma dalle lavagne di visualizzazione a colori diretti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-134">Gets the gamma ramp from direct color display boards.</span></span>                                                                                                |
| [<span data-ttu-id="c6f95-135">**GetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-135">**GetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | <span data-ttu-id="c6f95-136">Recupera il profilo colori registrato per lo spazio dei [colori](c.md)standard specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-136">Retrieves the color profile registered for the specified standard [color space](c.md).</span></span> |
| [<span data-ttu-id="c6f95-137">**InstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-137">**InstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-installcolorprofilew) | <span data-ttu-id="c6f95-138">Installa un determinato profilo da usare in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-138">Installs a given profile for use on a specified machine.</span></span> <span data-ttu-id="c6f95-139">Il profilo viene anche copiato nella directory dei colori.</span><span class="sxs-lookup"><span data-stu-id="c6f95-139">The profile is also copied to the COLOR directory.</span></span> |
| [<span data-ttu-id="c6f95-140">**RegisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-140">**RegisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-registercmmw) | <span data-ttu-id="c6f95-141">Associa un valore di identificazione specificato al modulo di gestione dei colori specificato (libreria a collegamento dinamico).</span><span class="sxs-lookup"><span data-stu-id="c6f95-141">Associates a specified identification value with the specified color management module dynamic link library (CMM DLL).</span></span> <span data-ttu-id="c6f95-142">Quando questo ID viene visualizzato in un profilo colori, Windows può individuare il CMM corrispondente in modo da creare una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="c6f95-142">When this ID appears in a color profile, Windows can then locate the corresponding CMM so as to create a transform.</span></span> |
| [<span data-ttu-id="c6f95-143">**SetDeviceGammaRamp**</span><span class="sxs-lookup"><span data-stu-id="c6f95-143">**SetDeviceGammaRamp**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | <span data-ttu-id="c6f95-144">Imposta la rampa gamma sulle lavagne di visualizzazione a colori diretti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-144">Sets the gamma ramp on direct color display boards.</span></span>                                                                                                  |
| [<span data-ttu-id="c6f95-145">**SetStandardColorSpaceProfileW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-145">**SetStandardColorSpaceProfileW**</span></span>](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | <span data-ttu-id="c6f95-146">Registra un profilo specificato per un determinato [spazio dei colori](c.md)standard.</span><span class="sxs-lookup"><span data-stu-id="c6f95-146">Registers a specified profile for a given standard [color space](c.md).</span></span> <span data-ttu-id="c6f95-147">È possibile eseguire query sul profilo utilizzando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span><span class="sxs-lookup"><span data-stu-id="c6f95-147">The profile can be queried using [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew).</span></span> |
| [<span data-ttu-id="c6f95-148">**UninstallColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-148">**UninstallColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | <span data-ttu-id="c6f95-149">Rimuove un profilo colori specificato da un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-149">Removes a specified color profile from a specified computer.</span></span> <span data-ttu-id="c6f95-150">Facoltativamente, i file associati vengono eliminati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-150">Associated files are optionally deleted from the system.</span></span> |
| [<span data-ttu-id="c6f95-151">**UnregisterCMMW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-151">**UnregisterCMMW**</span></span>](/windows/win32/api/icm/nf-icm-unregistercmmw) | <span data-ttu-id="c6f95-152">Annulla l'associazione di un valore ID specificato da una libreria di collegamento dinamico (DLL) del modulo di gestione colori specificata.</span><span class="sxs-lookup"><span data-stu-id="c6f95-152">Dissociates a specified ID value from a given color management module dynamic-link library (CMM DLL).</span></span> |
| [<span data-ttu-id="c6f95-153">**WcsAssociateColorProfileWithDevice**</span><span class="sxs-lookup"><span data-stu-id="c6f95-153">**WcsAssociateColorProfileWithDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | <span data-ttu-id="c6f95-154">Associa un profilo colori WCS specificato a un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-154">Associates a specified WCS color profile with a specified device.</span></span>                                                                                    |
| [<span data-ttu-id="c6f95-155">**WcsCreateIccProfile**</span><span class="sxs-lookup"><span data-stu-id="c6f95-155">**WcsCreateIccProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | <span data-ttu-id="c6f95-156">Converte un profilo WCS in un profilo ICC.</span><span class="sxs-lookup"><span data-stu-id="c6f95-156">Converts a WCS profile into an ICC profile.</span></span>                                                                                                          |
| [<span data-ttu-id="c6f95-157">**WcsDisassociateColorProfileFromDevice**</span><span class="sxs-lookup"><span data-stu-id="c6f95-157">**WcsDisassociateColorProfileFromDevice**</span></span>](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | <span data-ttu-id="c6f95-158">Annulla l'associazione di un profilo colori WCS specificato a un dispositivo specifico in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-158">Disassociates a specified WCS color profile with a specified device on a specified computer.</span></span>                                                         |
| [<span data-ttu-id="c6f95-159">**WcsEnumColorProfiles**</span><span class="sxs-lookup"><span data-stu-id="c6f95-159">**WcsEnumColorProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | <span data-ttu-id="c6f95-160">Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-160">Enumerates all color profiles that satisfy the enumeration criteria in the specified profile management scope.</span></span>                                       |
| [<span data-ttu-id="c6f95-161">**WcsEnumColorProfilesSize**</span><span class="sxs-lookup"><span data-stu-id="c6f95-161">**WcsEnumColorProfilesSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | <span data-ttu-id="c6f95-162">Restituisce la dimensione, in byte, del buffer richiesto dalla funzione [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) per enumerare i profili colori.</span><span class="sxs-lookup"><span data-stu-id="c6f95-162">Returns the size, in bytes, of the buffer required by the [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) function to enumerate color profiles.</span></span> |
| [<span data-ttu-id="c6f95-163">**WcsGetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="c6f95-163">**WcsGetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | <span data-ttu-id="c6f95-164">Recupera il profilo colori predefinito per un dispositivo o l'impostazione predefinita indipendente dal dispositivo se il dispositivo non è specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-164">Retrieves the default color profile for a device, or the device-independent default if the device is not specified.</span></span>                                  |
| [<span data-ttu-id="c6f95-165">**WcsGetDefaultColorProfileSize**</span><span class="sxs-lookup"><span data-stu-id="c6f95-165">**WcsGetDefaultColorProfileSize**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | <span data-ttu-id="c6f95-166">Restituisce la dimensione, in byte, del nome del profilo colori predefinito per un dispositivo, incluso il carattere di terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="c6f95-166">Returns the size, in bytes, of the default color profile name for a device, including the **NULL** terminator.</span></span>                                       |
| [<span data-ttu-id="c6f95-167">**WcsGetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="c6f95-167">**WcsGetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="c6f95-168">Recupera la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-168">Retrieves the default rendering intent in the specified profile management scope.</span></span>                                                                    |
| [<span data-ttu-id="c6f95-169">**WcsGetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="c6f95-169">**WcsGetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | <span data-ttu-id="c6f95-170">Determina se l'utente ha scelto di usare un elenco di associazioni del profilo per utente per il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-170">Determines whether the user has chosen to use a per-user profile association list for the specified device.</span></span>                                          |
| [<span data-ttu-id="c6f95-171">**WcsOpenColorProfileW**</span><span class="sxs-lookup"><span data-stu-id="c6f95-171">**WcsOpenColorProfileW**</span></span>](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | <span data-ttu-id="c6f95-172">Crea un handle per un profilo colori specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-172">Creates a handle to a specified color profile.</span></span>                                                                                                       |
| [<span data-ttu-id="c6f95-173">**WcsSetDefaultColorProfile**</span><span class="sxs-lookup"><span data-stu-id="c6f95-173">**WcsSetDefaultColorProfile**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | <span data-ttu-id="c6f95-174">Imposta il nome del profilo colori predefinito del tipo di profilo specificato nell'ambito di gestione del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-174">Sets the default color profile name of the specified profile type in the specified profile management scope.</span></span>                                         |
| [<span data-ttu-id="c6f95-175">**WcsSetDefaultRenderingIntent**</span><span class="sxs-lookup"><span data-stu-id="c6f95-175">**WcsSetDefaultRenderingIntent**</span></span>](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | <span data-ttu-id="c6f95-176">Imposta la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-176">Sets the default rendering intent in the specified profile management scope.</span></span>                                                                         |
| [<span data-ttu-id="c6f95-177">**WcsSetUsePerUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="c6f95-177">**WcsSetUsePerUserProfiles**</span></span>](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | <span data-ttu-id="c6f95-178">Consente all'utente di specificare se utilizzare un elenco di associazioni di profili per utente per il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-178">Allows the user to specify whether to use a per-user profile association list for the specified device.</span></span>                                              |



 

## <a name="profile-consumption-functions"></a><span data-ttu-id="c6f95-179">Funzioni di consumo del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-179">Profile Consumption Functions</span></span>

<span data-ttu-id="c6f95-180">Le API di utilizzo del profilo sono le API in ICM2 che accettano profili XML ICC o WCS, handle del profilo o il rendering di Intent come parametri e un set di nuove API per il supporto del profilo WCS per il codice di gestione dei colori dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6f95-180">The profile consumption APIs are those APIs in ICM2 that take ICC or WCS XML profiles, profile handles, or rendering intents as parameters, and a set of new APIs for WCS profile support for application color management code.</span></span>

 

## <a name="profiles-and-profile-management-functions"></a><span data-ttu-id="c6f95-181">Profili e funzioni di gestione del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-181">Profiles and Profile Management Functions</span></span>

<span data-ttu-id="c6f95-182">Il flusso di lavoro di gestione dei profili è basato sulle API ICM2 esistenti, che sono aumentate per fornire funzionalità aggiuntive per la revisione del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c6f95-182">The profile management workflow is based on existing ICM2 APIs that are augmented to provide additional functionality for revising application code.</span></span>

<span data-ttu-id="c6f95-183">I profili contengono informazioni utilizzate dagli algoritmi di elaborazione dei colori per tradurre il colore tra spazi colore diversi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-183">Profiles contain information used by color processing algorithms to translate color between different color spaces.</span></span> <span data-ttu-id="c6f95-184">La gestione dei profili fornisce un modo per eseguire query e specificare quali profili vengono usati in fasi diverse dal modello di elaborazione dei colori per gestire l'output dei colori di varie periferiche con caratteristiche cromatiche diverse.</span><span class="sxs-lookup"><span data-stu-id="c6f95-184">Profile management provides a way to query and specify which profiles get used at different stages by the color processing model to manage color output of various peripheral devices with diverse color characteristics.</span></span>

<span data-ttu-id="c6f95-185">Gestione profili fornisce il set di funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="c6f95-185">Profile management provides the following set of functionalities:</span></span>

 

1. <span data-ttu-id="c6f95-186">Installazione dei profili colori per l'utilizzo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-186">Installing color profiles for use in the system.</span></span>

 

2. <span data-ttu-id="c6f95-187">Associazione di uno o più profili colori installati a qualsiasi dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="c6f95-187">Associating one or more installed color profiles with any particular device.</span></span>

 

3. <span data-ttu-id="c6f95-188">Scelta di un profilo colori predefinito di un particolare tipo tra i profili disponibili per l'utilizzo in una determinata fase di elaborazione dei colori.</span><span class="sxs-lookup"><span data-stu-id="c6f95-188">Choosing a default color profile of a particular type among the profiles available for use in a particular stage of color processing.</span></span> <span data-ttu-id="c6f95-189">Potrebbe trattarsi di un dispositivo tra i profili associati o tra i profili installati nel sistema e non specifici del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-189">This could be for a device among the profiles associated with it, or among the profiles installed in the system and not device specific.</span></span>

 

4. <span data-ttu-id="c6f95-190">Enumerazione dei profili dei colori che soddisfano determinati criteri tra i profili installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-190">Enumerating color profiles that satisfy particular criteria among the profiles installed in the system.</span></span>

<span data-ttu-id="c6f95-191">Le estensioni del nome file del profilo WCS sono ". CDMP" per DMPs, ". Camp" per i campi e ". gmmp" per GMMPs.</span><span class="sxs-lookup"><span data-stu-id="c6f95-191">The WCS profile filename extensions are ".cdmp" for DMPs, ".camp" for CAMPs, and ".gmmp" for GMMPs.</span></span>

 

<span data-ttu-id="c6f95-192">**Gestione dei profili per utente e abilitazione dell'esecuzione in un contesto LUA**</span><span class="sxs-lookup"><span data-stu-id="c6f95-192">**Per-user profile management and enabling execution in LUA context**</span></span>

<span data-ttu-id="c6f95-193">L'obiettivo della progettazione descritta nel documento corrente è il seguente:</span><span class="sxs-lookup"><span data-stu-id="c6f95-193">The goal of the design described in the current document is as follows:</span></span>

 

1. <span data-ttu-id="c6f95-194">L'implementazione di ICM2 legacy non fornisce supporto per la gestione dei profili per utente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-194">Legacy ICM2 implementation does not provide support for per-user profile management.</span></span> <span data-ttu-id="c6f95-195">Utenti diversi non possono avere impostazioni del proprio profilo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-195">Different users cannot have their own profile settings.</span></span> <span data-ttu-id="c6f95-196">In vista, l'infrastruttura di gestione dei profili WCS consente agli utenti di configurare singole impostazioni del profilo per la maggior parte delle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6f95-196">In Vista, the WCS profile management infrastructure enables users to configure individual profile settings for most functionalities.</span></span>

 

2. <span data-ttu-id="c6f95-197">Tutte le API legacy di gestione del profilo ICM2 modificano le impostazioni a livello di sistema e richiedono privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-197">All legacy ICM2 profile management APIs modify settings system-wide and require administrative privileges.</span></span> <span data-ttu-id="c6f95-198">In Windows Vista tutti gli utenti eseguono la maggior parte delle impostazioni dell'account utente con privilegi minimi, mentre gli amministratori possono elevare i privilegi in modo selettivo per eseguire applicazioni che modificano le impostazioni a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-198">In Windows Vista, all users run in Least-privileged User Account (LUA) settings most of the time, and administrators can elevate privilege selectively to run applications that modify system-wide settings.</span></span> <span data-ttu-id="c6f95-199">Nella gestione dei profili WCS tutte le impostazioni del profilo per utente sono configurabili nel contesto LUA.</span><span class="sxs-lookup"><span data-stu-id="c6f95-199">In WCS profile management, all per-user profile settings are configurable in LUA context.</span></span> <span data-ttu-id="c6f95-200">Le applicazioni di gestione del profilo possono essere eseguite come impostazioni LUA, aumentando l'ambito di utilizzo e garantendo che la sicurezza del sistema non venga compromessa.</span><span class="sxs-lookup"><span data-stu-id="c6f95-200">Profile management applications can run as LUA settings, increasing their scope of use and ensuring that security of the system is not compromised.</span></span>

<span data-ttu-id="c6f95-201">La gestione dei profili in vista offre i miglioramenti seguenti rispetto all'infrastruttura ICM2 legacy:</span><span class="sxs-lookup"><span data-stu-id="c6f95-201">Profile management in Vista provides the following enhancements over legacy ICM2 infrastructure:</span></span>

 

1. <span data-ttu-id="c6f95-202">Consente l'associazione del profilo con i dispositivi, le impostazioni predefinite del profilo e l'enumerazione dei profili nell'ambito per utente e a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-202">It enables profile association with devices, default profile settings, and enumeration of profiles in both per-user and system-wide scope.</span></span>

 

2. <span data-ttu-id="c6f95-203">L'installazione di un profilo rimane a livello di sistema e richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="c6f95-203">Installing a profile remains system wide and requires administrator privileges.</span></span> <span data-ttu-id="c6f95-204">Questo è coerente con l'installazione del profilo durante l'installazione del dispositivo perché l'installazione del dispositivo è a livello di sistema e richiede privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-204">This is consistent with profile installation during device installation because device installation is system wide and requires administrative privileges.</span></span>

 

<span data-ttu-id="c6f95-205">Se i dispositivi possono essere installati dal contesto LUA sono specifici per ciò che è supportato per la classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-205">Whether devices can be installed from LUA context is particular to what is supported for that class of device.</span></span> <span data-ttu-id="c6f95-206">In vista, ad esempio, è possibile eseguire l'installazione della stampante dal contesto LUA se all'utente sono stati concessi i diritti per copiare i file nell'archivio driver da un amministratore di dominio usando i criteri di archivio driver.</span><span class="sxs-lookup"><span data-stu-id="c6f95-206">For example, in Vista, it is possible to do printer installation from LUA context if the user has been granted rights to copy files into the driver store by a domain administrator using driver store policies.</span></span> <span data-ttu-id="c6f95-207">L'infrastruttura di gestione dei profili dei colori non deve eseguire alcuna operazione speciale in quanto l'installazione viene eseguita nel contesto dello spooler.</span><span class="sxs-lookup"><span data-stu-id="c6f95-207">Color profile management infrastructure doesn't need to do anything special in this regard since the installation happens in spooler context.</span></span>

 

3. <span data-ttu-id="c6f95-208">La modifica delle impostazioni del profilo nell'ambito per utente può essere eseguita nel contesto LUA. le modifiche a livello di sistema richiedono privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-208">Modifying profile settings in per-user scope can be done in LUA context; system-wide modifications required administrative privileges.</span></span> <span data-ttu-id="c6f95-209">Le operazioni di gestione del profilo che richiedono la lettura delle informazioni di configurazione possono essere eseguite nel contesto LUA per le impostazioni per utente e a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-209">Profile management operations that require reading configuration information can be done in LUA context for both per-user and system-wide settings.</span></span>

<span data-ttu-id="c6f95-210">L'ambito di gestione dei profili indica l'ambito delle operazioni eseguite; per utente o a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-210">Profile management scope indicates the scope of the operations performed; either per-user or system wide.</span></span>

<span data-ttu-id="c6f95-211">Per ogni operazione, viene indicato se può essere eseguita dal contesto LUA.</span><span class="sxs-lookup"><span data-stu-id="c6f95-211">For each operation, it is indicated whether it can be done from LUA context.</span></span> <span data-ttu-id="c6f95-212">Se un'operazione non può essere eseguita nel contesto LUA, l'API di gestione del profilo corrispondente restituisce un errore con accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-212">If an operation cannot be performed in LUA context, the corresponding profile management API returns failure with access denied.</span></span> <span data-ttu-id="c6f95-213">Le applicazioni che usano l'API, ad esempio il pannello di controllo della gestione dei colori, possono consentire all'utente di elevare il contesto amministrativo (usando l'interfaccia utente OTS o di consenso), quindi chiamare l'API dal contesto con privilegi elevati in modo che l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-213">Applications using the API, such as Color Management Control Panel, can enable the user to elevate to administrative context (using OTS or Consent UI), and then call the API from the elevated context so that the operation will succeed.</span></span>



<span data-ttu-id="c6f95-214">Operazione</span><span class="sxs-lookup"><span data-stu-id="c6f95-214">Operation</span></span>

<span data-ttu-id="c6f95-215">Ambito di gestione del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-215">Profile Management Scope</span></span>

<span data-ttu-id="c6f95-216">Pre-condizione</span><span class="sxs-lookup"><span data-stu-id="c6f95-216">Pre-condition</span></span>

<span data-ttu-id="c6f95-217">Post-condizione</span><span class="sxs-lookup"><span data-stu-id="c6f95-217">Post-condition</span></span>

<span data-ttu-id="c6f95-218">Eseguibile nel contesto LUA</span><span class="sxs-lookup"><span data-stu-id="c6f95-218">Executable in LUA context</span></span>

<span data-ttu-id="c6f95-219">$ {ROWSPAN2} $Install profilo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-219">${ROWSPAN2}$Install profile${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-220">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-220">System wide</span></span>

<span data-ttu-id="c6f95-221">Profilo copiato, installato nel sistema e disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-221">Profile copied, installed into the system, and available for use.</span></span> <span data-ttu-id="c6f95-222">Il profilo è enumerabile nell'ambito dell'utente corrente e a livello di sistema per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-222">Profile is enumerable in system-wide and current-user scope for all users.</span></span>

<span data-ttu-id="c6f95-223">Durante l'installazione del driver di dispositivo, governato dai criteri di installazione dei driver.</span><span class="sxs-lookup"><span data-stu-id="c6f95-223">During device driver installation, governed by driver installation policies.</span></span> <span data-ttu-id="c6f95-224">No, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="c6f95-224">No, otherwise.</span></span>

<span data-ttu-id="c6f95-225">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-225">Current user</span></span>

<span data-ttu-id="c6f95-226">Non supportato</span><span class="sxs-lookup"><span data-stu-id="c6f95-226">Not supported</span></span>

<span data-ttu-id="c6f95-227">$ {ROWSPAN2} $Uninstall profilo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-227">${ROWSPAN2}$Uninstall profile${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-228">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-228">System wide</span></span>

<span data-ttu-id="c6f95-229">Il profilo è installato nel sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-229">Profile is installed in the system</span></span>

<span data-ttu-id="c6f95-230">Profilo disinstallato dal sistema ed eventualmente eliminato dall'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="c6f95-230">Profile uninstalled from the system and optionally deleted from the profile store.</span></span> <span data-ttu-id="c6f95-231">Il profilo non è più disponibile per l'uso e non è enumerabile in alcun ambito.</span><span class="sxs-lookup"><span data-stu-id="c6f95-231">Profile is no longer available for use and is not enumerable in any scope.</span></span>

<span data-ttu-id="c6f95-232">No</span><span class="sxs-lookup"><span data-stu-id="c6f95-232">No</span></span>

<span data-ttu-id="c6f95-233">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-233">Current user</span></span>

<span data-ttu-id="c6f95-234">Non supportato</span><span class="sxs-lookup"><span data-stu-id="c6f95-234">Not supported</span></span>

<span data-ttu-id="c6f95-235">$ {ROWSPAN2} $Associate profilo con dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-235">${ROWSPAN2}$Associate profile with device${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-236">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-236">System wide</span></span>

<span data-ttu-id="c6f95-237">Il profilo è installato ed è di tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="c6f95-237">Profile is installed and is of type ICC or CDMP</span></span>

<span data-ttu-id="c6f95-238">Il profilo è disponibile per l'uso con il dispositivo da parte di tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-238">Profile is available for use with the device by all users.</span></span> <span data-ttu-id="c6f95-239">È enumerabile, nell'ambito a livello di sistema e anche nell'ambito dell'utente corrente per tutti gli utenti, come associato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-239">It is enumerable, in system-wide scope and also current-user scope for all users, as associated with the device.</span></span>

<span data-ttu-id="c6f95-240">No</span><span class="sxs-lookup"><span data-stu-id="c6f95-240">No</span></span>

<span data-ttu-id="c6f95-241">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-241">Current user</span></span>

<span data-ttu-id="c6f95-242">Profilo installato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-242">Profile is installed.</span></span> <span data-ttu-id="c6f95-243">Non è importante se il profilo è già associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP.</span><span class="sxs-lookup"><span data-stu-id="c6f95-243">It does not matter whether the profile is already associated to the device in system-wide scope and is of type ICC or CDMP.</span></span>

<span data-ttu-id="c6f95-244">Il profilo è disponibile per l'uso con il dispositivo da parte dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-244">Profile is available for use with the device by current user.</span></span> <span data-ttu-id="c6f95-245">È enumerabile solo nell'ambito dell'utente corrente (a meno che non sia presente anche un'associazione a livello di sistema) come associato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-245">It is enumerable only in current-user scope (unless there is a system-wide association as well) as associated with the device.</span></span>

<span data-ttu-id="c6f95-246">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-246">Yes</span></span>

<span data-ttu-id="c6f95-247">$ {ROWSPAN2} $Disassociate profilo dal dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-247">${ROWSPAN2}$Disassociate profile from device${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-248">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-248">System wide</span></span>

<span data-ttu-id="c6f95-249">Il profilo è associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="c6f95-249">Profile is associated with the device in system-wide scope and is of type ICC or CDMP</span></span>

<span data-ttu-id="c6f95-250">Il profilo non è più disponibile per l'uso (ad eccezione degli utenti che hanno anche questa associazione nell'ambito dell'utente corrente).</span><span class="sxs-lookup"><span data-stu-id="c6f95-250">Profile is no longer available for use (except for users who have this association in their current-user scope as well).</span></span> <span data-ttu-id="c6f95-251">Non è enumerabile nell'ambito a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-251">It is not enumerable in system-wide scope.</span></span> <span data-ttu-id="c6f95-252">Potrebbe essere enumerabile nell'ambito dell'utente corrente, tuttavia, per un utente che dispone di questa associazione nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="c6f95-252">It could be enumerable in current-user scope though, for a user who has this association in its scope.</span></span>

<span data-ttu-id="c6f95-253">No</span><span class="sxs-lookup"><span data-stu-id="c6f95-253">No</span></span>

<span data-ttu-id="c6f95-254">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-254">Current user</span></span>

<span data-ttu-id="c6f95-255">Il profilo è associato al dispositivo nell'ambito dell'utente corrente (indipendentemente dal fatto che sia associato a un ambito a livello di sistema) ed è di tipo ICC o CDMP.</span><span class="sxs-lookup"><span data-stu-id="c6f95-255">Profile is associated with the device in current-user scope (irrespective of whether it is associated in system-wide scope) and is of type ICC or CDMP.</span></span>

<span data-ttu-id="c6f95-256">Il profilo non è più disponibile per l'uso, o enumerabile come associato al dispositivo, dall'utente corrente (a meno che non sia anche associato a un ambito a livello di sistema al dispositivo).</span><span class="sxs-lookup"><span data-stu-id="c6f95-256">Profile is no longer available for use, or enumerable as associated to the device, by current user (unless it is also associated in system-wide scope to the device).</span></span>

<span data-ttu-id="c6f95-257">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-257">Yes</span></span>

<span data-ttu-id="c6f95-258">$ {ROWSPAN2} $Set profilo per un tipo (DMP o ICC) come impostazione predefinita per un dispositivo $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-258">${ROWSPAN2}$Set profile for a type (DMP or ICC) as default for a device${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-259">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-259">System wide</span></span>

<span data-ttu-id="c6f95-260">Il profilo è di tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="c6f95-260">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="c6f95-261">Il profilo viene usato per impostazione predefinita, per il tipo specifico con il dispositivo, per tutti gli utenti ad eccezione di quelli che hanno eseguito l'override di questa impostazione nell'ambito dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-261">The profile is used by default, for the particular type with the device, for all users except for those who have overridden this setting in their current-user scope.</span></span> <span data-ttu-id="c6f95-262">Il profilo viene installato e associato al sistema del dispositivo a livello di sistema, se non lo è già.</span><span class="sxs-lookup"><span data-stu-id="c6f95-262">(The profile is installed and associated to the device system wide, if that is not already the case.)</span></span>

<span data-ttu-id="c6f95-263">No</span><span class="sxs-lookup"><span data-stu-id="c6f95-263">No</span></span>

<span data-ttu-id="c6f95-264">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-264">Current user</span></span>

<span data-ttu-id="c6f95-265">Il profilo è di tipo ICC o CDMP</span><span class="sxs-lookup"><span data-stu-id="c6f95-265">Profile is of type ICC or CDMP</span></span>

<span data-ttu-id="c6f95-266">Il profilo viene usato per impostazione predefinita per il tipo specifico con il dispositivo in caso di utente corrente, indipendentemente dall'impostazione predefinita a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-266">The profile is used by default for the particular type with the device in case of current user, irrespective of the system-wide default for this.</span></span> <span data-ttu-id="c6f95-267">Il profilo viene installato e associato al dispositivo per l'utente corrente, se questa situazione non è già presente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-267">(The profile is installed and associated to the device for current user, if that is not already the case.)</span></span>

<span data-ttu-id="c6f95-268">Sì, se il profilo è già installato</span><span class="sxs-lookup"><span data-stu-id="c6f95-268">Yes, if the profile is already installed</span></span>

<span data-ttu-id="c6f95-269">$ {ROWSPAN2} $Set profilo per un tipo (ICC, DMP, CAMP, GMMP) e una combinazione di sottotipo come valore predefinito globale $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-269">${ROWSPAN2}$Set profile for a type (ICC, DMP, CAMP, GMMP) and subtype combination as global default${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-270">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-270">System wide</span></span>

<span data-ttu-id="c6f95-271">È possibile associare solo i profili ICC e CDMP ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-271">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="c6f95-272">Per impostazione predefinita, il profilo viene usato per il tipo specifico.</span><span class="sxs-lookup"><span data-stu-id="c6f95-272">The profile is used by default for the particular type.</span></span> <span data-ttu-id="c6f95-273">Gli utenti possono eseguire l'override di questa impostazione nell'ambito dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-273">Users can override this setting in the current-user scope.</span></span> <span data-ttu-id="c6f95-274">(Il profilo è installato, se questa situazione non è già presente).</span><span class="sxs-lookup"><span data-stu-id="c6f95-274">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="c6f95-275">No</span><span class="sxs-lookup"><span data-stu-id="c6f95-275">No</span></span>

<span data-ttu-id="c6f95-276">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-276">Current user</span></span>

<span data-ttu-id="c6f95-277">È possibile associare solo i profili ICC e CDMP ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-277">Only ICC and CDMP profiles can be associated with devices.</span></span>

<span data-ttu-id="c6f95-278">Per impostazione predefinita, il profilo viene usato per il tipo specifico per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-278">The profile is used by default for the particular type for current user.</span></span> <span data-ttu-id="c6f95-279">(Il profilo è installato, se questa situazione non è già presente).</span><span class="sxs-lookup"><span data-stu-id="c6f95-279">(The profile is installed, if that is not already the case.)</span></span>

<span data-ttu-id="c6f95-280">Sì, se il profilo è già installato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-280">Yes, if the profile is already installed.</span></span>

<span data-ttu-id="c6f95-281">$ {ROWSPAN2} $Erase l'override dell'utente corrente per una particolare impostazione del profilo predefinito, in modo che l'impostazione predefinita del sistema venga sempre utilizzata (come fallback) anche per l'ambito dell'utente corrente. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-281">${ROWSPAN2}$Erase the current-user override for a particular default profile setting, so that the system default always gets used (as fallback) even for current-user scope.${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-282">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-282">System wide</span></span>

<span data-ttu-id="c6f95-283">Non applicabile</span><span class="sxs-lookup"><span data-stu-id="c6f95-283">Not applicable</span></span>

<span data-ttu-id="c6f95-284">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-284">Current user</span></span>

<span data-ttu-id="c6f95-285">Anche per le query utente correnti sulle impostazioni predefinite del profilo, le impostazioni a livello di sistema vengono restituite per l'uso.</span><span class="sxs-lookup"><span data-stu-id="c6f95-285">Even for current-user queries on default profile settings, system-wide settings are returned for use.</span></span>

<span data-ttu-id="c6f95-286">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-286">Yes</span></span>

<span data-ttu-id="c6f95-287">$ {ROWSPAN2} $Enumerate profili installati che soddisfano determinati criteri, ad esempio classe del dispositivo, classe del profilo e così via. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-287">${ROWSPAN2}$Enumerate installed profiles satisfying particular criteria (like device class, profile class, etc.)${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-288">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-288">System wide</span></span>

<span data-ttu-id="c6f95-289">È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-289">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="c6f95-290">I profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.</span><span class="sxs-lookup"><span data-stu-id="c6f95-290">Profiles that are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="c6f95-291">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-291">Yes</span></span>

<span data-ttu-id="c6f95-292">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-292">Current user</span></span>

<span data-ttu-id="c6f95-293">Solo i profili ICC e CDMP possono essere associati ai dispositivi e quindi enumerati per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-293">Only ICC and CDMP profiles can be associated with devices and thus enumerated for devices.</span></span>

<span data-ttu-id="c6f95-294">I profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.</span><span class="sxs-lookup"><span data-stu-id="c6f95-294">Profiles which are installed and satisfy the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="c6f95-295">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-295">Yes</span></span>

<span data-ttu-id="c6f95-296">$ {ROWSPAN2} $Enumerate profili associati a un particolare dispositivo che soddisfa determinati criteri, ad esempio la classe Device e la classe profile $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-296">${ROWSPAN2}$Enumerate profiles associated with a particular device satisfying particular criteria, such as device class, and profile class${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-297">A livello di sistema</span><span class="sxs-lookup"><span data-stu-id="c6f95-297">System wide</span></span>

<span data-ttu-id="c6f95-298">È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-298">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="c6f95-299">I profili associati al dispositivo nell'ambito a livello di sistema e soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.</span><span class="sxs-lookup"><span data-stu-id="c6f95-299">Profiles that are associated with the device in system-wide scope and satisfies the specified criteria in system-wide scope are enumerated.</span></span>

<span data-ttu-id="c6f95-300">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-300">Yes</span></span>

<span data-ttu-id="c6f95-301">Utente corrente</span><span class="sxs-lookup"><span data-stu-id="c6f95-301">Current user</span></span>

<span data-ttu-id="c6f95-302">È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-302">Only ICC and CDMP profiles can be associated with and enumerated for devices.</span></span>

<span data-ttu-id="c6f95-303">I profili disponibili come associati al dispositivo nell'ambito dell'utente corrente, che include le associazioni a livello di sistema e soddisfa i criteri specificati nell'ambito dell'utente corrente, vengono enumerati.</span><span class="sxs-lookup"><span data-stu-id="c6f95-303">Profiles that are available as associated with the device in current-user scope, which includes the system-wide associations and satisfies the specified criteria in current-user scope are enumerated.</span></span>

<span data-ttu-id="c6f95-304">Sì</span><span class="sxs-lookup"><span data-stu-id="c6f95-304">Yes</span></span>



 

<span data-ttu-id="c6f95-305">I tipi di profilo colori validi sono forniti dall'enumerazione COLORPROFILETYPE.</span><span class="sxs-lookup"><span data-stu-id="c6f95-305">The valid color profile types are provided by the COLORPROFILETYPE enumeration.</span></span>

<span data-ttu-id="c6f95-306">I sottotipi di profilo colori validi vengono forniti dall'enumerazione COLORPROFILESUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="c6f95-306">The valid color profile subtypes are provided by the COLORPROFILESUBTYPE enumeration.</span></span>

<span data-ttu-id="c6f95-307">Nella tabella seguente sono illustrate le combinazioni di tipi di profilo/sottotipi validi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-307">The valid profile type/subtype combinations are shown in the following table.</span></span>



<span data-ttu-id="c6f95-308">COLORPROFILETYPE</span><span class="sxs-lookup"><span data-stu-id="c6f95-308">COLORPROFILETYPE</span></span>

<span data-ttu-id="c6f95-309">COLORPROFILESUBTYPE valido</span><span class="sxs-lookup"><span data-stu-id="c6f95-309">Valid COLORPROFILESUBTYPE</span></span>

<span data-ttu-id="c6f95-310">Note</span><span class="sxs-lookup"><span data-stu-id="c6f95-310">Notes</span></span>

<span data-ttu-id="c6f95-311">Impostazione predefinita dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-311">Device Default</span></span>

<span data-ttu-id="c6f95-312">Impostazioni predefinite globali</span><span class="sxs-lookup"><span data-stu-id="c6f95-312">Global Default</span></span>

<span data-ttu-id="c6f95-313">Uso previsto</span><span class="sxs-lookup"><span data-stu-id="c6f95-313">Intended Use</span></span>

<span data-ttu-id="c6f95-314">Uso previsto</span><span class="sxs-lookup"><span data-stu-id="c6f95-314">Intended Use</span></span>

<span data-ttu-id="c6f95-315">CPI del CPT \_</span><span class="sxs-lookup"><span data-stu-id="c6f95-315">CPT\_ICC</span></span>

<span data-ttu-id="c6f95-316">CPST \_ None</span><span class="sxs-lookup"><span data-stu-id="c6f95-316">CPST\_NONE</span></span>

<span data-ttu-id="c6f95-317">Ottenere/impostare il profilo ICC predefinito associato a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-317">Get/Set default ICC profile associated with a device</span></span>

<span data-ttu-id="c6f95-318">CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="c6f95-318">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="c6f95-319">Ottenere/impostare il profilo ICC come profilo RGB globale o spazio di lavoro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-319">Get/Set ICC profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="c6f95-320">Vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="c6f95-320">See Note.</span></span>

<span data-ttu-id="c6f95-321">COLORPROFILETYPE CPT \_ ICC e CPT dmp si escludono a \_ vicenda.</span><span class="sxs-lookup"><span data-stu-id="c6f95-321">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="c6f95-322">Il profilo colori predefinito impostato per uno spazio di lavoro specificato (RGB o personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-322">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>

<span data-ttu-id="c6f95-323">\_DMP CPT</span><span class="sxs-lookup"><span data-stu-id="c6f95-323">CPT\_DMP</span></span>

<span data-ttu-id="c6f95-324">CPST \_ None</span><span class="sxs-lookup"><span data-stu-id="c6f95-324">CPST\_NONE</span></span>

<span data-ttu-id="c6f95-325">Ottenere/impostare il profilo DMP predefinito associato a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-325">Get/Set default DMP profile associated with a device</span></span>

<span data-ttu-id="c6f95-326">CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace</span><span class="sxs-lookup"><span data-stu-id="c6f95-326">CPST\_RGBWorkingSpace or CPST\_CustomWorkingSpace</span></span>

<span data-ttu-id="c6f95-327">Ottenere/impostare il profilo DMP come profilo RGB globale o spazio di lavoro personalizzato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-327">Get/Set DMP profile as global RGB or custom working space profile.</span></span> <span data-ttu-id="c6f95-328">Vedere la nota.</span><span class="sxs-lookup"><span data-stu-id="c6f95-328">See Note.</span></span>

<span data-ttu-id="c6f95-329">COLORPROFILETYPE CPT \_ ICC e CPT dmp si escludono a \_ vicenda.</span><span class="sxs-lookup"><span data-stu-id="c6f95-329">The COLORPROFILETYPE CPT\_ICC and CPT\_DMP are mutually exclusive.</span></span> <span data-ttu-id="c6f95-330">Il profilo colori predefinito impostato per uno spazio di lavoro specificato (RGB o personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.</span><span class="sxs-lookup"><span data-stu-id="c6f95-330">The default color profile you set for a given working space (RGB or Custom) can be either an ICC profile or a DMP profile, but not both.</span></span>



 

> [!Note]  
> <span data-ttu-id="c6f95-331">Quando WcsSetDefaultColorProfile viene chiamato per impostare un profilo DMP come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, solo un profilo DMP di tipo RGBVirtualDevice, LCD o CRT è valido.</span><span class="sxs-lookup"><span data-stu-id="c6f95-331">When WcsSetDefaultColorProfile is called to set a DMP profile as the default profile for the RGB working space or a custom working space, only a DMP profile that is of type RGBVirtualDevice, LCD, or CRT is valid.</span></span>
>
>  
>
> <span data-ttu-id="c6f95-332">Quando WcsSetDefaultColorProfile viene chiamato per impostare un profilo ICC come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, solo un profilo ICC la cui classe è "SPAC" o "disp" e il cui spazio colore è "RGB" è valido.</span><span class="sxs-lookup"><span data-stu-id="c6f95-332">When WcsSetDefaultColorProfile is called to set an ICC profile as the default profile for the RGB working space or a custom working space, only an ICC profile whose class is "spac" or "disp," and whose color space is "RGB" is valid.</span></span>

 

<span data-ttu-id="c6f95-333">L'architettura è progettata in base ai requisiti delle operazioni come indicato nelle enumerazioni e nelle tabelle precedenti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-333">The architecture is designed according to the requirements of the operations as mentioned in the enumerations and tables above.</span></span>

### <a name="profile-management-public-api-layer"></a><span data-ttu-id="c6f95-334">Livello API pubblico di gestione dei profili</span><span class="sxs-lookup"><span data-stu-id="c6f95-334">Profile management public API layer</span></span>

<span data-ttu-id="c6f95-335">Poiché l'ambito di gestione del profilo non è supportato dalle API ICM2 legacy, è necessario un nuovo set di API di gestione dei profili WCS che definisce l'ambito di gestione del profilo come utente corrente o a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-335">Because profile management scope is not supported by legacy ICM2 APIs, a new set of WCS profile management APIs is required that defines profile management scope as system wide or current user.</span></span> <span data-ttu-id="c6f95-336">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-336">?</span></span> <span data-ttu-id="c6f95-337">Le API ICM2 legacy continuano a essere supportate per la compatibilità con le versioni precedenti e funzionano nell'ambito della gestione del profilo implicito per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="c6f95-337">Legacy ICM2 APIs continue to be supported for backward compatibility, and work on profile management scope that is implicit for the call.</span></span> <span data-ttu-id="c6f95-338">o ICM2 API che funzionano nell'ambito dell'utente corrente?</span><span class="sxs-lookup"><span data-stu-id="c6f95-338">o ICM2 APIs that work on current-user scope ?</span></span> <span data-ttu-id="c6f95-339">Si tratta di operazioni supportate sia per l'ambito a livello di sistema che per l'utente corrente nella gestione dei profili WCS.</span><span class="sxs-lookup"><span data-stu-id="c6f95-339">This is for operations that are supported for both system wide and current-user scope in WCS profile management.</span></span> <span data-ttu-id="c6f95-340">Le API ICM2 legacy chiamano le nuove API WCS con ambito di gestione del profilo come utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-340">Legacy ICM2 APIs call on new WCS APIs with profile management scope as current user.</span></span> <span data-ttu-id="c6f95-341">Questa operazione è utile dal punto di vista dell'utente perché consente le impostazioni per utente dalle applicazioni legacy e anche l'esecuzione della maggior parte delle operazioni nel contesto LUA.</span><span class="sxs-lookup"><span data-stu-id="c6f95-341">This makes sense from user perspective because this enables per-user settings from legacy applications and also executing most of the operations in LUA context.</span></span> <span data-ttu-id="c6f95-342">o ICM2 API che funzionano nell'ambito a livello di sistema?</span><span class="sxs-lookup"><span data-stu-id="c6f95-342">o ICM2 APIs that work on system-wide scope ?</span></span> <span data-ttu-id="c6f95-343">Si tratta di operazioni (profili di installazione e profili di disinstallazione) che supportano solo l'ambito a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-343">This is for operations (install profiles and uninstall profiles) that support only system-wide scope.</span></span> <span data-ttu-id="c6f95-344">Non vengono create nuove API di gestione dei profili WCS ed è possibile modificare le API esistenti.</span><span class="sxs-lookup"><span data-stu-id="c6f95-344">No new WCS profile management APIs are created and existing APIs can be modified.</span></span>

<span data-ttu-id="c6f95-345">Le implementazioni sottostanti delle operazioni di gestione dei profili funzionano sulle seguenti entità di dati di configurazione per creare il contesto per gli algoritmi di elaborazione dei colori per fornire funzionalità di gestione dei colori.</span><span class="sxs-lookup"><span data-stu-id="c6f95-345">The underlying implementations of the profile management operations work on the following configuration data entities to create the context for color processing algorithms to provide color management functionalities.</span></span> <span data-ttu-id="c6f95-346">Si tratta di impostazioni specifiche del dispositivo o globali (indipendenti dal dispositivo).</span><span class="sxs-lookup"><span data-stu-id="c6f95-346">They are either device specific or global (device independent) settings.</span></span> <span data-ttu-id="c6f95-347">o dati di configurazione specifici del dispositivo:?</span><span class="sxs-lookup"><span data-stu-id="c6f95-347">o Device specific configuration data: ?</span></span> <span data-ttu-id="c6f95-348">Elenco di profili associati a un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-348">List of profiles associated with a particular device.</span></span> <span data-ttu-id="c6f95-349">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-349">?</span></span> <span data-ttu-id="c6f95-350">Profilo predefinito per i diversi tipi di profilo associati a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-350">Default profile for different profile types associated with a device.</span></span> <span data-ttu-id="c6f95-351">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-351">?</span></span> <span data-ttu-id="c6f95-352">Modalità di corrispondenza dei profili utilizzati per l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="c6f95-352">Matching mode of profiles used for enumeration.</span></span> <span data-ttu-id="c6f95-353">o dati di configurazione globali:?</span><span class="sxs-lookup"><span data-stu-id="c6f95-353">o Global configuration data: ?</span></span> <span data-ttu-id="c6f95-354">Elenco di profili installati nel sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-354">List of profiles installed in the system.</span></span> <span data-ttu-id="c6f95-355">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-355">?</span></span> <span data-ttu-id="c6f95-356">Profilo predefinito globale per diversi tipi di profilo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-356">Global default profile for different profile types.</span></span> <span data-ttu-id="c6f95-357">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-357">?</span></span> <span data-ttu-id="c6f95-358">Le implementazioni sottostanti dell'archiviazione dei dati di configurazione accettano l'ambito di archiviazione per i dati di configurazione (indipendente dal dispositivo o dispositivo specifico), che può essere l'utente corrente o a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-358">The underlying implementations of configuration data storage take in storage scope for configuration data (either device independent or device specific), which can be either system wide or current user.</span></span> <span data-ttu-id="c6f95-359">Questa operazione è diversa dall'ambito di gestione del profilo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-359">This is different from profile management scope.</span></span> <span data-ttu-id="c6f95-360">Un'operazione con ambito di gestione del profilo utente corrente può causare la lettura da un ambito di archiviazione a livello di sistema se l'impostazione dell'utente corrente per l'operazione non è presente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-360">An operation with current-user profile management scope can cause a read from a system-wide storage scope if the current-user setting for that operation is not present.</span></span> <span data-ttu-id="c6f95-361">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-361">?</span></span> <span data-ttu-id="c6f95-362">Il livello API ICM2/WCS chiama in questo livello di archiviazione per ottenere e impostare i dati con l'ambito di archiviazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-362">The ICM2/WCS API layer calls in this storage layer for getting and setting data with appropriate storage scope.</span></span> <span data-ttu-id="c6f95-363">Il livello di archiviazione è trasparente per l'ambito di gestione del profilo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-363">The storage layer is transparent to profile management scope.</span></span> <span data-ttu-id="c6f95-364">Logica per combinare i dati dagli ambiti di archiviazione dell'utente corrente e dell'intero sistema per creare o aggiornare una configurazione in base all'ambito di gestione del profilo specificato dal chiamante dell'API.</span><span class="sxs-lookup"><span data-stu-id="c6f95-364">The logic for combining data from current-user and system-wide storage scopes to create or update a configuration according to the profile management scope specified by the API caller.</span></span> <span data-ttu-id="c6f95-365">Questa logica è presente nel livello API ICM2/WCS.</span><span class="sxs-lookup"><span data-stu-id="c6f95-365">This logic is present in the ICM2/WCS API layer.</span></span>

### <a name="device-specific-storage-layer"></a><span data-ttu-id="c6f95-366">Livello di archiviazione specifico del dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-366">Device-specific storage layer</span></span>

<span data-ttu-id="c6f95-367">Lo spazio di archiviazione per classi diverse di dispositivi quali stampa, acquisizione o visualizzazione potrebbe essere diverso l'uno dall'altro.</span><span class="sxs-lookup"><span data-stu-id="c6f95-367">The storage for different classes of devices like print, capture or display could be different from each other.</span></span> <span data-ttu-id="c6f95-368">Ad esempio, i dati di configurazione per un dispositivo di stampa devono essere archiviati usando le API di stampa standard, ad esempio SetPrinterDataEx e GetPrinterDataEx, per consentire la copia dei profili e le impostazioni da trasferire in un computer client durante la connessione di tipo punto e stampa.</span><span class="sxs-lookup"><span data-stu-id="c6f95-368">For example, configuration data for a print device must be stored using standard print APIs, such as SetPrinterDataEx and GetPrinterDataEx, to enable the profiles to be copied and settings to be transferred to a client machine during Point-and-Print connection.</span></span> <span data-ttu-id="c6f95-369">?</span><span class="sxs-lookup"><span data-stu-id="c6f95-369">?</span></span> <span data-ttu-id="c6f95-370">Questo livello esporta la funzionalità per aprire lo Store, recuperare i dati, impostare i dati e chiudere l'archivio usando interfacce predefinite comuni, in modo che il livello di archiviazione della configurazione di gestione del profilo possa chiamarli mentre è trasparente per il modo in cui vengono archiviati i dati per tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c6f95-370">This layer exports functionality to open store, get data, set data and close store using common pre-defined interfaces so that the profile management configuration storage layer can call into them while being transparent to the way the data gets stored for that device.</span></span>

<span data-ttu-id="c6f95-371">Nella figura seguente viene illustrata questa architettura.</span><span class="sxs-lookup"><span data-stu-id="c6f95-371">The following diagram illustrates this architecture.</span></span>



<span data-ttu-id="c6f95-372">Livello API pubblico di gestione dei profili</span><span class="sxs-lookup"><span data-stu-id="c6f95-372">Profile Management Public API Layer</span></span>

<span data-ttu-id="c6f95-373">$ {ROWSPAN2} $Legacy API ICM2 per le operazioni che supportano solo l'ambito di gestione del profilo a livello di sistema in vista (installare, disinstallare e ottenere la directory dei colori).</span><span class="sxs-lookup"><span data-stu-id="c6f95-373">${ROWSPAN2}$Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista (install, uninstall, and get color directory).</span></span> <span data-ttu-id="c6f95-374">Chiamano il livello di archiviazione della configurazione con ambito di archiviazione appropriato. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-374">They call the configuration storage layer with appropriate storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-375">API ICM2 legacy per operazioni che supportano l'ambito di gestione dei profili utente e di sistema in vista (tutte le operazioni diverse da installazione, disinstallazione e ottenere la directory dei colori).</span><span class="sxs-lookup"><span data-stu-id="c6f95-375">Legacy ICM2 API for operations that support both system-wide and current-user profile management scope in Vista (all operations other than install, uninstall, and get color directory).</span></span> <span data-ttu-id="c6f95-376">Operano in modo implicito nell'ambito dell'utente corrente e chiamano la nuova API WCS con ambito di gestione del profilo come utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-376">They implicitly work on current-user scope, and call into new WCS API with profile management scope as current user.</span></span>

<span data-ttu-id="c6f95-377">Nuova API WCS con supporto dell'ambito di gestione dei profili utente corrente e a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-377">New WCS API with system-wide and current-user profile management scope support.</span></span> <span data-ttu-id="c6f95-378">Chiamano il livello di archiviazione della configurazione con ambito di archiviazione appropriato.</span><span class="sxs-lookup"><span data-stu-id="c6f95-378">They call the configuration storage layer with appropriate storage scope.</span></span>



 



<span data-ttu-id="c6f95-379">Livello di archiviazione della configurazione di gestione del profilo</span><span class="sxs-lookup"><span data-stu-id="c6f95-379">Profile Management Configuration Storage Layer</span></span>

<span data-ttu-id="c6f95-380">Routine di configurazione globali indipendenti dal dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-380">Device-independent global configuration routines</span></span>

<span data-ttu-id="c6f95-381">Routine di configurazione specifiche del dispositivo</span><span class="sxs-lookup"><span data-stu-id="c6f95-381">Device-specific configuration routines</span></span>

<span data-ttu-id="c6f95-382">$ {ROWSPAN3} $Profile l'installazione e la gestione delle impostazioni del profilo predefinite indipendenti dal dispositivo, supportata nell'ambito di archiviazione dell'utente corrente e a livello di sistema. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="c6f95-382">${ROWSPAN3}$Profile installation and device-independent default profile settings management, supported in system-wide and current-user storage scope.${REMOVE}$</span></span>  

<span data-ttu-id="c6f95-383">Associazione del dispositivo e gestione delle impostazioni del profilo predefinito specifiche del dispositivo, supportata nell'ambito di archiviazione dell'utente corrente e a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="c6f95-383">Device association and device-specific default profile settings management, supported in system-wide and current-user storage scope.</span></span>

<span data-ttu-id="c6f95-384">Livello di archiviazione Device-Specific</span><span class="sxs-lookup"><span data-stu-id="c6f95-384">Device-Specific Storage layer</span></span>

<span data-ttu-id="c6f95-385">Archiviazione specifica di stampa</span><span class="sxs-lookup"><span data-stu-id="c6f95-385">Print specific storage</span></span>

<span data-ttu-id="c6f95-386">Visualizza archiviazione specifica</span><span class="sxs-lookup"><span data-stu-id="c6f95-386">Display specific storage</span></span>

<span data-ttu-id="c6f95-387">Acquisisci archiviazione specifica</span><span class="sxs-lookup"><span data-stu-id="c6f95-387">Capture specific storage</span></span>



 

<span data-ttu-id="c6f95-388">Le API ICM2 legacy per le operazioni che supportano solo l'ambito di gestione dei profili a livello di sistema in vista non hanno alcuna modifica nel comportamento.</span><span class="sxs-lookup"><span data-stu-id="c6f95-388">Legacy ICM2 APIs for operations that support only system-wide profile management scope in Vista have no changes in behavior.</span></span> <span data-ttu-id="c6f95-389">Le operazioni di installazione e disinstallazione rientrino in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="c6f95-389">Install and uninstall operations fall in this category.</span></span>

<span data-ttu-id="c6f95-390">Le API legacy di ICM2 per le operazioni che supportano l'ambito di gestione dei profili utente corrente e a livello di sistema sono state modificate per eseguire query e configurare le impostazioni dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="c6f95-390">Legacy ICM2 APIs for operations that support both system-wide and current-user profile management scope have their behavior changed to query and configure current-user settings.</span></span> <span data-ttu-id="c6f95-391">Tutte le operazioni diverse da Install e Uninstall rientreranno in questa categoria.</span><span class="sxs-lookup"><span data-stu-id="c6f95-391">All operations other than install and uninstall fall in this category.</span></span>

 

 




