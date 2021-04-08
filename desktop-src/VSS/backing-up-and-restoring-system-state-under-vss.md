---
description: Si noti che questo argomento si applica solo a Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1).
ms.assetid: a192d9a7-1c65-4251-acb1-4df03ebfe910
title: Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de2fdb50e3f719a5208c2894f5659f927bcc922d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968489"
---
# <a name="backing-up-and-restoring-system-state-in-windows-server-2003-r2-and-windows-server-2003-sp1"></a><span data-ttu-id="c968c-103">Backup e ripristino dello stato del sistema in Windows Server 2003 R2 e Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="c968c-103">Backing Up and Restoring System State in Windows Server 2003 R2 and Windows Server 2003 SP1</span></span>

> [!Note]  
> <span data-ttu-id="c968c-104">Questo argomento si applica solo a Windows Server 2003 R2 e Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c968c-104">This topic only applies to Windows Server 2003 R2 and Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="c968c-105">Per informazioni su altre versioni del sistema operativo, vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md).</span><span class="sxs-lookup"><span data-stu-id="c968c-105">For information about other operating system versions, see [Backing Up and Restoring System State](locating-additional-system-files.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="c968c-106">Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni).</span><span class="sxs-lookup"><span data-stu-id="c968c-106">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span> <span data-ttu-id="c968c-107">Per informazioni sull'uso di API e procedure fornite da Microsoft per implementare il ripristino dello stato del sistema online, vedere le risorse della community disponibili in [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="c968c-107">For information about using Microsoft-provided APIs and procedures to implement online system state restores, see the community resources available at the [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).</span></span>

 

<span data-ttu-id="c968c-108">Quando si esegue un backup o un ripristino VSS, lo stato del sistema Windows viene definito come una raccolta di diversi elementi chiave del sistema operativo e dei relativi file.</span><span class="sxs-lookup"><span data-stu-id="c968c-108">When performing a VSS backup or restore, the Windows system state is defined as being a collection of several key operating system elements and their files.</span></span> <span data-ttu-id="c968c-109">Questi elementi devono essere sempre gestiti da operazioni di backup e ripristino come unità.</span><span class="sxs-lookup"><span data-stu-id="c968c-109">These elements should always be treated by backup and restore operations as a unit.</span></span>

<span data-ttu-id="c968c-110">In Windows Server 2003 R2 e Windows Server 2003 con SP1, non è disponibile alcuna API Windows progettata per trattare questi oggetti come uno, quindi è consigliabile che i richiedenti dispongano di un proprio oggetto stato del sistema in modo da poter elaborare questi componenti in modo coerente.</span><span class="sxs-lookup"><span data-stu-id="c968c-110">In Windows Server 2003 R2 and Windows Server 2003 with SP1, there is no Windows API designed to treat these objects as one, so it is recommended that requesters have their own system state object so that they can process these components in a consistent manner.</span></span>

<span data-ttu-id="c968c-111">Poiché VSS viene eseguito nelle versioni di Windows in cui la [*protezione dei file di sistema*](vssgloss-s.md) (WFP) protegge i file di stato del sistema dal danneggiamento, sono necessari passaggi speciali per eseguire il backup e il ripristino dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-111">Because VSS runs on versions of Windows where [*System File Protection*](vssgloss-s.md) (WFP) protects system state files from corruption, special steps are needed to back up and restore system state.</span></span>

<span data-ttu-id="c968c-112">Lo stato del sistema è costituito dagli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c968c-112">System state consists of the following:</span></span>

