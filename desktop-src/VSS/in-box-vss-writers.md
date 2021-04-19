---
description: Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows. Questi vengono definiti &\# 0034,&\# 0034; writer.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: VSS writer inclusi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310705"
---
# <a name="in-box-vss-writers"></a><span data-ttu-id="37d5c-104">VSS writer inclusi</span><span class="sxs-lookup"><span data-stu-id="37d5c-104">In-Box VSS Writers</span></span>

<span data-ttu-id="37d5c-105">Il sistema operativo Windows include un set di VSS writer responsabili dell'enumerazione dei dati necessari alle varie funzionalità Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="37d5c-106">Questi vengono definiti writer "in-box".</span><span class="sxs-lookup"><span data-stu-id="37d5c-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="37d5c-107">Il writer in-box di MSDE non è disponibile in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37d5c-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="37d5c-108">Al contrario, il writer SQL deve essere utilizzato per eseguire il backup di SQL Server database.</span><span class="sxs-lookup"><span data-stu-id="37d5c-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="37d5c-109">Solo SQL Server 2005 SP2 e versioni successive sono supportati in Windows Vista, Windows Server 2008 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="37d5c-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="37d5c-110">Writer VSS Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="37d5c-111">Writer di Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="37d5c-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="37d5c-112">Writer VSS di Active Directory Lightweight Directory Services (LDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="37d5c-113">Writer di Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="37d5c-114">Writer ripristino automatico di sistema (ASR)</span><span class="sxs-lookup"><span data-stu-id="37d5c-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="37d5c-115">Writer di Servizio trasferimento intelligente in background (BITS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="37d5c-116">Writer autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="37d5c-117">Writer del servizio cluster</span><span class="sxs-lookup"><span data-stu-id="37d5c-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="37d5c-118">Writer VSS Volume condiviso cluster (CSV)</span><span class="sxs-lookup"><span data-stu-id="37d5c-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="37d5c-119">Writer del database di registrazione della classe COM+</span><span class="sxs-lookup"><span data-stu-id="37d5c-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="37d5c-120">Writer Deduplicazione dati</span><span class="sxs-lookup"><span data-stu-id="37d5c-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="37d5c-121">Replica DFS (Distributed File System)</span><span class="sxs-lookup"><span data-stu-id="37d5c-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="37d5c-122">Writer di Dynamic Host Configuration Protocol (DHCP)</span><span class="sxs-lookup"><span data-stu-id="37d5c-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="37d5c-123">Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="37d5c-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="37d5c-124">Writer di Gestione risorse file server (FSRM)</span><span class="sxs-lookup"><span data-stu-id="37d5c-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="37d5c-125">Writer di Hyper-V</span><span class="sxs-lookup"><span data-stu-id="37d5c-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="37d5c-126">Writer di configurazione IIS</span><span class="sxs-lookup"><span data-stu-id="37d5c-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="37d5c-127">Writer metabase IIS</span><span class="sxs-lookup"><span data-stu-id="37d5c-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="37d5c-128">Writer di Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="37d5c-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="37d5c-129">Writer del servizio MSSearch</span><span class="sxs-lookup"><span data-stu-id="37d5c-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="37d5c-130">Writer VSS server dei criteri di servizio</span><span class="sxs-lookup"><span data-stu-id="37d5c-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="37d5c-131">Writer dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="37d5c-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="37d5c-132">Writer del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="37d5c-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="37d5c-133">Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="37d5c-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="37d5c-134">Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="37d5c-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="37d5c-135">Writer di ottimizzazione copia shadow</span><span class="sxs-lookup"><span data-stu-id="37d5c-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="37d5c-136">Writer del servizio di condivisione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="37d5c-137">Writer di sistema</span><span class="sxs-lookup"><span data-stu-id="37d5c-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="37d5c-138">Writer di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="37d5c-139">Writer archivio metadati VSS</span><span class="sxs-lookup"><span data-stu-id="37d5c-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="37d5c-140">Writer di servizi di distribuzione Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="37d5c-141">Writer database interno di Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="37d5c-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="37d5c-142">Writer WINS (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="37d5c-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="37d5c-143">Writer WMI</span><span class="sxs-lookup"><span data-stu-id="37d5c-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="37d5c-144">Writer VSS Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="37d5c-145">Questo writer segnala il file di database NTDS (NTDS. dit) e i file di log associati.</span><span class="sxs-lookup"><span data-stu-id="37d5c-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="37d5c-146">Questi file sono necessari per ripristinare correttamente il Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37d5c-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="37d5c-147">È presente un solo file NTDS. dit per controller di dominio e viene segnalato nei metadati del writer come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="37d5c-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="37d5c-148">Di seguito è riportato un esempio in cui viene illustrato come elencare i componenti nei metadati del writer:</span><span class="sxs-lookup"><span data-stu-id="37d5c-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="37d5c-149">Al momento del backup, il writer imposta l'ora di scadenza del backup nei metadati di backup del writer.</span><span class="sxs-lookup"><span data-stu-id="37d5c-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="37d5c-150">I richiedenti devono recuperare questi metadati usando [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto.</span><span class="sxs-lookup"><span data-stu-id="37d5c-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="37d5c-151">Impossibile ripristinare i database scaduti.</span><span class="sxs-lookup"><span data-stu-id="37d5c-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="37d5c-152">Se il computer che contiene il database NTDS è un controller di dominio, l'applicazione di backup deve sempre eseguire un backup dello stato del sistema in tutti i volumi contenenti informazioni critiche sullo stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="37d5c-153">Al momento del ripristino, l'applicazione deve prima riavviare il computer in modalità ripristino servizi directory e quindi eseguire un ripristino dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="37d5c-154">La stringa del nome del writer per questo writer è "NTDS".</span><span class="sxs-lookup"><span data-stu-id="37d5c-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="37d5c-155">L'ID del writer per questo writer è B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="37d5c-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="37d5c-156">Writer di Active Directory Federation Services</span><span class="sxs-lookup"><span data-stu-id="37d5c-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="37d5c-157">Questo writer segnala i file di dati di Active Directory Federation Services (ADFS).</span><span class="sxs-lookup"><span data-stu-id="37d5c-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="37d5c-158">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-159">La stringa del nome del writer per questo writer è "ADFS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="37d5c-160">L'ID del writer per questo writer è 772C45F8-AE01-4F94-940C-94961864ACAD.</span><span class="sxs-lookup"><span data-stu-id="37d5c-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="37d5c-161">Writer VSS di Active Directory Lightweight Directory Services (LDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="37d5c-162">Questo writer segnala il file di database ADAM (Adamntds. dit) e i file di log associati per ogni istanza nei dati% programmi% \\ Microsoft Adam \\ istanza *n* \\ , dove *N* è il numero di istanza di Adam.</span><span class="sxs-lookup"><span data-stu-id="37d5c-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="37d5c-163">Questi file di log del database sono necessari per ripristinare le istanze di ADAM.</span><span class="sxs-lookup"><span data-stu-id="37d5c-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="37d5c-164">**Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-165">Di seguito è riportato un esempio in cui viene illustrato come elencare i componenti nei metadati del writer:</span><span class="sxs-lookup"><span data-stu-id="37d5c-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

