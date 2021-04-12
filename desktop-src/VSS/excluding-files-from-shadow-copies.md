---
description: In Windows Vista e Windows Server 2008 e versioni successive lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.
ms.assetid: 4fe1ae94-7b2f-421a-9009-3a7e88822458
title: Esclusione di file dalle copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52546c8ddc6da62433dc610f2bf4fc2c46c5e53f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233825"
---
# <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="d0a03-103">Esclusione di file dalle copie shadow</span><span class="sxs-lookup"><span data-stu-id="d0a03-103">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="d0a03-104">In Windows Vista e Windows Server 2008 e versioni successive lo sviluppatore di un VSS writer o di un'applicazione può scegliere di escludere determinati file dalle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-104">In Windows Vista and Windows Server 2008 and later, the developer of a VSS writer or application may choose to exclude certain files from shadow copies.</span></span>

<span data-ttu-id="d0a03-105">L'utilizzo dell'area di archiviazione delle copie shadow e dell'effetto sulle prestazioni (detto anche "area diff") di un file in una copia shadow è direttamente correlato alla quantità di modifiche apportate al contenuto del file dopo la creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-105">The performance impact and shadow copy storage area (also called "diff area") usage of a file in a shadow copy are directly related to the amount of change in the file's contents after the shadow copy is created.</span></span> <span data-ttu-id="d0a03-106">Inoltre, l'esclusione dei file dalle copie shadow può rallentare la creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-106">In addition, excluding files from shadow copies may slow down shadow copy creation.</span></span>

<span data-ttu-id="d0a03-107">Per questi motivi, un file deve essere escluso dalle copie shadow solo se è di grandi dimensioni, subisce una modifica significativa tra una copia shadow e la successiva e non è necessario eseguirne il backup.</span><span class="sxs-lookup"><span data-stu-id="d0a03-107">For these reasons, a file should be excluded from shadow copies only if it is large, undergoes significant change between one shadow copy and the next, and does not need to be backed up.</span></span>

<span data-ttu-id="d0a03-108">È necessario escludere solo i file che appartengono all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d0a03-108">You should only exclude files that belong to your application.</span></span>

<span data-ttu-id="d0a03-109">Se \_ \_ \_ \_ nel contesto della copia shadow non è impostato il flag VolSnap attr senza recupero automatico, significa che il ripristino automatico è disabilitato e non è possibile escludere alcun file dalla copia shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-109">If the VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY flag is set in the shadow copy context, this means that auto-recovery is disabled, and no files can be excluded from the shadow copy.</span></span> <span data-ttu-id="d0a03-110">Per ulteriori informazioni, vedere l'enumerazione [**\_ VSS \_ volume \_ snapshot \_ Attributes**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) .</span><span class="sxs-lookup"><span data-stu-id="d0a03-110">For more information, see the [**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration.</span></span>

## <a name="using-the-addexcludefilesfromsnapshot-method"></a><span data-ttu-id="d0a03-111">Utilizzo del metodo AddExcludeFilesFromSnapshot</span><span class="sxs-lookup"><span data-stu-id="d0a03-111">Using the AddExcludeFilesFromSnapshot Method</span></span>

<span data-ttu-id="d0a03-112">Un VSS writer può escludere i file da una copia shadow come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d0a03-112">A VSS writer can exclude files from a shadow copy as follows:</span></span>

1.  <span data-ttu-id="d0a03-113">Chiamare il metodo [**IVssCreateWriterMetadataEx:: AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) per segnalare i file da escludere.</span><span class="sxs-lookup"><span data-stu-id="d0a03-113">Call the [**IVssCreateWriterMetadataEx::AddExcludeFilesFromSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadataex-addexcludefilesfromsnapshot) method to report the files to be excluded.</span></span>
2.  <span data-ttu-id="d0a03-114">Nel metodo [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) del writer eliminare i file dalla copia shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-114">In the writer's [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) method, delete the files from the shadow copy.</span></span>

## <a name="using-the-filesnottosnapshot-registry-key"></a><span data-ttu-id="d0a03-115">Uso della chiave del registro di sistema FilesNotToSnapshot</span><span class="sxs-lookup"><span data-stu-id="d0a03-115">Using the FilesNotToSnapshot Registry Key</span></span>

