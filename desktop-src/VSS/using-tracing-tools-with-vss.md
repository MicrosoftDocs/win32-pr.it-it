---
description: Per raccogliere informazioni di traccia per l'infrastruttura del servizio Copia Shadow del volume, è possibile utilizzare lo strumento VssTrace, lo strumento Logman o lo strumento tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Uso degli strumenti di traccia con VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226114"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="04dee-103">Uso degli strumenti di traccia con VSS</span><span class="sxs-lookup"><span data-stu-id="04dee-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="04dee-104">Per raccogliere informazioni di traccia per l'infrastruttura del servizio Copia Shadow del volume, è possibile utilizzare lo strumento VssTrace, lo strumento Logman o lo strumento tracelog.</span><span class="sxs-lookup"><span data-stu-id="04dee-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="04dee-105">VssTrace è disponibile nel Software Development Kit (SDK) di Microsoft Windows e può essere utilizzato per tracciare le applicazioni VSS in Windows 7 e versioni successive del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="04dee-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="04dee-106">Logman è un controller di traccia per gli eventi di traccia e i contatori delle prestazioni. può essere usato anche per tracciare le applicazioni VSS in Windows 7 e versioni successive del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="04dee-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="04dee-107">Tracelog è incluso in Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="04dee-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="04dee-108">Per usare gli strumenti di traccia con [Ripristino automatico del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), vedere [uso degli strumenti di traccia con le applicazioni ASR](using-tracing-tools-with-vss-asr-applications.md).</span><span class="sxs-lookup"><span data-stu-id="04dee-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="04dee-109">VssTrace, Logman e tracelog richiedono tutti privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="04dee-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="04dee-110">Per informazioni su ogni strumento, vedere le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="04dee-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="04dee-111">Uso di VssTrace</span><span class="sxs-lookup"><span data-stu-id="04dee-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="04dee-112">Opzioni Command-Line VssTrace</span><span class="sxs-lookup"><span data-stu-id="04dee-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="04dee-113">Uso di logman</span><span class="sxs-lookup"><span data-stu-id="04dee-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="04dee-114">Uso di tracelog</span><span class="sxs-lookup"><span data-stu-id="04dee-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="04dee-115">Uso di VssTrace</span><span class="sxs-lookup"><span data-stu-id="04dee-115">Using VssTrace</span></span>

<span data-ttu-id="04dee-116">Per eseguire lo strumento VssTrace dalla riga di comando, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="04dee-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="04dee-117"> *Opzioni della riga di comando di* vsstrace</span><span class="sxs-lookup"><span data-stu-id="04dee-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="04dee-118">Per visualizzare la guida concisa della riga di comando per lo strumento VssTrace, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="04dee-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="04dee-119">**vsstrace-Guida**</span><span class="sxs-lookup"><span data-stu-id="04dee-119">**vsstrace -help**</span></span>

