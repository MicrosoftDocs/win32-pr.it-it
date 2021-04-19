---
title: Chiavi del registro di sistema WCS
description: WCS usa le chiavi del registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori. Le app devono eseguire una query su queste chiavi del registro di sistema per aggiornare lo stato del profilo colori
ms.assetid: e728efa0-e547-45b9-af85-1312766d2fe7
keywords:
- Windows Color System (WCS), chiavi del registro di sistema
- WCS (sistema di colori Windows), chiavi del registro di sistema
- Gestione colori immagine, chiavi del registro di sistema
- gestione dei colori, chiavi del registro di sistema
- colori, chiavi del registro di sistema
- Riferimento a WCS, chiavi del registro di sistema
- informazioni di riferimento su WCS, chiavi del registro di sistema
- Windows Color System (WCS), registro di sistema
- WCS (sistema di colori Windows), registro di sistema
- Gestione colori immagine, registro di sistema
- gestione dei colori, registro di sistema
- colori, registro di sistema
- Riferimento a WCS, registro di sistema
- informazioni di riferimento su WCS, registro di sistema
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a1c0072d9a00fe0cff4a4dbe57af839f65731b
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320204"
---
# <a name="wcs-registry-keys"></a><span data-ttu-id="658c4-118">Chiavi del registro di sistema WCS</span><span class="sxs-lookup"><span data-stu-id="658c4-118">WCS Registry Keys</span></span>

<span data-ttu-id="658c4-119">WCS usa le chiavi del registro di sistema per segnalare che si sono verificati determinati eventi del profilo colori.</span><span class="sxs-lookup"><span data-stu-id="658c4-119">WCS uses registry keys to signal that certain color profile events have occurred.</span></span> <span data-ttu-id="658c4-120">Le app devono eseguire una query su queste chiavi del registro di sistema per aggiornare lo stato del profilo colori</span><span class="sxs-lookup"><span data-stu-id="658c4-120">Apps should query these registry keys for updated system color profile state.</span></span>

## <a name="active-color-profile-changed"></a><span data-ttu-id="658c4-121">Profilo colore attivo modificato</span><span class="sxs-lookup"><span data-stu-id="658c4-121">Active color profile changed</span></span>

<span data-ttu-id="658c4-122">Le app potrebbero voler rispondere agli eventi di modifica del profilo colori per un dispositivo di monitoraggio; in questo modo si garantisce che siano sempre disponibili informazioni accurate sui colori per la destinazione, anche se l'utente o un'altra app ha modificato il profilo attivo per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="658c4-122">Apps may want to respond to color profile change events for a monitor device; this ensures that they always have accurate color information for their target, even if the user or another app has changed the active profile for the device.</span></span>

### <a name="desktop-applications"></a><span data-ttu-id="658c4-123">Applicazioni desktop</span><span class="sxs-lookup"><span data-stu-id="658c4-123">Desktop applications</span></span>