> [!Note]  
> <span data-ttu-id="d0a03-116">La chiave del Registro di sistema **FilesNotToSnapshot** deve essere usata solo dalle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d0a03-116">The **FilesNotToSnapshot** registry key is intended to be used only by applications.</span></span> <span data-ttu-id="d0a03-117">Gli utenti che tentano di usarla incontreranno limitazioni come le seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0a03-117">Users who attempt to use it will encounter limitations such as the following:</span></span>
>
> -   <span data-ttu-id="d0a03-118">Non è possibile eliminare file da una copia shadow creata in un server Windows usando la funzionalità Versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d0a03-118">It cannot delete files from a shadow copy that was created on a Windows Server by using the Previous Versions feature.</span></span>
> -   <span data-ttu-id="d0a03-119">Non è possibile eliminare file dalle copie shadow per cartelle condivise.</span><span class="sxs-lookup"><span data-stu-id="d0a03-119">It cannot delete files from shadow copies for shared folders.</span></span>
> -   <span data-ttu-id="d0a03-120">Consente di eliminare i file da una copia shadow creata con l'utilità [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) , ma non di eliminare i file da una copia shadow creata tramite l'utilità [vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="d0a03-120">It can delete files from a shadow copy that was created by using the [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) utility, but it cannot delete files from a shadow copy that was created by using the [Vssadmin](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) utility.</span></span>
> -   <span data-ttu-id="d0a03-121">I file vengono eliminati da una copia shadow in base al massimo sforzo.</span><span class="sxs-lookup"><span data-stu-id="d0a03-121">Files are deleted from a shadow copy on a best-effort basis.</span></span> <span data-ttu-id="d0a03-122">Ciò significa che non è garantito che vengano eliminati.</span><span class="sxs-lookup"><span data-stu-id="d0a03-122">This means that they are not guaranteed to be deleted.</span></span>

 

<span data-ttu-id="d0a03-123">Un'applicazione VSS può eliminare i file da una copia shadow durante la creazione della copia shadow utilizzando la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="d0a03-123">A VSS application can delete files from a shadow copy during shadow copy creation by using the following registry key:</span></span>

<span data-ttu-id="d0a03-124">**HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ backuprestore \\ FilesNotToSnapshot**</span><span class="sxs-lookup"><span data-stu-id="d0a03-124">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\BackupRestore\\FilesNotToSnapshot**</span></span>

<span data-ttu-id="d0a03-125">Questa chiave del registro di sistema contiene \_ \_ i valori reg multisz per ogni applicazione i cui file possono essere esclusi.</span><span class="sxs-lookup"><span data-stu-id="d0a03-125">This registry key has REG\_MULTI\_SZ values for each application whose files can be excluded.</span></span> <span data-ttu-id="d0a03-126">I file vengono specificati da percorsi completi che possono contenere il \* carattere jolly.</span><span class="sxs-lookup"><span data-stu-id="d0a03-126">The files are specified by fully qualified paths, which can contain the \* wildcard.</span></span>

<span data-ttu-id="d0a03-127">In tutti i casi, la voce viene ignorata se non sono presenti file che corrispondono alla stringa di percorso.</span><span class="sxs-lookup"><span data-stu-id="d0a03-127">In all cases, the entry is ignored if there are no files that match the path string.</span></span>

<span data-ttu-id="d0a03-128">Dopo l'aggiunta di un file al valore appropriato della chiave del registro di sistema, questo viene eliminato dalla copia shadow durante la creazione da parte del writer di ottimizzazione della copia shadow nel modo più semplice possibile.</span><span class="sxs-lookup"><span data-stu-id="d0a03-128">After a file is added to the appropriate registry key value, it is deleted from the shadow copy during creation by the shadow copy optimization writer on a best-effort basis.</span></span>

<span data-ttu-id="d0a03-129">Se non è possibile specificare un percorso completo, è possibile usare anche un percorso usando la variabile $UserProfile $ o $AllVolumes $.</span><span class="sxs-lookup"><span data-stu-id="d0a03-129">If a fully qualified path cannot be specified, then a path can also be implied by using the $UserProfile$ or $AllVolumes$ variable.</span></span> <span data-ttu-id="d0a03-130">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d0a03-130">For example:</span></span>

-   <span data-ttu-id="d0a03-131">\\ \\ Nome file della sottodirectory $USERPROFILE $ directory \\ .\*</span><span class="sxs-lookup"><span data-stu-id="d0a03-131">$UserProfile$\\Directory\\Subdirectory\\FileName.\*</span></span>
-   <span data-ttu-id="d0a03-132">$AllVolumes $ \\ TemporaryFiles \\ \* .\*</span><span class="sxs-lookup"><span data-stu-id="d0a03-132">$AllVolumes$\\TemporaryFiles\\\*.\*</span></span>

<span data-ttu-id="d0a03-133">Per rendere ricorsivo il percorso, aggiungere "/s" alla fine.</span><span class="sxs-lookup"><span data-stu-id="d0a03-133">To make the path recursive, append " /s" to the end.</span></span> <span data-ttu-id="d0a03-134">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="d0a03-134">For example:</span></span>

-   <span data-ttu-id="d0a03-135">$UserProfile $ \\ directory \\ subdirectory \\ filename. \* /s</span><span class="sxs-lookup"><span data-stu-id="d0a03-135">$UserProfile$\\Directory\\Subdirectory\\FileName.\* /s</span></span>
-   <span data-ttu-id="d0a03-136">$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s</span><span class="sxs-lookup"><span data-stu-id="d0a03-136">$AllVolumes$\\TemporaryFiles\\\*.\* /s</span></span>

<span data-ttu-id="d0a03-137">La variabile $UserProfile $ fa sì che la stringa di percorso venga applicata a tutti i profili utente nel computer.</span><span class="sxs-lookup"><span data-stu-id="d0a03-137">The $UserProfile$ variable causes the path string to be applied to all user profiles on the computer.</span></span> <span data-ttu-id="d0a03-138">Per enumerare i profili utente, esaminare la seguente chiave del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="d0a03-138">The user profiles are enumerated by examining the following registry key:</span></span>

<span data-ttu-id="d0a03-139">**HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Profiler**</span><span class="sxs-lookup"><span data-stu-id="d0a03-139">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\ProfileList**</span></span>

<span data-ttu-id="d0a03-140">La variabile $AllVolumes $ fa sì che la stringa di percorso venga applicata a tutte le copie shadow nel computer.</span><span class="sxs-lookup"><span data-stu-id="d0a03-140">The $AllVolumes$ variable causes the path string to be applied to all shadow copies on the computer.</span></span> <span data-ttu-id="d0a03-141">Si supponga, ad esempio, che il percorso sia "$AllVolumes $ \\ TemporaryFiles \\ \* . \* /s "e il computer dispone di tre volumi: C:, D: e E:.</span><span class="sxs-lookup"><span data-stu-id="d0a03-141">For example, suppose the path is "$AllVolumes$\\TemporaryFiles\\\*.\* /s", and the computer has three volumes: C:, D:, and E:.</span></span> <span data-ttu-id="d0a03-142">Se C: e e: contengono il percorso " \\ TemporaryFiles \\ " e volume d: contiene solo il percorso D: \\ dati \\ , l'albero di directory C: \\ TemporaryFiles \\ viene eliminato dalle copie shadow di c: e la struttura di directory e: \\ TemporaryFiles \\ viene eliminata dalle copie shadow di E:.</span><span class="sxs-lookup"><span data-stu-id="d0a03-142">If C: and E: contain the path "\\TemporaryFiles\\", and volume D: contains only the path D:\\Data\\, the directory tree C:\\TemporaryFiles\\ is deleted from shadow copies of C:, and the directory tree E:\\TemporaryFiles\\ is deleted from shadow copies of E:.</span></span>

<span data-ttu-id="d0a03-143">Gli amministratori possono disabilitare l'espansione della variabile $UserProfile $ usando la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="d0a03-143">Administrators can disable expansion of the $UserProfile$ variable by using the following registry key:</span></span>

<span data-ttu-id="d0a03-144">**\_Impostazioni del \_ servizio Copia Shadow del volume del \\ sistema \\ CurrentControlSet \\ \\ \\ HKEY**</span><span class="sxs-lookup"><span data-stu-id="d0a03-144">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services\\Vss\\Settings**</span></span>

<span data-ttu-id="d0a03-145">In questa chiave del registro di sistema specificare DisableUserProfileExpansion per il nome del valore, REG \_ DWORD per il tipo di valore e un valore diverso da zero per i dati del valore.</span><span class="sxs-lookup"><span data-stu-id="d0a03-145">Under this registry key, specify DisableUserProfileExpansion for the value name, REG\_DWORD for the value type, and a nonzero value for the value data.</span></span>

## <a name="about-the-filesnottobackup-registry-key"></a><span data-ttu-id="d0a03-146">Informazioni sulla chiave del registro di sistema FilesNotToBackup</span><span class="sxs-lookup"><span data-stu-id="d0a03-146">About the FilesNotToBackup Registry Key</span></span>

<span data-ttu-id="d0a03-147">La chiave del registro di sistema **FilesNotToBackup** può essere utilizzata per specificare i nomi dei file e delle directory per le quali le applicazioni di backup non devono eseguire il backup o il ripristino.</span><span class="sxs-lookup"><span data-stu-id="d0a03-147">The **FilesNotToBackup** registry key can be used to specify the names of the files and directories that backup applications should not backup or restore.</span></span> <span data-ttu-id="d0a03-148">Tuttavia, non esclude tali file dalle copie shadow.</span><span class="sxs-lookup"><span data-stu-id="d0a03-148">However, it does not exclude those files from shadow copies.</span></span> <span data-ttu-id="d0a03-149">Per ulteriori informazioni su questa chiave del registro di sistema, vedere [chiavi e valori del registro di sistema per il backup e il ripristino](../backup/registry-keys-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="d0a03-149">For more information about this registry key, see [Registry Keys and Values for Backup and Restore](../backup/registry-keys-for-backup-and-restore.md).</span></span>

 

 