<span data-ttu-id="37d5c-166">Al momento del backup, il writer imposta l'ora di scadenza del backup nei metadati di backup.</span><span class="sxs-lookup"><span data-stu-id="37d5c-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="37d5c-167">Le applicazioni di backup devono recuperare questi metadati usando il metodo [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) per determinare se il database è scaduto.</span><span class="sxs-lookup"><span data-stu-id="37d5c-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="37d5c-168">Impossibile ripristinare i database scaduti.</span><span class="sxs-lookup"><span data-stu-id="37d5c-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="37d5c-169">La stringa del nome del writer per questo writer è "ADAM (instance *N*) writer", dove *N* è il numero di istanza di Adam, ad esempio, "Adam (instance1) writer", "Adam (Instance2) writer" e così via.</span><span class="sxs-lookup"><span data-stu-id="37d5c-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="37d5c-170">L'ID del writer per questo writer è DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="37d5c-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="37d5c-171">Questo ID writer è lo stesso per tutte le istanze.</span><span class="sxs-lookup"><span data-stu-id="37d5c-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="37d5c-172">Writer di Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="37d5c-173">Questo writer segnala i file di dati del servizio Active Directory Rights Management (AD RMS).</span><span class="sxs-lookup"><span data-stu-id="37d5c-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="37d5c-174">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-175">La stringa del nome del writer per questo writer è "AD RMS writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="37d5c-176">L'ID del writer per questo writer è 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span><span class="sxs-lookup"><span data-stu-id="37d5c-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="37d5c-177">Writer ripristino automatico di sistema (ASR)</span><span class="sxs-lookup"><span data-stu-id="37d5c-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="37d5c-178">Il writer ASR archivia la configurazione dei dischi nel sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="37d5c-179">Questo writer segnala il database di configurazione di avvio (BCD) ed è anche responsabile dello smontaggio dell'hive del registro di sistema che rappresenta il BCD durante la creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="37d5c-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="37d5c-180">Il writer di ASR deve essere incluso nei backup necessari per il ripristino bare metal.</span><span class="sxs-lookup"><span data-stu-id="37d5c-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="37d5c-181">Per ulteriori informazioni su ASR, vedere [utilizzo del ripristino automatico del sistema VSS per il ripristino di emergenza](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="37d5c-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="37d5c-182">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-183">La stringa del nome del writer per questo writer è "ASR writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="37d5c-184">L'ID writer per il writer ASR è BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="37d5c-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="37d5c-185">Writer di Servizio trasferimento intelligente in background (BITS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="37d5c-186">Il writer BITS usa la chiave del registro di sistema **FilesNotToBackup** per escludere i file dalla cartella della cache BITS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="37d5c-187">Il percorso predefinito della cache è% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ cache.</span><span class="sxs-lookup"><span data-stu-id="37d5c-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="37d5c-188">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-189">Inoltre, il writer BITS esclude i file seguenti dal backup: i file di stato BITS (Qmgr0. dat e Qmgr1. dat), il file di log di debug BITS e i file scaricati parzialmente.</span><span class="sxs-lookup"><span data-stu-id="37d5c-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="37d5c-190">Se il file di destinazione per il download BITS è un file SMB, è necessario che l'account client disponga di una relazione di trust con il server. in caso contrario, i backup potrebbero non riuscire.</span><span class="sxs-lookup"><span data-stu-id="37d5c-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="37d5c-191">La stringa del nome del writer per questo writer è "BITS writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="37d5c-192">L'ID del writer per il writer BITS è 4969D978-BE47-48B0-B100-F328F07AC1E0.</span><span class="sxs-lookup"><span data-stu-id="37d5c-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="37d5c-193">Writer autorità di certificazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-193">Certificate Authority Writer</span></span>

