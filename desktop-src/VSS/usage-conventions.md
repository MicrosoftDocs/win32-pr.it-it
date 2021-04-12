---
description: Quando si sviluppa un'applicazione VSS personalizzata, è necessario osservare le linee guida e le restrizioni seguenti.
ms.assetid: d4edc16c-f768-4095-9b2a-b706f19f9e61
title: Compatibilità delle applicazioni VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9cc19b6a6d88365a67569bc4729855077c9da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343581"
---
# <a name="vss-application-compatibility"></a><span data-ttu-id="91226-103">Compatibilità delle applicazioni VSS</span><span class="sxs-lookup"><span data-stu-id="91226-103">VSS Application Compatibility</span></span>

<span data-ttu-id="91226-104">Quando si sviluppa un'applicazione VSS personalizzata, è necessario osservare le linee guida e le restrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="91226-104">When developing your own VSS application, you should observe the following guidelines and restrictions.</span></span> <span data-ttu-id="91226-105">Può essere utile fare riferimento al codice di esempio per i richiedenti VSS, i provider e i writer forniti in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="91226-105">You may find it helpful to refer to the sample code for VSS requesters, providers, and writers that is provided in the Microsoft Windows Software Development Kit (SDK).</span></span>

> [!Note]  
> <span data-ttu-id="91226-106">Il Windows SDK può essere utilizzato per sviluppare applicazioni VSS solo per Windows Vista e versioni successive del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="91226-106">The Windows SDK can be used to develop VSS applications only for Windows Vista and later Windows operating system versions.</span></span> <span data-ttu-id="91226-107">Non può essere utilizzato per sviluppare richiedenti VSS, provider o writer per Windows Server 2003 R2, Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91226-107">It cannot be used to develop VSS requesters, providers, or writers for Windows Server 2003 R2, Windows Server 2003, or Windows XP.</span></span>

 