<span data-ttu-id="658c4-124">Le applicazioni desktop devono restare in ascolto delle modifiche al registro di sistema per determinare quando le associazioni del profilo colori sono state modificate usando [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span><span class="sxs-lookup"><span data-stu-id="658c4-124">Desktop apps should listen for changes to the registry to determine when a color profile associations has changed using [**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue).</span></span> <span data-ttu-id="658c4-125">Un'app deve registrarsi sia per le modifiche dell'associazione del profilo per utente che per le modifiche a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="658c4-125">An app should register both for per-user profile association changes, and for system-wide changes.</span></span>

<span data-ttu-id="658c4-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) deve essere inizializzato con un HKEY fornito da [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span><span class="sxs-lookup"><span data-stu-id="658c4-126">[**RegNotifyChangeKeyValue**](/windows/win32/api/winreg/nf-winreg-regnotifychangekeyvalue) should be initialized with an HKEY provided by [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa).</span></span> <span data-ttu-id="658c4-127">**RegOpenKeyEx** deve essere inizializzato utilizzando i seguenti percorsi dell'albero del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="658c4-127">**RegOpenKeyEx** should be initialized using the following registry tree locations:</span></span>



|                                  |                                                                                                                                                    |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="658c4-128">Associazioni di profili per utente</span><span class="sxs-lookup"><span data-stu-id="658c4-128">Per-user profile associations</span></span>    | <span data-ttu-id="658c4-129">**HKEY \_ \_ software utente corrente \\ Microsoft \\ Windows NT \\ CurrentVersion \\ ICM \\ ProfileAssociations \\ display \\ {4D36E96E-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="658c4-129">**HKEY\_CURRENT\_USER SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\ICM\\ProfileAssociations\\Display\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span> |
| <span data-ttu-id="658c4-130">Associazioni profilo a livello di sistema</span><span class="sxs-lookup"><span data-stu-id="658c4-130">System-wide profile associations</span></span> | <span data-ttu-id="658c4-131">**HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Class \\ {4D36E96E-E325-11CE-BFC1-08002BE10318}**</span><span class="sxs-lookup"><span data-stu-id="658c4-131">**HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Class\\{4d36e96e-e325-11ce-bfc1-08002be10318}**</span></span>                                        |



 

<span data-ttu-id="658c4-132">Quando l'app riceve una notifica di una modifica della chiave del registro di sistema, deve prima eseguire una query se le associazioni per utente o a livello di sistema vengono utilizzate chiamando [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span><span class="sxs-lookup"><span data-stu-id="658c4-132">When the app is notified of a registry key change, it should first query whether per-user or system-wide associations are being used by calling [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent).</span></span> <span data-ttu-id="658c4-133">Deve quindi chiamare [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) con il valore dell' [**\_ ambito di \_ gestione \_ del profilo WCS**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) appropriato per ottenere il nuovo profilo colore attivo per il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="658c4-133">It should then call [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile) with the right [**WCS\_PROFILE\_MANAGEMENT\_SCOPE**](/windows/win32/api/icm/ne-icm-wcs_profile_management_scope) value to obtain the new active color profile for the monitor.</span></span> <span data-ttu-id="658c4-134">Si noti che non tutte le modifiche apportate alla chiave del registro di sistema corrispondono a una modifica effettiva nel profilo colori attualmente attivo; l'app deve controllare se il profilo restituito da **WcsGetDefaultColorProfile** è stato effettivamente modificato.</span><span class="sxs-lookup"><span data-stu-id="658c4-134">Note that not all registry key changes will correspond to an actual change in the currently active color profile; the app mush check whether the profile returned by **WcsGetDefaultColorProfile** has actually changed.</span></span>

### <a name="universal-windows-uwp-apps"></a><span data-ttu-id="658c4-135">App di Windows universale (UWP)</span><span class="sxs-lookup"><span data-stu-id="658c4-135">Universal Windows (UWP) apps</span></span>

<span data-ttu-id="658c4-136">Le app di Windows universale non hanno accesso alle chiavi del registro di sistema indicate sopra.</span><span class="sxs-lookup"><span data-stu-id="658c4-136">Universal Windows Apps do not have access to the above registry keys.</span></span> <span data-ttu-id="658c4-137">Devono invece registrare un gestore per l'evento [**DisplayInformation. ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) .</span><span class="sxs-lookup"><span data-stu-id="658c4-137">Instead, they should register a handler for the [**DisplayInformation.ColorProfileChanged**](/uwp/api/Windows.Graphics.Display.DisplayInformation) event.</span></span> <span data-ttu-id="658c4-138">Questo evento viene generato ogni volta che viene modificato il profilo colori attivo per il monitoraggio in cui è in esecuzione l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="658c4-138">This event fires whenever the active color profile for the monitor on which the application is running has changed.</span></span> <span data-ttu-id="658c4-139">ColorProfileChanged prende in considerazione la possibilità di usare associazioni di profili per singolo utente o a livello di sistema; Queste informazioni sono astratte dalle app UWP.</span><span class="sxs-lookup"><span data-stu-id="658c4-139">ColorProfileChanged takes into account whether per-user or system-wide profile associations are being used; this information is abstracted from UWP apps.</span></span>

<span data-ttu-id="658c4-140">Quando si risponde all'evento ColorProfileChanged, l'app deve eseguire una query sul profilo attualmente attivo usando [**DisplayInformation. GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span><span class="sxs-lookup"><span data-stu-id="658c4-140">When responding to the ColorProfileChanged event, the app should query the currently active profile using [**DisplayInformation.GetColorProfileAsync**](/uwp/api/Windows.Graphics.Display.DisplayInformation).</span></span>

 

 