<span data-ttu-id="37d5c-194">Questo writer è responsabile dell'enumerazione dei file di dati per il server dei certificati.</span><span class="sxs-lookup"><span data-stu-id="37d5c-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="37d5c-195">La stringa del nome del writer per questo writer è "autorità di certificazione".</span><span class="sxs-lookup"><span data-stu-id="37d5c-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="37d5c-196">**Windows XP:** La stringa del nome del writer per questo writer è "Certificate Server Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="37d5c-197">L'ID del writer per il writer è 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span><span class="sxs-lookup"><span data-stu-id="37d5c-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="37d5c-198">Writer del servizio cluster</span><span class="sxs-lookup"><span data-stu-id="37d5c-198">Cluster Service Writer</span></span>

<span data-ttu-id="37d5c-199">Il VSS writer del servizio cluster è documentato nella documentazione dell'API del [servizio cluster](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .</span><span class="sxs-lookup"><span data-stu-id="37d5c-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="37d5c-200">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con Service Pack 1 (SP1) e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="37d5c-201">Writer VSS Volume condiviso cluster (CSV)</span><span class="sxs-lookup"><span data-stu-id="37d5c-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="37d5c-202">Questo writer segnala i file di dati di Volume condiviso cluster (CSV).</span><span class="sxs-lookup"><span data-stu-id="37d5c-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="37d5c-203">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-204">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-205">La stringa del nome del writer per questo writer è "Volume condiviso cluster VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="37d5c-206">L'ID del writer per il writer è 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span><span class="sxs-lookup"><span data-stu-id="37d5c-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="37d5c-207">Writer del database di registrazione della classe COM+</span><span class="sxs-lookup"><span data-stu-id="37d5c-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="37d5c-208">Questo writer è responsabile del contenuto della directory di registrazione% SystemRoot% \\ .</span><span class="sxs-lookup"><span data-stu-id="37d5c-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="37d5c-209">Il catalogo COM+ è un file nella registrazione% SystemRoot% \\ con un nome che segue il modello R *xxxxxxxxxxxx*. CLB, dove *xxxxxxxxxxxx* è un numero esadecimale a 12 cifre.</span><span class="sxs-lookup"><span data-stu-id="37d5c-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="37d5c-210">Se le applicazioni COM+ sono state configurate nel computer, potrebbero essere presenti più file di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="37d5c-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="37d5c-211">Il file che contiene il catalogo COM+ corrente è il file con il valore più grande di *xxxxxxxxxxxx*.</span><span class="sxs-lookup"><span data-stu-id="37d5c-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="37d5c-212">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-213">Il database di registrazione della classe COM+ dipende da una chiave del registro di sistema di cui viene eseguito il backup e che pertanto deve essere sottoposta a backup e ripristino insieme al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="37d5c-214">Per ripristinare il database di registrazione COM+, un'applicazione di backup (richiedente) deve chiamare il metodo [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="37d5c-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="37d5c-215">La stringa del nome del writer per questo writer è "COM+ REGDB writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="37d5c-216">L'ID del writer per il writer del database di registrazione della classe COM+ è 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span><span class="sxs-lookup"><span data-stu-id="37d5c-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="37d5c-217">Writer Deduplicazione dati</span><span class="sxs-lookup"><span data-stu-id="37d5c-217">Data Deduplication Writer</span></span>

