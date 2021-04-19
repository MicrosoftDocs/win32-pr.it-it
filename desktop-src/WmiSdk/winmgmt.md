---
description: WinMgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione nel &\# 0034; LocalSystem&\# 0034; account.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: winmgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318170"
---
# <a name="winmgmt"></a><span data-ttu-id="b3e4c-103">winmgmt</span><span class="sxs-lookup"><span data-stu-id="b3e4c-103">winmgmt</span></span>

<span data-ttu-id="b3e4c-104">WinMgmt è il servizio WMI all'interno del processo SVCHOST in esecuzione con l'account "LocalSystem".</span><span class="sxs-lookup"><span data-stu-id="b3e4c-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="b3e4c-105">In tutti i casi, il servizio WMI viene avviato automaticamente quando il primo script o un'applicazione di gestione richiede la connessione a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="b3e4c-106">Per altre informazioni, vedere [Avvio e arresto del servizio WMI](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="b3e4c-107">WMI è un componente fondamentale del sistema operativo Windows che consente agli sviluppatori e agli amministratori IT di scrivere script e applicazioni per automatizzare determinate attività.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="b3e4c-108">Winmgmt.exe è il servizio che consente l'esecuzione di WMI nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="b3e4c-109">Per ulteriori informazioni sull'utilizzo di WMI, vedere [utilizzo di WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="b3e4c-110">Se è stato ricevuto un messaggio di errore relativo winmgmt.exe, vedere la pagina relativa alla [risoluzione dei problemi di WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="b3e4c-111">Per ulteriori informazioni su Winmgmt.exe, vedere [utilizzo degli strumenti di gestione WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="b3e4c-112">Quando viene eseguito dal prompt dei comandi, il servizio WMI presenta le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="b3e4c-113">Commutatori</span><span class="sxs-lookup"><span data-stu-id="b3e4c-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="b3e4c-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="b3e4c-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e4c-115">Fa in modo che WMI Esegui il backup del repository nel nome file specificato.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="b3e4c-116">L'argomento *filename* deve contenere il percorso completo del percorso del file.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="b3e4c-117">Questo processo richiede un blocco di scrittura nel repository, in modo che le operazioni di scrittura nel repository vengano sospese fino al completamento del processo di backup.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="b3e4c-118">Se non si specifica un percorso per il file, questo viene inserito nella directory% windir% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/Restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="b3e4c-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e4c-120">Ripristina manualmente il repository WMI dal file di backup specificato.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="b3e4c-121">L'argomento *filename* deve contenere il percorso completo del percorso del file di backup.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="b3e4c-122">Per eseguire l'operazione di ripristino, WMI Salva il repository esistente per eseguire il writeback se l'operazione ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="b3e4c-123">Il repository viene quindi ripristinato dal file di backup specificato nell'argomento *filename* .</span><span class="sxs-lookup"><span data-stu-id="b3e4c-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="b3e4c-124">Se non è possibile ottenere l'accesso esclusivo al repository, i client esistenti vengono disconnessi da WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="b3e4c-125">Il *flag* argument deve essere 1 (Force Disconnect Users and Restore) o 0 (ripristino predefinito se nessun utente connesso) e specifica la modalità di ripristino.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<WinMgmt-Service-process-ID>*</span><span class="sxs-lookup"><span data-stu-id="b3e4c-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e4c-127">Registra le librerie di prestazioni del computer con WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="b3e4c-128">Il PID WMI è l'ID del processo per il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="b3e4c-129">Necessaria solo se le classi di performance monitor non restituiscono risultati affidabili.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="b3e4c-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e4c-131">Sposta il servizio WinMgmt in un processo Svchost autonomo con un endpoint DCOM fisso.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="b3e4c-132">L'endpoint predefinito è "ncacn \_ IP \_ TCP. 0.24158".</span><span class="sxs-lookup"><span data-stu-id="b3e4c-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="b3e4c-133">Tuttavia, l'endpoint può essere modificato eseguendo Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="b3e4c-134">Per ulteriori informazioni sulla configurazione di una porta fissa per WMI, vedere la pagina [relativa alla configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="b3e4c-135">L'argomento *Level* è il livello di autenticazione per il processo Svchost.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="b3e4c-136">WMI viene in genere eseguito come parte di un host del servizio condiviso e non è possibile aumentare il livello di autenticazione solo per WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="b3e4c-137">Se *Level* non è specificato, il valore predefinito è 4 (**RPC \_ C Authentication \_ \_ level \_ PKT** o **WbemAuthenticationLevelPkt**).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="b3e4c-138">È possibile eseguire WMI in modo più sicuro aumentando il livello di autenticazione alla privacy dei pacchetti (**RPC \_ C \_ AuthN \_ level \_ PKT \_ privacy** o **WbemAuthenticationLevelPktPrivacy**).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="b3e4c-139">I livelli di autenticazione per Visual Basic e scripting sono descritti in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="b3e4c-140">Per C++, vedere [impostazione del livello di sicurezza del processo predefinito con c++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="b3e4c-141">Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="b3e4c-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="b3e4c-143">Sposta il servizio WinMgmt nel processo Svchost condiviso.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="b3e4c-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="b3e4c-145">Esegue una verifica di coerenza nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="b3e4c-146">Quando si aggiunge l'opzione **/verifyrepository** senza l' *<path>* argomento, viene verificato il repository Live attualmente utilizzato da WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="b3e4c-147">Quando si specifica l'argomento *path* , è possibile verificare qualsiasi copia salvata del repository.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="b3e4c-148">In questo caso, l'argomento path deve contenere il percorso completo della copia del repository salvata.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="b3e4c-149">Il repository salvato deve essere una copia dell'intera cartella del repository.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="b3e4c-150">Per ulteriori informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="b3e4c-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="b3e4c-152">Esegue una verifica di coerenza sul repository WMI e, se viene rilevata un'incoerenza, ricompila il repository.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="b3e4c-153">Il contenuto del repository non coerente viene unito al repository ricompilato, se può essere letto.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="b3e4c-154">L'operazione di salvataggio funziona sempre con il repository attualmente utilizzato dal servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="b3e4c-155">Per ulteriori informazioni sugli errori restituiti da questo comando, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="b3e4c-156">% File MOF che contengono l'istruzione del preprocessore [**\# pragma autorecupero**](pragma-autorecover.md) vengono ripristinati nel repository.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="b3e4c-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="b3e4c-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="b3e4c-158">Il repository viene reimpostato sullo stato iniziale quando viene installato per la prima volta il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="b3e4c-159">I file MOF contenenti l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) vengono ripristinati nel repository.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3e4c-160">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3e4c-160">Remarks</span></span>

<span data-ttu-id="b3e4c-161">Questo strumento si trova nella directory% windir% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="b3e4c-162">Per un elenco delle opzioni disponibili, digitare `WinMgmt /?` al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="b3e4c-163">Il repository WMI, noto anche come repository CIM, non è solo un singolo file, ma una raccolta di file all'interno della cartella del repository che operano insieme come database.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="b3e4c-164">Quando si usa l'opzione **/backup** per eseguire il backup del repository, il backup risultante è un singolo file compresso.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="b3e4c-165">WMI restituisce il **\_ \_ \_ danneggiamento interno del database** di errore (NET HELPMSG 1358) se un'operazione di verifica indica che lo stato del repository non è coerente.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="b3e4c-166">Questo errore può essere restituito da qualsiasi comando che esegua la verifica del repository, ad esempio **/verifyrepository** o **/salvagerepository**.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="b3e4c-167">Se WMI restituisce messaggi di errore, tenere presente che potrebbero non indicare problemi nel servizio WMI o nei provider WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="b3e4c-168">Gli errori possono provenire in altre parti del sistema operativo e emergono come errori tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="b3e4c-169">In qualsiasi circostanza, non eliminare il repository WMI come prima azione perché l'eliminazione del repository può causare danni al sistema o alle applicazioni installate.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="b3e4c-170">Per ulteriori informazioni sull'origine del problema, scaricare ed eseguire lo strumento da riga di comando [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) Diagnostic.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="b3e4c-171">Questo strumento genera un report che in genere può isolare l'origine del problema e fornire istruzioni su come risolverlo.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="b3e4c-172">Il report contribuisce inoltre ai servizi di supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3e4c-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="b3e4c-173">È possibile scaricare il [utilità di diagnosi di WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="b3e4c-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b3e4c-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3e4c-174">Requirements</span></span>



| <span data-ttu-id="b3e4c-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e4c-175">Requirement</span></span> | <span data-ttu-id="b3e4c-176">Valore</span><span class="sxs-lookup"><span data-stu-id="b3e4c-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b3e4c-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e4c-177">Minimum supported client</span></span><br/> | <span data-ttu-id="b3e4c-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3e4c-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b3e4c-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3e4c-179">Minimum supported server</span></span><br/> | <span data-ttu-id="b3e4c-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3e4c-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3e4c-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3e4c-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e4c-182">Risoluzione dei problemi WMI</span><span class="sxs-lookup"><span data-stu-id="b3e4c-182">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="b3e4c-183">Connessione a WMI in modalità remota a partire da vista</span><span class="sxs-lookup"><span data-stu-id="b3e4c-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