<span data-ttu-id="91226-108">**Windows server 2003 R2, Windows server 2003 e Windows XP:** VSS è disponibile nel Servizio Copia Shadow del volume 7,2 SDK, che è possibile scaricare da [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490) .</span><span class="sxs-lookup"><span data-stu-id="91226-108">**Windows Server 2003 R2, Windows Server 2003 and Windows XP:** VSS is available in the Volume Shadow Copy Service 7.2 SDK, which you can download from [https://www.microsoft.com/download/details.aspx?id=23490](https://www.microsoft.com/download/details.aspx?id=23490).</span></span> <span data-ttu-id="91226-109">Si noti che i file vssapi. lib a 64 bit nelle directory sotto la \\ directory Win2003 obj possono essere usati per le versioni a 64 bit di Windows server 2003 R2, Windows server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91226-109">Note that the 64-bit vssapi.lib files in the directories under the Win2003\\Obj directory can be used for the 64-bit versions of Windows Server 2003 R2, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="91226-110">Questo SDK fornisce anche codice di esempio per i richiedenti VSS, i provider e i writer.</span><span class="sxs-lookup"><span data-stu-id="91226-110">This SDK also provides sample code for VSS requesters, providers, and writers.</span></span>

## <a name="compiling-vss-applications"></a><span data-ttu-id="91226-111">Compilazione di applicazioni VSS</span><span class="sxs-lookup"><span data-stu-id="91226-111">Compiling VSS Applications</span></span>

<span data-ttu-id="91226-112">Quando si sviluppa un richiedente, ad esempio un'applicazione di backup:</span><span class="sxs-lookup"><span data-stu-id="91226-112">When developing a requester, such as a backup application:</span></span>

-   <span data-ttu-id="91226-113">Includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="91226-113">Include the following headers:</span></span> <dl> <span data-ttu-id="91226-114">VSS. h</span><span class="sxs-lookup"><span data-stu-id="91226-114">Vss.h</span></span>  
    <span data-ttu-id="91226-115">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="91226-115">VsWriter.h</span></span>  
    <span data-ttu-id="91226-116">VsBackup. h</span><span class="sxs-lookup"><span data-stu-id="91226-116">VsBackup.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="91226-117">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="91226-117">VssApi.Lib</span></span>  
    </dl>

<span data-ttu-id="91226-118">Quando si sviluppa un writer:</span><span class="sxs-lookup"><span data-stu-id="91226-118">When developing a writer:</span></span>

-   <span data-ttu-id="91226-119">Includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="91226-119">Include the following headers:</span></span> <dl> <span data-ttu-id="91226-120">VSS. h</span><span class="sxs-lookup"><span data-stu-id="91226-120">Vss.h</span></span>  
    <span data-ttu-id="91226-121">VsWriter. h</span><span class="sxs-lookup"><span data-stu-id="91226-121">VsWriter.h</span></span>  
    </dl>
-   Link the following library: <dl> <span data-ttu-id="91226-122">VssApi. lib</span><span class="sxs-lookup"><span data-stu-id="91226-122">VssApi.lib</span></span>  
    </dl>

## <a name="supported-configurations-and-restrictions"></a><span data-ttu-id="91226-123">Configurazioni e restrizioni supportate</span><span class="sxs-lookup"><span data-stu-id="91226-123">Supported Configurations and Restrictions</span></span>

<span data-ttu-id="91226-124">Nell'elenco seguente vengono descritte le configurazioni e le restrizioni supportate:</span><span class="sxs-lookup"><span data-stu-id="91226-124">The following list describes supported configurations and restrictions:</span></span>

-   <span data-ttu-id="91226-125">VSS viene fornito e supportato nelle versioni del sistema operativo Windows a partire da Windows XP.</span><span class="sxs-lookup"><span data-stu-id="91226-125">VSS is provided and supported on versions of the Windows operating system beginning with Windows XP.</span></span>
-   <span data-ttu-id="91226-126">Nella tabella seguente sono riepilogate le informazioni sulla compatibilità tra le versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="91226-126">The following table summarizes compatibility information across Windows versions.</span></span> <span data-ttu-id="91226-127">Si noti che se un'applicazione VSS viene "compilata per" una versione di Windows specificata, significa che l'applicazione è stata compilata utilizzando i file di intestazione e le librerie specifiche di tale versione.</span><span class="sxs-lookup"><span data-stu-id="91226-127">Note that if a VSS application is "compiled for" a specified Windows version, this means that the application was compiled using the header files and libraries that are specific to that version.</span></span>

    > [!Note]  
    > <span data-ttu-id="91226-128">I provider hardware vengono eseguiti solo nelle versioni del sistema operativo Windows Server.</span><span class="sxs-lookup"><span data-stu-id="91226-128">Hardware providers will run only on Windows server operating system versions.</span></span> <span data-ttu-id="91226-129">Non verranno eseguite nelle versioni del sistema operativo client Windows.</span><span class="sxs-lookup"><span data-stu-id="91226-129">They will not run on Windows client operating system versions.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="91226-130">Nelle tabelle seguenti, Windows Server 2008 con Service Pack 2 (SP2) deve essere considerato uguale a quello di Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="91226-130">In the following tables, Windows Server 2008 with Service Pack 2 (SP2) should be considered the same as Windows Server 2008.</span></span> <span data-ttu-id="91226-131">Per ulteriori informazioni su Windows Server 2008 con SP2, vedere <https://go.microsoft.com/fwlink/p/?linkid=178730> .</span><span class="sxs-lookup"><span data-stu-id="91226-131">For more information about Windows Server 2008 with SP2, see <https://go.microsoft.com/fwlink/p/?linkid=178730>.</span></span> <span data-ttu-id="91226-132">Windows Server 2003 R2 deve essere considerato uguale a quello di Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91226-132">Windows Server 2003 R2 should be considered the same as Windows Server 2003.</span></span>

     

    > [!Note]  
    > <span data-ttu-id="91226-133">Se un'applicazione VSS viene compilata per Windows Server 2003 o versione successiva, verrà eseguita anche nelle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="91226-133">If a VSS application is compiled for Windows Server 2003 or later, it will also run on later versions of Windows.</span></span>

     

    

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="91226-134">Richiedenti VSS, writer e provider compilati per</span><span class="sxs-lookup"><span data-stu-id="91226-134">VSS requesters, writers, and providers compiled for</span></span></th>
    <th><span data-ttu-id="91226-135">Viene eseguito in</span><span class="sxs-lookup"><span data-stu-id="91226-135">Will run on</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="91226-136">Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-136">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    <td><span data-ttu-id="91226-137">Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit) e Windows Vista (64 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-137">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit) and Windows Vista (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="91226-138">Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-138">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    <td><span data-ttu-id="91226-139">Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit) e Windows Vista (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-139">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit) and Windows Vista (32-bit)</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="91226-140">Windows Server 2003 (64 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-140">Windows Server 2003 (64-bit)</span></span></td>
    <td><span data-ttu-id="91226-141">Windows Server 2008 R2 (64 bit), Windows 7 (64 bit), Windows Server 2008 (64 bit), Windows Vista (64 bit) e Windows Server 2003 (64 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-141">Windows Server 2008 R2 (64-bit), Windows 7 (64-bit), Windows Server 2008 (64-bit), Windows Vista (64-bit), and Windows Server 2003 (64-bit)</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="91226-142">Windows Server 2003 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-142">Windows Server 2003 (32-bit)</span></span></td>
    <td><span data-ttu-id="91226-143">Windows Server 2008 R2 (32 bit), Windows 7 (32 bit), Windows Server 2008 (32 bit), Windows Vista (32 bit) e Windows Server 2003 (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-143">Windows Server 2008 R2 (32-bit), Windows 7 (32-bit), Windows Server 2008 (32-bit), Windows Vista (32-bit), and Windows Server 2003 (32-bit)</span></span> <blockquote>
    [!Note]<br />
<span data-ttu-id="91226-144">I richiedenti vengono eseguiti anche in Windows Server 2003 (64 bit).</span><span class="sxs-lookup"><span data-stu-id="91226-144">Requesters will also run on Windows Server 2003 (64-bit).</span></span>
    </blockquote>
    <br/></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="91226-145">Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="91226-145">Windows XP 64-Bit Edition</span></span></td>
    <td><span data-ttu-id="91226-146">Windows Server 2003 (64-bit) e Windows XP 64-bit Edition</span><span class="sxs-lookup"><span data-stu-id="91226-146">Windows Server 2003 (64-bit) and Windows XP 64-Bit Edition</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="91226-147">Windows XP (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-147">Windows XP (32-bit)</span></span></td>
    <td><span data-ttu-id="91226-148">Windows XP (32 bit)</span><span class="sxs-lookup"><span data-stu-id="91226-148">Windows XP (32-bit)</span></span></td>
    </tr>
    </tbody>
    </table>

    

     

    

    | <span data-ttu-id="91226-149">Per compilare un richiedente VSS, un writer o un provider per</span><span class="sxs-lookup"><span data-stu-id="91226-149">To compile a VSS requester, writer, or provider for</span></span>        | <span data-ttu-id="91226-150">Uso</span><span class="sxs-lookup"><span data-stu-id="91226-150">Use</span></span>                                                                                                                                       |
    |------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="91226-151">Windows Server 2008 R2 o Windows 7</span><span class="sxs-lookup"><span data-stu-id="91226-151">Windows Server 2008 R2 or Windows 7</span></span>                        | <span data-ttu-id="91226-152">Windows SDK per Windows 7, disponibile nell' [area download di Windows](https://www.microsoft.com/download/details.aspx?id=8279).</span><span class="sxs-lookup"><span data-stu-id="91226-152">Windows SDK for Windows 7 (Available from the [Windows Download Center](https://www.microsoft.com/download/details.aspx?id=8279).)</span></span>                |
    | <span data-ttu-id="91226-153">Windows Server 2008 o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91226-153">Windows Server 2008 or Windows Vista</span></span>                       | <span data-ttu-id="91226-154">Windows SDK per Windows Server 2008 (disponibile da [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx)).</span><span class="sxs-lookup"><span data-stu-id="91226-154">Windows SDK for Windows Server 2008 (Available from the [Windows SDK Developer Center](https://msdn.microsoft.com/windows/bb980924.aspx).)</span></span> |
    | <span data-ttu-id="91226-155">Windows Server 2003 R2, Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="91226-155">Windows Server 2003 R2, Windows Server 2003, or Windows XP</span></span> | [<span data-ttu-id="91226-156">SDK Servizio Copia Shadow del volume 7,2</span><span class="sxs-lookup"><span data-stu-id="91226-156">Volume Shadow Copy Service 7.2 SDK</span></span>](https://www.microsoft.com/download/details.aspx?id=23490)                                                      |

    

     

-   <span data-ttu-id="91226-157">Tutte le applicazioni VSS a 32 bit, ovvero i richiedenti, i provider e i writer, devono essere eseguite come applicazioni native a 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="91226-157">All 32-bit VSS applications (requesters, providers, and writers) must run as native 32-bit or 64-bit applications.</span></span> <span data-ttu-id="91226-158">L'esecuzione in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="91226-158">Running them under WOW64 is not supported.</span></span>

    <span data-ttu-id="91226-159">**Windows Server 2003 e Windows XP:** L'esecuzione di richiedenti VSS a 32 bit in WOW64 è supportata, ma non per i backup dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="91226-159">**Windows Server 2003 and Windows XP:** Running 32-bit VSS requesters under WOW64 is supported, but not for system-state backups.</span></span> <span data-ttu-id="91226-160">L'esecuzione di provider e writer VSS a 32 bit in WOW64 non è supportata.</span><span class="sxs-lookup"><span data-stu-id="91226-160">Running 32-bit VSS providers and writers under WOW64 is not supported.</span></span> <span data-ttu-id="91226-161">Il supporto per l'esecuzione di richiedenti a 32 bit in WOW64 è stato rimosso in Windows Vista e nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="91226-161">Support for running 32- bit requesters under WOW64 was removed in Windows Vista and subsequent versions.</span></span>

-   <span data-ttu-id="91226-162">Non è possibile usare una copia shadow creata in Windows Server 2003 R2 o Windows Server 2003 in un computer che esegue Windows Server 2008 R2 o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="91226-162">A shadow copy that was created on Windows Server 2003 R2 or Windows Server 2003 cannot be used on a computer that is running Windows Server 2008 R2 or Windows Server 2008.</span></span> <span data-ttu-id="91226-163">Non è possibile usare una copia shadow creata in Windows Server 2008 R2 o Windows Server 2008 in un computer che esegue Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="91226-163">A shadow copy that was created on Windows Server 2008 R2 or Windows Server 2008 cannot be used on a computer that is running Windows Server 2003.</span></span> <span data-ttu-id="91226-164">Tuttavia, una copia shadow creata in Windows Server 2008 può essere usata in un computer che esegue Windows Server 2008 R2 e viceversa.</span><span class="sxs-lookup"><span data-stu-id="91226-164">However, a shadow copy that was created on Windows Server 2008 can be used on a computer that is running Windows Server 2008 R2, and vice versa.</span></span>
-   <span data-ttu-id="91226-165">Per supportare le copie shadow, un sistema che esegue VSS deve avere almeno un file system NTFS.</span><span class="sxs-lookup"><span data-stu-id="91226-165">To support shadow copies, a system running VSS must have at least one NTFS file system.</span></span> <span data-ttu-id="91226-166">In questo file system verrà ospitata l'"area diff" della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="91226-166">This file system will host the shadow copy's "diff area."</span></span> <span data-ttu-id="91226-167">Per ulteriori informazioni, vedere [provider di sistema](providers.md).</span><span class="sxs-lookup"><span data-stu-id="91226-167">For more information, see [System Provider](providers.md).</span></span>
-   <span data-ttu-id="91226-168">Data la presenza di un file system NTFS e data la scelta appropriata del contesto (vedere [configurazioni del contesto di copia shadow](shadow-copy-context-configurations.md)), qualsiasi file system locale supportato può essere replicata.</span><span class="sxs-lookup"><span data-stu-id="91226-168">Given the presence of one NTFS file system, and given the appropriate choice of context (see [Shadow Copy Context Configurations](shadow-copy-context-configurations.md)), any supported local file system can be shadow copied.</span></span>
-   <span data-ttu-id="91226-169">È possibile creare copie shadow solo per i file system montati localmente.</span><span class="sxs-lookup"><span data-stu-id="91226-169">You can make shadow copies only for locally mounted file systems.</span></span> <span data-ttu-id="91226-170">Le condivisioni remote e altri file System Cross-mounted non possono essere replicati dal sistema che li monta.</span><span class="sxs-lookup"><span data-stu-id="91226-170">Remote shares and other cross-mounted file systems cannot be shadow copied by the system that mounts them.</span></span> <span data-ttu-id="91226-171">Questi file System possono essere replicati solo dai sistemi che gestiscono i file System.</span><span class="sxs-lookup"><span data-stu-id="91226-171">These file systems can be shadow copied only by the systems that serve out the file systems.</span></span>
-   <span data-ttu-id="91226-172">I writer e i richiedenti devono specificare solo le risorse locali.</span><span class="sxs-lookup"><span data-stu-id="91226-172">Writers and requesters should specify only local resources.</span></span> <span data-ttu-id="91226-173">Le risorse locali sono set di file il cui percorso assoluto inizia con una lettera di unità e la lettera di unità non può essere associata a una cartella montata in una condivisione remota.</span><span class="sxs-lookup"><span data-stu-id="91226-173">Local resources are sets of files whose absolute path starts with a drive letter, and the drive letter cannot be associated with a mounted folder on a remote share.</span></span>
-   <span data-ttu-id="91226-174">Il numero massimo di copie shadow software per ogni volume è 512.</span><span class="sxs-lookup"><span data-stu-id="91226-174">The maximum number is of software shadow copies for each volume is 512.</span></span> <span data-ttu-id="91226-175">Tuttavia, per impostazione predefinita, puoi gestire solo 64 copie shadow usate dalla funzionalità Copie shadow di cartelle condivise.</span><span class="sxs-lookup"><span data-stu-id="91226-175">However, by default you can only maintain 64 shadow copies that are used by the Shadow Copies of Shared Folders feature.</span></span> <span data-ttu-id="91226-176">Per modificare il limite per le copie shadow della funzionalità cartelle condivise, usare la chiave del registro di sistema [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="91226-176">To change the limit for the Shadow Copies of Shared Folders feature, use the [MaxShadowCopies](../backup/registry-keys-for-backup-and-restore.md) registry key.</span></span>
-   <span data-ttu-id="91226-177">L'infrastruttura dei componenti di backup non supporta il backup delle risorse cluster come componenti del writer.</span><span class="sxs-lookup"><span data-stu-id="91226-177">The Backup Components infrastructure does not support backing up cluster resources as writer components.</span></span> <span data-ttu-id="91226-178">Per eseguire il backup delle risorse cluster, le applicazioni devono presupporre che il percorso sia locale a un determinato nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="91226-178">To back up cluster resources, applications should assume that the path is local to a specified particular cluster node.</span></span>
-   [!Note]  
    > <span data-ttu-id="91226-179">Microsoft non fornisce supporto tecnico per sviluppatori o professionisti IT per l'implementazione di ripristini dello stato del sistema online in Windows (tutte le versioni).</span><span class="sxs-lookup"><span data-stu-id="91226-179">Microsoft does not provide developer or IT professional technical support for implementing online system state restores on Windows (all releases).</span></span>

     

    <span data-ttu-id="91226-180">Quando si esegue il backup e il ripristino dello stato del sistema, la strategia consigliata consiste nel eseguire il backup e il ripristino dei volumi di sistema e di avvio oltre ai file enumerati dai writer dello stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="91226-180">When backing up and recovering system state, the recommended strategy is to back up and recover the system and boot volumes in addition to the files enumerated by the system state writers.</span></span>

    > [!Note]  
    > <span data-ttu-id="91226-181">I writer dello stato del sistema sono writer per i quali l'attributo del [**\_ \_ tipo di utilizzo VSS**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) è impostato su VSS \_ ut \_ BOOTABLESYSTEMSTATE o VSS \_ ut \_ SYSTEMSERVICE.</span><span class="sxs-lookup"><span data-stu-id="91226-181">System state writers are writers that have the [**VSS\_USAGE\_TYPE**](/windows/win32/api/VsWriter/ne-vswriter-vss_usage_type) attribute set to either VSS\_UT\_BOOTABLESYSTEMSTATE or VSS\_UT\_SYSTEMSERVICE.</span></span>

     

 

 