<span data-ttu-id="37d5c-218">Il VSS writer di deduplicazione dati è documentato nella documentazione dell'API [Deduplicazione dati](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) .</span><span class="sxs-lookup"><span data-stu-id="37d5c-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="37d5c-219">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-220">**Windows server 2008 R2, Windows server 2008 e Windows server 2003:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="37d5c-221">Replica DFS (Distributed File System)</span><span class="sxs-lookup"><span data-stu-id="37d5c-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="37d5c-222">Il componente seguente include un VSS writer: [replica file System distribuito (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="37d5c-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="37d5c-223">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="37d5c-224">Writer di Dynamic Host Configuration Protocol (DHCP)</span><span class="sxs-lookup"><span data-stu-id="37d5c-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="37d5c-225">Questo writer è responsabile dell'enumerazione dei file necessari per il ruolo server DHCP.</span><span class="sxs-lookup"><span data-stu-id="37d5c-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="37d5c-226">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-227">La stringa del nome del writer per questo writer è "DHCP Jet writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="37d5c-228">L'ID del writer per questo writer è BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="37d5c-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="37d5c-229">Servizio Replica file</span><span class="sxs-lookup"><span data-stu-id="37d5c-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="37d5c-230">Il writer del servizio Replica file è documentato per il [backup e il ripristino di una cartella FRS-Replicated SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span><span class="sxs-lookup"><span data-stu-id="37d5c-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="37d5c-231">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="37d5c-232">Writer di Gestione risorse file server (FSRM)</span><span class="sxs-lookup"><span data-stu-id="37d5c-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="37d5c-233">Questo writer enumera i file di configurazione FSRM usati per il backup dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="37d5c-234">Durante le operazioni di ripristino, impedisce le modifiche nella configurazione di FSRM e interrompe temporaneamente l'applicazione di quote e schermate di file.</span><span class="sxs-lookup"><span data-stu-id="37d5c-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="37d5c-235">Al termine del ripristino, il writer Aggiorna FSRM con la configurazione che è stata ripristinata.</span><span class="sxs-lookup"><span data-stu-id="37d5c-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="37d5c-236">Questo writer è presente solo quando FSRM (parte del ruolo Servizi file) è installato e in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="37d5c-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="37d5c-237">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-238">**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="37d5c-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="37d5c-239">La stringa del nome del writer per questo writer è "FSRM writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="37d5c-240">L'ID del writer per questo writer è 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span><span class="sxs-lookup"><span data-stu-id="37d5c-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="37d5c-241">Writer di Hyper-V</span><span class="sxs-lookup"><span data-stu-id="37d5c-241">Hyper-V Writer</span></span>

<span data-ttu-id="37d5c-242">Il VSS writer di Hyper-V è documentato nella documentazione dell'API di [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) .</span><span class="sxs-lookup"><span data-stu-id="37d5c-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="37d5c-243">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-244">**Windows Server 2003:** Questo writer non è supportato fino a Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="37d5c-245">Writer di configurazione IIS</span><span class="sxs-lookup"><span data-stu-id="37d5c-245">IIS Configuration Writer</span></span>

