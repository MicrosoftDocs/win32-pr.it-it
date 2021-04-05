---
description: Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file. Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.
ms.assetid: 48721358-8450-462f-8f99-23e207311041
title: Backup e ripristino dello stato del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed61c3ccad51ebd8cd632fab292160c795741c9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755543"
---
# <a name="backing-up-and-restoring-system-state"></a><span data-ttu-id="710d2-104">Backup e ripristino dello stato del sistema</span><span class="sxs-lookup"><span data-stu-id="710d2-104">Backing Up and Restoring System State</span></span>

> [!Note]  
> <span data-ttu-id="710d2-105">Questo argomento si applica a Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="710d2-105">This topic applies to Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="710d2-106">Per informazioni su Windows Server 2003, vedere [backup e ripristino dello stato del sistema in Windows server 2003 R2 e Windows server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span><span class="sxs-lookup"><span data-stu-id="710d2-106">For information about Windows Server 2003, see [Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1](backing-up-and-restoring-system-state-under-vss.md)</span></span>

 

<span data-ttu-id="710d2-107">Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file.</span><span class="sxs-lookup"><span data-stu-id="710d2-107">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="710d2-108">Questi elementi devono essere sempre considerati come un'unità dalle operazioni di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="710d2-108">These elements should always be treated as a unit by backup and restore operations.</span></span>

> [!Note]  
> <span data-ttu-id="710d2-109">Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni).</span><span class="sxs-lookup"><span data-stu-id="710d2-109">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

 

<span data-ttu-id="710d2-110">Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="710d2-110">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span> <span data-ttu-id="710d2-111">I writer dello stato del sistema sono writer per i quali l'attributo del [**\_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) è impostato su VSS \_ ut \_ BOOTABLESYSTEMSTATE o VSS \_ ut \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="710d2-111">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="710d2-112">Se un writer VSS è identificato dal relativo [**\_ \_ tipo di utilizzo VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) come writer dello stato del sistema, deve essere incluso in un backup dello stato del sistema anche se è selezionabile.</span><span class="sxs-lookup"><span data-stu-id="710d2-112">If a VSS Writer is identified by its [**VSS\_USAGE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type) as a system state writer it must be included in a system state backup even if it is selectable.</span></span>

 

<span data-ttu-id="710d2-113">Oltre al sistema operativo enumerato e ai file binari del driver enumerati dai writer dello stato del sistema, è necessario eseguire il backup di alcuni file come parte dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="710d2-113">In addition to the enumerated operating system and driver binary files that are enumerated by the system state writers, there are certain other files that must be backed up as part of system state.</span></span>

<span data-ttu-id="710d2-114">Tutti i componenti restituiti da un writer dello stato del sistema VSS fanno parte dello stato del sistema, ad eccezione di quelli per cui \_ \_ è impostato il flag VSS CF Not \_ System \_ state.</span><span class="sxs-lookup"><span data-stu-id="710d2-114">All the components reported by a VSS system state writer are part of system state except those for which the VSS\_CF\_NOT\_SYSTEM\_STATE flag is set.</span></span>

<span data-ttu-id="710d2-115">Anche i programmi di backup devono impostare la chiave del registro di sistema **LastRestoreId** .</span><span class="sxs-lookup"><span data-stu-id="710d2-115">Backup programs should also set the **LastRestoreId** registry key.</span></span> <span data-ttu-id="710d2-116">Per ulteriori informazioni, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="710d2-116">For more information, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

> [!Note]  
> <span data-ttu-id="710d2-117">In Windows Vista, Windows Server 2008 e versioni successive, i nomi e le posizioni di alcuni file di sistema sono stati modificati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="710d2-117">In Windows Vista, Windows Server 2008, and later, the names and locations of some system files have been changed as follows.</span></span>

 

## <a name="system-state"></a><span data-ttu-id="710d2-118">Stato del sistema</span><span class="sxs-lookup"><span data-stu-id="710d2-118">System State</span></span>

<span data-ttu-id="710d2-119">Per Windows Server 2012 e versioni successive, oltre ai file segnalati dai vari writer di stato del sistema VSS, è necessario includere in modo esplicito solo i file di licenza seguenti e i file DRM seguenti devono essere esclusi in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="710d2-119">For Windows Server 2012 and later, in addition to the files reported by the various VSS system-state writers, only the following licensing files need to be included explicitly, and the following DRM files need to be excluded explicitly.</span></span>

## <a name="windows-media-digital-rights-management-files"></a><span data-ttu-id="710d2-120">File di Rights Management digitali di Windows Media</span><span class="sxs-lookup"><span data-stu-id="710d2-120">Windows Media Digital Rights Management Files</span></span>

<span data-ttu-id="710d2-121">In Windows Server 2008 e versioni successive, i file seguenti, incluse tutte le sottodirectory nel percorso seguente, sono esclusi dallo stato del sistema e non devono essere sottoposti a backup:</span><span class="sxs-lookup"><span data-stu-id="710d2-121">In Windows Server 2008 and later, the following files, including all subdirectories under the following path, are excluded from system state and must not be backed up:</span></span>