-   <span data-ttu-id="c968c-113">Tutti i file protetti da WFP, i file di avvio, tra cui NTLDR, Ntdetect e le configurazioni dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="c968c-113">All files protected by WFP, boot files including ntldr, ntdetect, and performance counter configurations</span></span>
-   <span data-ttu-id="c968c-114">Il Active Directory (ADSI) (nei sistemi che sono controller di dominio)</span><span class="sxs-lookup"><span data-stu-id="c968c-114">The Active Directory (ADSI) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="c968c-115">Cartella del volume di sistema (SYSVOL) replicata dal servizio Replica file (FRS) (nei sistemi che sono controller di dominio)</span><span class="sxs-lookup"><span data-stu-id="c968c-115">The System Volume Folder (SYSVOL) that is replicated by the File Replication Service (FRS) (on systems that are domain controllers)</span></span>
-   <span data-ttu-id="c968c-116">Server di certificazione (nei sistemi che forniscono autorità di certificazione)</span><span class="sxs-lookup"><span data-stu-id="c968c-116">Certificate server (on systems that provide Certification Authority)</span></span>
-   <span data-ttu-id="c968c-117">Database cluster (nei sistemi che costituiscono un nodo di un cluster Windows)</span><span class="sxs-lookup"><span data-stu-id="c968c-117">Cluster database (on systems that are a node of a Windows cluster)</span></span>
-   <span data-ttu-id="c968c-118">Servizio Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="c968c-118">Registry service</span></span>
-   <span data-ttu-id="c968c-119">Database di registrazione della classe COM+</span><span class="sxs-lookup"><span data-stu-id="c968c-119">COM+ class registration database</span></span>

<span data-ttu-id="c968c-120">È possibile eseguire il backup dello stato del sistema in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="c968c-120">The system state can be backed up in any order.</span></span>

<span data-ttu-id="c968c-121">Tuttavia, il ripristino dello stato del sistema dovrebbe sostituire prima i file di avvio ed eseguire il commit della sezione di sistema (hive) del registro di sistema come passaggio finale del processo e potrebbe verificarsi nell'ordine seguente:</span><span class="sxs-lookup"><span data-stu-id="c968c-121">However, the restoration of the system state should replace boot files first and commit the system section (hive) of the registry as a final step in the process, and might occur in the following order:</span></span>

1.  <span data-ttu-id="c968c-122">Ripristinare i file di avvio.</span><span class="sxs-lookup"><span data-stu-id="c968c-122">Restore the boot files.</span></span>
2.  <span data-ttu-id="c968c-123">Database di registrazione della classe COM+</span><span class="sxs-lookup"><span data-stu-id="c968c-123">COM+ class registration database</span></span>
3.  <span data-ttu-id="c968c-124">Ripristinare SYSVOL, server dei certificati e database cluster (se necessario).</span><span class="sxs-lookup"><span data-stu-id="c968c-124">Restore SYSVOL, Certificate Server, and Cluster databases (if needed).</span></span>
4.  <span data-ttu-id="c968c-125">Ripristinare Active Directory (se necessario).</span><span class="sxs-lookup"><span data-stu-id="c968c-125">Restore Active Directory (if needed).</span></span>
5.  <span data-ttu-id="c968c-126">Ripristinare il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-126">Restore the registry.</span></span>

<span data-ttu-id="c968c-127">Alcuni servizi di sistema, ad esempio l'autorità di certificazione, hanno writer VSS convenzionali e seguono gli algoritmi di backup e ripristino VSS.</span><span class="sxs-lookup"><span data-stu-id="c968c-127">Some system services, such as the Certification Authority, have conventional VSS writers and follow the VSS backup and restore algorithms.</span></span> <span data-ttu-id="c968c-128">Altri, ad esempio il registro di sistema, richiedono operazioni di backup o ripristino personalizzate. per altre informazioni, vedere [backup e ripristini personalizzati](custom-backups-and-restores.md).</span><span class="sxs-lookup"><span data-stu-id="c968c-128">Others, such as the registry, require custom backup or restore operations; for more information, see [Custom Backups and Restores](custom-backups-and-restores.md).</span></span>

## <a name="vss-backup-and-restores-of-boot-and-system-files"></a><span data-ttu-id="c968c-129">Backup e ripristini VSS dei file di avvio e di sistema</span><span class="sxs-lookup"><span data-stu-id="c968c-129">VSS Backup and Restores of Boot and System Files</span></span>

<span data-ttu-id="c968c-130">È necessario eseguire il backup e il ripristino dei file di avvio e di sistema solo come singola entità.</span><span class="sxs-lookup"><span data-stu-id="c968c-130">The boot and system files should be backed up and restored only as a single entity.</span></span>