<span data-ttu-id="37d5c-246">Il writer di configurazione di IIS è responsabile dell'enumerazione dei file di configurazione di IIS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="37d5c-247">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="37d5c-248">I richiedenti sono necessari per eseguire il backup dei file di configurazione di IIS, incluso il file di machine.config .NET FX o il file di web.config radice ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="37d5c-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="37d5c-249">Questo writer non esegue il backup del file di machine.config .NET FX o del file web.config radice di ASP.NET perché questi file sono enumerati dal writer di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="37d5c-250">Questo writer esegue il backup di tutti i file presenti nello schema di configurazione% windir% \\ system32 \\ inetsrv \\ e di \\ % windir% \\ system32 \\ inetsrv \\ config directory, ad eccezione dei file enumerati dal writer di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="37d5c-251">L'ID writer per il writer di configurazione IIS è 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span><span class="sxs-lookup"><span data-stu-id="37d5c-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="37d5c-252">Writer metabase IIS</span><span class="sxs-lookup"><span data-stu-id="37d5c-252">IIS Metabase Writer</span></span>

<span data-ttu-id="37d5c-253">Il writer della metabase di Internet Information Server (IIS) è responsabile dell'enumerazione del file della metabase di IIS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="37d5c-254">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="37d5c-255">I richiedenti sono necessari per eseguire il backup del file della metabase di IIS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="37d5c-256">L'ID del writer per il writer della metabase di IIS è 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span><span class="sxs-lookup"><span data-stu-id="37d5c-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="37d5c-257">Writer di Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="37d5c-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="37d5c-258">Questo writer segnala i file di dati di Microsoft Message Queuing (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="37d5c-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="37d5c-259">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-260">La stringa del nome del writer per questo writer è "MSMQ Writer (*SvcName*)", dove *SvcName* è il nome del servizio MSMQ a cui è associato il writer.</span><span class="sxs-lookup"><span data-stu-id="37d5c-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="37d5c-261">Per l'installazione predefinita, il nome del servizio è "MSMQ".</span><span class="sxs-lookup"><span data-stu-id="37d5c-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="37d5c-262">Per le istanze cluster, il nome del servizio è MSMQ $*resourceName*, dove *resourceName* è il nome della risorsa MSMQ in cluster.</span><span class="sxs-lookup"><span data-stu-id="37d5c-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="37d5c-263">L'ID del writer per questo writer è 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span><span class="sxs-lookup"><span data-stu-id="37d5c-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="37d5c-264">Writer del servizio MSSearch</span><span class="sxs-lookup"><span data-stu-id="37d5c-264">MSSearch Service Writer</span></span>

<span data-ttu-id="37d5c-265">Questo writer esiste per eliminare i file di indice di ricerca dalle copie shadow dopo la creazione.</span><span class="sxs-lookup"><span data-stu-id="37d5c-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="37d5c-266">Questa operazione viene eseguita per ridurre al minimo l'effetto delle operazioni di I/O copy-on-Write durante le operazioni di I/o regolari su questi file nel volume copiato Shadow.</span><span class="sxs-lookup"><span data-stu-id="37d5c-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="37d5c-267">**Windows Server 2003:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-268">Per installare questo writer nel server, è necessario installare il ruolo Servizi file e abilitare Windows servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="37d5c-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="37d5c-269">La stringa del nome del writer per questo writer è "MSSearch Service writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="37d5c-270">L'ID writer per il writer del servizio MSSearch è CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="37d5c-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="37d5c-271">Writer VSS server dei criteri di servizio</span><span class="sxs-lookup"><span data-stu-id="37d5c-271">NPS VSS Writer</span></span>

<span data-ttu-id="37d5c-272">Il writer NPS è responsabile dell'enumerazione dei file di configurazione del server dei criteri di rete (NPS) per i server in cui è installato il ruolo Servizi di accesso e criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="37d5c-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="37d5c-273">**Windows Vista, Windows Server 2003 e Windows XP:** Questo writer non è supportato fino a Windows Vista con SP1 e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="37d5c-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="37d5c-274">La stringa del nome del writer per questo writer è "NPS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="37d5c-275">L'ID del writer per la VSS writer NPS è 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="37d5c-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="37d5c-276">Writer dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="37d5c-276">Performance Counters Writer</span></span>

<span data-ttu-id="37d5c-277">Questo writer segnala i file di configurazione del contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="37d5c-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="37d5c-278">Questi file vengono modificati solo durante l'installazione dell'applicazione ed è necessario eseguirne il backup e il ripristino durante i backup e i ripristini dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="37d5c-279">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="37d5c-280">I richiedenti sono necessari per eseguire manualmente il backup di questi file.</span><span class="sxs-lookup"><span data-stu-id="37d5c-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="37d5c-281">(Vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md)).</span><span class="sxs-lookup"><span data-stu-id="37d5c-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="37d5c-282">La stringa del nome del writer per questo writer è "performance counters writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="37d5c-283">L'ID writer per il writer dei contatori delle prestazioni è 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span><span class="sxs-lookup"><span data-stu-id="37d5c-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="37d5c-284">Writer del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="37d5c-284">Registry Writer</span></span>