-   <span data-ttu-id="710d2-122">% ProgramData% \\ Microsoft \\ Windows \\ DRM</span><span class="sxs-lookup"><span data-stu-id="710d2-122">%ProgramData%\\Microsoft\\Windows\\DRM</span></span>\\

<span data-ttu-id="710d2-123">Questa operazione sostituisce le informazioni contenute nella sezione Windows Media Digital Rights Management di [utilizzo delle funzionalità di sicurezza e del file System](working-with-file-system-and-security-features.md).</span><span class="sxs-lookup"><span data-stu-id="710d2-123">This supersedes the information in the Windows Media Digital Rights Management section of [Working with File System and Security Features](working-with-file-system-and-security-features.md).</span></span>

## <a name="performance-counter-configuration-files"></a><span data-ttu-id="710d2-124">File di configurazione dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="710d2-124">Performance Counter Configuration Files</span></span>

<span data-ttu-id="710d2-125">I file di configurazione del contatore delle prestazioni si trovano nella directory% SystemRoot% \\ system32 \\ e hanno i nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="710d2-125">The performance counter configuration files are located in the %SystemRoot%\\System32\\ directory and have the following names:</span></span>

<dl> <span data-ttu-id="710d2-126">Prestazioni? 00?. dat</span><span class="sxs-lookup"><span data-stu-id="710d2-126">Perf?00?.dat</span></span>  
<span data-ttu-id="710d2-127">??. Perfc0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-127">Perfc0??.dat</span></span>  
<span data-ttu-id="710d2-128">??. Perfd0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-128">Perfd0??.dat</span></span>  
<span data-ttu-id="710d2-129">??. Perfh0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-129">Perfh0??.dat</span></span>  
<span data-ttu-id="710d2-130">??. Perfi0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-130">Perfi0??.dat</span></span>  
<span data-ttu-id="710d2-131">???. Prfc0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-131">Prfc0???.dat</span></span>  
<span data-ttu-id="710d2-132">???. Prfd0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-132">Prfd0???.dat</span></span>  
<span data-ttu-id="710d2-133">???. Prfh0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-133">Prfh0???.dat</span></span>  
<span data-ttu-id="710d2-134">???. Prfi0 dat</span><span class="sxs-lookup"><span data-stu-id="710d2-134">Prfi0???.dat</span></span>  
</dl>

<span data-ttu-id="710d2-135">Questi file vengono modificati solo durante l'installazione dell'applicazione ed è necessario eseguirne il backup e il ripristino durante i backup e i ripristini dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="710d2-135">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

## <a name="iis-configuration-files"></a><span data-ttu-id="710d2-136">File di configurazione di IIS</span><span class="sxs-lookup"><span data-stu-id="710d2-136">IIS Configuration Files</span></span>

