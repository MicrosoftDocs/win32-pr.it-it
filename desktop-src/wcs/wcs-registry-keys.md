---
title: Chiavi del Registro di sistema WCS
description: WCS usa le chiavi del Registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire query su queste chiavi del Registro di sistema per trovare lo stato aggiornato del profilo colori di sistema.
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), chiavi del Registro di sistema
- WCS (Windows Color System),chiavi del Registro di sistema
- gestione dei colori delle immagini, chiavi del Registro di sistema
- gestione dei colori, chiavi del Registro di sistema
- colori, chiavi del Registro di sistema
- Informazioni di riferimento su WCS, chiavi del Registro di sistema
- informazioni di riferimento per WCS, chiavi del Registro di sistema
- Windows Color System (WCS),Registro di sistema
- WCS (Windows Color System),Registro di sistema
- gestione dei colori delle immagini, Registro di sistema
- gestione dei colori, Registro di sistema
- colori, registro
- Informazioni di riferimento su WCS, Registro di sistema
- informazioni di riferimento per WCS, Registro di sistema
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058ec839b226e96542604f151f06e2654a4180d5
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444672"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="e7e3b-118">Chiavi del Registro di sistema WCS</span><span class="sxs-lookup"><span data-stu-id="e7e3b-118">WCS Registry Keys</span></span>

<span data-ttu-id="e7e3b-119">WCS usa le chiavi del Registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="e7e3b-120">Le app devono eseguire query su queste chiavi del Registro di sistema per trovare lo stato aggiornato del profilo colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="e7e3b-121">Profilo colori attivo modificato</span><span class="sxs-lookup"><span data-stu-id="e7e3b-121">Active color profile changed</span></span>

<span data-ttu-id="e7e3b-122">Le app potrebbero voler rispondere agli eventi di modifica del profilo colori per un dispositivo di monitoraggio. In questo modo si garantisce che siano sempre disponibili informazioni accurate sul colore per la destinazione, anche se l'utente o un'altra app ha modificato il profilo attivo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="e7e3b-123">Applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="e7e3b-123">Desktop applications</span></span>

<span data-ttu-id="e7e3b-124">Le app desktop devono restare in ascolto delle modifiche apportate al Registro di sistema per determinare quando le associazioni di un profilo colori sono state modificate usando [**RegNotifyChangeKeyValue.**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="e7e3b-125">Un'app deve registrare sia per le modifiche di associazione del profilo per utente che per le modifiche a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="e7e3b-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve essere inizializzato con una chiave HKEY fornita da [**RegOpenKeyEx.**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="e7e3b-127">**RegOpenKeyEx deve** essere inizializzato usando i percorsi dell'albero del Registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7e3b-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|    &nbsp;  |  &nbsp;      | 
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e3b-128">Associazioni di profili per utente</span><span class="sxs-lookup"><span data-stu-id="e7e3b-128">Per-user profile associations</span></span>    | <span data-ttu-id="e7e3b-129">**HKEY \_ CURRENT USER SOFTWARE Microsoft Windows NT \_ \\ \\ \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ Display \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="e7e3b-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="e7e3b-130">Associazioni di profilo a livello di sistema</span><span class="sxs-lookup"><span data-stu-id="e7e3b-130">System-wide profile associations</span></span> | <span data-ttu-id="e7e3b-131">**HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Class \\ \\ {4d36e96e-e325-11ce-bfc1-08002be10318}**</span><span class="sxs-lookup"><span data-stu-id="e7e3b-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="e7e3b-132">Quando l'app viene notificata in caso di modifica della chiave del Registro di sistema, deve prima di tutto eseguire una query per determinare se le associazioni per utente o a livello di sistema vengono usate chiamando [**WcsGetUsePerUserProfiles.**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="e7e3b-133">Deve quindi chiamare [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con il valore [**WCS \_ PROFILE MANAGEMENT \_ \_ SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) per ottenere il nuovo profilo colori attivo per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="e7e3b-134">Si noti che non tutte le modifiche alle chiavi del Registro di sistema corrisponderanno a una modifica effettiva nel profilo colori attualmente attivo. L'oggetto mush dell'app controlla se il profilo restituito da **WcsGetDefaultColorProfile** è stato effettivamente modificato.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="e7e3b-135">App UWP (Universal Windows)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="e7e3b-136">Le app di Windows universali non hanno accesso alle chiavi del Registro di sistema indicate sopra.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="e7e3b-137">Devono invece registrare un gestore per [**l'evento DisplayInformation.ColorProfileChanged.**](/uwp/api/Windows.Graphics.Display.DisplayInformation)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="e7e3b-138">Questo evento viene generato ogni volta che viene modificato il profilo colori attivo per il monitoraggio in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="e7e3b-139">ColorProfileChanged tiene conto dell'uso delle associazioni di profilo per utente o a livello di sistema. Queste informazioni vengono astratte dalle app UWP.</span><span class="sxs-lookup"><span data-stu-id="e7e3b-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="e7e3b-140">Quando risponde all'evento ColorProfileChanged, l'app deve eseguire una query sul profilo attualmente attivo usando [**DisplayInformation.GetColorProfileAsync.**](/uwp/api/Windows.Graphics.Display.DisplayInformation)</span><span class="sxs-lookup"><span data-stu-id="e7e3b-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 