<span data-ttu-id="37d5c-285">Il writer del registro di sistema segnala i file del registro di sistema di Windows per abilitare i backup sul posto e il ripristino del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="37d5c-286">Non segnala gli hive degli utenti.</span><span class="sxs-lookup"><span data-stu-id="37d5c-286">It does not report user hives.</span></span>

<span data-ttu-id="37d5c-287">**Windows Server 2003:** In Windows Server 2003, questo writer usa un file di repository intermedio (talvolta denominato "file spit") per archiviare i dati del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="37d5c-288">(Vedere [operazioni di backup e ripristino del registro di sistema in VSS](registry-backup-and-restore-operations-under-vss.md)).</span><span class="sxs-lookup"><span data-stu-id="37d5c-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="37d5c-289">**Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="37d5c-290">(Vedere [operazioni di backup e ripristino del registro di sistema in VSS](registry-backup-and-restore-operations-under-vss.md)).</span><span class="sxs-lookup"><span data-stu-id="37d5c-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="37d5c-291">La stringa del nome del writer per questo writer è "Registry writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="37d5c-292">L'ID del writer per il writer del registro di sistema è AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="37d5c-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="37d5c-293">Writer VSS del gateway Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="37d5c-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="37d5c-294">Questo writer è responsabile dell'enumerazione dei file del gateway Servizi Desktop remoto (Servizi terminal) per i server con Desktop remoto Gateway, un sottoruolo del ruolo Servizi Desktop remoto, installato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="37d5c-295">**Windows Server 2003:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-296">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-297">Il gateway Servizi Desktop remoto dipende da diverse chiavi del registro di sistema di cui viene eseguito il backup e pertanto deve essere eseguito il backup e il ripristino insieme al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="37d5c-298">La stringa del nome del writer per questo writer è "TS Gateway writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="37d5c-299">L'ID del writer per questo writer è 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span><span class="sxs-lookup"><span data-stu-id="37d5c-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="37d5c-300">Writer VSS di gestione licenze Servizi Desktop remoto (Servizi terminal)</span><span class="sxs-lookup"><span data-stu-id="37d5c-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="37d5c-301">Questo writer è responsabile dell'enumerazione dei file Servizi Desktop remoto Licensing (licenze Desktop remoto) o licenze Servizi terminal (licenze Servizi terminal) per i server che dispongono di licenze Desktop remoto, un sottoruolo del ruolo Servizi Desktop remoto, installato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="37d5c-302">**Windows Server 2003:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-303">Questo writer è un writer in-box per le versioni del sistema operativo Windows Server. non viene fornito nel client Windows.</span><span class="sxs-lookup"><span data-stu-id="37d5c-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="37d5c-304">Servizi Desktop remoto le licenze dipendono da diverse chiavi del registro di sistema di cui viene eseguito il backup e pertanto devono essere sottoposte a backup e ripristinate insieme al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="37d5c-305">La stringa del nome del writer per questo writer è "TermServLicensing".</span><span class="sxs-lookup"><span data-stu-id="37d5c-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="37d5c-306">L'ID del writer per questo writer è 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span><span class="sxs-lookup"><span data-stu-id="37d5c-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="37d5c-307">Writer di ottimizzazione copia shadow</span><span class="sxs-lookup"><span data-stu-id="37d5c-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="37d5c-308">Questo writer Elimina alcuni file dalle copie shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="37d5c-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="37d5c-309">Questa operazione viene eseguita per ridurre al minimo l'effetto delle operazioni di I/O copy-on-Write durante le operazioni di I/o regolari su questi file nel volume copiato Shadow.</span><span class="sxs-lookup"><span data-stu-id="37d5c-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="37d5c-310">I file eliminati sono in genere file temporanei o file che non contengono l'utente o lo stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="37d5c-311">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-312">La stringa del nome del writer per questo writer è "writer di ottimizzazione per la copia shadow".</span><span class="sxs-lookup"><span data-stu-id="37d5c-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="37d5c-313">L'ID del writer per il writer di ottimizzazione della copia shadow è 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span><span class="sxs-lookup"><span data-stu-id="37d5c-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="37d5c-314">Writer del servizio di condivisione di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-314">Sync Share Service Writer</span></span>