> [!Note]  
> <span data-ttu-id="710d2-137">In Windows Vista con Service Pack 1 (SP1) e versioni successive, non è consigliabile eseguire il backup di questi file.</span><span class="sxs-lookup"><span data-stu-id="710d2-137">In Windows Vista with Service Pack 1 (SP1) and later, you should not back up these files.</span></span> <span data-ttu-id="710d2-138">Usare invece il writer di configurazione di IIS in-box.</span><span class="sxs-lookup"><span data-stu-id="710d2-138">Instead, use the in-box IIS configuration writer.</span></span> <span data-ttu-id="710d2-139">Per ulteriori informazioni su questo writer, vedere la pagina relativa ai [writer VSS](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="710d2-139">For more information about this writer, see [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

<span data-ttu-id="710d2-140">Di seguito sono elencati i file di configurazione IIS pertinenti e i relativi percorsi:</span><span class="sxs-lookup"><span data-stu-id="710d2-140">The relevant IIS configuration files and their locations are listed below:</span></span>

-   <span data-ttu-id="710d2-141">Il file di machine.config .NET FX si trova nella directory della versione del Framework.</span><span class="sxs-lookup"><span data-stu-id="710d2-141">The .NET FX machine.config file is located in the framework version directory.</span></span>
-   <span data-ttu-id="710d2-142">Il file di web.config radice ASP.NET si trova nella directory della versione del Framework.</span><span class="sxs-lookup"><span data-stu-id="710d2-142">The ASP.NET root web.config file is located in the framework version directory.</span></span>
    > [!Note]  
    > <span data-ttu-id="710d2-143">I file di configurazione per .NET FX e ASP.NET si trovano nella directory della versione del Framework.</span><span class="sxs-lookup"><span data-stu-id="710d2-143">The configuration files for both .NET FX and ASP.NET are in the framework version directory.</span></span> <span data-ttu-id="710d2-144">Se nel computer sono installate più versioni del Framework, questa directory conterrà un file di configurazione per ogni versione installata.</span><span class="sxs-lookup"><span data-stu-id="710d2-144">If multiple versions of the framework are installed on the computer, this directory will contain one configuration file for each installed version.</span></span>

     

-   <span data-ttu-id="710d2-145">Il file di configurazione centrale di IIS applicationHost.config si trova nella directory% windir% \\ system32 \\ inetsrv \\ config.</span><span class="sxs-lookup"><span data-stu-id="710d2-145">The IIS applicationHost.config central configuration file is located in the %windir%\\system32\\inetsrv\\config directory.</span></span> <span data-ttu-id="710d2-146">Poiché il server è in grado di comprendere questo file di configurazione, sono presenti file di schema che ne determinano la grammatica e la struttura.</span><span class="sxs-lookup"><span data-stu-id="710d2-146">For the server to understand this configuration file, there are schema files that determine its grammar and structure.</span></span> <span data-ttu-id="710d2-147">Questi file si trovano nella directory% windir% \\ system32 \\ inetsrv \\ config \\ schema.</span><span class="sxs-lookup"><span data-stu-id="710d2-147">These files are located in the %windir%\\system32\\inetsrv\\config\\schema directory.</span></span>

<span data-ttu-id="710d2-148">Il percorso della directory della versione del Framework è archiviato nella chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="710d2-148">The framework version directory path is stored in the following registry key:</span></span>

<span data-ttu-id="710d2-149">**HKEY \_ \_ computer locale \\ software \\ Microsoft \\ . \\InstallRoot NETFramework**</span><span class="sxs-lookup"><span data-stu-id="710d2-149">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\.NETFramework\\InstallRoot**</span></span>

<span data-ttu-id="710d2-150">Inoltre, è necessario eseguire il backup delle chiavi di crittografia seguenti:</span><span class="sxs-lookup"><span data-stu-id="710d2-150">In addition, the following cryptography keys must be backed up:</span></span><dl> <span data-ttu-id="710d2-151">% ProgramData% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="710d2-151">%ProgramData%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span>  
<span data-ttu-id="710d2-152">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="710d2-152">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
</dl>

## <a name="framework-files"></a><span data-ttu-id="710d2-153">File di Framework</span><span class="sxs-lookup"><span data-stu-id="710d2-153">Framework Files</span></span>

<span data-ttu-id="710d2-154">È necessario eseguire il backup di tutte le versioni di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="710d2-154">All versions of the .NET framework must be backed up.</span></span> <span data-ttu-id="710d2-155">I file si trovano in una o in entrambe le directory seguenti:</span><span class="sxs-lookup"><span data-stu-id="710d2-155">The files are located in one or both of the following directories:</span></span>

<dl> <span data-ttu-id="710d2-156">% WINDIR% \\ Microsoft.NET \\ Framework</span><span class="sxs-lookup"><span data-stu-id="710d2-156">%windir%\\Microsoft.Net\\Framework</span></span>  
<span data-ttu-id="710d2-157">% WINDIR% \\ Microsoft.NET \\ Framework64</span><span class="sxs-lookup"><span data-stu-id="710d2-157">%windir%\\Microsoft.Net\\Framework64</span></span>  
</dl>

<span data-ttu-id="710d2-158">Inoltre, è necessario eseguire il backup dei file di assembly.</span><span class="sxs-lookup"><span data-stu-id="710d2-158">In addition, the assembly files must be backed up.</span></span> <span data-ttu-id="710d2-159">Questi file sono disponibili nella directory seguente:</span><span class="sxs-lookup"><span data-stu-id="710d2-159">These files are located in the following directory:</span></span><dl> <span data-ttu-id="710d2-160">assembly% windir% \\</span><span class="sxs-lookup"><span data-stu-id="710d2-160">%windir%\\assembly</span></span>  
</dl>

## <a name="task-scheduler-task-files"></a><span data-ttu-id="710d2-161">File Utilità di pianificazione attività</span><span class="sxs-lookup"><span data-stu-id="710d2-161">Task Scheduler Task Files</span></span>

<span data-ttu-id="710d2-162">È necessario eseguire il backup dei file delle attività dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="710d2-162">The task scheduler's task files must be backed up.</span></span> <span data-ttu-id="710d2-163">I file si trovano in una o in entrambe le posizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="710d2-163">The files are located in one or both of the following locations:</span></span>

<dl> <span data-ttu-id="710d2-164">% WINDIR% \\ system32 \\ attività e qualsiasi sottodirectory (in modo ricorsivo)</span><span class="sxs-lookup"><span data-stu-id="710d2-164">%windir%\\system32\\tasks and any subdirectories (recursively)</span></span>  
<span data-ttu-id="710d2-165">% WINDIR% \\ attività (nessuna sottodirectory)</span><span class="sxs-lookup"><span data-stu-id="710d2-165">%windir%\\tasks (no subdirectories)</span></span>  
</dl>

 

 