<span data-ttu-id="04dee-120">Per visualizzare informazioni dettagliate della guida della riga di comando per lo strumento VssTrace, usare la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="04dee-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="04dee-121">**vsstrace-Help All**</span><span class="sxs-lookup"><span data-stu-id="04dee-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="04dee-122">Opzioni Command-Line VssTrace</span><span class="sxs-lookup"><span data-stu-id="04dee-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="04dee-123">Lo strumento VssTrace usa le seguenti opzioni della riga di comando:</span><span class="sxs-lookup"><span data-stu-id="04dee-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="04dee-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>*flag* **-f**</span><span class="sxs-lookup"><span data-stu-id="04dee-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-125">Abilitare i moduli i cui flag sono specificati dalla maschera di maschera dei *flag* .</span><span class="sxs-lookup"><span data-stu-id="04dee-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="04dee-126">Ogni flag corrisponde a un modulo VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="04dee-127">Se *Flags* è zero, non sono abilitati moduli.</span><span class="sxs-lookup"><span data-stu-id="04dee-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="04dee-128">Si noti che la maggior parte dei moduli è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="04dee-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="04dee-129">Questa opzione può essere combinata con l' **+** opzione del _modulo_ .</span><span class="sxs-lookup"><span data-stu-id="04dee-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="04dee-130">Ad esempio, **vsstrace-f 0 + Writer + Coord** Disabilita la traccia di tutti i moduli abilitati per impostazione predefinita e Abilita la traccia dei writer VSS e del servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="04dee-131">In alternativa, **vsstrace + f 0xFFFF-Coord** Abilita la traccia di tutti i moduli tranne il servizio VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="04dee-132">Se si usa l'opzione **-f** con l'opzione del **+** _modulo_ , il **-f** deve essere visualizzato prima dell'opzione del **+** _modulo_ .</span><span class="sxs-lookup"><span data-stu-id="04dee-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="04dee-133">La tabella seguente elenca il nome e il flag del modulo per ogni modulo disponibile.</span><span class="sxs-lookup"><span data-stu-id="04dee-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="04dee-134">Modulo</span><span class="sxs-lookup"><span data-stu-id="04dee-134">Module</span></span> | <span data-ttu-id="04dee-135">Contrassegno</span><span class="sxs-lookup"><span data-stu-id="04dee-135">Flag</span></span>       | <span data-ttu-id="04dee-136">Abilitato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="04dee-136">Enabled by default</span></span> | <span data-ttu-id="04dee-137">Elementi tracciati</span><span class="sxs-lookup"><span data-stu-id="04dee-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04dee-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="04dee-138">EXCEPT</span></span> | <span data-ttu-id="04dee-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="04dee-139">0x00000001</span></span> | <span data-ttu-id="04dee-140">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-140">Yes</span></span>                | <span data-ttu-id="04dee-141">Gestione delle eccezioni C++.</span><span class="sxs-lookup"><span data-stu-id="04dee-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="04dee-142">COORD</span><span class="sxs-lookup"><span data-stu-id="04dee-142">COORD</span></span>  | <span data-ttu-id="04dee-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="04dee-143">0x00000002</span></span> | <span data-ttu-id="04dee-144">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-144">Yes</span></span>                | <span data-ttu-id="04dee-145">Il servizio VSS, denominato anche coordinatore VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="04dee-146">SWPRV</span><span class="sxs-lookup"><span data-stu-id="04dee-146">SWPRV</span></span>  | <span data-ttu-id="04dee-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="04dee-147">0x00000004</span></span> | <span data-ttu-id="04dee-148">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-148">Yes</span></span>                | <span data-ttu-id="04dee-149">Servizio del provider di copia shadow di sistema VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="04dee-150">BUCOMP</span><span class="sxs-lookup"><span data-stu-id="04dee-150">BUCOMP</span></span> | <span data-ttu-id="04dee-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="04dee-151">0x00000008</span></span> | <span data-ttu-id="04dee-152">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-152">Yes</span></span>                | <span data-ttu-id="04dee-153">Il richiedente VSS e l'elaborazione dei metadati di backup.</span><span class="sxs-lookup"><span data-stu-id="04dee-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="04dee-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="04dee-154">WRITER</span></span> | <span data-ttu-id="04dee-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04dee-155">0x00000010</span></span> | <span data-ttu-id="04dee-156">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-156">Yes</span></span>                | <span data-ttu-id="04dee-157">VSS writer operazioni e implementazioni di writer ospitate VSS, ad esempio il writer del registro di sistema di Windows.</span><span class="sxs-lookup"><span data-stu-id="04dee-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="04dee-158">VSSAPI</span><span class="sxs-lookup"><span data-stu-id="04dee-158">VSSAPI</span></span> | <span data-ttu-id="04dee-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="04dee-159">0x00000020</span></span> | <span data-ttu-id="04dee-160">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-160">Yes</span></span>                | <span data-ttu-id="04dee-161">Varie funzioni dell'API VSS esportate da VSSAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="04dee-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="04dee-162">HWDIAG</span><span class="sxs-lookup"><span data-stu-id="04dee-162">HWDIAG</span></span> | <span data-ttu-id="04dee-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="04dee-163">0x00000040</span></span> | <span data-ttu-id="04dee-164">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-164">Yes</span></span>                | <span data-ttu-id="04dee-165">Infrastruttura e operazioni del provider hardware VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="04dee-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="04dee-166">ADMIN</span></span>  | <span data-ttu-id="04dee-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="04dee-167">0x00000080</span></span> | <span data-ttu-id="04dee-168">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-168">Yes</span></span>                | <span data-ttu-id="04dee-169">Utilità della riga di comando VSS, ad esempio VSSADMIN.EXE e DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="04dee-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="04dee-170">VSSUI</span><span class="sxs-lookup"><span data-stu-id="04dee-170">VSSUI</span></span>  | <span data-ttu-id="04dee-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="04dee-171">0x00000100</span></span> | <span data-ttu-id="04dee-172">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-172">Yes</span></span>                | <span data-ttu-id="04dee-173">Interfaccia utente di configurazione copie shadow per cartelle condivise.</span><span class="sxs-lookup"><span data-stu-id="04dee-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="04dee-174">L'interfaccia utente è disponibile solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="04dee-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="04dee-175">TEST</span><span class="sxs-lookup"><span data-stu-id="04dee-175">TEST</span></span>   | <span data-ttu-id="04dee-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="04dee-176">0x00000200</span></span> | <span data-ttu-id="04dee-177">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-177">Yes</span></span>                | <span data-ttu-id="04dee-178">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="04dee-178">Not applicable.</span></span> <span data-ttu-id="04dee-179">(Questo modulo di traccia è riservato).</span><span class="sxs-lookup"><span data-stu-id="04dee-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="04dee-180">IOCTL</span><span class="sxs-lookup"><span data-stu-id="04dee-180">IOCTL</span></span>  | <span data-ttu-id="04dee-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="04dee-181">0x00000400</span></span> | <span data-ttu-id="04dee-182">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-182">Yes</span></span>                | <span data-ttu-id="04dee-183">Dettagli delle operazioni FSCTL e IOCTL avviate dal servizio VSS chiamando la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="04dee-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="04dee-184">GENERAZIONE</span><span class="sxs-lookup"><span data-stu-id="04dee-184">GEN</span></span>    | <span data-ttu-id="04dee-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="04dee-185">0x00000800</span></span> | <span data-ttu-id="04dee-186">Sì</span><span class="sxs-lookup"><span data-stu-id="04dee-186">Yes</span></span>                | <span data-ttu-id="04dee-187">Funzioni di utilità VSS generali, ad esempio allocatori, classi stringa e operazioni del registro di sistema e del volume.</span><span class="sxs-lookup"><span data-stu-id="04dee-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="04dee-188">WRXML</span><span class="sxs-lookup"><span data-stu-id="04dee-188">WRXML</span></span>  | <span data-ttu-id="04dee-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="04dee-189">0x00001000</span></span> | <span data-ttu-id="04dee-190">No</span><span class="sxs-lookup"><span data-stu-id="04dee-190">No</span></span>                 | <span data-ttu-id="04dee-191">Elaborazione XML per i metadati del writer.</span><span class="sxs-lookup"><span data-stu-id="04dee-191">XML processing for writer metadata.</span></span> <span data-ttu-id="04dee-192">Questo modulo ha un livello di disturbo molto elevato.</span><span class="sxs-lookup"><span data-stu-id="04dee-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="04dee-193">VSSXML</span><span class="sxs-lookup"><span data-stu-id="04dee-193">VSSXML</span></span> | <span data-ttu-id="04dee-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="04dee-194">0x00002000</span></span> | <span data-ttu-id="04dee-195">No</span><span class="sxs-lookup"><span data-stu-id="04dee-195">No</span></span>                 | <span data-ttu-id="04dee-196">Classi base di elaborazione XML.</span><span class="sxs-lookup"><span data-stu-id="04dee-196">XML processing base classes.</span></span> <span data-ttu-id="04dee-197">Questo modulo ha un livello di disturbo molto elevato.</span><span class="sxs-lookup"><span data-stu-id="04dee-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="04dee-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Modulo_</span><span class="sxs-lookup"><span data-stu-id="04dee-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="04dee-199">Abilitare il modulo specificato dal *modulo*.</span><span class="sxs-lookup"><span data-stu-id="04dee-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="04dee-200">È possibile abilitare più di un modulo alla volta.</span><span class="sxs-lookup"><span data-stu-id="04dee-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="04dee-201">Per elencare i moduli disponibili, digitare **vsstrace-Help Modules** al prompt della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="04dee-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Modulo_</span><span class="sxs-lookup"><span data-stu-id="04dee-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="04dee-203">Disabilitare il modulo specificato dal *modulo*.</span><span class="sxs-lookup"><span data-stu-id="04dee-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="04dee-204">Per elencare i moduli disponibili, digitare **vsstrace-Help Modules** al prompt della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="04dee-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+ PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="04dee-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-206">Consente di abilitare il processo specificato da *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="04dee-207">Per abilitare tutti i processi, usare " \* " come valore di *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="04dee-208">È possibile specificare più di un'opzione **PID** alla volta.</span><span class="sxs-lookup"><span data-stu-id="04dee-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="04dee-209">L'ordine delle opzioni determina quali processi sono abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="04dee-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="04dee-210">Ad esempio, per abilitare solo il processo il cui identificatore di processo è 0xe8c, usare **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="04dee-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-PID** *ProcessID*</span><span class="sxs-lookup"><span data-stu-id="04dee-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-212">Disabilitare il processo specificato da *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="04dee-213">Per disabilitare tutti i processi, usare " \* " come valore di *ProcessID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="04dee-214">È possibile specificare più di un'opzione **PID** alla volta.</span><span class="sxs-lookup"><span data-stu-id="04dee-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="04dee-215">L'ordine delle opzioni determina quali processi sono abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="04dee-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="04dee-216">Ad esempio, per disabilitare tutti i processi ad eccezione del processo il cui identificatore di processo è 0xe8c, usare **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="04dee-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+ TID** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="04dee-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-218">Abilitare il thread specificato da *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="04dee-219">Per abilitare tutti i thread, usare " \* " come valore di *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="04dee-220">È possibile specificare più di un'opzione **TID** alla volta.</span><span class="sxs-lookup"><span data-stu-id="04dee-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="04dee-221">L'ordine delle opzioni determina quali thread sono abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="04dee-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="04dee-222">Ad esempio, per abilitare solo il thread il cui identificatore del processo è 0x31a, usare **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="04dee-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-TID** *ThreadID*</span><span class="sxs-lookup"><span data-stu-id="04dee-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-224">Disabilitare il thread specificato da *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="04dee-225">Per disabilitare tutti i thread, usare " \* " come valore di *ThreadID*.</span><span class="sxs-lookup"><span data-stu-id="04dee-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="04dee-226">È possibile specificare più di un'opzione **TID** alla volta.</span><span class="sxs-lookup"><span data-stu-id="04dee-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="04dee-227">L'ordine delle opzioni determina quali thread sono abilitati o disabilitati.</span><span class="sxs-lookup"><span data-stu-id="04dee-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="04dee-228">Ad esempio, per disabilitare tutti i thread eccetto il thread il cui identificatore di processo è 0x31a, usare **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="04dee-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *livello*</span><span class="sxs-lookup"><span data-stu-id="04dee-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-230">Utilizzare il livello di traccia specificato in base al *livello*.</span><span class="sxs-lookup"><span data-stu-id="04dee-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="04dee-231">Maggiore è il livello, più dettagliato è l'output di traccia.</span><span class="sxs-lookup"><span data-stu-id="04dee-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="04dee-232">Ogni livello include tutti i livelli inferiori.</span><span class="sxs-lookup"><span data-stu-id="04dee-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="04dee-233">Il livello predefinito è 170.</span><span class="sxs-lookup"><span data-stu-id="04dee-233">The default level is 170.</span></span> <span data-ttu-id="04dee-234">Sono disponibili i livelli seguenti.</span><span class="sxs-lookup"><span data-stu-id="04dee-234">The following levels are available.</span></span>