<span data-ttu-id="37d5c-315">**Windows Server 2012 R2:** Questo writer è incluso in Windows Server 2012 R2 e versioni più recenti del server.</span><span class="sxs-lookup"><span data-stu-id="37d5c-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="37d5c-316">Non è compatibile con le versioni desktop.</span><span class="sxs-lookup"><span data-stu-id="37d5c-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="37d5c-317">Questo writer è responsabile dell'enumerazione delle condivisioni di sincronizzazione nei server in cui è installato il servizio di condivisione di sincronizzazione e per garantire che i metadati e i dati rimangano coerenti durante il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="37d5c-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="37d5c-318">Questo writer è presente solo quando il servizio di condivisione di sincronizzazione è installato e in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="37d5c-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="37d5c-319">Ci sarà un componente VSS writer per ogni condivisione di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="37d5c-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="37d5c-320">Sono inclusi i metadati e i percorsi dati.</span><span class="sxs-lookup"><span data-stu-id="37d5c-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="37d5c-321">È necessario eseguirne il backup insieme per verificarne la coerenza.</span><span class="sxs-lookup"><span data-stu-id="37d5c-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="37d5c-322">La stringa del nome del writer è "Sync Share service VSS writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="37d5c-323">L'ID del writer è D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="37d5c-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="37d5c-324">Writer di sistema</span><span class="sxs-lookup"><span data-stu-id="37d5c-324">System Writer</span></span>

<span data-ttu-id="37d5c-325">Il writer di sistema enumera tutti i file binari del sistema operativo e dei driver ed è necessario per il backup dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="37d5c-326">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-327">Questo writer viene eseguito come parte del servizio servizi di crittografia (CryptSvc).</span><span class="sxs-lookup"><span data-stu-id="37d5c-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="37d5c-328">Il writer di sistema genera un elenco di file che contiene i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="37d5c-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="37d5c-329">Tutti i file statici installati.</span><span class="sxs-lookup"><span data-stu-id="37d5c-329">All static files that have been installed.</span></span> <span data-ttu-id="37d5c-330">Un file statico è un file elencato nel manifesto del componente con l'attributo del file **attributo writeableType** impostato su "static" o "".</span><span class="sxs-lookup"><span data-stu-id="37d5c-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="37d5c-331">I file statici includono tutti i file protetti da Protezione risorse di Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="37d5c-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="37d5c-332">Tuttavia, non tutti i file statici sono file protetti con WRP.</span><span class="sxs-lookup"><span data-stu-id="37d5c-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="37d5c-333">Ad esempio, i file di gioco sono statici, ma non protetti da WRP, in modo che gli amministratori possano modificare le impostazioni di controllo padre.</span><span class="sxs-lookup"><span data-stu-id="37d5c-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="37d5c-334">Il contenuto della directory side-by-side di Windows (WinSxS), inclusi tutti i manifesti, i componenti facoltativi e i file Win32 di terze parti.</span><span class="sxs-lookup"><span data-stu-id="37d5c-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="37d5c-335">Molti dei file nella directory% windir% \\ System32 sono collegamenti reali a file nella directory WinSxS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="37d5c-336">Tutti i file PnP per i driver installati (di proprietà di PnP).</span><span class="sxs-lookup"><span data-stu-id="37d5c-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="37d5c-337">Tutti i servizi in modalità utente e i driver non PnP.</span><span class="sxs-lookup"><span data-stu-id="37d5c-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="37d5c-338">Tutti i cataloghi di proprietà di CryptSvc.</span><span class="sxs-lookup"><span data-stu-id="37d5c-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="37d5c-339">L'applicazione di ripristino è responsabile della disinstallazione dei file e del registro di sistema e dell'impostazione degli ACL in modo che corrispondano alla copia shadow di sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="37d5c-340">Per avere esito positivo, è necessario creare anche i collegamenti reali appropriati per il ripristino dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="37d5c-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="37d5c-341">La stringa del nome del writer per questo writer è "System Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="37d5c-342">L'ID writer per il writer di sistema è E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="37d5c-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="37d5c-343">Writer di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="37d5c-343">Task Scheduler Writer</span></span>

