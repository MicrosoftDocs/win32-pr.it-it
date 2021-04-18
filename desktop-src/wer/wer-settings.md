---
title: Impostazioni di Segnalazione errori Windows
description: Impostazioni per personalizzare l'esperienza di segnalazione dei problemi. Tutte queste impostazioni possono essere impostate utilizzando Criteri di gruppo. Alcuni possono anche essere modificati in centro operativo per Windows 7 e Windows 8. Per Windows 10, utilizzare la funzione di ricerca in impostazioni per individuare Visualizza impostazioni di sistema avanzate.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Segnalazione errori Windows segnalazione errori Windows, impostazioni
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/13/2021
ms.locfileid: "106322047"
---
# <a name="wer-settings"></a><span data-ttu-id="fea57-107">Impostazioni di Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="fea57-107">WER Settings</span></span>

<span data-ttu-id="fea57-108">Segnalazione errori Windows (WER) fornisce molte impostazioni per personalizzare l'esperienza di segnalazione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="fea57-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="fea57-109">Tutte queste impostazioni possono essere impostate utilizzando Criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="fea57-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="fea57-110">Alcuni possono anche essere modificati in **centro operativo** per Windows 7 e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fea57-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="fea57-111">Per Windows 10, utilizzare la funzione di ricerca in impostazioni per individuare **Visualizza impostazioni di sistema avanzate**.</span><span class="sxs-lookup"><span data-stu-id="fea57-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="fea57-112">Le impostazioni WER si trovano in una delle sottochiavi del registro di sistema seguenti:</span><span class="sxs-lookup"><span data-stu-id="fea57-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="fea57-113">**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **segnalazione errori Windows**</span><span class="sxs-lookup"><span data-stu-id="fea57-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="fea57-114">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **segnalazione errori Windows**</span><span class="sxs-lookup"><span data-stu-id="fea57-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="fea57-115">Sottochiave Segnalazione errori Windows</span><span class="sxs-lookup"><span data-stu-id="fea57-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="fea57-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span><span class="sxs-lookup"><span data-stu-id="fea57-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-117">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-117">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-118">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="fea57-119">0-Disabilita la limitazione dei dati ignorata.</span><span class="sxs-lookup"><span data-stu-id="fea57-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="fea57-120">Se il bypass è disabilitato o non è configurato come impostazione di criteri, WER limita i dati per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fea57-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="fea57-121">WER non carica più di un file CAB per un report che contiene dati sugli stessi tipi di evento.</span><span class="sxs-lookup"><span data-stu-id="fea57-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="fea57-122">1-abilitare la limitazione dei dati bypass.</span><span class="sxs-lookup"><span data-stu-id="fea57-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="fea57-123">WER non limita i dati.</span><span class="sxs-lookup"><span data-stu-id="fea57-123">WER does not throttle data.</span></span> <span data-ttu-id="fea57-124">WER carica i file CAB aggiuntivi che possono contenere dati sugli stessi tipi di evento di un report caricato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="fea57-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="fea57-125">Indica se abilitare il bypass della limitazione dei dati del client WER</span><span class="sxs-lookup"><span data-stu-id="fea57-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="fea57-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span><span class="sxs-lookup"><span data-stu-id="fea57-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-127">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-127">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-128">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-128">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-129">1-solo parametri (impostazione predefinita in Windows 7)</span><span class="sxs-lookup"><span data-stu-id="fea57-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="fea57-130">2-tutti i dati (impostazione predefinita in Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="fea57-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="fea57-131">Indica se archiviare solo i parametri o tutti i dati</span><span class="sxs-lookup"><span data-stu-id="fea57-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="fea57-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consenso \\ DefaultConsent**</span><span class="sxs-lookup"><span data-stu-id="fea57-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-133">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-133">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-134">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-134">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-135">1-Richiedi sempre (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="fea57-136">2-solo parametri</span><span class="sxs-lookup"><span data-stu-id="fea57-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="fea57-137">3-parametri e dati sicuri</span><span class="sxs-lookup"><span data-stu-id="fea57-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="fea57-138">4-tutti i dati</span><span class="sxs-lookup"><span data-stu-id="fea57-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="fea57-139">Scelta di consenso predefinita</span><span class="sxs-lookup"><span data-stu-id="fea57-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="fea57-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consenso \\ DefaultOverrideBehavior**</span><span class="sxs-lookup"><span data-stu-id="fea57-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-141">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-141">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-142">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-142">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-143">0: il consenso verticale sostituirà il consenso predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="fea57-144">1-il consenso predefinito sostituirà il consenso specifico dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="fea57-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="fea57-145">Indica se il consenso predefinito sostituisce il consenso verticale</span><span class="sxs-lookup"><span data-stu-id="fea57-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="fea57-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consenso \\ \[ verticale\]**</span><span class="sxs-lookup"><span data-stu-id="fea57-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-147">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-148">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-148">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-149">1-Richiedi sempre (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="fea57-150">2-solo parametri</span><span class="sxs-lookup"><span data-stu-id="fea57-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="fea57-151">3-parametri e dati sicuri</span><span class="sxs-lookup"><span data-stu-id="fea57-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="fea57-152">4-tutti i dati</span><span class="sxs-lookup"><span data-stu-id="fea57-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="fea57-153">Scelta di consenso per il plug-in WER</span><span class="sxs-lookup"><span data-stu-id="fea57-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="fea57-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span><span class="sxs-lookup"><span data-stu-id="fea57-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-155">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fea57-155">**REG\_SZ**</span></span>

