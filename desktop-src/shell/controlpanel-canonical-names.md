---
description: A partire da Windows Vista, agli elementi del pannello di controllo inclusi in Windows viene assegnato un nome canonico che può essere utilizzato in una chiamata API o un'istruzione della riga di comando per avviare l'elemento a livello di codice.
ms.assetid: A02DFC9F-646D-40d8-901C-7239A820DE2C
title: Nomi canonici degli elementi del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55fc360b0d3db0f85a057977d1898c59d09d5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966525"
---
# <a name="canonical-names-of-control-panel-items"></a><span data-ttu-id="cdf72-103">Nomi canonici degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-103">Canonical Names of Control Panel Items</span></span>

<span data-ttu-id="cdf72-104">A partire da Windows Vista, agli elementi del pannello di controllo inclusi in Windows viene assegnato un nome canonico che può essere utilizzato in una [chiamata API o un'istruzione della riga di comando](executing-control-panel-items.md) per avviare l'elemento a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="cdf72-104">As of Windows Vista, Control Panel items included with Windows are given a canonical name that can be used in an [API call or a command-line instruction](executing-control-panel-items.md) to programmatically launch that item.</span></span> <span data-ttu-id="cdf72-105">A partire da Windows 7 e Windows Server 2008 R2, i nomi canonici possono essere usati in un criterio di gruppo per nascondere elementi specifici del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-105">As of Windows 7 and Windows Server 2008 R2, canonical names can be used in a group policy to hide specific Control Panel items.</span></span> <span data-ttu-id="cdf72-106">Questo argomento fornisce informazioni dettagliate per ogni elemento del pannello di controllo: nome canonico, GUID, nome del modulo e versioni del sistema operativo che riconoscono il nome canonico.</span><span class="sxs-lookup"><span data-stu-id="cdf72-106">This topic provides details for each Control Panel item: canonical name, GUID, module name, and the operating system versions that recognize the canonical name.</span></span>

> [!Note]  
> <span data-ttu-id="cdf72-107">I nomi canonici per gli elementi del pannello di controllo non sono supportati prima di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cdf72-107">Canonical names for Control Panel items are not supported prior to Windows Vista.</span></span>

 

-   [<span data-ttu-id="cdf72-108">Nomi canonici del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-108">Control Panel Canonical Names</span></span>](#control-panel-canonical-names)
-   [<span data-ttu-id="cdf72-109">Nomi canonici del pannello di controllo deprecati</span><span class="sxs-lookup"><span data-stu-id="cdf72-109">Deprecated Control Panel Canonical Names</span></span>](#deprecated-control-panel-canonical-names)
-   [<span data-ttu-id="cdf72-110">Uso di nomi canonici in Criteri di gruppo</span><span class="sxs-lookup"><span data-stu-id="cdf72-110">Using Canonical Names in Group Policy</span></span>](#using-canonical-names-in-local-group-policy)
-   [<span data-ttu-id="cdf72-111">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="cdf72-111">Remarks</span></span>](#remarks)

## <a name="control-panel-canonical-names"></a><span data-ttu-id="cdf72-112">Nomi canonici del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-112">Control Panel Canonical Names</span></span>

<span data-ttu-id="cdf72-113">Punti da ricordare quando si utilizzano questi valori:</span><span class="sxs-lookup"><span data-stu-id="cdf72-113">Points to remember when working with these values:</span></span>

-   <span data-ttu-id="cdf72-114">Per definizione, i nomi canonici non cambiano in base alla lingua del sistema; sono sempre in inglese, anche se la lingua del sistema non lo è.</span><span class="sxs-lookup"><span data-stu-id="cdf72-114">By definition, canonical names do not change based on the system language; they're always in English, even if the system's language is not.</span></span>
-   <span data-ttu-id="cdf72-115">Non tutti gli elementi del pannello di controllo sono presenti in tutte le varietà di finestre.</span><span class="sxs-lookup"><span data-stu-id="cdf72-115">Not all Control Panel items are present in all varieties of Windows.</span></span>
-   <span data-ttu-id="cdf72-116">Alcuni elementi del pannello di controllo vengono visualizzati solo se viene rilevato l'hardware corretto nel sistema.</span><span class="sxs-lookup"><span data-stu-id="cdf72-116">Some Control Panel items only appear if the right hardware is detected on the system.</span></span>
-   <span data-ttu-id="cdf72-117">Anche le terze parti possono aggiungere elementi del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-117">Third parties can also add Control Panel items.</span></span> <span data-ttu-id="cdf72-118">I nomi canonici elencati di seguito sono solo per gli elementi del pannello di controllo inclusi in Windows.</span><span class="sxs-lookup"><span data-stu-id="cdf72-118">The canonical names listed here are only for Control Panel items that are included with Windows.</span></span>

<span data-ttu-id="cdf72-119">Di seguito sono riportati gli elementi del pannello di controllo disponibili in Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="cdf72-119">The following are the Control Panel items available in Windows 8.1:</span></span>

-   [<span data-ttu-id="cdf72-120">Centro notifiche</span><span class="sxs-lookup"><span data-stu-id="cdf72-120">Action Center</span></span>](#action-center)
-   [<span data-ttu-id="cdf72-121">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-121">Administrative Tools</span></span>](#administrative-tools)
-   [<span data-ttu-id="cdf72-122">AutoPlay</span><span class="sxs-lookup"><span data-stu-id="cdf72-122">AutoPlay</span></span>](#autoplay)
-   [<span data-ttu-id="cdf72-123">Dispositivi biometrici</span><span class="sxs-lookup"><span data-stu-id="cdf72-123">Biometric Devices</span></span>](#biometric-devices)
-   [<span data-ttu-id="cdf72-124">Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="cdf72-124">BitLocker Drive Encryption</span></span>](#bitlocker-drive-encryption)
-   [<span data-ttu-id="cdf72-125">Gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="cdf72-125">Color Management</span></span>](#color-management)
-   [<span data-ttu-id="cdf72-126">Gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="cdf72-126">Credential Manager</span></span>](#credential-manager)
-   [<span data-ttu-id="cdf72-127">Data e ora</span><span class="sxs-lookup"><span data-stu-id="cdf72-127">Date and Time</span></span>](#date-and-time)
-   [<span data-ttu-id="cdf72-128">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="cdf72-128">Default Programs</span></span>](#default-programs)
-   [<span data-ttu-id="cdf72-129">Gestione dispositivi</span><span class="sxs-lookup"><span data-stu-id="cdf72-129">Device Manager</span></span>](#device-manager)
-   [<span data-ttu-id="cdf72-130">Dispositivi e stampanti</span><span class="sxs-lookup"><span data-stu-id="cdf72-130">Devices and Printers</span></span>](#devices-and-printers)
-   [<span data-ttu-id="cdf72-131">Schermo</span><span class="sxs-lookup"><span data-stu-id="cdf72-131">Display</span></span>](#display)
-   [<span data-ttu-id="cdf72-132">Centro accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="cdf72-132">Ease of Access Center</span></span>](#ease-of-access-center)
-   [<span data-ttu-id="cdf72-133">Protezione per la famiglia</span><span class="sxs-lookup"><span data-stu-id="cdf72-133">Family Safety</span></span>](#family-safety)
-   [<span data-ttu-id="cdf72-134">Cronologia file</span><span class="sxs-lookup"><span data-stu-id="cdf72-134">File History</span></span>](#file-history)
-   [<span data-ttu-id="cdf72-135">Opzioni cartella</span><span class="sxs-lookup"><span data-stu-id="cdf72-135">Folder Options</span></span>](#folder-options)
-   [<span data-ttu-id="cdf72-136">Tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="cdf72-136">Fonts</span></span>](#fonts)
-   [<span data-ttu-id="cdf72-137">Gruppo Home</span><span class="sxs-lookup"><span data-stu-id="cdf72-137">HomeGroup</span></span>](#homegroup)
-   [<span data-ttu-id="cdf72-138">Opzioni di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-138">Indexing Options</span></span>](#indexing-options)
-   [<span data-ttu-id="cdf72-139">Infrarossi</span><span class="sxs-lookup"><span data-stu-id="cdf72-139">Infrared</span></span>](#infrared)
-   [<span data-ttu-id="cdf72-140">Opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="cdf72-140">Internet Options</span></span>](#internet-options)
-   [<span data-ttu-id="cdf72-141">Iniziatore iSCSI</span><span class="sxs-lookup"><span data-stu-id="cdf72-141">iSCSI Initiator</span></span>](#iscsi-initiator)
-   [<span data-ttu-id="cdf72-142">Server iSNS</span><span class="sxs-lookup"><span data-stu-id="cdf72-142">iSNS Server</span></span>](#isns-server)
-   [<span data-ttu-id="cdf72-143">Tastiera</span><span class="sxs-lookup"><span data-stu-id="cdf72-143">Keyboard</span></span>](#keyboard)
-   [<span data-ttu-id="cdf72-144">Impostazioni percorso</span><span class="sxs-lookup"><span data-stu-id="cdf72-144">Location Settings</span></span>](#location-settings)
-   [<span data-ttu-id="cdf72-145">Mouse</span><span class="sxs-lookup"><span data-stu-id="cdf72-145">Mouse</span></span>](#mouse)
-   [<span data-ttu-id="cdf72-146">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdf72-146">MPIOConfiguration</span></span>](#mpioconfiguration)
-   [<span data-ttu-id="cdf72-147">Centro connessioni di rete e condivisione</span><span class="sxs-lookup"><span data-stu-id="cdf72-147">Network and Sharing Center</span></span>](#network-and-sharing-center)
-   [<span data-ttu-id="cdf72-148">Icone dell'area di notifica</span><span class="sxs-lookup"><span data-stu-id="cdf72-148">Notification Area Icons</span></span>](#notification-area-icons)
-   [<span data-ttu-id="cdf72-149">Penna e tocco</span><span class="sxs-lookup"><span data-stu-id="cdf72-149">Pen and Touch</span></span>](#pen-and-touch)
-   [<span data-ttu-id="cdf72-150">Personalizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-150">Personalization</span></span>](#personalization)
-   [<span data-ttu-id="cdf72-151">Telefono e modem</span><span class="sxs-lookup"><span data-stu-id="cdf72-151">Phone and Modem</span></span>](#phone-and-modem)
-   [<span data-ttu-id="cdf72-152">Opzioni risparmio energia</span><span class="sxs-lookup"><span data-stu-id="cdf72-152">Power Options</span></span>](#power-options)
-   [<span data-ttu-id="cdf72-153">Programmi e funzionalità</span><span class="sxs-lookup"><span data-stu-id="cdf72-153">Programs and Features</span></span>](#programs-and-features)
-   [<span data-ttu-id="cdf72-154">Ripristino</span><span class="sxs-lookup"><span data-stu-id="cdf72-154">Recovery</span></span>](#recovery)
-   [<span data-ttu-id="cdf72-155">Area</span><span class="sxs-lookup"><span data-stu-id="cdf72-155">Region</span></span>](#region)
-   [<span data-ttu-id="cdf72-156">Connessioni RemoteApp e desktop</span><span class="sxs-lookup"><span data-stu-id="cdf72-156">RemoteApp and Desktop Connections</span></span>](#remoteapp-and-desktop-connections)
-   [<span data-ttu-id="cdf72-157">Suoni</span><span class="sxs-lookup"><span data-stu-id="cdf72-157">Sound</span></span>](#sound)
-   [<span data-ttu-id="cdf72-158">Riconoscimento vocale</span><span class="sxs-lookup"><span data-stu-id="cdf72-158">Speech Recognition</span></span>](#speech-recognition)
-   [<span data-ttu-id="cdf72-159">Spazi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-159">Storage Spaces</span></span>](#storage-spaces)
-   [<span data-ttu-id="cdf72-160">Centro sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-160">Sync Center</span></span>](#sync-center)
-   [<span data-ttu-id="cdf72-161">Sistema</span><span class="sxs-lookup"><span data-stu-id="cdf72-161">System</span></span>](#system)
-   [<span data-ttu-id="cdf72-162">Impostazioni Tablet PC</span><span class="sxs-lookup"><span data-stu-id="cdf72-162">Tablet PC Settings</span></span>](#tablet-pc-settings)
-   [<span data-ttu-id="cdf72-163">Barra delle applicazioni e navigazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-163">Taskbar and Navigation</span></span>](#taskbar-and-navigation)
-   [<span data-ttu-id="cdf72-164">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="cdf72-164">Troubleshooting</span></span>](#troubleshooting)
-   [<span data-ttu-id="cdf72-165">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="cdf72-165">TSAppInstall</span></span>](#tsappinstall)
-   [<span data-ttu-id="cdf72-166">Account utente</span><span class="sxs-lookup"><span data-stu-id="cdf72-166">User Accounts</span></span>](#user-accounts)
-   [<span data-ttu-id="cdf72-167">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="cdf72-167">Windows Anytime Upgrade</span></span>](#windows-anytime-upgrade)
-   [<span data-ttu-id="cdf72-168">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="cdf72-168">Windows Defender</span></span>](#windows-defender)
-   [<span data-ttu-id="cdf72-169">Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="cdf72-169">Windows Firewall</span></span>](#windows-firewall)
-   [<span data-ttu-id="cdf72-170">Centro PC portatile Windows</span><span class="sxs-lookup"><span data-stu-id="cdf72-170">Windows Mobility Center</span></span>](#windows-mobility-center)
-   [<span data-ttu-id="cdf72-171">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="cdf72-171">Windows To Go</span></span>](#windows-to-go)
-   [<span data-ttu-id="cdf72-172">Windows Update</span><span class="sxs-lookup"><span data-stu-id="cdf72-172">Windows Update</span></span>](#windows-update)
-   [<span data-ttu-id="cdf72-173">Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="cdf72-173">Work Folders</span></span>](#work-folders)

### <a name="action-center"></a><span data-ttu-id="cdf72-174">Centro notifiche</span><span class="sxs-lookup"><span data-stu-id="cdf72-174">Action Center</span></span>

-   <span data-ttu-id="cdf72-175">**Nome canonico**: Microsoft. ActionCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-175">**Canonical name**: Microsoft.ActionCenter</span></span>
-   <span data-ttu-id="cdf72-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span><span class="sxs-lookup"><span data-stu-id="cdf72-176">**GUID**: {BB64F8A7-BEE7-4E1A-AB8D-7D8273F7FDB6}</span></span>
-   <span data-ttu-id="cdf72-177">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-177">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-178">**Nome modulo**: @% systemroot% \\ system32 \\ActionCenterCPL.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-178">**Module name**: @%SystemRoot%\\System32\\ActionCenterCPL.dll,-1</span></span>
-   <span data-ttu-id="cdf72-179">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-179">**Pages**</span></span>

    | <span data-ttu-id="cdf72-180">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-180">Page Name</span></span>           | <span data-ttu-id="cdf72-181">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-181">Opens</span></span>                      |
    |---------------------|----------------------------|
    | <span data-ttu-id="cdf72-182">MaintenanceSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-182">MaintenanceSettings</span></span> | <span data-ttu-id="cdf72-183">Manutenzione automatica</span><span class="sxs-lookup"><span data-stu-id="cdf72-183">Automatic Maintenance</span></span>      |
    | <span data-ttu-id="cdf72-184">pageProblems</span><span class="sxs-lookup"><span data-stu-id="cdf72-184">pageProblems</span></span>        | <span data-ttu-id="cdf72-185">Segnalazioni di problemi</span><span class="sxs-lookup"><span data-stu-id="cdf72-185">Problem Reports</span></span>            |
    | <span data-ttu-id="cdf72-186">pageReliabilityView</span><span class="sxs-lookup"><span data-stu-id="cdf72-186">pageReliabilityView</span></span> | <span data-ttu-id="cdf72-187">Monitoraggio affidabilità</span><span class="sxs-lookup"><span data-stu-id="cdf72-187">Reliability Monitor</span></span>        |
    | <span data-ttu-id="cdf72-188">pageResponseArchive</span><span class="sxs-lookup"><span data-stu-id="cdf72-188">pageResponseArchive</span></span> | <span data-ttu-id="cdf72-189">Messaggi archiviati</span><span class="sxs-lookup"><span data-stu-id="cdf72-189">Archived Messages</span></span>          |
    | <span data-ttu-id="cdf72-190">pageSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-190">pageSettings</span></span>        | <span data-ttu-id="cdf72-191">Impostazioni segnalazione problemi</span><span class="sxs-lookup"><span data-stu-id="cdf72-191">Problem Reporting Settings</span></span> |

    

     

### <a name="administrative-tools"></a><span data-ttu-id="cdf72-192">Strumenti di amministrazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-192">Administrative Tools</span></span>

-   <span data-ttu-id="cdf72-193">**Nome canonico**: Microsoft. AdministrativeTools</span><span class="sxs-lookup"><span data-stu-id="cdf72-193">**Canonical name**: Microsoft.AdministrativeTools</span></span>
-   <span data-ttu-id="cdf72-194">**GUID**: {D20EA4E1-3957-11D2-A40B-0C5020524153}</span><span class="sxs-lookup"><span data-stu-id="cdf72-194">**GUID**: {D20EA4E1-3957-11d2-A40B-0C5020524153}</span></span>
-   <span data-ttu-id="cdf72-195">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-195">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-196">**Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-22982</span><span class="sxs-lookup"><span data-stu-id="cdf72-196">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22982</span></span>

### <a name="autoplay"></a><span data-ttu-id="cdf72-197">AutoPlay</span><span class="sxs-lookup"><span data-stu-id="cdf72-197">AutoPlay</span></span>

-   <span data-ttu-id="cdf72-198">**Nome canonico**: Microsoft. AutoPlay</span><span class="sxs-lookup"><span data-stu-id="cdf72-198">**Canonical name**: Microsoft.AutoPlay</span></span>
-   <span data-ttu-id="cdf72-199">**GUID**: {9C60DE1E-E5FC-40F4-A487-460851A8D915}</span><span class="sxs-lookup"><span data-stu-id="cdf72-199">**GUID**: {9C60DE1E-E5FC-40f4-A487-460851A8D915}</span></span>
-   <span data-ttu-id="cdf72-200">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-200">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-201">**Nome modulo**: @% systemroot% \\ system32 \\autoplay.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-201">**Module name**: @%SystemRoot%\\System32\\autoplay.dll,-1</span></span>

### <a name="biometric-devices"></a><span data-ttu-id="cdf72-202">Dispositivi biometrici</span><span class="sxs-lookup"><span data-stu-id="cdf72-202">Biometric Devices</span></span>

-   <span data-ttu-id="cdf72-203">**Nome canonico**: Microsoft. BiometricDevices</span><span class="sxs-lookup"><span data-stu-id="cdf72-203">**Canonical name**: Microsoft.BiometricDevices</span></span>
-   <span data-ttu-id="cdf72-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span><span class="sxs-lookup"><span data-stu-id="cdf72-204">**GUID**: {0142e4d0-fb7a-11dc-ba4a-000ffe7ab428}</span></span>
-   <span data-ttu-id="cdf72-205">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-205">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-206">**Nome modulo**: @% systemroot% \\ system32 \\biocpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-206">**Module name**: @%SystemRoot%\\System32\\biocpl.dll,-1</span></span>

### <a name="bitlocker-drive-encryption"></a><span data-ttu-id="cdf72-207">Crittografia unità BitLocker</span><span class="sxs-lookup"><span data-stu-id="cdf72-207">BitLocker Drive Encryption</span></span>

-   <span data-ttu-id="cdf72-208">**Nome canonico**: Microsoft. BitLockerDriveEncryption</span><span class="sxs-lookup"><span data-stu-id="cdf72-208">**Canonical name**: Microsoft.BitLockerDriveEncryption</span></span>
-   <span data-ttu-id="cdf72-209">**GUID**: {D9EF8727-CaC2-4E60-809E-86F80A666C91}</span><span class="sxs-lookup"><span data-stu-id="cdf72-209">**GUID**: {D9EF8727-CAC2-4e60-809E-86F80A666C91}</span></span>
-   <span data-ttu-id="cdf72-210">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-210">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-211">**Nome modulo**: @% systemroot% \\ system32 \\fvecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-211">**Module name**: @%SystemRoot%\\System32\\fvecpl.dll,-1</span></span>

### <a name="color-management"></a><span data-ttu-id="cdf72-212">Gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="cdf72-212">Color Management</span></span>

-   <span data-ttu-id="cdf72-213">**Nome canonico**: Microsoft. ColorManagement</span><span class="sxs-lookup"><span data-stu-id="cdf72-213">**Canonical name**: Microsoft.ColorManagement</span></span>
-   <span data-ttu-id="cdf72-214">**GUID**: {B2C761C6-29BC-4F19-9251-E6195265BAF1}</span><span class="sxs-lookup"><span data-stu-id="cdf72-214">**GUID**: {B2C761C6-29BC-4f19-9251-E6195265BAF1}</span></span>
-   <span data-ttu-id="cdf72-215">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-215">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-216">**Nome modulo**: @% systemroot% \\ system32 \\colorcpl.exe,-6</span><span class="sxs-lookup"><span data-stu-id="cdf72-216">**Module name**: @%systemroot%\\system32\\colorcpl.exe,-6</span></span>

### <a name="credential-manager"></a><span data-ttu-id="cdf72-217">Gestione credenziali</span><span class="sxs-lookup"><span data-stu-id="cdf72-217">Credential Manager</span></span>

-   <span data-ttu-id="cdf72-218">**Nome canonico**: Microsoft. CredentialManager</span><span class="sxs-lookup"><span data-stu-id="cdf72-218">**Canonical name**: Microsoft.CredentialManager</span></span>
-   <span data-ttu-id="cdf72-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span><span class="sxs-lookup"><span data-stu-id="cdf72-219">**GUID**: {1206F5F1-0569-412C-8FEC-3204630DFB70}</span></span>
-   <span data-ttu-id="cdf72-220">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-220">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-221">**Nome modulo**: @% systemroot% \\ system32 \\Vault.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-221">**Module name**: @%SystemRoot%\\system32\\Vault.dll,-1</span></span>
-   <span data-ttu-id="cdf72-222">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-222">**Pages**</span></span>

    | <span data-ttu-id="cdf72-223">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-223">Page Name</span></span>                   | <span data-ttu-id="cdf72-224">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-224">Opens</span></span>               |
    |-----------------------------|---------------------|
    | <span data-ttu-id="cdf72-225">? SelectedVault = CredmanVault</span><span class="sxs-lookup"><span data-stu-id="cdf72-225">?SelectedVault=CredmanVault</span></span> | <span data-ttu-id="cdf72-226">Credenziali di Windows</span><span class="sxs-lookup"><span data-stu-id="cdf72-226">Windows Credentials</span></span> |

    

     

### <a name="date-and-time"></a><span data-ttu-id="cdf72-227">Data e ora</span><span class="sxs-lookup"><span data-stu-id="cdf72-227">Date and Time</span></span>

-   <span data-ttu-id="cdf72-228">**Nome canonico**: Microsoft. DateAndTime</span><span class="sxs-lookup"><span data-stu-id="cdf72-228">**Canonical name**: Microsoft.DateAndTime</span></span>
-   <span data-ttu-id="cdf72-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span><span class="sxs-lookup"><span data-stu-id="cdf72-229">**GUID**: {E2E7934B-DCE5-43C4-9576-7FE4F75E7480}</span></span>
-   <span data-ttu-id="cdf72-230">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-230">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-231">**Nome del modulo**: @% systemroot% \\ system32 \\timedate.cpl,-51</span><span class="sxs-lookup"><span data-stu-id="cdf72-231">**Module name**: @%SystemRoot%\\System32\\timedate.cpl,-51</span></span>
-   <span data-ttu-id="cdf72-232">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-232">**Pages**</span></span>

    | <span data-ttu-id="cdf72-233">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-233">Page Name</span></span> | <span data-ttu-id="cdf72-234">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-234">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="cdf72-235">1</span><span class="sxs-lookup"><span data-stu-id="cdf72-235">1</span></span>         | <span data-ttu-id="cdf72-236">Orologi aggiuntivi</span><span class="sxs-lookup"><span data-stu-id="cdf72-236">Additional Clocks</span></span> |

    

     

### <a name="default-programs"></a><span data-ttu-id="cdf72-237">Programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="cdf72-237">Default Programs</span></span>

-   <span data-ttu-id="cdf72-238">**Nome canonico**: Microsoft. DefaultPrograms</span><span class="sxs-lookup"><span data-stu-id="cdf72-238">**Canonical name**: Microsoft.DefaultPrograms</span></span>
-   <span data-ttu-id="cdf72-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span><span class="sxs-lookup"><span data-stu-id="cdf72-239">**GUID**: {17cd9488-1228-4b2f-88ce-4298e93e0966}</span></span>
-   <span data-ttu-id="cdf72-240">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-240">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-241">**Nome modulo**: @% systemroot% \\ system32 \\sud.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-241">**Module name**: @%SystemRoot%\\System32\\sud.dll,-1</span></span>
-   <span data-ttu-id="cdf72-242">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-242">**Pages**</span></span>

    | <span data-ttu-id="cdf72-243">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-243">Page Name</span></span>          | <span data-ttu-id="cdf72-244">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-244">Opens</span></span>                |
    |--------------------|----------------------|
    | <span data-ttu-id="cdf72-245">pageDefaultProgram</span><span class="sxs-lookup"><span data-stu-id="cdf72-245">pageDefaultProgram</span></span> | <span data-ttu-id="cdf72-246">Imposta programmi predefiniti</span><span class="sxs-lookup"><span data-stu-id="cdf72-246">Set Default Programs</span></span> |
    | <span data-ttu-id="cdf72-247">pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="cdf72-247">pageFileAssoc</span></span>      | <span data-ttu-id="cdf72-248">Imposta associazioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-248">Set Associations</span></span>     |

    

     

### <a name="device-manager"></a><span data-ttu-id="cdf72-249">Gestione dispositivi</span><span class="sxs-lookup"><span data-stu-id="cdf72-249">Device Manager</span></span>

-   <span data-ttu-id="cdf72-250">**Nome canonico**: Microsoft. devicemanager</span><span class="sxs-lookup"><span data-stu-id="cdf72-250">**Canonical name**: Microsoft.DeviceManager</span></span>
-   <span data-ttu-id="cdf72-251">**GUID**: {74246bfc-4c96-11D0-abef-0020af6b0b7a}</span><span class="sxs-lookup"><span data-stu-id="cdf72-251">**GUID**: {74246bfc-4c96-11d0-abef-0020af6b0b7a}</span></span>
-   <span data-ttu-id="cdf72-252">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-252">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-253">**Nome modulo**: @% systemroot% \\ system32 \\devmgr.dll,-4</span><span class="sxs-lookup"><span data-stu-id="cdf72-253">**Module name**: @%SystemRoot%\\System32\\devmgr.dll,-4</span></span>

### <a name="devices-and-printers"></a><span data-ttu-id="cdf72-254">Dispositivi e stampanti</span><span class="sxs-lookup"><span data-stu-id="cdf72-254">Devices and Printers</span></span>

-   <span data-ttu-id="cdf72-255">**Nome canonico**: Microsoft. DevicesAndPrinters</span><span class="sxs-lookup"><span data-stu-id="cdf72-255">**Canonical name**: Microsoft.DevicesAndPrinters</span></span>
-   <span data-ttu-id="cdf72-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-256">**GUID**: {A8A91A66-3A7D-4424-8D24-04E180695C7A}</span></span>
-   <span data-ttu-id="cdf72-257">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-257">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-258">**Nome del modulo**: @% systemroot% \\ system32 \\DeviceCenter.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="cdf72-258">**Module name**: @%systemroot%\\system32\\DeviceCenter.dll,-1000</span></span>

### <a name="display"></a><span data-ttu-id="cdf72-259">Visualizza</span><span class="sxs-lookup"><span data-stu-id="cdf72-259">Display</span></span>

-   <span data-ttu-id="cdf72-260">**Nome canonico**: Microsoft. display</span><span class="sxs-lookup"><span data-stu-id="cdf72-260">**Canonical name**: Microsoft.Display</span></span>
-   <span data-ttu-id="cdf72-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-261">**GUID**: {C555438B-3C23-4769-A71F-B6D3D9B6053A}</span></span>
-   <span data-ttu-id="cdf72-262">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-262">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-263">**Nome modulo**: @% systemroot% \\ system32 \\Display.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-263">**Module name**: @%SystemRoot%\\System32\\Display.dll,-1</span></span>
-   <span data-ttu-id="cdf72-264">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-264">**Pages**</span></span>

    | <span data-ttu-id="cdf72-265">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-265">Page Name</span></span> | <span data-ttu-id="cdf72-266">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-266">Opens</span></span>             |
    |-----------|-------------------|
    | <span data-ttu-id="cdf72-267">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-267">Settings</span></span>  | <span data-ttu-id="cdf72-268">Risoluzione dello schermo</span><span class="sxs-lookup"><span data-stu-id="cdf72-268">Screen Resolution</span></span> |

    

     

### <a name="ease-of-access-center"></a><span data-ttu-id="cdf72-269">Centro accesso facilitato</span><span class="sxs-lookup"><span data-stu-id="cdf72-269">Ease of Access Center</span></span>

-   <span data-ttu-id="cdf72-270">**Nome canonico**: Microsoft. EaseOfAccessCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-270">**Canonical name**: Microsoft.EaseOfAccessCenter</span></span>
-   <span data-ttu-id="cdf72-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-271">**GUID**: {D555645E-D4F8-4c29-A827-D93C859C4F2A}</span></span>
-   <span data-ttu-id="cdf72-272">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-272">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-273">**Nome del modulo**: @% systemroot% \\ system32 \\accessibilitycpl.dll,-10</span><span class="sxs-lookup"><span data-stu-id="cdf72-273">**Module name**: @%SystemRoot%\\System32\\accessibilitycpl.dll,-10</span></span>
-   <span data-ttu-id="cdf72-274">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-274">**Pages**</span></span>

    | <span data-ttu-id="cdf72-275">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-275">Page Name</span></span>               | <span data-ttu-id="cdf72-276">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-276">Opens</span></span>                                                               |
    |-------------------------|---------------------------------------------------------------------|
    | <span data-ttu-id="cdf72-277">pageEasierToClick</span><span class="sxs-lookup"><span data-stu-id="cdf72-277">pageEasierToClick</span></span>       | <span data-ttu-id="cdf72-278">Semplifica l'uso del mouse</span><span class="sxs-lookup"><span data-stu-id="cdf72-278">Make the mouse easier to use</span></span>                                        |
    | <span data-ttu-id="cdf72-279">pageEasierToSee</span><span class="sxs-lookup"><span data-stu-id="cdf72-279">pageEasierToSee</span></span>         | <span data-ttu-id="cdf72-280">Semplifica la visualizzazione del computer</span><span class="sxs-lookup"><span data-stu-id="cdf72-280">Make the computer easier to see</span></span>                                     |
    | <span data-ttu-id="cdf72-281">pageEasierWithSounds</span><span class="sxs-lookup"><span data-stu-id="cdf72-281">pageEasierWithSounds</span></span>    | <span data-ttu-id="cdf72-282">Usare il testo o le alternative visive per i suoni</span><span class="sxs-lookup"><span data-stu-id="cdf72-282">Use text or visual alternatives for sounds</span></span>                          |
    | <span data-ttu-id="cdf72-283">pageFilterKeysSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-283">pageFilterKeysSettings</span></span>  | <span data-ttu-id="cdf72-284">Configurare chiavi di filtro</span><span class="sxs-lookup"><span data-stu-id="cdf72-284">Set up Filter Keys</span></span>                                                  |
    | <span data-ttu-id="cdf72-285">pageKeyboardEasierToUse</span><span class="sxs-lookup"><span data-stu-id="cdf72-285">pageKeyboardEasierToUse</span></span> | <span data-ttu-id="cdf72-286">Semplifica l'uso della tastiera</span><span class="sxs-lookup"><span data-stu-id="cdf72-286">Make the keyboard easier to use</span></span>                                     |
    | <span data-ttu-id="cdf72-287">pageNoMouseOrKeyboard</span><span class="sxs-lookup"><span data-stu-id="cdf72-287">pageNoMouseOrKeyboard</span></span>   | <span data-ttu-id="cdf72-288">Utilizzare il computer senza mouse o tastiera</span><span class="sxs-lookup"><span data-stu-id="cdf72-288">Use the computer without a mouse or keyboard</span></span>                        |
    | <span data-ttu-id="cdf72-289">pageNoVisual</span><span class="sxs-lookup"><span data-stu-id="cdf72-289">pageNoVisual</span></span>            | <span data-ttu-id="cdf72-290">Usare il computer senza visualizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-290">Use the computer without a display</span></span>                                  |
    | <span data-ttu-id="cdf72-291">pageQuestionsCognitive</span><span class="sxs-lookup"><span data-stu-id="cdf72-291">pageQuestionsCognitive</span></span>  | <span data-ttu-id="cdf72-292">Ottenere consigli per semplificare l'uso del computer (cognitive)</span><span class="sxs-lookup"><span data-stu-id="cdf72-292">Get recommendations to make your computer easier to use (cognitive)</span></span> |
    | <span data-ttu-id="cdf72-293">pageQuestionsEyesight</span><span class="sxs-lookup"><span data-stu-id="cdf72-293">pageQuestionsEyesight</span></span>   | <span data-ttu-id="cdf72-294">Ottenere consigli per semplificare l'uso del computer (vista)</span><span class="sxs-lookup"><span data-stu-id="cdf72-294">Get recommendations to make your computer easier to use (eyesight)</span></span>  |

    

     

### <a name="family-safety"></a><span data-ttu-id="cdf72-295">Protezione per la famiglia</span><span class="sxs-lookup"><span data-stu-id="cdf72-295">Family Safety</span></span>

-   <span data-ttu-id="cdf72-296">**Nome canonico**: Microsoft. parentalcontrols</span><span class="sxs-lookup"><span data-stu-id="cdf72-296">**Canonical name**: Microsoft.ParentalControls</span></span>
-   <span data-ttu-id="cdf72-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-297">**GUID**: {96AE8D84-A250-4520-95A5-A47A7E3C548B}</span></span>
-   <span data-ttu-id="cdf72-298">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-298">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-299">**Nome del modulo**: @% systemroot% \\ system32 \\wpccpl.dll,-100</span><span class="sxs-lookup"><span data-stu-id="cdf72-299">**Module name**: @%SystemRoot%\\System32\\wpccpl.dll,-100</span></span>
-   <span data-ttu-id="cdf72-300">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-300">**Pages**</span></span>

    | <span data-ttu-id="cdf72-301">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-301">Page Name</span></span>   | <span data-ttu-id="cdf72-302">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-302">Opens</span></span>                                  |
    |-------------|----------------------------------------|
    | <span data-ttu-id="cdf72-303">pageUserHub</span><span class="sxs-lookup"><span data-stu-id="cdf72-303">pageUserHub</span></span> | <span data-ttu-id="cdf72-304">Scegliere un utente e configurare la sicurezza delle famiglie</span><span class="sxs-lookup"><span data-stu-id="cdf72-304">Choose a user and set up Family Safety</span></span> |

    

     

### <a name="file-history"></a><span data-ttu-id="cdf72-305">Cronologia file</span><span class="sxs-lookup"><span data-stu-id="cdf72-305">File History</span></span>

-   <span data-ttu-id="cdf72-306">**Nome canonico**: Microsoft. filehistory</span><span class="sxs-lookup"><span data-stu-id="cdf72-306">**Canonical name**: Microsoft.FileHistory</span></span>
-   <span data-ttu-id="cdf72-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span><span class="sxs-lookup"><span data-stu-id="cdf72-307">**GUID**: {F6B6E965-E9B2-444B-9286-10C9152EDBC5}</span></span>
-   <span data-ttu-id="cdf72-308">**Sistema operativo supportato**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-308">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-309">**Nome del modulo**: @% systemroot% \\ system32 \\fhcpl.dll,-52</span><span class="sxs-lookup"><span data-stu-id="cdf72-309">**Module name**: @%SystemRoot%\\System32\\fhcpl.dll,-52</span></span>
-   <span data-ttu-id="cdf72-310">La cronologia file include una versione più recente dell'elemento di backup e ripristino, ma il nome canonico dell'elemento precedente non viene rimappato alla cronologia file.</span><span class="sxs-lookup"><span data-stu-id="cdf72-310">File History includes a newer version of the Backup and Restore item, but that older item's canonical name does not remap to File History.</span></span>

### <a name="folder-options"></a><span data-ttu-id="cdf72-311">Opzioni cartella</span><span class="sxs-lookup"><span data-stu-id="cdf72-311">Folder Options</span></span>

-   <span data-ttu-id="cdf72-312">**Nome canonico**: Microsoft. FolderOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-312">**Canonical name**: Microsoft.FolderOptions</span></span>
-   <span data-ttu-id="cdf72-313">**GUID**: {6DFD7C5C-2451-11D3-A299-00C04F8EF6AF}</span><span class="sxs-lookup"><span data-stu-id="cdf72-313">**GUID**: {6DFD7C5C-2451-11d3-A299-00C04F8EF6AF}</span></span>
-   <span data-ttu-id="cdf72-314">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-314">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-315">**Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-22985</span><span class="sxs-lookup"><span data-stu-id="cdf72-315">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-22985</span></span>

### <a name="fonts"></a><span data-ttu-id="cdf72-316">Tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="cdf72-316">Fonts</span></span>

-   <span data-ttu-id="cdf72-317">**Nome canonico**: Microsoft. Fonts</span><span class="sxs-lookup"><span data-stu-id="cdf72-317">**Canonical name**: Microsoft.Fonts</span></span>
-   <span data-ttu-id="cdf72-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span><span class="sxs-lookup"><span data-stu-id="cdf72-318">**GUID**: {93412589-74D4-4E4E-AD0E-E0CB621440FD}</span></span>
-   <span data-ttu-id="cdf72-319">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-319">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-320">**Nome del modulo**: @% systemroot% \\ system32 \\FontExt.dll,-8007</span><span class="sxs-lookup"><span data-stu-id="cdf72-320">**Module name**: @%SystemRoot%\\System32\\FontExt.dll,-8007</span></span>

### <a name="homegroup"></a><span data-ttu-id="cdf72-321">Gruppo Home</span><span class="sxs-lookup"><span data-stu-id="cdf72-321">HomeGroup</span></span>

-   <span data-ttu-id="cdf72-322">**Nome canonico**: Microsoft. Gruppo Home</span><span class="sxs-lookup"><span data-stu-id="cdf72-322">**Canonical name**: Microsoft.HomeGroup</span></span>
-   <span data-ttu-id="cdf72-323">**GUID**: {67CA7650-96E6-4fdd-BB43-A8E774F73A57}</span><span class="sxs-lookup"><span data-stu-id="cdf72-323">**GUID**: {67CA7650-96E6-4FDD-BB43-A8E774F73A57}</span></span>
-   <span data-ttu-id="cdf72-324">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-324">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-325">**Nome modulo**: @% systemroot% \\ system32 \\hgcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-325">**Module name**: @%SystemRoot%\\System32\\hgcpl.dll,-1</span></span>

### <a name="indexing-options"></a><span data-ttu-id="cdf72-326">Opzioni di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-326">Indexing Options</span></span>

-   <span data-ttu-id="cdf72-327">**Nome canonico**: Microsoft. IndexingOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-327">**Canonical name**: Microsoft.IndexingOptions</span></span>
-   <span data-ttu-id="cdf72-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span><span class="sxs-lookup"><span data-stu-id="cdf72-328">**GUID**: {87D66A43-7B11-4A28-9811-C86EE395ACF7}</span></span>
-   <span data-ttu-id="cdf72-329">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-329">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-330">**Nome del modulo**: @% systemroot% \\ system32 \\srchadmin.dll,-601</span><span class="sxs-lookup"><span data-stu-id="cdf72-330">**Module name**: @%SystemRoot%\\System32\\srchadmin.dll,-601</span></span>

### <a name="infrared"></a><span data-ttu-id="cdf72-331">Infrarossi</span><span class="sxs-lookup"><span data-stu-id="cdf72-331">Infrared</span></span>

-   <span data-ttu-id="cdf72-332">**Nome canonico**: Microsoft. Infrared</span><span class="sxs-lookup"><span data-stu-id="cdf72-332">**Canonical name**: Microsoft.Infrared</span></span>
-   <span data-ttu-id="cdf72-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="cdf72-333">**GUID**: {A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span>
-   <span data-ttu-id="cdf72-334">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-334">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-335">**Nome modulo**: @% systemroot% \\ system32 \\irprops.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-335">**Module name**: @%SystemRoot%\\System32\\irprops.cpl,-1</span></span>

### <a name="internet-options"></a><span data-ttu-id="cdf72-336">Opzioni Internet</span><span class="sxs-lookup"><span data-stu-id="cdf72-336">Internet Options</span></span>

-   <span data-ttu-id="cdf72-337">**Nome canonico**: Microsoft. InternetOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-337">**Canonical name**: Microsoft.InternetOptions</span></span>
-   <span data-ttu-id="cdf72-338">**GUID**: {A3DD4F92-658A-410f-84FD-6FBBBEF2FFFE}</span><span class="sxs-lookup"><span data-stu-id="cdf72-338">**GUID**: {A3DD4F92-658A-410F-84FD-6FBBBEF2FFFE}</span></span>
-   <span data-ttu-id="cdf72-339">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-339">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-340">**Nome del modulo**: @C: \\ Windows \\ system32 \\inetcpl.cpl,-4312</span><span class="sxs-lookup"><span data-stu-id="cdf72-340">**Module name**: @C:\\Windows\\System32\\inetcpl.cpl,-4312</span></span>
-   <span data-ttu-id="cdf72-341">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-341">**Pages**</span></span>

    | <span data-ttu-id="cdf72-342">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-342">Page Name</span></span> | <span data-ttu-id="cdf72-343">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-343">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="cdf72-344">1</span><span class="sxs-lookup"><span data-stu-id="cdf72-344">1</span></span>         | <span data-ttu-id="cdf72-345">Sicurezza</span><span class="sxs-lookup"><span data-stu-id="cdf72-345">Security</span></span>    |
    | <span data-ttu-id="cdf72-346">2</span><span class="sxs-lookup"><span data-stu-id="cdf72-346">2</span></span>         | <span data-ttu-id="cdf72-347">Privacy</span><span class="sxs-lookup"><span data-stu-id="cdf72-347">Privacy</span></span>     |
    | <span data-ttu-id="cdf72-348">3</span><span class="sxs-lookup"><span data-stu-id="cdf72-348">3</span></span>         | <span data-ttu-id="cdf72-349">Content</span><span class="sxs-lookup"><span data-stu-id="cdf72-349">Content</span></span>     |
    | <span data-ttu-id="cdf72-350">4</span><span class="sxs-lookup"><span data-stu-id="cdf72-350">4</span></span>         | <span data-ttu-id="cdf72-351">Connessioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-351">Connections</span></span> |
    | <span data-ttu-id="cdf72-352">5</span><span class="sxs-lookup"><span data-stu-id="cdf72-352">5</span></span>         | <span data-ttu-id="cdf72-353">Programmi</span><span class="sxs-lookup"><span data-stu-id="cdf72-353">Programs</span></span>    |
    | <span data-ttu-id="cdf72-354">6</span><span class="sxs-lookup"><span data-stu-id="cdf72-354">6</span></span>         | <span data-ttu-id="cdf72-355">Avanzato</span><span class="sxs-lookup"><span data-stu-id="cdf72-355">Advanced</span></span>    |

    

     

### <a name="iscsi-initiator"></a><span data-ttu-id="cdf72-356">Iniziatore iSCSI</span><span class="sxs-lookup"><span data-stu-id="cdf72-356">iSCSI Initiator</span></span>

-   <span data-ttu-id="cdf72-357">**Nome canonico**: Microsoft. iSCSIInitiator</span><span class="sxs-lookup"><span data-stu-id="cdf72-357">**Canonical name**: Microsoft.iSCSIInitiator</span></span>
-   <span data-ttu-id="cdf72-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span><span class="sxs-lookup"><span data-stu-id="cdf72-358">**GUID**: {A304259D-52B8-4526-8B1A-A1D6CECC8243}</span></span>
-   <span data-ttu-id="cdf72-359">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-359">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-360">**Nome del modulo**: @% systemroot% \\ system32 \\iscsicpl.dll,-5001</span><span class="sxs-lookup"><span data-stu-id="cdf72-360">**Module name**: @%SystemRoot%\\System32\\iscsicpl.dll,-5001</span></span>

### <a name="isns-server"></a><span data-ttu-id="cdf72-361">Server iSNS</span><span class="sxs-lookup"><span data-stu-id="cdf72-361">iSNS Server</span></span>

-   <span data-ttu-id="cdf72-362">**Nome canonico**: Microsoft. iSNSServer</span><span class="sxs-lookup"><span data-stu-id="cdf72-362">**Canonical name**: Microsoft.iSNSServer</span></span>
-   <span data-ttu-id="cdf72-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span><span class="sxs-lookup"><span data-stu-id="cdf72-363">**GUID**: {0D2A3442-5181-4E3A-9BD4-83BD10AF3D76}</span></span>
-   <span data-ttu-id="cdf72-364">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-364">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-365">**Nome del modulo**: @% systemroot% \\ system32 \\isnssrv.dll,-5005</span><span class="sxs-lookup"><span data-stu-id="cdf72-365">**Module name**: @%SystemRoot%\\System32\\isnssrv.dll,-5005</span></span>
-   <span data-ttu-id="cdf72-366">Questo elemento del pannello di controllo verrà visualizzato solo nelle versioni server di Windows.</span><span class="sxs-lookup"><span data-stu-id="cdf72-366">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="keyboard"></a><span data-ttu-id="cdf72-367">Tastiera</span><span class="sxs-lookup"><span data-stu-id="cdf72-367">Keyboard</span></span>

-   <span data-ttu-id="cdf72-368">**Nome canonico**: Microsoft. Keyboard</span><span class="sxs-lookup"><span data-stu-id="cdf72-368">**Canonical name**: Microsoft.Keyboard</span></span>
-   <span data-ttu-id="cdf72-369">**GUID**: {725BE8F7-668E-4c7b-8F90-46BDB0936430}</span><span class="sxs-lookup"><span data-stu-id="cdf72-369">**GUID**: {725BE8F7-668E-4C7B-8F90-46BDB0936430}</span></span>
-   <span data-ttu-id="cdf72-370">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-370">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-371">**Nome del modulo**: @% systemroot% \\ system32 \\main.cpl,-102</span><span class="sxs-lookup"><span data-stu-id="cdf72-371">**Module name**: @%SystemRoot%\\System32\\main.cpl,-102</span></span>

### <a name="location-settings"></a><span data-ttu-id="cdf72-372">Impostazioni percorso</span><span class="sxs-lookup"><span data-stu-id="cdf72-372">Location Settings</span></span>

-   <span data-ttu-id="cdf72-373">**Nome canonico**: Microsoft. LocationSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-373">**Canonical name**: Microsoft.LocationSettings</span></span>
-   <span data-ttu-id="cdf72-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-374">**GUID**: {E9950154-C418-419e-A90A-20C5287AE24B}</span></span>
-   <span data-ttu-id="cdf72-375">**Sistema operativo supportato**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-375">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-376">**Nome modulo**: @% systemroot% \\ system32 \\SensorsCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-376">**Module name**: @%SystemRoot%\\System32\\SensorsCpl.dll,-1</span></span>

### <a name="mouse"></a><span data-ttu-id="cdf72-377">Mouse</span><span class="sxs-lookup"><span data-stu-id="cdf72-377">Mouse</span></span>

-   <span data-ttu-id="cdf72-378">**Nome canonico**: Microsoft. mouse</span><span class="sxs-lookup"><span data-stu-id="cdf72-378">**Canonical name**: Microsoft.Mouse</span></span>
-   <span data-ttu-id="cdf72-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span><span class="sxs-lookup"><span data-stu-id="cdf72-379">**GUID**: {6C8EEC18-8D75-41B2-A177-8831D59D2D50}</span></span>
-   <span data-ttu-id="cdf72-380">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-380">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-381">**Nome del modulo**: @% systemroot% \\ system32 \\main.cpl,-100</span><span class="sxs-lookup"><span data-stu-id="cdf72-381">**Module name**: @%SystemRoot%\\System32\\main.cpl,-100</span></span>
-   <span data-ttu-id="cdf72-382">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-382">**Pages**</span></span>

    | <span data-ttu-id="cdf72-383">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-383">Page Name</span></span> | <span data-ttu-id="cdf72-384">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-384">Opens</span></span>           |
    |-----------|-----------------|
    | <span data-ttu-id="cdf72-385">1</span><span class="sxs-lookup"><span data-stu-id="cdf72-385">1</span></span>         | <span data-ttu-id="cdf72-386">Pointers</span><span class="sxs-lookup"><span data-stu-id="cdf72-386">Pointers</span></span>        |
    | <span data-ttu-id="cdf72-387">2</span><span class="sxs-lookup"><span data-stu-id="cdf72-387">2</span></span>         | <span data-ttu-id="cdf72-388">Opzioni puntatore</span><span class="sxs-lookup"><span data-stu-id="cdf72-388">Pointer Options</span></span> |
    | <span data-ttu-id="cdf72-389">3</span><span class="sxs-lookup"><span data-stu-id="cdf72-389">3</span></span>         | <span data-ttu-id="cdf72-390">Selettore circolare</span><span class="sxs-lookup"><span data-stu-id="cdf72-390">Wheel</span></span>           |
    | <span data-ttu-id="cdf72-391">4</span><span class="sxs-lookup"><span data-stu-id="cdf72-391">4</span></span>         | <span data-ttu-id="cdf72-392">Hardware</span><span class="sxs-lookup"><span data-stu-id="cdf72-392">Hardware</span></span>        |

    

     

### <a name="mpioconfiguration"></a><span data-ttu-id="cdf72-393">MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdf72-393">MPIOConfiguration</span></span>

-   <span data-ttu-id="cdf72-394">**Nome canonico**: Microsoft. MPIOConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdf72-394">**Canonical name**: Microsoft.MPIOConfiguration</span></span>
-   <span data-ttu-id="cdf72-395">**GUID**: {AB3BE6AA-7561-4838-ab77-ACF8427DF426}</span><span class="sxs-lookup"><span data-stu-id="cdf72-395">**GUID**: {AB3BE6AA-7561-4838-AB77-ACF8427DF426}</span></span>
-   <span data-ttu-id="cdf72-396">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-396">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-397">**Nome del modulo**: @% systemroot% \\ system32 \\mpiocpl.dll,-1000</span><span class="sxs-lookup"><span data-stu-id="cdf72-397">**Module name**: @%SystemRoot%\\System32\\mpiocpl.dll,-1000</span></span>
-   <span data-ttu-id="cdf72-398">Questo elemento del pannello di controllo verrà visualizzato solo nelle versioni server di Windows.</span><span class="sxs-lookup"><span data-stu-id="cdf72-398">This Control Panel item will be seen only in server versions of Windows.</span></span>

### <a name="network-and-sharing-center"></a><span data-ttu-id="cdf72-399">Centro connessioni di rete e condivisione</span><span class="sxs-lookup"><span data-stu-id="cdf72-399">Network and Sharing Center</span></span>

-   <span data-ttu-id="cdf72-400">**Nome canonico**: Microsoft. NetworkAndSharingCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-400">**Canonical name**: Microsoft.NetworkAndSharingCenter</span></span>
-   <span data-ttu-id="cdf72-401">**GUID**: {8E908FC9-Becc-40f6-915B-F4CA0E70D03D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-401">**GUID**: {8E908FC9-BECC-40f6-915B-F4CA0E70D03D}</span></span>
-   <span data-ttu-id="cdf72-402">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-402">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-403">**Nome modulo**: @% systemroot% \\ system32 \\netcenter.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-403">**Module name**: @%SystemRoot%\\System32\\netcenter.dll,-1</span></span>
-   <span data-ttu-id="cdf72-404">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-404">**Pages**</span></span>

    | <span data-ttu-id="cdf72-405">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-405">Page Name</span></span>  | <span data-ttu-id="cdf72-406">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-406">Opens</span></span>                     |
    |------------|---------------------------|
    | <span data-ttu-id="cdf72-407">Avanzato</span><span class="sxs-lookup"><span data-stu-id="cdf72-407">Advanced</span></span>   | <span data-ttu-id="cdf72-408">Impostazioni di condivisione avanzate</span><span class="sxs-lookup"><span data-stu-id="cdf72-408">Advanced sharing settings</span></span> |
    | <span data-ttu-id="cdf72-409">ShareMedia</span><span class="sxs-lookup"><span data-stu-id="cdf72-409">ShareMedia</span></span> | <span data-ttu-id="cdf72-410">Opzioni di streaming multimediale</span><span class="sxs-lookup"><span data-stu-id="cdf72-410">Media streaming options</span></span>   |

    

     

### <a name="notification-area-icons"></a><span data-ttu-id="cdf72-411">Icone dell'area di notifica</span><span class="sxs-lookup"><span data-stu-id="cdf72-411">Notification Area Icons</span></span>

-   <span data-ttu-id="cdf72-412">**Nome canonico**: Microsoft. NotificationAreaIcons</span><span class="sxs-lookup"><span data-stu-id="cdf72-412">**Canonical name**: Microsoft.NotificationAreaIcons</span></span>
-   <span data-ttu-id="cdf72-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span><span class="sxs-lookup"><span data-stu-id="cdf72-413">**GUID**: {05d7b0f4-2121-4eff-bf6b-ed3f69b894d9}</span></span>
-   <span data-ttu-id="cdf72-414">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-414">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-415">**Nome modulo**: @% systemroot% \\ system32 \\taskbarcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-415">**Module name**: @%SystemRoot%\\System32\\taskbarcpl.dll,-1</span></span>

### <a name="pen-and-touch"></a><span data-ttu-id="cdf72-416">Penna e tocco</span><span class="sxs-lookup"><span data-stu-id="cdf72-416">Pen and Touch</span></span>

-   <span data-ttu-id="cdf72-417">**Nome canonico**: Microsoft. PenAndTouch</span><span class="sxs-lookup"><span data-stu-id="cdf72-417">**Canonical name**: Microsoft.PenAndTouch</span></span>
-   <span data-ttu-id="cdf72-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-418">**GUID**: {F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span>
-   <span data-ttu-id="cdf72-419">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-419">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-420">**Nome del modulo**: @% systemroot% \\ system32 \\tabletpc.cpl,-10103</span><span class="sxs-lookup"><span data-stu-id="cdf72-420">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10103</span></span>
-   <span data-ttu-id="cdf72-421">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-421">**Pages**</span></span>

    | <span data-ttu-id="cdf72-422">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-422">Page Name</span></span> | <span data-ttu-id="cdf72-423">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-423">Opens</span></span>       |
    |-----------|-------------|
    | <span data-ttu-id="cdf72-424">1</span><span class="sxs-lookup"><span data-stu-id="cdf72-424">1</span></span>         | <span data-ttu-id="cdf72-425">I gesti rapidi</span><span class="sxs-lookup"><span data-stu-id="cdf72-425">Flicks</span></span>      |
    | <span data-ttu-id="cdf72-426">2</span><span class="sxs-lookup"><span data-stu-id="cdf72-426">2</span></span>         | <span data-ttu-id="cdf72-427">Scrittura a mano</span><span class="sxs-lookup"><span data-stu-id="cdf72-427">Handwriting</span></span> |

    

     

### <a name="personalization"></a><span data-ttu-id="cdf72-428">Personalization</span><span class="sxs-lookup"><span data-stu-id="cdf72-428">Personalization</span></span>

-   <span data-ttu-id="cdf72-429">**Nome canonico**: Microsoft. personalizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-429">**Canonical name**: Microsoft.Personalization</span></span>
-   <span data-ttu-id="cdf72-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span><span class="sxs-lookup"><span data-stu-id="cdf72-430">**GUID**: {ED834ED6-4B5A-4bfe-8F11-A626DCB6A921}</span></span>
-   <span data-ttu-id="cdf72-431">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-431">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-432">**Nome modulo**: @% systemroot% \\ system32 \\themecpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-432">**Module name**: @%SystemRoot%\\System32\\themecpl.dll,-1</span></span>
-   <span data-ttu-id="cdf72-433">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-433">**Pages**</span></span>

    | <span data-ttu-id="cdf72-434">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-434">Page Name</span></span>        | <span data-ttu-id="cdf72-435">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-435">Opens</span></span>                |
    |------------------|----------------------|
    | <span data-ttu-id="cdf72-436">pageColorization</span><span class="sxs-lookup"><span data-stu-id="cdf72-436">pageColorization</span></span> | <span data-ttu-id="cdf72-437">Colore e aspetto</span><span class="sxs-lookup"><span data-stu-id="cdf72-437">Color and Appearance</span></span> |
    | <span data-ttu-id="cdf72-438">pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="cdf72-438">pageWallpaper</span></span>    | <span data-ttu-id="cdf72-439">Sfondo del desktop</span><span class="sxs-lookup"><span data-stu-id="cdf72-439">Desktop Background</span></span>   |

    

     

### <a name="phone-and-modem"></a><span data-ttu-id="cdf72-440">Telefono e modem</span><span class="sxs-lookup"><span data-stu-id="cdf72-440">Phone and Modem</span></span>

-   <span data-ttu-id="cdf72-441">**Nome canonico**: Microsoft. PhoneAndModem</span><span class="sxs-lookup"><span data-stu-id="cdf72-441">**Canonical name**: Microsoft.PhoneAndModem</span></span>
-   <span data-ttu-id="cdf72-442">**GUID**: {40419485-c444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-442">**GUID**: {40419485-C444-4567-851A-2DD7BFA1684D}</span></span>
-   <span data-ttu-id="cdf72-443">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-443">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-444">**Nome modulo**: @% systemroot% \\ system32 \\telephon.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-444">**Module name**: @%SystemRoot%\\System32\\telephon.cpl,-1</span></span>
-   <span data-ttu-id="cdf72-445">La finestra avviata da questo valore è intitolata "Information location" nelle versioni di Windows precedenti a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-445">The window that this value launches is titled "Location Information" in versions of Windows prior to Windows 8.</span></span> <span data-ttu-id="cdf72-446">L'interfaccia utente dell'elemento è notevolmente cambiata a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-446">The item's UI is considerably changed as of Windows 8.</span></span>

### <a name="power-options"></a><span data-ttu-id="cdf72-447">Opzioni risparmio energia</span><span class="sxs-lookup"><span data-stu-id="cdf72-447">Power Options</span></span>

-   <span data-ttu-id="cdf72-448">**Nome canonico**: Microsoft. PowerOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-448">**Canonical name**: Microsoft.PowerOptions</span></span>
-   <span data-ttu-id="cdf72-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-449">**GUID**: {025A5937-A6BE-4686-A844-36FE4BEC8B6D}</span></span>
-   <span data-ttu-id="cdf72-450">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-450">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-451">**Nome modulo**: @% systemroot% \\ system32 \\powercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-451">**Module name**: @%SystemRoot%\\System32\\powercpl.dll,-1</span></span>
-   <span data-ttu-id="cdf72-452">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-452">**Pages**</span></span>

    | <span data-ttu-id="cdf72-453">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-453">Page Name</span></span>          | <span data-ttu-id="cdf72-454">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-454">Opens</span></span>              |
    |--------------------|--------------------|
    | <span data-ttu-id="cdf72-455">pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-455">pageGlobalSettings</span></span> | <span data-ttu-id="cdf72-456">Impostazioni sistema</span><span class="sxs-lookup"><span data-stu-id="cdf72-456">System Settings</span></span>    |
    | <span data-ttu-id="cdf72-457">pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-457">pagePlanSettings</span></span>   | <span data-ttu-id="cdf72-458">Modificare le impostazioni del piano</span><span class="sxs-lookup"><span data-stu-id="cdf72-458">Edit Plan Settings</span></span> |

    

     

### <a name="programs-and-features"></a><span data-ttu-id="cdf72-459">Programmi e funzionalità</span><span class="sxs-lookup"><span data-stu-id="cdf72-459">Programs and Features</span></span>

-   <span data-ttu-id="cdf72-460">**Nome canonico**: Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="cdf72-460">**Canonical name**: Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="cdf72-461">**GUID**: {7b81be6a-ce2b-4676-A29E-eb907a5126c5}</span><span class="sxs-lookup"><span data-stu-id="cdf72-461">**GUID**: {7b81be6a-ce2b-4676-a29e-eb907a5126c5}</span></span>
-   <span data-ttu-id="cdf72-462">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-462">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-463">**Nome del modulo**: @% systemroot% \\ system32 \\appwiz.cpl,-159</span><span class="sxs-lookup"><span data-stu-id="cdf72-463">**Module name**: @%systemroot%\\system32\\appwiz.cpl,-159</span></span>
-   <span data-ttu-id="cdf72-464">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-464">**Pages**</span></span>

    | <span data-ttu-id="cdf72-465">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-465">Page Name</span></span>                                | <span data-ttu-id="cdf72-466">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-466">Opens</span></span>             |
    |------------------------------------------|-------------------|
    | <span data-ttu-id="cdf72-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span><span class="sxs-lookup"><span data-stu-id="cdf72-467">::{D450A8A1-9568-45C7-9C0E-B4F9FB4537BD}</span></span> | <span data-ttu-id="cdf72-468">Aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="cdf72-468">Installed Updates</span></span> |

    

     

### <a name="recovery"></a><span data-ttu-id="cdf72-469">Ripristino</span><span class="sxs-lookup"><span data-stu-id="cdf72-469">Recovery</span></span>

-   <span data-ttu-id="cdf72-470">**Nome canonico**: Microsoft. Recovery</span><span class="sxs-lookup"><span data-stu-id="cdf72-470">**Canonical name**: Microsoft.Recovery</span></span>
-   <span data-ttu-id="cdf72-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span><span class="sxs-lookup"><span data-stu-id="cdf72-471">**GUID**: {9FE63AFD-59CF-4419-9775-ABCC3849F861}</span></span>
-   <span data-ttu-id="cdf72-472">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-472">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-473">**Nome del modulo**: @% systemroot% \\ system32 \\recovery.dll,-101</span><span class="sxs-lookup"><span data-stu-id="cdf72-473">**Module name**: @%SystemRoot%\\System32\\recovery.dll,-101</span></span>

### <a name="region"></a><span data-ttu-id="cdf72-474">Region</span><span class="sxs-lookup"><span data-stu-id="cdf72-474">Region</span></span>

-   <span data-ttu-id="cdf72-475">**Nome canonico**: Microsoft. RegionAndLanguage</span><span class="sxs-lookup"><span data-stu-id="cdf72-475">**Canonical name**: Microsoft.RegionAndLanguage</span></span>
-   <span data-ttu-id="cdf72-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="cdf72-476">**GUID**: {62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span>
-   <span data-ttu-id="cdf72-477">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-477">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-478">**Nome modulo**: @% systemroot% \\ system32 \\intl.cpl,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-478">**Module name**: @%SystemRoot%\\System32\\intl.cpl,-1</span></span>
-   <span data-ttu-id="cdf72-479">L'elemento Region e Language trovato in Windows 7 è stato suddiviso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-479">The Region and Language item found in Windows 7 was split as of Windows 8.</span></span> <span data-ttu-id="cdf72-480">Microsoft. RegionAndLanguage ora avvia l'elemento Region.</span><span class="sxs-lookup"><span data-stu-id="cdf72-480">Microsoft.RegionAndLanguage now launches the Region item.</span></span> <span data-ttu-id="cdf72-481">Per avviare l'elemento della lingua, utilizzare [Microsoft. Language](#location-settings).</span><span class="sxs-lookup"><span data-stu-id="cdf72-481">To launch the Language item, use [Microsoft.Language](#location-settings).</span></span>
-   <span data-ttu-id="cdf72-482">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-482">**Pages**</span></span>

    | <span data-ttu-id="cdf72-483">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-483">Page Name</span></span> | <span data-ttu-id="cdf72-484">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-484">Opens</span></span>          |
    |-----------|----------------|
    | <span data-ttu-id="cdf72-485">1</span><span class="sxs-lookup"><span data-stu-id="cdf72-485">1</span></span>         | <span data-ttu-id="cdf72-486">Location</span><span class="sxs-lookup"><span data-stu-id="cdf72-486">Location</span></span>       |
    | <span data-ttu-id="cdf72-487">2</span><span class="sxs-lookup"><span data-stu-id="cdf72-487">2</span></span>         | <span data-ttu-id="cdf72-488">Amministrativo</span><span class="sxs-lookup"><span data-stu-id="cdf72-488">Administrative</span></span> |

    

     

### <a name="remoteapp-and-desktop-connections"></a><span data-ttu-id="cdf72-489">Connessioni RemoteApp e desktop</span><span class="sxs-lookup"><span data-stu-id="cdf72-489">RemoteApp and Desktop Connections</span></span>

-   <span data-ttu-id="cdf72-490">**Nome canonico**: Microsoft. RemoteAppAndDesktopConnections</span><span class="sxs-lookup"><span data-stu-id="cdf72-490">**Canonical name**: Microsoft.RemoteAppAndDesktopConnections</span></span>
-   <span data-ttu-id="cdf72-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-491">**GUID**: {241D7C96-F8BF-4F85-B01F-E2B043341A4B}</span></span>
-   <span data-ttu-id="cdf72-492">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-492">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-493">**Nome del modulo**: @% systemroot% \\ system32 \\tsworkspace.dll,-15300</span><span class="sxs-lookup"><span data-stu-id="cdf72-493">**Module name**: @%SystemRoot%\\System32\\tsworkspace.dll,-15300</span></span>

### <a name="sound"></a><span data-ttu-id="cdf72-494">Suoni</span><span class="sxs-lookup"><span data-stu-id="cdf72-494">Sound</span></span>

-   <span data-ttu-id="cdf72-495">**Nome canonico**: Microsoft. Sound</span><span class="sxs-lookup"><span data-stu-id="cdf72-495">**Canonical name**: Microsoft.Sound</span></span>
-   <span data-ttu-id="cdf72-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-496">**GUID**: {F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span>
-   <span data-ttu-id="cdf72-497">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-497">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-498">**Nome del modulo**: @% systemroot% \\ system32 \\mmsys.cpl,-300</span><span class="sxs-lookup"><span data-stu-id="cdf72-498">**Module name**: @%SystemRoot%\\System32\\mmsys.cpl,-300</span></span>

### <a name="speech-recognition"></a><span data-ttu-id="cdf72-499">Riconoscimento vocale</span><span class="sxs-lookup"><span data-stu-id="cdf72-499">Speech Recognition</span></span>

-   <span data-ttu-id="cdf72-500">**Nome canonico**: Microsoft. sintesi vocale</span><span class="sxs-lookup"><span data-stu-id="cdf72-500">**Canonical name**: Microsoft.SpeechRecognition</span></span>
-   <span data-ttu-id="cdf72-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-501">**GUID**: {58E3C745-D971-4081-9034-86E34B30836A}</span></span>
-   <span data-ttu-id="cdf72-502">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-502">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-503">**Nome del modulo**: @% systemroot% \\ System32 \\ Speech \\ SpeechUX \\speechuxcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-503">**Module name**: @%SystemRoot%\\System32\\Speech\\SpeechUX\\speechuxcpl.dll,-1</span></span>

### <a name="storage-spaces"></a><span data-ttu-id="cdf72-504">Spazi di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-504">Storage Spaces</span></span>

-   <span data-ttu-id="cdf72-505">**Nome canonico**: Microsoft. StorageSpaces</span><span class="sxs-lookup"><span data-stu-id="cdf72-505">**Canonical name**: Microsoft.StorageSpaces</span></span>
-   <span data-ttu-id="cdf72-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span><span class="sxs-lookup"><span data-stu-id="cdf72-506">**GUID**: {F942C606-0914-47AB-BE56-1321B8035096}</span></span>
-   <span data-ttu-id="cdf72-507">**Sistema operativo supportato**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-507">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-508">**Nome del modulo**: @C: \\ Windows \\ system32 \\SpaceControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-508">**Module name**: @C:\\Windows\\System32\\SpaceControl.dll,-1</span></span>

### <a name="sync-center"></a><span data-ttu-id="cdf72-509">Centro sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-509">Sync Center</span></span>

-   <span data-ttu-id="cdf72-510">**Nome canonico**: Microsoft. synccenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-510">**Canonical name**: Microsoft.SyncCenter</span></span>
-   <span data-ttu-id="cdf72-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span><span class="sxs-lookup"><span data-stu-id="cdf72-511">**GUID**: {9C73F5E5-7AE7-4E32-A8E8-8D23B85255BF}</span></span>
-   <span data-ttu-id="cdf72-512">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-512">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-513">**Nome del modulo**: @% systemroot% \\ system32 \\SyncCenter.dll,-3000</span><span class="sxs-lookup"><span data-stu-id="cdf72-513">**Module name**: @%SystemRoot%\\System32\\SyncCenter.dll,-3000</span></span>

### <a name="system"></a><span data-ttu-id="cdf72-514">Sistema</span><span class="sxs-lookup"><span data-stu-id="cdf72-514">System</span></span>

-   <span data-ttu-id="cdf72-515">**Nome canonico**: Microsoft.System</span><span class="sxs-lookup"><span data-stu-id="cdf72-515">**Canonical name**: Microsoft.System</span></span>
-   <span data-ttu-id="cdf72-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span><span class="sxs-lookup"><span data-stu-id="cdf72-516">**GUID**: {BB06C0E4-D293-4f75-8A90-CB05B6477EEE}</span></span>
-   <span data-ttu-id="cdf72-517">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-517">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-518">**Nome modulo**: @% systemroot% \\ system32 \\systemcpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-518">**Module name**: @%SystemRoot%\\System32\\systemcpl.dll,-1</span></span>

### <a name="tablet-pc-settings"></a><span data-ttu-id="cdf72-519">Impostazioni Tablet PC</span><span class="sxs-lookup"><span data-stu-id="cdf72-519">Tablet PC Settings</span></span>

-   <span data-ttu-id="cdf72-520">**Nome canonico**: Microsoft. TabletPCSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-520">**Canonical name**: Microsoft.TabletPCSettings</span></span>
-   <span data-ttu-id="cdf72-521">**GUID**: {80F3F1D5-Feca-45F3-BC32-752C152E456E}</span><span class="sxs-lookup"><span data-stu-id="cdf72-521">**GUID**: {80F3F1D5-FECA-45F3-BC32-752C152E456E}</span></span>
-   <span data-ttu-id="cdf72-522">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-522">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-523">**Nome del modulo**: @% systemroot% \\ system32 \\tabletpc.cpl,-10100</span><span class="sxs-lookup"><span data-stu-id="cdf72-523">**Module name**: @%SystemRoot%\\System32\\tabletpc.cpl,-10100</span></span>

### <a name="taskbar-and-navigation"></a><span data-ttu-id="cdf72-524">Barra delle applicazioni e navigazione</span><span class="sxs-lookup"><span data-stu-id="cdf72-524">Taskbar and Navigation</span></span>

-   <span data-ttu-id="cdf72-525">**Nome canonico**: Microsoft. Taskbar</span><span class="sxs-lookup"><span data-stu-id="cdf72-525">**Canonical name**: Microsoft.Taskbar</span></span>
-   <span data-ttu-id="cdf72-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="cdf72-526">**GUID**: {0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span>
-   <span data-ttu-id="cdf72-527">**Sistema operativo supportato**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-527">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-528">**Nome del modulo**: @% systemroot% \\ system32 \\shell32.dll,-32517</span><span class="sxs-lookup"><span data-stu-id="cdf72-528">**Module name**: @%SystemRoot%\\system32\\shell32.dll,-32517</span></span>

### <a name="troubleshooting"></a><span data-ttu-id="cdf72-529">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="cdf72-529">Troubleshooting</span></span>

-   <span data-ttu-id="cdf72-530">**Nome canonico**: Microsoft. Troubleshooting</span><span class="sxs-lookup"><span data-stu-id="cdf72-530">**Canonical name**: Microsoft.Troubleshooting</span></span>
-   <span data-ttu-id="cdf72-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span><span class="sxs-lookup"><span data-stu-id="cdf72-531">**GUID**: {C58C4893-3BE0-4B45-ABB5-A63E4B8C8651}</span></span>
-   <span data-ttu-id="cdf72-532">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-532">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-533">**Nome modulo**: @% systemroot% \\ system32 \\DiagCpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-533">**Module name**: @%SystemRoot%\\System32\\DiagCpl.dll,-1</span></span>
-   <span data-ttu-id="cdf72-534">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-534">**Pages**</span></span>

    | <span data-ttu-id="cdf72-535">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-535">Page Name</span></span>   | <span data-ttu-id="cdf72-536">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-536">Opens</span></span>   |
    |-------------|---------|
    | <span data-ttu-id="cdf72-537">HistoryPage</span><span class="sxs-lookup"><span data-stu-id="cdf72-537">HistoryPage</span></span> | <span data-ttu-id="cdf72-538">Cronologia</span><span class="sxs-lookup"><span data-stu-id="cdf72-538">History</span></span> |

    

     

### <a name="tsappinstall"></a><span data-ttu-id="cdf72-539">TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="cdf72-539">TSAppInstall</span></span>

-   <span data-ttu-id="cdf72-540">**Nome canonico**: Microsoft. TSAppInstall</span><span class="sxs-lookup"><span data-stu-id="cdf72-540">**Canonical name**: Microsoft.TSAppInstall</span></span>
-   <span data-ttu-id="cdf72-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span><span class="sxs-lookup"><span data-stu-id="cdf72-541">**GUID**: {BAA884F4-3432-48b8-AA72-9BF20EEF31D5}</span></span>
-   <span data-ttu-id="cdf72-542">**Sistema operativo supportato**: Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-542">**Supported OS**: Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-543">**Nome del modulo**: @% systemroot% \\ system32 \\tsappinstall.exe,-2001</span><span class="sxs-lookup"><span data-stu-id="cdf72-543">**Module name**: @%systemroot%\\system32\\tsappinstall.exe,-2001</span></span>

### <a name="user-accounts"></a><span data-ttu-id="cdf72-544">Account utente</span><span class="sxs-lookup"><span data-stu-id="cdf72-544">User Accounts</span></span>

-   <span data-ttu-id="cdf72-545">**Nome canonico**: Microsoft. UserAccounts</span><span class="sxs-lookup"><span data-stu-id="cdf72-545">**Canonical name**: Microsoft.UserAccounts</span></span>
-   <span data-ttu-id="cdf72-546">**GUID**: {60632754-C523-4b62-B45C-4172da012619}</span><span class="sxs-lookup"><span data-stu-id="cdf72-546">**GUID**: {60632754-c523-4b62-b45c-4172da012619}</span></span>
-   <span data-ttu-id="cdf72-547">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-547">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-548">**Nome modulo**: @% systemroot% \\ system32 \\usercpl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-548">**Module name**: @%SystemRoot%\\System32\\usercpl.dll,-1</span></span>

### <a name="windows-anytime-upgrade"></a><span data-ttu-id="cdf72-549">Windows Anytime Upgrade</span><span class="sxs-lookup"><span data-stu-id="cdf72-549">Windows Anytime Upgrade</span></span>

-   <span data-ttu-id="cdf72-550">**Nome canonico**: Microsoft. WindowsAnytimeUpgrade</span><span class="sxs-lookup"><span data-stu-id="cdf72-550">**Canonical name**: Microsoft.WindowsAnytimeUpgrade</span></span>
-   <span data-ttu-id="cdf72-551">**GUID**: {BE122A0E-4503-11da-8BDE-F66BAD1E3F3A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-551">**GUID**: {BE122A0E-4503-11DA-8BDE-F66BAD1E3F3A}</span></span>
-   <span data-ttu-id="cdf72-552">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-552">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-553">**Nome modulo**: @ $ (resourceString. \_ \_Percorso sys mod \_ ),-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-553">**Module name**: @$(resourceString.\_SYS\_MOD\_PATH),-1</span></span>

### <a name="windows-defender"></a><span data-ttu-id="cdf72-554">Windows Defender</span><span class="sxs-lookup"><span data-stu-id="cdf72-554">Windows Defender</span></span>

-   <span data-ttu-id="cdf72-555">**Nome canonico**: Microsoft. Windowsdefender</span><span class="sxs-lookup"><span data-stu-id="cdf72-555">**Canonical name**: Microsoft.WindowsDefender</span></span>
-   <span data-ttu-id="cdf72-556">**GUID**: {D8559EB9-20C0-410e-Beda-7ED416AECC2A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-556">**GUID**: {D8559EB9-20C0-410E-BEDA-7ED416AECC2A}</span></span>
-   <span data-ttu-id="cdf72-557">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-557">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-558">**Nome modulo**: @% ProgramFiles% \\ Windows Defender \\MsMpRes.dll,-104</span><span class="sxs-lookup"><span data-stu-id="cdf72-558">**Module name**: @%ProgramFiles%\\Windows Defender\\MsMpRes.dll,-104</span></span>

### <a name="windows-firewall"></a><span data-ttu-id="cdf72-559">Windows Firewall</span><span class="sxs-lookup"><span data-stu-id="cdf72-559">Windows Firewall</span></span>

-   <span data-ttu-id="cdf72-560">**Nome canonico**: Microsoft. WindowsFirewall</span><span class="sxs-lookup"><span data-stu-id="cdf72-560">**Canonical name**: Microsoft.WindowsFirewall</span></span>
-   <span data-ttu-id="cdf72-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span><span class="sxs-lookup"><span data-stu-id="cdf72-561">**GUID**: {4026492F-2F69-46B8-B9BF-5654FC07E423}</span></span>
-   <span data-ttu-id="cdf72-562">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-562">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-563">**Nome del modulo**: @C: \\ Windows \\ system32 \\FirewallControlPanel.dll,-12122</span><span class="sxs-lookup"><span data-stu-id="cdf72-563">**Module name**: @C:\\Windows\\system32\\FirewallControlPanel.dll,-12122</span></span>
-   <span data-ttu-id="cdf72-564">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-564">**Pages**</span></span>

    | <span data-ttu-id="cdf72-565">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-565">Page Name</span></span>         | <span data-ttu-id="cdf72-566">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-566">Opens</span></span>        |
    |-------------------|--------------|
    | <span data-ttu-id="cdf72-567">pageConfigureApps</span><span class="sxs-lookup"><span data-stu-id="cdf72-567">pageConfigureApps</span></span> | <span data-ttu-id="cdf72-568">App consentite</span><span class="sxs-lookup"><span data-stu-id="cdf72-568">Allowed apps</span></span> |

    

     

### <a name="windows-mobility-center"></a><span data-ttu-id="cdf72-569">Centro PC portatile Windows</span><span class="sxs-lookup"><span data-stu-id="cdf72-569">Windows Mobility Center</span></span>

-   <span data-ttu-id="cdf72-570">**Nome canonico**: Microsoft. MobilityCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-570">**Canonical name**: Microsoft.MobilityCenter</span></span>
-   <span data-ttu-id="cdf72-571">**GUID**: {5ea4f148-308C-46d7-98a9-49041b1dd468}</span><span class="sxs-lookup"><span data-stu-id="cdf72-571">**GUID**: {5ea4f148-308c-46d7-98a9-49041b1dd468}</span></span>
-   <span data-ttu-id="cdf72-572">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-572">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-573">**Nome del modulo**: @% systemroot% \\ system32 \\mblctr.exe,-1002</span><span class="sxs-lookup"><span data-stu-id="cdf72-573">**Module name**: @%SystemRoot%\\system32\\mblctr.exe,-1002</span></span>

### <a name="windows-to-go"></a><span data-ttu-id="cdf72-574">Windows To Go</span><span class="sxs-lookup"><span data-stu-id="cdf72-574">Windows To Go</span></span>

-   <span data-ttu-id="cdf72-575">**Nome canonico**: Microsoft. PortableWorkspaceCreator</span><span class="sxs-lookup"><span data-stu-id="cdf72-575">**Canonical name**: Microsoft.PortableWorkspaceCreator</span></span>
-   <span data-ttu-id="cdf72-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span><span class="sxs-lookup"><span data-stu-id="cdf72-576">**GUID**: {8E0C279D-0BD1-43C3-9EBD-31C3DC5B8A77}</span></span>
-   <span data-ttu-id="cdf72-577">**Sistema operativo supportato**: Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-577">**Supported OS**: Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-578">**Nome del modulo**: @% systemroot% \\ system32 \\pwcreator.exe,-151</span><span class="sxs-lookup"><span data-stu-id="cdf72-578">**Module name**: @%SystemRoot%\\System32\\pwcreator.exe,-151</span></span>

### <a name="windows-update"></a><span data-ttu-id="cdf72-579">Windows Update</span><span class="sxs-lookup"><span data-stu-id="cdf72-579">Windows Update</span></span>

-   <span data-ttu-id="cdf72-580">**Nome canonico**: Microsoft. windowsupdate</span><span class="sxs-lookup"><span data-stu-id="cdf72-580">**Canonical name**: Microsoft.WindowsUpdate</span></span>
-   <span data-ttu-id="cdf72-581">**GUID**: {36eef7db-88ad-4E81-ad49-0e313f0c35f8}</span><span class="sxs-lookup"><span data-stu-id="cdf72-581">**GUID**: {36eef7db-88ad-4e81-ad49-0e313f0c35f8}</span></span>
-   <span data-ttu-id="cdf72-582">**Sistema operativo supportato**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-582">**Supported OS**: Windows Vista, Windows 7, Windows 8, Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-583">**Nome modulo**: @% systemroot% \\ system32 \\wucltux.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-583">**Module name**: @%SystemRoot%\\system32\\wucltux.dll,-1</span></span>
-   <span data-ttu-id="cdf72-584">**Pagine**</span><span class="sxs-lookup"><span data-stu-id="cdf72-584">**Pages**</span></span>

    | <span data-ttu-id="cdf72-585">Nome pagina</span><span class="sxs-lookup"><span data-stu-id="cdf72-585">Page Name</span></span>         | <span data-ttu-id="cdf72-586">Opens</span><span class="sxs-lookup"><span data-stu-id="cdf72-586">Opens</span></span>               |
    |-------------------|---------------------|
    | <span data-ttu-id="cdf72-587">pageSettings</span><span class="sxs-lookup"><span data-stu-id="cdf72-587">pageSettings</span></span>      | <span data-ttu-id="cdf72-588">Cambia impostazioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-588">Change settings</span></span>     |
    | <span data-ttu-id="cdf72-589">pageUpdateHistory</span><span class="sxs-lookup"><span data-stu-id="cdf72-589">pageUpdateHistory</span></span> | <span data-ttu-id="cdf72-590">Visualizza cronologia aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="cdf72-590">View update history</span></span> |

    

     

### <a name="work-folders"></a><span data-ttu-id="cdf72-591">Cartelle di lavoro</span><span class="sxs-lookup"><span data-stu-id="cdf72-591">Work Folders</span></span>

-   <span data-ttu-id="cdf72-592">**Nome canonico**: Microsoft. cartellelavoro</span><span class="sxs-lookup"><span data-stu-id="cdf72-592">**Canonical name**: Microsoft.WorkFolders</span></span>
-   <span data-ttu-id="cdf72-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span><span class="sxs-lookup"><span data-stu-id="cdf72-593">**GUID**: {ECDB0924-4208-451E-8EE0-373C0956DE16}</span></span>
-   <span data-ttu-id="cdf72-594">**Sistema operativo supportato**: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cdf72-594">**Supported OS**: Windows 8.1</span></span>
-   <span data-ttu-id="cdf72-595">**Nome del modulo**: @C: \\ Windows \\ system32 \\WorkfoldersControl.dll,-1</span><span class="sxs-lookup"><span data-stu-id="cdf72-595">**Module name**: @C:\\Windows\\System32\\WorkfoldersControl.dll,-1</span></span>

## <a name="deprecated-control-panel-canonical-names"></a><span data-ttu-id="cdf72-596">Nomi canonici del pannello di controllo deprecati</span><span class="sxs-lookup"><span data-stu-id="cdf72-596">Deprecated Control Panel Canonical Names</span></span>

<span data-ttu-id="cdf72-597">Di seguito sono riportati nomi canonici che non sono più in uso a partire da Windows 8.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="cdf72-597">The following are canonical names that are no longer in use as of Windows 8.1 or later.</span></span> <span data-ttu-id="cdf72-598">Alcune sono state rimosse completamente.</span><span class="sxs-lookup"><span data-stu-id="cdf72-598">Some have been removed altogether.</span></span> <span data-ttu-id="cdf72-599">Altre sono state rimappate in queste situazioni:</span><span class="sxs-lookup"><span data-stu-id="cdf72-599">Others have been remapped in these situations:</span></span>

-   <span data-ttu-id="cdf72-600">Un elemento del pannello di controllo è stato rinominato.</span><span class="sxs-lookup"><span data-stu-id="cdf72-600">A Control Panel item is renamed.</span></span> <span data-ttu-id="cdf72-601">All'elemento rinominato viene assegnato un nuovo nome canonico ma viene mantenuto lo stesso GUID.</span><span class="sxs-lookup"><span data-stu-id="cdf72-601">The renamed item is given a new canonical name but keeps the same GUID.</span></span> <span data-ttu-id="cdf72-602">In questo caso, il vecchio nome canonico avvia l'elemento del pannello di controllo rinominato.</span><span class="sxs-lookup"><span data-stu-id="cdf72-602">In this case, the old canonical name launches the renamed Control Panel item.</span></span> <span data-ttu-id="cdf72-603">Tenere presente che l'elemento avviato potrebbe non utilizzare la stessa interfaccia utente della versione precedente di tale elemento.</span><span class="sxs-lookup"><span data-stu-id="cdf72-603">Be aware that the item that's launched might not use the same UI as that item's older version.</span></span>
-   <span data-ttu-id="cdf72-604">La funzionalità di uno o più elementi del pannello di controllo viene spostata o consolidata in un nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="cdf72-604">The functionality of one or more Control Panel items is moved or consolidated into a new item.</span></span> <span data-ttu-id="cdf72-605">In questo caso, il nome canonico precedente esegue il mapping al nuovo elemento del pannello di controllo più appropriato.</span><span class="sxs-lookup"><span data-stu-id="cdf72-605">In this case, the old canonical name maps to the most appropriate new Control Panel item.</span></span>

> [!Note]  
> <span data-ttu-id="cdf72-606">Sono disponibili nuovi mapping per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="cdf72-606">Remappings exist for backward compatibility.</span></span> <span data-ttu-id="cdf72-607">Non usare valori deprecati nel nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="cdf72-607">You should not use deprecated values in new code.</span></span>

 



| <span data-ttu-id="cdf72-608">Nome canonico deprecato</span><span class="sxs-lookup"><span data-stu-id="cdf72-608">Deprecated canonical name</span></span>                                   | <span data-ttu-id="cdf72-609">Elemento del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-609">Control Panel Item</span></span>                | <span data-ttu-id="cdf72-610">GUID</span><span class="sxs-lookup"><span data-stu-id="cdf72-610">GUID</span></span>                                   | <span data-ttu-id="cdf72-611">Note</span><span class="sxs-lookup"><span data-stu-id="cdf72-611">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdf72-612">Microsoft. AddHardware</span><span class="sxs-lookup"><span data-stu-id="cdf72-612">Microsoft.AddHardware</span></span>                                       | <span data-ttu-id="cdf72-613">Aggiungi hardware</span><span class="sxs-lookup"><span data-stu-id="cdf72-613">Add Hardware</span></span>                      | <span data-ttu-id="cdf72-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span><span class="sxs-lookup"><span data-stu-id="cdf72-614">{7A979262-40CE-46ff-AEEE-7884AC3B6136}</span></span> | <span data-ttu-id="cdf72-615">Esegue il mapping a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-615">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cdf72-616">Microsoft. AudioDevicesAndSoundThemes</span><span class="sxs-lookup"><span data-stu-id="cdf72-616">Microsoft.AudioDevicesAndSoundThemes</span></span>                        | <span data-ttu-id="cdf72-617">Suoni</span><span class="sxs-lookup"><span data-stu-id="cdf72-617">Sound</span></span>                             | <span data-ttu-id="cdf72-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-618">{F2DDFC82-8F12-4CDD-B7DC-D4FE1425AA4D}</span></span> | <span data-ttu-id="cdf72-619">Esegue il mapping a [Microsoft. Sound](#sound) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-619">Maps to [Microsoft.Sound](#sound) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="cdf72-620">Microsoft. BackupAndRestoreCenter/Microsoft. BackupAndRestore</span><span class="sxs-lookup"><span data-stu-id="cdf72-620">Microsoft.BackupAndRestoreCenter/Microsoft.BackupAndRestore</span></span> | <span data-ttu-id="cdf72-621">Centro di backup e ripristino</span><span class="sxs-lookup"><span data-stu-id="cdf72-621">Backup and Restore Center</span></span>         | <span data-ttu-id="cdf72-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span><span class="sxs-lookup"><span data-stu-id="cdf72-622">{B98A2BEA-7D42-4558-8BD1-832F41BAC6FD}</span></span> | <span data-ttu-id="cdf72-623">Microsoft. BackupAndRestoreCenter esegue il mapping a Microsoft. BackupAndRestore in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-623">Microsoft.BackupAndRestoreCenter maps to Microsoft.BackupAndRestore in Windows 7.</span></span> <span data-ttu-id="cdf72-624">Entrambi vengono rimossi a partire da Windows 8. in alternativa, utilizzare [Microsoft. filehistory](#file-history) .</span><span class="sxs-lookup"><span data-stu-id="cdf72-624">Both are removed as of Windows 8; use [Microsoft.FileHistory](#file-history) instead.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="cdf72-625">Microsoft. CardSpace</span><span class="sxs-lookup"><span data-stu-id="cdf72-625">Microsoft.CardSpace</span></span>                                         | <span data-ttu-id="cdf72-626">Windows CardSpace</span><span class="sxs-lookup"><span data-stu-id="cdf72-626">Windows CardSpace</span></span>                 | <span data-ttu-id="cdf72-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span><span class="sxs-lookup"><span data-stu-id="cdf72-627">{78CB147A-98EA-4AA6-B0DF-C8681F69341C}</span></span> | <span data-ttu-id="cdf72-628">Rimosso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-628">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cdf72-629">Microsoft. DesktopGadgets</span><span class="sxs-lookup"><span data-stu-id="cdf72-629">Microsoft.DesktopGadgets</span></span>                                    | <span data-ttu-id="cdf72-630">Gadget desktop</span><span class="sxs-lookup"><span data-stu-id="cdf72-630">Desktop Gadgets</span></span>                   | <span data-ttu-id="cdf72-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="cdf72-631">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="cdf72-632">Rimosso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-632">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cdf72-633">Microsoft. GetProgramsOnline</span><span class="sxs-lookup"><span data-stu-id="cdf72-633">Microsoft.GetProgramsOnline</span></span>                                 | <span data-ttu-id="cdf72-634">Windows Marketplace</span><span class="sxs-lookup"><span data-stu-id="cdf72-634">Windows Marketplace</span></span>               | <span data-ttu-id="cdf72-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span><span class="sxs-lookup"><span data-stu-id="cdf72-635">{3e7efb4c-faf1-453d-89eb-56026875ef90}</span></span> | <span data-ttu-id="cdf72-636">Rimosso a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-636">Removed as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cdf72-637">Microsoft. InfraredOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-637">Microsoft.InfraredOptions</span></span>                                   | <span data-ttu-id="cdf72-638">Infrarossi</span><span class="sxs-lookup"><span data-stu-id="cdf72-638">Infrared</span></span>                          | <span data-ttu-id="cdf72-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span><span class="sxs-lookup"><span data-stu-id="cdf72-639">{A0275511-0E86-4ECA-97C2-ECD8F1221D08}</span></span> | <span data-ttu-id="cdf72-640">Esegue il mapping a [Microsoft. Infrared](#infrared) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-640">Maps to [Microsoft.Infrared](#infrared) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cdf72-641">Microsoft. Language</span><span class="sxs-lookup"><span data-stu-id="cdf72-641">Microsoft.Language</span></span>                                          | <span data-ttu-id="cdf72-642">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="cdf72-642">Language</span></span>                          | <span data-ttu-id="cdf72-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span><span class="sxs-lookup"><span data-stu-id="cdf72-643">{BF782CC9-5A52-4A17-806C-2A894FFEEAC5}</span></span> | <span data-ttu-id="cdf72-644">Rimosso a partire da Windows 10, versione 1803</span><span class="sxs-lookup"><span data-stu-id="cdf72-644">Removed as of Windows 10, version 1803</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cdf72-645">Microsoft. LocationAndOtherSensors</span><span class="sxs-lookup"><span data-stu-id="cdf72-645">Microsoft.LocationAndOtherSensors</span></span>                           | <span data-ttu-id="cdf72-646">Posizione e altri sensori</span><span class="sxs-lookup"><span data-stu-id="cdf72-646">Location and Other Sensors</span></span>        | <span data-ttu-id="cdf72-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-647">{E9950154-C418-419e-A90A-20C5287AE24B}</span></span> | <span data-ttu-id="cdf72-648">Esegue il mapping a [Microsoft. LocationSettings](#infrared) a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-648">Maps to [Microsoft.LocationSettings](#infrared) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cdf72-649">Microsoft. PenAndInputDevices</span><span class="sxs-lookup"><span data-stu-id="cdf72-649">Microsoft.PenAndInputDevices</span></span>                                | <span data-ttu-id="cdf72-650">Dispositivi di input e penna</span><span class="sxs-lookup"><span data-stu-id="cdf72-650">Pen and Input Devices</span></span>             | <span data-ttu-id="cdf72-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-651">{F82DF8F7-8B9F-442E-A48C-818EA735FF9B}</span></span> | <span data-ttu-id="cdf72-652">Esegue il mapping a [Microsoft. PenAndTouch](#pen-and-touch) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-652">Maps to [Microsoft.PenAndTouch](#pen-and-touch) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cdf72-653">Microsoft. PeopleNearMe</span><span class="sxs-lookup"><span data-stu-id="cdf72-653">Microsoft.PeopleNearMe</span></span>                                      | <span data-ttu-id="cdf72-654">Persone nelle vicinanze</span><span class="sxs-lookup"><span data-stu-id="cdf72-654">People Near Me</span></span>                    | <span data-ttu-id="cdf72-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span><span class="sxs-lookup"><span data-stu-id="cdf72-655">{5224F545-A443-4859-BA23-7B5A95BDC8EF}</span></span> | <span data-ttu-id="cdf72-656">Rimosso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-656">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="cdf72-657">Microsoft. PerformanceInformationAndTools</span><span class="sxs-lookup"><span data-stu-id="cdf72-657">Microsoft.PerformanceInformationAndTools</span></span>                    | <span data-ttu-id="cdf72-658">Strumenti e informazioni sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-658">Performance Information and Tools</span></span> | <span data-ttu-id="cdf72-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span><span class="sxs-lookup"><span data-stu-id="cdf72-659">{78F3955E-3B90-4184-BD14-5397C15F1EFC}</span></span> | <span data-ttu-id="cdf72-660">Rimosso a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="cdf72-660">Removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="cdf72-661">Microsoft. PhoneAndModemOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-661">Microsoft.PhoneAndModemOptions</span></span>                              | <span data-ttu-id="cdf72-662">Telefono e modem</span><span class="sxs-lookup"><span data-stu-id="cdf72-662">Phone and Modem</span></span>                   | <span data-ttu-id="cdf72-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-663">{40419485-C444-4567-851A-2DD7BFA1684D}</span></span> | <span data-ttu-id="cdf72-664">Esegue il mapping a [Microsoft. PhoneAndModem](#phone-and-modem) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-664">Maps to [Microsoft.PhoneAndModem](#phone-and-modem) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cdf72-665">Microsoft. stampanti</span><span class="sxs-lookup"><span data-stu-id="cdf72-665">Microsoft.Printers</span></span>                                          | <span data-ttu-id="cdf72-666">Stampanti</span><span class="sxs-lookup"><span data-stu-id="cdf72-666">Printers</span></span>                          | <span data-ttu-id="cdf72-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span><span class="sxs-lookup"><span data-stu-id="cdf72-667">{2227A280-3AEA-1069-A2DE-08002B30309D}</span></span> | <span data-ttu-id="cdf72-668">Esegue il mapping a [Microsoft. DevicesAndPrinters](#devices-and-printers) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-668">Maps to [Microsoft.DevicesAndPrinters](#devices-and-printers) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cdf72-669">Microsoft. ProblemReportsAndSolutions</span><span class="sxs-lookup"><span data-stu-id="cdf72-669">Microsoft.ProblemReportsAndSolutions</span></span>                        | <span data-ttu-id="cdf72-670">Segnalazioni di problemi e soluzioni</span><span class="sxs-lookup"><span data-stu-id="cdf72-670">Problem Reports and Solutions</span></span>     | <span data-ttu-id="cdf72-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span><span class="sxs-lookup"><span data-stu-id="cdf72-671">{FCFEECAE-EE1B-4849-AE50-685DCF7717EC}</span></span> | <span data-ttu-id="cdf72-672">Esegue il mapping a [Microsoft. ActionCenter](#action-center) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-672">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cdf72-673">Microsoft. RegionalAndLanguageOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-673">Microsoft.RegionalAndLanguageOptions</span></span>                        | <span data-ttu-id="cdf72-674">Opzioni internazionali e della lingua</span><span class="sxs-lookup"><span data-stu-id="cdf72-674">Regional and Language Options</span></span>     | <span data-ttu-id="cdf72-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span><span class="sxs-lookup"><span data-stu-id="cdf72-675">{62D8ED13-C9D0-4CE8-A914-47DD628FB1B0}</span></span> | <span data-ttu-id="cdf72-676">Esegue il mapping a [Microsoft. RegionAndLanguage](#region) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-676">Maps to [Microsoft.RegionAndLanguage](#region) as of Windows 7.</span></span> <span data-ttu-id="cdf72-677">Si noti che a partire da Windows 8, Region e Language sono stati assegnati a ogni elemento del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-677">Note that as of Windows 8, Region and Language were each given their own Control Panel item.</span></span> <span data-ttu-id="cdf72-678">Microsoft. RegionalAndLanguageOptions e Microsoft. RegionAndLanguage Attualmente aprono l'elemento Region.</span><span class="sxs-lookup"><span data-stu-id="cdf72-678">Both Microsoft.RegionalAndLanguageOptions and Microsoft.RegionAndLanguage currently open the Region item.</span></span> <span data-ttu-id="cdf72-679">Per accedere all'elemento del linguaggio, è necessario utilizzare [Microsoft. Language](#location-settings) .</span><span class="sxs-lookup"><span data-stu-id="cdf72-679">You must use [Microsoft.Language](#location-settings) to access the Language item.</span></span> |
| <span data-ttu-id="cdf72-680">Microsoft. SecurityCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-680">Microsoft.SecurityCenter</span></span>                                    | <span data-ttu-id="cdf72-681">Centro sicurezza Windows</span><span class="sxs-lookup"><span data-stu-id="cdf72-681">Windows Security Center</span></span>           | <span data-ttu-id="cdf72-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span><span class="sxs-lookup"><span data-stu-id="cdf72-682">{087DA31B-0DD3-4537-8E23-64A18591F88B}</span></span> | <span data-ttu-id="cdf72-683">Esegue il mapping a [Microsoft. ActionCenter](#action-center) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-683">Maps to [Microsoft.ActionCenter](#action-center) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cdf72-684">Microsoft. SpeechRecognitionOptions</span><span class="sxs-lookup"><span data-stu-id="cdf72-684">Microsoft.SpeechRecognitionOptions</span></span>                          | <span data-ttu-id="cdf72-685">Opzioni di riconoscimento vocale</span><span class="sxs-lookup"><span data-stu-id="cdf72-685">Speech Recognition Options</span></span>        | <span data-ttu-id="cdf72-686">{58E3C745-D971-4081-9034-86E34B30836A}</span><span class="sxs-lookup"><span data-stu-id="cdf72-686">{58E3C745-D971-4081-9034-86E34B30836A}</span></span> | <span data-ttu-id="cdf72-687">Esegue il mapping a [Microsoft. sintesi vocale](#speech-recognition) a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-687">Maps to [Microsoft.SpeechRecognition](#speech-recognition) as of Windows 7.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="cdf72-688">Microsoft. TaskbarAndStartMenu</span><span class="sxs-lookup"><span data-stu-id="cdf72-688">Microsoft.TaskbarAndStartMenu</span></span>                               | <span data-ttu-id="cdf72-689">Barra delle applicazioni e menu Start</span><span class="sxs-lookup"><span data-stu-id="cdf72-689">Taskbar and Start Menu</span></span>            | <span data-ttu-id="cdf72-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span><span class="sxs-lookup"><span data-stu-id="cdf72-690">{0DF44EAA-FF21-4412-828E-260A8728E7F1}</span></span> | <span data-ttu-id="cdf72-691">Esegue il mapping a [Microsoft. Taskbar](#speech-recognition) a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-691">Maps to [Microsoft.Taskbar](#speech-recognition) as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cdf72-692">Microsoft. WelcomeCenter</span><span class="sxs-lookup"><span data-stu-id="cdf72-692">Microsoft.WelcomeCenter</span></span>                                     | <span data-ttu-id="cdf72-693">Centro di benvenuto</span><span class="sxs-lookup"><span data-stu-id="cdf72-693">Welcome Center</span></span>                    | <span data-ttu-id="cdf72-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span><span class="sxs-lookup"><span data-stu-id="cdf72-694">{CB1B7F8C-C50A-4176-B604-9E24DEE8D4D1}</span></span> | <span data-ttu-id="cdf72-695">Esegue il mapping a Microsoft. GettingStarted in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-695">Maps to Microsoft.GettingStarted in Windows 7.</span></span> <span data-ttu-id="cdf72-696">Avvia il pannello di controllo home page a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-696">Launches the Control Panel home page as of Windows 8.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cdf72-697">Microsoft. WindowsSidebarProperties</span><span class="sxs-lookup"><span data-stu-id="cdf72-697">Microsoft.WindowsSidebarProperties</span></span>                          | <span data-ttu-id="cdf72-698">Proprietà sidebar di Windows</span><span class="sxs-lookup"><span data-stu-id="cdf72-698">Windows Sidebar Properties</span></span>        | <span data-ttu-id="cdf72-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span><span class="sxs-lookup"><span data-stu-id="cdf72-699">{37efd44d-ef8d-41b1-940d-96973a50e9e0}</span></span> | <span data-ttu-id="cdf72-700">Esegue il mapping a Microsoft. DesktopGadgets in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdf72-700">Maps to Microsoft.DesktopGadgets in Windows 7.</span></span> <span data-ttu-id="cdf72-701">Rimosso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdf72-701">Removed as of Windows 8.</span></span>                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cdf72-702">Microsoft. WindowsSideShow</span><span class="sxs-lookup"><span data-stu-id="cdf72-702">Microsoft.WindowsSideShow</span></span>                                   | <span data-ttu-id="cdf72-703">Windows SideShow</span><span class="sxs-lookup"><span data-stu-id="cdf72-703">Windows SideShow</span></span>                  | <span data-ttu-id="cdf72-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span><span class="sxs-lookup"><span data-stu-id="cdf72-704">{E95A4861-D57A-4be1-AD0F-35267E261739}</span></span> | <span data-ttu-id="cdf72-705">Funzionalità deprecata in Windows 8, rimossa a partire da Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="cdf72-705">Feature deprecated in Windows 8, removed as of Windows 8.1.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="using-canonical-names-in-local-group-policy"></a><span data-ttu-id="cdf72-706">Uso di nomi canonici in Criteri di gruppo locali</span><span class="sxs-lookup"><span data-stu-id="cdf72-706">Using Canonical Names in Local Group Policy</span></span>

<span data-ttu-id="cdf72-707">A partire da Windows 7, è possibile usare i nomi canonici per limitare l'accesso ai singoli elementi del pannello di controllo tramite criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-707">As of Windows 7, you can use canonical names to restrict access to individual Control Panel items through group policy.</span></span> <span data-ttu-id="cdf72-708">Questa stessa procedura può essere utilizzata in Windows Vista, ma è necessario utilizzare il nome del modulo anziché il nome canonico.</span><span class="sxs-lookup"><span data-stu-id="cdf72-708">This same procedure can be used in Windows Vista, but you have to use the module name instead of the canonical name.</span></span>

### <a name="hiding-individual-control-panel-items"></a><span data-ttu-id="cdf72-709">Nascondere singoli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-709">Hiding individual Control Panel items</span></span>

<span data-ttu-id="cdf72-710">Utilizzare questo metodo se si desidera visualizzare più elementi del pannello di controllo che si desidera nascondere.</span><span class="sxs-lookup"><span data-stu-id="cdf72-710">Use this method if you want to show more Control Panel items than you want to hide.</span></span>

1.  <span data-ttu-id="cdf72-711">Eseguire il file gpedit. msc per avviare il Editor Criteri di gruppo locali.</span><span class="sxs-lookup"><span data-stu-id="cdf72-711">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="cdf72-712">È anche possibile digitare "criteri di gruppo" nella schermata Start Windows 8.1 e selezionare **modifica criteri di gruppo** nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cdf72-712">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="cdf72-713">Selezionare **Configurazione utente**  >  **modelli amministrativi**  >  **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-713">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="cdf72-714">Selezionare **Nascondi elementi specificati del pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-714">Select **Hide specified Control Panel items**.</span></span>
4.  <span data-ttu-id="cdf72-715">Nella finestra **Nascondi elementi del pannello di controllo specificati** visualizzata fare clic su **abilitato**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-715">In the **Hide Specified Control Panel Items** window that opens, click **Enabled**.</span></span>
5.  <span data-ttu-id="cdf72-716">Fare clic sul pulsante **Mostra** nel pannello opzioni per visualizzare l'elenco degli elementi del pannello di controllo non consentiti.</span><span class="sxs-lookup"><span data-stu-id="cdf72-716">Click the **Show** button in the Options panel to show the list of disallowed Control Panel items.</span></span>
6.  <span data-ttu-id="cdf72-717">Nella finestra **Mostra contenuto** visualizzata digitare un nome canonico nella colonna **valore** .</span><span class="sxs-lookup"><span data-stu-id="cdf72-717">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="cdf72-718">Ripetere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cdf72-718">Repeat as necessary.</span></span>
7.  <span data-ttu-id="cdf72-719">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-719">Click **OK**.</span></span>

### <a name="showing-individual-control-panel-items"></a><span data-ttu-id="cdf72-720">Visualizzazione di singoli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-720">Showing individual Control Panel items</span></span>

<span data-ttu-id="cdf72-721">Utilizzare questo metodo se si desidera nascondere più elementi del pannello di controllo che si desidera visualizzare.</span><span class="sxs-lookup"><span data-stu-id="cdf72-721">Use this method if you want to hide more Control Panel items than you want to show.</span></span>

1.  <span data-ttu-id="cdf72-722">Eseguire il file gpedit. msc per avviare il Editor Criteri di gruppo locali.</span><span class="sxs-lookup"><span data-stu-id="cdf72-722">Run the Gpedit.msc file to launch the Local Group Policy Editor.</span></span> <span data-ttu-id="cdf72-723">È anche possibile digitare "criteri di gruppo" nella schermata Start Windows 8.1 e selezionare **modifica criteri di gruppo** nei risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="cdf72-723">You can also type "group policy" at the Windows 8.1 Start screen and select **Edit group policy** from the search results.</span></span>
2.  <span data-ttu-id="cdf72-724">Selezionare **Configurazione utente**  >  **modelli amministrativi**  >  **Pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-724">Select **User Configuration** > **Administrative Templates** > **Control Panel**.</span></span>
3.  <span data-ttu-id="cdf72-725">Selezionare **Mostra solo elementi specificati del pannello di controllo**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-725">Select **Show only specified Control Panel items**.</span></span>
4.  <span data-ttu-id="cdf72-726">Nella finestra **Mostra solo elementi del pannello di controllo specificati** visualizzata fare clic su **abilitato**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-726">In the **Show Only Specified Control Panel Items** window that opens, click **Enabled**.</span></span> <span data-ttu-id="cdf72-727">Questa operazione nasconde tutti gli elementi nel pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="cdf72-727">This hides everything in the Control Panel.</span></span>
5.  <span data-ttu-id="cdf72-728">Fare clic sul pulsante **Mostra** nel pannello opzioni per visualizzare l'elenco degli elementi del pannello di controllo consentiti.</span><span class="sxs-lookup"><span data-stu-id="cdf72-728">Click the **Show** button in the Options panel to show the list of allowed Control Panel items.</span></span>
6.  <span data-ttu-id="cdf72-729">Nella finestra **Mostra contenuto** visualizzata digitare un nome canonico nella colonna **valore** .</span><span class="sxs-lookup"><span data-stu-id="cdf72-729">In the **Show Contents** window that opens, type a canonical name into the **Value** column.</span></span> <span data-ttu-id="cdf72-730">Ripetere la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cdf72-730">Repeat as necessary.</span></span>
7.  <span data-ttu-id="cdf72-731">Fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-731">Click **OK**.</span></span>

<span data-ttu-id="cdf72-732">Se si desidera rimuovere tutte le voci aggiunte a un elenco Mostra o Nascondi elementi del pannello di controllo, tornare alla schermata nel passaggio 4 e selezionare **non configurato** per cancellare l'elenco.</span><span class="sxs-lookup"><span data-stu-id="cdf72-732">If you want to remove all of the entries that you've added to a Show or Hide Control Panel items list, return to the screen in step 4 and select **Not Configured** to clear the list.</span></span> <span data-ttu-id="cdf72-733">Se si desidera mantenere le voci ma sospendere le restrizioni, selezionare **disabilitato**.</span><span class="sxs-lookup"><span data-stu-id="cdf72-733">If you want to retain your entries but suspend the restrictions, select **Disabled**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdf72-734">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdf72-734">Remarks</span></span>

<span data-ttu-id="cdf72-735">È possibile visualizzare gli elementi nel pannello di controllo che non sono elencati qui.</span><span class="sxs-lookup"><span data-stu-id="cdf72-735">You might see items in your Control Panel that are not listed here.</span></span> <span data-ttu-id="cdf72-736">Tali elementi non fanno parte di Windows, ma vengono invece aggiunti durante l'installazione di diversi software e hardware, ad esempio Microsoft Office o una scheda video.</span><span class="sxs-lookup"><span data-stu-id="cdf72-736">Those items are not part of Windows, but instead are added during the installation of various software and hardware, such as Microsoft Office or a video card.</span></span> <span data-ttu-id="cdf72-737">Gli elementi del pannello di controllo non Windows possono avere o meno un nome canonico.</span><span class="sxs-lookup"><span data-stu-id="cdf72-737">Non-Windows Control Panel items may or may not have a canonical name.</span></span> <span data-ttu-id="cdf72-738">Per trovare il nome canonico di un elemento del pannello di controllo non elencato qui, cercare nel registro di sistema nei percorsi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cdf72-738">To find the canonical name of a Control Panel item not listed here, look in the registry under these paths:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {CLSID of the Control Panel item}
         System.ApplicationName
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         CLSID
            {CLSID of the Control Panel item}
               System.ApplicationName
```

<span data-ttu-id="cdf72-739">Per ulteriori informazioni che consentono di individuare i CLSID necessari, vedere [come registrare gli elementi del pannello di controllo eseguibile](how-to-register-an-executable-control-panel-item-registration-.md) e [come registrare gli elementi del pannello di controllo dll](how-to-register-dll-control-panel-item-registration-.md).</span><span class="sxs-lookup"><span data-stu-id="cdf72-739">For more information that can help you discover the necessary CLSIDs, see [How to Register Executable Control Panel Items](how-to-register-an-executable-control-panel-item-registration-.md) and [How to Register DLL Control Panel Items](how-to-register-dll-control-panel-item-registration-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdf72-740">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cdf72-740">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdf72-741">Esecuzione degli elementi del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="cdf72-741">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="cdf72-742">**IOpenControlPanel**</span><span class="sxs-lookup"><span data-stu-id="cdf72-742">**IOpenControlPanel**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iopencontrolpanel)
</dt> </dl>

 

 