| <span data-ttu-id="04dee-235">Level</span><span class="sxs-lookup"><span data-stu-id="04dee-235">Level</span></span> | <span data-ttu-id="04dee-236">Informazioni incluse nell'output di traccia</span><span class="sxs-lookup"><span data-stu-id="04dee-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="04dee-237">7000</span><span class="sxs-lookup"><span data-stu-id="04dee-237">000</span></span>   | <span data-ttu-id="04dee-238">nessuno</span><span class="sxs-lookup"><span data-stu-id="04dee-238">None</span></span>                                     |
| <span data-ttu-id="04dee-239">020</span><span class="sxs-lookup"><span data-stu-id="04dee-239">020</span></span>   | <span data-ttu-id="04dee-240">Errori irreversibili</span><span class="sxs-lookup"><span data-stu-id="04dee-240">Fatal errors</span></span>                             |
| <span data-ttu-id="04dee-241">030</span><span class="sxs-lookup"><span data-stu-id="04dee-241">030</span></span>   | <span data-ttu-id="04dee-242">Eccezioni non gestite</span><span class="sxs-lookup"><span data-stu-id="04dee-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="04dee-243">040</span><span class="sxs-lookup"><span data-stu-id="04dee-243">040</span></span>   | <span data-ttu-id="04dee-244">Errors</span><span class="sxs-lookup"><span data-stu-id="04dee-244">Errors</span></span>                                   |
| <span data-ttu-id="04dee-245">050</span><span class="sxs-lookup"><span data-stu-id="04dee-245">050</span></span>   | <span data-ttu-id="04dee-246">Asserzioni</span><span class="sxs-lookup"><span data-stu-id="04dee-246">Assertions</span></span>                               |
| <span data-ttu-id="04dee-247">060</span><span class="sxs-lookup"><span data-stu-id="04dee-247">060</span></span>   | <span data-ttu-id="04dee-248">Avvisi</span><span class="sxs-lookup"><span data-stu-id="04dee-248">Warnings</span></span>                                 |
| <span data-ttu-id="04dee-249">080</span><span class="sxs-lookup"><span data-stu-id="04dee-249">080</span></span>   | <span data-ttu-id="04dee-250">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="04dee-250">Exception handling</span></span>                       |
| <span data-ttu-id="04dee-251">100</span><span class="sxs-lookup"><span data-stu-id="04dee-251">100</span></span>   | <span data-ttu-id="04dee-252">Attività registro eventi</span><span class="sxs-lookup"><span data-stu-id="04dee-252">Event Log activity</span></span>                       |
| <span data-ttu-id="04dee-253">120</span><span class="sxs-lookup"><span data-stu-id="04dee-253">120</span></span>   | <span data-ttu-id="04dee-254">Informazioni generali</span><span class="sxs-lookup"><span data-stu-id="04dee-254">General information</span></span>                      |
| <span data-ttu-id="04dee-255">140</span><span class="sxs-lookup"><span data-stu-id="04dee-255">140</span></span>   | <span data-ttu-id="04dee-256">flusso del codice</span><span class="sxs-lookup"><span data-stu-id="04dee-256">Code flow</span></span>                                |
| <span data-ttu-id="04dee-257">160</span><span class="sxs-lookup"><span data-stu-id="04dee-257">160</span></span>   | <span data-ttu-id="04dee-258">Immettere ed uscire dalla funzione</span><span class="sxs-lookup"><span data-stu-id="04dee-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="04dee-259">170</span><span class="sxs-lookup"><span data-stu-id="04dee-259">170</span></span>   | <span data-ttu-id="04dee-260">Valori restituiti dalla funzione</span><span class="sxs-lookup"><span data-stu-id="04dee-260">Function return values</span></span>                   |
| <span data-ttu-id="04dee-261">180</span><span class="sxs-lookup"><span data-stu-id="04dee-261">180</span></span>   | <span data-ttu-id="04dee-262">Parametri della funzione (conciso)</span><span class="sxs-lookup"><span data-stu-id="04dee-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="04dee-263">190</span><span class="sxs-lookup"><span data-stu-id="04dee-263">190</span></span>   | <span data-ttu-id="04dee-264">Parametri della funzione (verbose)</span><span class="sxs-lookup"><span data-stu-id="04dee-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="04dee-265">200</span><span class="sxs-lookup"><span data-stu-id="04dee-265">200</span></span>   | <span data-ttu-id="04dee-266">Livello informazioni dettagliate 1</span><span class="sxs-lookup"><span data-stu-id="04dee-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="04dee-267">210</span><span class="sxs-lookup"><span data-stu-id="04dee-267">210</span></span>   | <span data-ttu-id="04dee-268">Livello informazioni dettagliate 2</span><span class="sxs-lookup"><span data-stu-id="04dee-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="04dee-269">220</span><span class="sxs-lookup"><span data-stu-id="04dee-269">220</span></span>   | <span data-ttu-id="04dee-270">Livello informazioni dettagliate 3</span><span class="sxs-lookup"><span data-stu-id="04dee-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="04dee-271">230</span><span class="sxs-lookup"><span data-stu-id="04dee-271">230</span></span>   | <span data-ttu-id="04dee-272">Livello di codice veloce 1</span><span class="sxs-lookup"><span data-stu-id="04dee-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="04dee-273">240</span><span class="sxs-lookup"><span data-stu-id="04dee-273">240</span></span>   | <span data-ttu-id="04dee-274">Livello di codice veloce 2</span><span class="sxs-lookup"><span data-stu-id="04dee-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="04dee-275">250</span><span class="sxs-lookup"><span data-stu-id="04dee-275">250</span></span>   | <span data-ttu-id="04dee-276">Livello di codice veloce 3</span><span class="sxs-lookup"><span data-stu-id="04dee-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="04dee-277">255</span><span class="sxs-lookup"><span data-stu-id="04dee-277">255</span></span>   | <span data-ttu-id="04dee-278">Tutti</span><span class="sxs-lookup"><span data-stu-id="04dee-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="04dee-279"><span id="_indent"></span><span id="_INDENT"></span>**+ rientro**</span><span class="sxs-lookup"><span data-stu-id="04dee-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="04dee-280">Rientrare nell'output di traccia formattato per ogni funzione e limite di funzione.</span><span class="sxs-lookup"><span data-stu-id="04dee-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-281"><span id="-indent"></span><span id="-INDENT"></span>**-rientro**</span><span class="sxs-lookup"><span data-stu-id="04dee-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="04dee-282">Non rientrare nell'output di traccia formattato.</span><span class="sxs-lookup"><span data-stu-id="04dee-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-ETL** *EtlFile*</span><span class="sxs-lookup"><span data-stu-id="04dee-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-284">Converte il file di output logman specificato da *EtlFile* in un formato di testo leggibile.</span><span class="sxs-lookup"><span data-stu-id="04dee-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *outputfile*</span><span class="sxs-lookup"><span data-stu-id="04dee-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-286">Salvare le informazioni di traccia nel file di output specificato da *outputfile*.</span><span class="sxs-lookup"><span data-stu-id="04dee-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="04dee-287">Per prestazioni ottimali, il file di output deve trovarsi in un volume che non fa parte della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="04dee-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="04dee-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*</span><span class="sxs-lookup"><span data-stu-id="04dee-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="04dee-289">Consente di visualizzare la guida della riga di comando come specificato da *HelpOption*.</span><span class="sxs-lookup"><span data-stu-id="04dee-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="04dee-290">I valori di *HelpOption* validi sono **moduli**, **livelli** e **tutti**.</span><span class="sxs-lookup"><span data-stu-id="04dee-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="04dee-291">Se si specificano i **moduli** , i moduli verranno elencati.</span><span class="sxs-lookup"><span data-stu-id="04dee-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="04dee-292">Se si specificano i **livelli** , verranno elencati i livelli disponibili.</span><span class="sxs-lookup"><span data-stu-id="04dee-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="04dee-293">Se si specifica **All** , viene visualizzata una guida dettagliata.</span><span class="sxs-lookup"><span data-stu-id="04dee-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="04dee-294">Se non viene usata alcuna opzione, viene visualizzata la guida concisa.</span><span class="sxs-lookup"><span data-stu-id="04dee-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="04dee-295">Uso di logman</span><span class="sxs-lookup"><span data-stu-id="04dee-295">Using Logman</span></span>