<span data-ttu-id="fea57-156">Percorso della directory</span><span class="sxs-lookup"><span data-stu-id="fea57-156">The directory path</span></span>

<span data-ttu-id="fea57-157">Directory di destinazione nel server</span><span class="sxs-lookup"><span data-stu-id="fea57-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="fea57-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span><span class="sxs-lookup"><span data-stu-id="fea57-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-159">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-159">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-160">Numero di porta</span><span class="sxs-lookup"><span data-stu-id="fea57-160">The port number</span></span>

<span data-ttu-id="fea57-161">Numero di porta da utilizzare con il server aziendale</span><span class="sxs-lookup"><span data-stu-id="fea57-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="fea57-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span><span class="sxs-lookup"><span data-stu-id="fea57-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-163">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fea57-163">**REG\_SZ**</span></span>

<span data-ttu-id="fea57-164">Nome host del server.</span><span class="sxs-lookup"><span data-stu-id="fea57-164">The name of the server</span></span>

<span data-ttu-id="fea57-165">Nome del server aziendale</span><span class="sxs-lookup"><span data-stu-id="fea57-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="fea57-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span><span class="sxs-lookup"><span data-stu-id="fea57-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-167">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-167">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-168">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-168">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-169">0-No (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="fea57-170">1 - Sì</span><span class="sxs-lookup"><span data-stu-id="fea57-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="fea57-171">Indica se utilizzare l'autenticazione integrata di Windows</span><span class="sxs-lookup"><span data-stu-id="fea57-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="fea57-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span><span class="sxs-lookup"><span data-stu-id="fea57-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-173">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-173">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-174">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-174">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-175">0-No (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="fea57-176">1 - Sì</span><span class="sxs-lookup"><span data-stu-id="fea57-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="fea57-177">Indica se utilizzare SSL</span><span class="sxs-lookup"><span data-stu-id="fea57-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="fea57-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ exename \] (sostituire " \[ exename \] " con il nome effettivo di un file con estensione exe, ad esempio "notepad.exe")**</span><span class="sxs-lookup"><span data-stu-id="fea57-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-179">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-179">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-180">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="fea57-181">0: i processi con un nome di immagine eseguibile di **\[ exename \]** non richiedono all'utente di scegliere **debug** o **continua** (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="fea57-182">1-i processi con un nome di immagine eseguibile di **\[ exename \]** richiedono all'utente di scegliere **debug** o **continua**</span><span class="sxs-lookup"><span data-stu-id="fea57-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="fea57-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " è il nome del valore letterale)**</span><span class="sxs-lookup"><span data-stu-id="fea57-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-184">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-184">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-185">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="fea57-186">0: tutti i processi ad eccezione di quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ \] exename** non richiedono all'utente di scegliere **debug** o **continua** (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="fea57-187">1-tutti i processi ad eccezione di quelli specificati in modo esplicito nell'impostazione **DebugApplications \\ \[ \] exename** richiedono all'utente di scegliere **debug** o **continua**</span><span class="sxs-lookup"><span data-stu-id="fea57-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="fea57-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span><span class="sxs-lookup"><span data-stu-id="fea57-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-189">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-189">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-190">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-190">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-191">0 - Attivato</span><span class="sxs-lookup"><span data-stu-id="fea57-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="fea57-192">1 - Disattivato</span><span class="sxs-lookup"><span data-stu-id="fea57-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="fea57-193">Abilitare o disabilitare l'archivio</span><span class="sxs-lookup"><span data-stu-id="fea57-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="fea57-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato**</span><span class="sxs-lookup"><span data-stu-id="fea57-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-195">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-195">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-196">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-196">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-197">0: abilitato (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="fea57-198">1 - Disattivato</span><span class="sxs-lookup"><span data-stu-id="fea57-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="fea57-199">Abilitare o disabilitare WER</span><span class="sxs-lookup"><span data-stu-id="fea57-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="fea57-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span><span class="sxs-lookup"><span data-stu-id="fea57-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-201">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-201">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-202">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-202">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-203">0 - Attivato</span><span class="sxs-lookup"><span data-stu-id="fea57-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="fea57-204">1 - Disattivato</span><span class="sxs-lookup"><span data-stu-id="fea57-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="fea57-205">Abilitare o disabilitare l'accodamento di report</span><span class="sxs-lookup"><span data-stu-id="fea57-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="fea57-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="fea57-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-207">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-207">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-208">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-208">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-209">0-interfaccia utente (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="fea57-210">1: nessuna interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="fea57-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="fea57-211">Abilitare o disabilitare l'interfaccia utente di WER</span><span class="sxs-lookup"><span data-stu-id="fea57-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="fea57-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span><span class="sxs-lookup"><span data-stu-id="fea57-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-213">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-213">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-214">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-214">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-215">0-invia (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="fea57-216">1-non inviare</span><span class="sxs-lookup"><span data-stu-id="fea57-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="fea57-217">Indica se impedire l'invio di dati di secondo livello</span><span class="sxs-lookup"><span data-stu-id="fea57-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="fea57-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**\\ \[ Nome dell'applicazione ExcludedApplications\]**</span><span class="sxs-lookup"><span data-stu-id="fea57-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-219">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fea57-219">**REG\_SZ**</span></span>

<span data-ttu-id="fea57-220">Usare [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="fea57-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="fea57-221">Elenco di applicazioni escluse</span><span class="sxs-lookup"><span data-stu-id="fea57-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="fea57-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span><span class="sxs-lookup"><span data-stu-id="fea57-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-223">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-223">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-224">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-224">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-225">0-No (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="fea57-226">1 - Sì</span><span class="sxs-lookup"><span data-stu-id="fea57-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="fea57-227">Indica se inviare tutti i report alla coda dell'utente</span><span class="sxs-lookup"><span data-stu-id="fea57-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="fea57-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpFolder o LocalDumps DumpFolder**</span><span class="sxs-lookup"><span data-stu-id="fea57-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-229">**REG \_ Espandi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fea57-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="fea57-230">Percorso della directory.</span><span class="sxs-lookup"><span data-stu-id="fea57-230">The directory path.</span></span> <span data-ttu-id="fea57-231">Il valore predefinito è% LOCALAPPDATA% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="fea57-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="fea57-232">Se il valore predefinito non viene utilizzato, l'applicazione deve verificare che la cartella disponga di un ACL sufficiente.</span><span class="sxs-lookup"><span data-stu-id="fea57-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="fea57-233">**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="fea57-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="fea57-234">Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="fea57-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="fea57-235">Percorso in cui archiviare i file di dump.</span><span class="sxs-lookup"><span data-stu-id="fea57-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="fea57-236">Si noti che le impostazioni per processo sostituiranno le impostazioni globali esistenti per ulteriori informazioni, vedere [raccolta di dump di User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="fea57-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="fea57-237">Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fea57-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpCount o LocalDumps DumpCount**</span><span class="sxs-lookup"><span data-stu-id="fea57-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-239">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-239">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-240">Numero massimo.</span><span class="sxs-lookup"><span data-stu-id="fea57-240">The maximum number.</span></span> <span data-ttu-id="fea57-241">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="fea57-241">The default is 10.</span></span> <span data-ttu-id="fea57-242">Quando viene superato il valore massimo, il file di dump meno recente nella cartella verrà sostituito con il nuovo file di dump.</span><span class="sxs-lookup"><span data-stu-id="fea57-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="fea57-243">**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="fea57-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="fea57-244">Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="fea57-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="fea57-245">Numero massimo di file di dump nella cartella.</span><span class="sxs-lookup"><span data-stu-id="fea57-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="fea57-246">Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fea57-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ DumpType o LocalDumps DumpType**</span><span class="sxs-lookup"><span data-stu-id="fea57-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-248">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-248">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-249">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-249">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-250">0-dump personalizzato</span><span class="sxs-lookup"><span data-stu-id="fea57-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="fea57-251">1-minidump (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="fea57-252">2-dump completo</span><span class="sxs-lookup"><span data-stu-id="fea57-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="fea57-253">**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="fea57-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="fea57-254">Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="fea57-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="fea57-255">Tipo di dump.</span><span class="sxs-lookup"><span data-stu-id="fea57-255">The dump type.</span></span>

<span data-ttu-id="fea57-256">Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fea57-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\** **\\ \[ Nome dell'applicazione \] \\ CustomDumpFlags o LocalDumps CustomDumpFlags**</span><span class="sxs-lookup"><span data-stu-id="fea57-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-258">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-258">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-259">Uno o più valori dell'enumerazione [**del \_ tipo di MINIDUMP**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="fea57-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="fea57-260">Il valore predefinito è {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.</span><span class="sxs-lookup"><span data-stu-id="fea57-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="fea57-261">**Windows Vista:** I valori del registro di sistema nella chiave **LocalDumps** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="fea57-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="fea57-262">Si noti che questo comportamento è stato modificato con Windows Server 2008 e Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="fea57-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="fea57-263">Opzioni di dump personalizzate da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="fea57-263">The custom dump options to be used.</span></span> <span data-ttu-id="fea57-264">Questo valore viene utilizzato solo quando **DumpType** è impostato su 0.</span><span class="sxs-lookup"><span data-stu-id="fea57-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="fea57-265">Questa impostazione non è supportata nell'hive del registro di sistema **\_ \_ dell'utente corrente di HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fea57-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span><span class="sxs-lookup"><span data-stu-id="fea57-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-267">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-267">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-268">Valori possibili:</span><span class="sxs-lookup"><span data-stu-id="fea57-268">Possible values:</span></span><dl> <dd><span data-ttu-id="fea57-269">0: abilitato (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fea57-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="fea57-270">1: disabilitato</span><span class="sxs-lookup"><span data-stu-id="fea57-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="fea57-271">Abilitare o disabilitare la registrazione</span><span class="sxs-lookup"><span data-stu-id="fea57-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="fea57-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span><span class="sxs-lookup"><span data-stu-id="fea57-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-273">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-273">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-274">Intervallo di valori possibili: 1 – 5000.</span><span class="sxs-lookup"><span data-stu-id="fea57-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="fea57-275">Il valore predefinito è 1000.</span><span class="sxs-lookup"><span data-stu-id="fea57-275">The default is 1000.</span></span>

<span data-ttu-id="fea57-276">Dimensioni massime dell'archivio in file</span><span class="sxs-lookup"><span data-stu-id="fea57-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="fea57-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span><span class="sxs-lookup"><span data-stu-id="fea57-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-278">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-278">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-279">Intervallo di valori possibili: 1 – 500.</span><span class="sxs-lookup"><span data-stu-id="fea57-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="fea57-280">Il valore predefinito è 50.</span><span class="sxs-lookup"><span data-stu-id="fea57-280">The default is 50.</span></span>

<span data-ttu-id="fea57-281">Dimensioni massime della coda</span><span class="sxs-lookup"><span data-stu-id="fea57-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="fea57-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span><span class="sxs-lookup"><span data-stu-id="fea57-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-283">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-283">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-284">Numero di giorni</span><span class="sxs-lookup"><span data-stu-id="fea57-284">Number of days</span></span>

<span data-ttu-id="fea57-285">Intervallo tra i promemoria dell'utente per verificare la presenza di soluzioni, in giorni</span><span class="sxs-lookup"><span data-stu-id="fea57-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="fea57-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nome pwszOutOfProcessCallbackDll con percorso\]**</span><span class="sxs-lookup"><span data-stu-id="fea57-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-287">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-287">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-288">Il contenuto del valore viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="fea57-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="fea57-289">Il nome del valore viene usato per recuperare il valore pwszOutOfProcessCallbackDll.</span><span class="sxs-lookup"><span data-stu-id="fea57-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="fea57-290">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Il valore del registro di sistema non è supportato.</span><span class="sxs-lookup"><span data-stu-id="fea57-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="fea57-291">Impostazioni report del kernel Live di WER</span><span class="sxs-lookup"><span data-stu-id="fea57-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="fea57-292">Le impostazioni dei report del kernel Live di WER, descritte di seguito, si trovano entrambi nella sottochiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="fea57-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="fea57-293">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="fea57-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="fea57-294">Sottochiave FullLiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="fea57-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="fea57-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="fea57-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-296">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-296">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-297">Soglia (in ore) della frequenza con cui un singolo componente può creare un dump Live completo.</span><span class="sxs-lookup"><span data-stu-id="fea57-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="fea57-298">Questo valore deve essere maggiore o uguale a **SystemThrottleThreshold**.</span><span class="sxs-lookup"><span data-stu-id="fea57-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="fea57-299">Se si imposta su zero (0), tutte le limitazioni basate sul tempo vengono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="fea57-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="fea57-300">Il valore predefinito è 168 (7 giorni).</span><span class="sxs-lookup"><span data-stu-id="fea57-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="fea57-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span><span class="sxs-lookup"><span data-stu-id="fea57-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-302">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-302">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-303">Numero massimo di dump Live completi che possono trovarsi sul disco in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="fea57-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="fea57-304">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="fea57-304">The default is 1.</span></span> <span data-ttu-id="fea57-305">Se questo valore viene impostato su zero (0), la funzionalità di dump in tempo reale verrà disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fea57-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span><span class="sxs-lookup"><span data-stu-id="fea57-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-307">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-307">**REG\_QWORD**</span></span>

<span data-ttu-id="fea57-308">Oggetto [SYSTEMTIME](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) che indica l'ora dell'ultimo report live completo, per il sistema o un reportType specifico.</span><span class="sxs-lookup"><span data-stu-id="fea57-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="fea57-309">Viene usato per calcolare se una soglia dei criteri è stata soddisfatta.</span><span class="sxs-lookup"><span data-stu-id="fea57-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="fea57-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="fea57-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-311">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fea57-311">**REG\_DWORD**</span></span>

<span data-ttu-id="fea57-312">Soglia (in ore) della frequenza con cui un componente del sistema può creare un dump Live completo.</span><span class="sxs-lookup"><span data-stu-id="fea57-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="fea57-313">Il valore predefinito è 120 (5 giorni).</span><span class="sxs-lookup"><span data-stu-id="fea57-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="fea57-314">Sottochiave LiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="fea57-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="fea57-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span><span class="sxs-lookup"><span data-stu-id="fea57-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="fea57-316">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="fea57-316">**REG\_SZ**</span></span>


<span data-ttu-id="fea57-317">Percorso di archiviazione reindirizzato dei report del kernel attivo.</span><span class="sxs-lookup"><span data-stu-id="fea57-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="fea57-318">Il percorso predefinito è%systemroot%\LiveKernelReports.</span><span class="sxs-lookup"><span data-stu-id="fea57-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="fea57-319">Questo valore deve essere un percorso valido.</span><span class="sxs-lookup"><span data-stu-id="fea57-319">This value must be a valid path.</span></span> <span data-ttu-id="fea57-320">Il percorso deve essere in formato NT.</span><span class="sxs-lookup"><span data-stu-id="fea57-320">The path must be in NT path format.</span></span> <span data-ttu-id="fea57-321">Ad esempio, \? ? \c: \LiveDumpsFolder.</span><span class="sxs-lookup"><span data-stu-id="fea57-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="fea57-322">Per ulteriori informazioni sui formati di percorso, vedere  [formati di percorso dei file nei sistemi Windows](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="fea57-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="fea57-323">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fea57-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fea57-324">Riferimento a WER</span><span class="sxs-lookup"><span data-stu-id="fea57-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