<span data-ttu-id="c968c-131">Un richiedente può utilizzare in modo sicuro versioni di questi file con copia shadow e verificare che il volume di sistema e il dispositivo di avvio siano [*copiati*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="c968c-131">A requester can safely use shadow-copied versions of these files, and should be sure that the system volume and boot device are [*shadow copied*](vssgloss-s.md).</span></span>

<span data-ttu-id="c968c-132">I file di sistema e di avvio includono:</span><span class="sxs-lookup"><span data-stu-id="c968c-132">The system and boot files include:</span></span>

-   <span data-ttu-id="c968c-133">I file di avvio principali:</span><span class="sxs-lookup"><span data-stu-id="c968c-133">The core boot files:</span></span> <dl> <span data-ttu-id="c968c-134">NtLdr.exe</span><span class="sxs-lookup"><span data-stu-id="c968c-134">NtLdr.exe</span></span>  
    <span data-ttu-id="c968c-135">Boot.ini</span><span class="sxs-lookup"><span data-stu-id="c968c-135">Boot.ini</span></span>  
    <span data-ttu-id="c968c-136">NtDetect.com</span><span class="sxs-lookup"><span data-stu-id="c968c-136">NtDetect.com</span></span>  
    <span data-ttu-id="c968c-137">NtBootDD.sys (se presente)</span><span class="sxs-lookup"><span data-stu-id="c968c-137">NtBootDD.sys (if present)</span></span>  
    </dl>
-   The WFP service catalog file must be backed up prior to backing up the WFP files, and it is found under: <dl> <span data-ttu-id="c968c-138">% SystemRoot% \\ system32 \\ Catroot \\ {F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span><span class="sxs-lookup"><span data-stu-id="c968c-138">%SystemRoot%\\System32\\CatRoot\\{F750E6C3-38EE-11D1-85E5-00C04FC295EE}</span></span> </dl><span data-ttu-id="c968c-139">
-   Tutti i file protetti dalla [\*protezione dei file di sistema*](vssgloss-s.md) ed enumerati da [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (vedere operazioni di ripristino VSS dei file protetti con WFP) -   i file di configurazione del contatore delle prestazioni:</span><span class="sxs-lookup"><span data-stu-id="c968c-139">
-   All files protected by [\*System File Protection*](vssgloss-s.md) and enumerated by [\*\*SfcGetNextProtectedFile**](/windows/win32/api/sfc/nf-sfc-sfcgetnextprotectedfile) (see VSS Restore Operations of WFP Protected Files) -   The Performance Counter Configuration files:</span></span> <dl> <span data-ttu-id="c968c-140">% SystemRoot% \\ system32 \\ ? 00?. dat</span><span class="sxs-lookup"><span data-stu-id="c968c-140">%SystemRoot%\\System32\\Perf?00?.dat</span></span>  
    <span data-ttu-id="c968c-141">% SystemRoot% \\ system32 \\ ? 00?. bak</span><span class="sxs-lookup"><span data-stu-id="c968c-141">%SystemRoot%\\System32\\Perf?00?.bak</span></span> </dl><span data-ttu-id="c968c-142">
-   Se presente, il file della metabase di Internet Information Server (IIS) deve essere incluso nelle operazioni di backup e ripristino perché contiene lo stato utilizzato da Microsoft Exchange e altre applicazioni di rete.</span><span class="sxs-lookup"><span data-stu-id="c968c-142">
-   If present, the Internet Information Server (IIS) metabase file should be included in backup and restore operations because it contains state that is used by Microsoft Exchange and other network applications.</span></span> <span data-ttu-id="c968c-143">Questo file è disponibile nel percorso:</span><span class="sxs-lookup"><span data-stu-id="c968c-143">This file can be found at:</span></span> <dl> <span data-ttu-id="c968c-144">% SystemRoot% \\ system32 \\ inetsrv \\ metabase. bin</span><span class="sxs-lookup"><span data-stu-id="c968c-144">%SystemRoot%\\System32\\InetSrv\\Metabase.bin</span></span> </dl><span data-ttu-id="c968c-145">
-   Se viene eseguito il backup del file della metabase IIS, le chiavi per consentire alle applicazioni di leggere determinate voci crittografate devono essere ripristinate come parte dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-145">
-   If the IIS metabase file is backed up, keys to enable applications to read certain encrypted entries should be restored as part of the system state.</span></span> <span data-ttu-id="c968c-146">I file sono disponibili in:</span><span class="sxs-lookup"><span data-stu-id="c968c-146">The files can be found under:</span></span> <dl> <span data-ttu-id="c968c-147">% SystemRoot% \\ system32 \\ Microsoft \\ Protect\\\*</span><span class="sxs-lookup"><span data-stu-id="c968c-147">%SystemRoot%\\System32\\Microsoft\\Protect\\\*</span></span>  
    <span data-ttu-id="c968c-148">% AllUsersProfile% \\ Microsoft \\ Crypto \\ RSA \\ MachineKeys\\\*</span><span class="sxs-lookup"><span data-stu-id="c968c-148">%AllUsersProfile%\\Microsoft\\Crypto\\RSA\\MachineKeys\\\*</span></span> </dl><span data-ttu-id="c968c-149">
-Quando si esegue il backup dei file di avvio e di sistema, potrebbe essere necessario determinare il dispositivo di avvio DOS eseguendo le operazioni seguenti: 1. trovare la partizione di sistema in \*\*HKEY \_ Local \_ Machine*\* \\ \*\*System*\* \\ \*\*Setup*\* \\ \*\*SYSTEMPARTITION\**.</span><span class="sxs-lookup"><span data-stu-id="c968c-149">
-   When backing up boot and system files, it may become necessary to determine the DOS boot device by doing the following: 1.  Find the system partition under \*\*HKEY\_LOCAL\_MACHINE\*\*\\*\*System\*\*\\*\*Setup\*\*\\*\*SystemPartition\**.</span></span>
    <span data-ttu-id="c968c-150">2.  Passare la variabile di ambiente radice del sistema (% SystemRoot%) al gestore del montaggio per ottenere il nome del dispositivo NT.</span><span class="sxs-lookup"><span data-stu-id="c968c-150">2.  Pass the System Root environment variable (%SystemRoot%) to the mount manager to obtain the NT device name.</span></span>

## <a name="vss-restore-operations-of-wfp-protected-files"></a><span data-ttu-id="c968c-151">Operazioni di ripristino VSS dei file protetti da WFP</span><span class="sxs-lookup"><span data-stu-id="c968c-151">VSS Restore Operations of WFP Protected Files</span></span>

<span data-ttu-id="c968c-152">Il servizio WFP è progettato per impedire la sostituzione accidentale o a fasi dei file di sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-152">The WFP service is designed to prevent accidental or piecemeal replacement of system files.</span></span> <span data-ttu-id="c968c-153">Pertanto, è necessario eseguire passaggi speciali per ripristinare i dati di WFP.</span><span class="sxs-lookup"><span data-stu-id="c968c-153">Therefore, special steps need to be undertaken to restore WFP data.</span></span>

<span data-ttu-id="c968c-154">Indica che il writer del servizio Copia Shadow del volume deve specificare il **\_ ripristino VSS RME \_ \_ al \_** Metodo Restore del ripristino durante la definizione del documento di metadati del writer.</span><span class="sxs-lookup"><span data-stu-id="c968c-154">The means the WFP writer should specify the **VSS\_RME\_RESTORE\_AT\_REBOOT** restore method when defining its Writer Metadata Document.</span></span> <span data-ttu-id="c968c-155">Se un richiedente determina che il writer del Pam non è stato in grado di specificare questo metodo di ripristino, significa che si è verificato un errore del writer.</span><span class="sxs-lookup"><span data-stu-id="c968c-155">If a requester determines that the WFP writer has failed to specify this restore method, it indicates a writer error.</span></span>

<span data-ttu-id="c968c-156">Un richiedente deve implementare un metodo Restore **del \_ ripristino VSS RME \_ \_ al \_ riavvio** usando la funzione Win32 [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) con il **ritardo MOVEFILE fino al parametro \_ \_ \_ reboot** per sostituire i file di sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-156">A requester should implement a restore method of **VSS\_RME\_RESTORE\_AT\_REBOOT** using the Win32 function [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) with the **MOVEFILE\_DELAY\_UNTIL\_REBOOT** parameter to replace system files.</span></span> <span data-ttu-id="c968c-157">I file ripristinati non vengono copiati nelle directory effettive dei file di sistema fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="c968c-157">The restored files are not copied into the actual system file directories until after system reboot.</span></span> <span data-ttu-id="c968c-158">La sovrascrittura dei file di sistema protetti verrà eseguita solo se il valore della voce **reg \_ Word** del registro di sistema seguente è impostato su 1:</span><span class="sxs-lookup"><span data-stu-id="c968c-158">The overwriting of protected system files will occur only if the value of the following **REG\_WORD** registry entry is set to 1:</span></span>

<span data-ttu-id="c968c-159">**HKEY \_ \_** \\  \\ Gestore sessioni **CurrentControlSet** controllo di sistema del computer locale \\  \\  \\ **AllowProtectedRenames** = 1</span><span class="sxs-lookup"><span data-stu-id="c968c-159">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Session Manager**\\**AllowProtectedRenames** = 1</span></span>

<span data-ttu-id="c968c-160">Questo valore deve essere impostato prima di qualsiasi avvio in cui i file protetti devono essere sostituiti tramite [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) e viene eliminato dopo il riavvio.</span><span class="sxs-lookup"><span data-stu-id="c968c-160">This value must be set before any boot where protected files are to be replaced via [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) and is deleted after reboot.</span></span>

<span data-ttu-id="c968c-161">È necessario eseguire il backup o il ripristino della directory dllcache di sistema, con backup e ripristino del volume di avvio, ed esaminando la voce del registro di sistema **reg \_ expand \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="c968c-161">The system dllcache directory should also be backed up or restored, with boot volume backup and restore, and is located by examining the **REG\_EXPAND\_SZ** registry entry:</span></span>

<span data-ttu-id="c968c-162">**HKEY \_ Software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **SfcDllCache**</span><span class="sxs-lookup"><span data-stu-id="c968c-162">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**SfcDllCache**</span></span><dl> <dt>

                  Data type
</dt> <dd>                  <span data-ttu-id="c968c-163">REG \_ Espandi \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c968c-163">REG\_EXPAND\_SZ</span></span></dd> </dl>

<span data-ttu-id="c968c-164">Il contenuto della directory dllcache di sistema viene ricompilato tramite il controllo file di sistema (SFC) dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="c968c-164">The contents of the system dllcache directory are rebuilt by using the System File Checker (SFC) from the command prompt:</span></span>

-   <span data-ttu-id="c968c-165">L'opzione **/scanonce** analizza tutti i file protetti all'avvio del sistema successivo.</span><span class="sxs-lookup"><span data-stu-id="c968c-165">The **/SCANONCE** option scans all protected files at the next system boot.</span></span>
-   <span data-ttu-id="c968c-166">L'opzione **/scannow** analizza immediatamente tutti i file protetti.</span><span class="sxs-lookup"><span data-stu-id="c968c-166">The **/SCANNOW** option scans all protected files immediately.</span></span>

<span data-ttu-id="c968c-167">Tutti i file protetti verranno analizzati e tutte le versioni non valide verranno sostituite nella directory e nel percorso dllcache.</span><span class="sxs-lookup"><span data-stu-id="c968c-167">All protected files will be scanned, and any versions that are not valid will be replaced in both the directory and dllcache location.</span></span>

<span data-ttu-id="c968c-168">Sono presenti quattro file che fanno parte del WFP che non possono essere ripristinati con i file WFP:</span><span class="sxs-lookup"><span data-stu-id="c968c-168">There are four files that are part of the WFP that cannot be restored with the WFP files:</span></span>

<dl> <span data-ttu-id="c968c-169">Ctl3dv2.dll</span><span class="sxs-lookup"><span data-stu-id="c968c-169">Ctl3dv2.dll</span></span>  
<span data-ttu-id="c968c-170">DtcSetup.exe</span><span class="sxs-lookup"><span data-stu-id="c968c-170">DtcSetup.exe</span></span>  
<span data-ttu-id="c968c-171">NtDll.dll</span><span class="sxs-lookup"><span data-stu-id="c968c-171">NtDll.dll</span></span>  
<span data-ttu-id="c968c-172">Smss.exe</span><span class="sxs-lookup"><span data-stu-id="c968c-172">Smss.exe</span></span>  
</dl>

<span data-ttu-id="c968c-173">Questi file consentono di ripristinare i file del WFP e, di conseguenza, esiste una dipendenza circolare.</span><span class="sxs-lookup"><span data-stu-id="c968c-173">These files help in the process of restoring the WFP files and as such there is a circular dependency.</span></span> <span data-ttu-id="c968c-174">Attualmente, non è possibile ripristinare questi file tranne che per reinstallare Windows.</span><span class="sxs-lookup"><span data-stu-id="c968c-174">Currently, there is no way to restore these files except to reinstall Windows.</span></span>

 

 