<span data-ttu-id="04dee-296">Nella procedura seguente viene descritto come utilizzare logman con l'applicazione VSS.</span><span class="sxs-lookup"><span data-stu-id="04dee-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="04dee-297">**Per usare logman con l'applicazione VSS**</span><span class="sxs-lookup"><span data-stu-id="04dee-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="04dee-298">Usare il comando seguente per avviare la traccia:</span><span class="sxs-lookup"><span data-stu-id="04dee-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="04dee-299">**logman start VSS-o** *x: \\ \* \* \* VSS. etl-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xFFF 170*\*</span><span class="sxs-lookup"><span data-stu-id="04dee-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="04dee-300">Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.</span><span class="sxs-lookup"><span data-stu-id="04dee-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="04dee-301">Usare il comando seguente per arrestare la traccia:</span><span class="sxs-lookup"><span data-stu-id="04dee-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="04dee-302">**logman stop VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="04dee-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="04dee-303">Il file di log di traccia è *x: \\* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="04dee-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="04dee-304">Per ulteriori informazioni sullo strumento Logman, vedere [logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="04dee-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="04dee-305">Uso di tracelog</span><span class="sxs-lookup"><span data-stu-id="04dee-305">Using Tracelog</span></span>

<span data-ttu-id="04dee-306">Nella procedura seguente viene descritto come utilizzare tracelog.</span><span class="sxs-lookup"><span data-stu-id="04dee-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="04dee-307">**Per usare tracelog**</span><span class="sxs-lookup"><span data-stu-id="04dee-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="04dee-308">Creare un file di testo denominato VSS. CTL contenente solo il testo seguente:</span><span class="sxs-lookup"><span data-stu-id="04dee-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="04dee-309">**VSS 9138500e-3648-4edb-aa4c-859e9f7b7c38**</span><span class="sxs-lookup"><span data-stu-id="04dee-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="04dee-310">Usare il comando seguente per avviare la traccia:</span><span class="sxs-lookup"><span data-stu-id="04dee-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="04dee-311">**tracelog-Start VSS-f** *x: \\ \* \* \* VSS. etl-GUID VSS. CTL-flag 0xAA a livello 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="04dee-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="04dee-312">Sostituire "x: \\ " con il percorso della directory in cui si desidera archiviare il file di log di traccia.</span><span class="sxs-lookup"><span data-stu-id="04dee-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="04dee-313">Usare il comando seguente per arrestare la traccia:</span><span class="sxs-lookup"><span data-stu-id="04dee-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="04dee-314">**tracelog-arresta VSS**</span><span class="sxs-lookup"><span data-stu-id="04dee-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="04dee-315">Il file di log di traccia è *x: \\* VSS. etl.</span><span class="sxs-lookup"><span data-stu-id="04dee-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="04dee-316">Per ulteriori informazioni sullo strumento tracelog, vedere [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="04dee-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