<span data-ttu-id="37d5c-344">Questo writer segnala i file delle attività dell'utilità di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="37d5c-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="37d5c-345">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="37d5c-346">I richiedenti sono necessari per eseguire manualmente il backup di questi file.</span><span class="sxs-lookup"><span data-stu-id="37d5c-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="37d5c-347">(Vedere [backup e ripristino dello stato del sistema](locating-additional-system-files.md)).</span><span class="sxs-lookup"><span data-stu-id="37d5c-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="37d5c-348">La stringa del nome del writer per questo writer è "Utilità di pianificazione writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="37d5c-349">L'ID del writer per il writer è D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="37d5c-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="37d5c-350">Writer archivio metadati VSS</span><span class="sxs-lookup"><span data-stu-id="37d5c-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="37d5c-351">Questo writer segnala i file di metadati del writer per tutti i writer VSS Express.</span><span class="sxs-lookup"><span data-stu-id="37d5c-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="37d5c-352">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-353">La stringa del nome del writer per questo writer è "writer dell'archivio di metadati di VSS Express writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="37d5c-354">L'ID del writer per il writer è 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span><span class="sxs-lookup"><span data-stu-id="37d5c-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="37d5c-355">Writer di servizi di distribuzione Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="37d5c-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="37d5c-356">Questo writer segnala i file di dati di servizi di distribuzione Windows (WDS).</span><span class="sxs-lookup"><span data-stu-id="37d5c-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="37d5c-357">**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-358">La stringa del nome del writer per questo writer è "WDS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="37d5c-359">L'ID del writer per questo writer è 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span><span class="sxs-lookup"><span data-stu-id="37d5c-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="37d5c-360">Writer database interno di Windows (WID)</span><span class="sxs-lookup"><span data-stu-id="37d5c-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="37d5c-361">Questo writer segnala i file di dati del database interno di Windows (WID).</span><span class="sxs-lookup"><span data-stu-id="37d5c-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="37d5c-362">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-363">La stringa del nome del writer per questo writer è "WIDWriter".</span><span class="sxs-lookup"><span data-stu-id="37d5c-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="37d5c-364">L'ID del writer per questo writer è 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span><span class="sxs-lookup"><span data-stu-id="37d5c-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="37d5c-365">Writer WINS (Windows Internet Name Service)</span><span class="sxs-lookup"><span data-stu-id="37d5c-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="37d5c-366">Questo writer è responsabile dell'enumerazione dei file richiesti per WINS.</span><span class="sxs-lookup"><span data-stu-id="37d5c-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="37d5c-367">**Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-368">La stringa del nome del writer per questo writer è "WINS Jet writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="37d5c-369">L'ID del writer per questo writer è F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="37d5c-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="37d5c-370">Writer WMI</span><span class="sxs-lookup"><span data-stu-id="37d5c-370">WMI Writer</span></span>

<span data-ttu-id="37d5c-371">Questo writer viene utilizzato per identificare lo stato e i dati specifici di WMI durante le operazioni di backup.</span><span class="sxs-lookup"><span data-stu-id="37d5c-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="37d5c-372">I dati includono i file del repository WBEM.</span><span class="sxs-lookup"><span data-stu-id="37d5c-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="37d5c-373">**Windows Server 2003 e Windows XP:** Questo writer non è supportato.</span><span class="sxs-lookup"><span data-stu-id="37d5c-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="37d5c-374">La stringa del nome del writer per questo writer è "WMI writer".</span><span class="sxs-lookup"><span data-stu-id="37d5c-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="37d5c-375">L'ID del writer per questo writer è A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="37d5c-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
