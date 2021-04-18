---
description: Windows Server 2008 R2 e Windows 7 introducono le seguenti modifiche al Servizio Copia Shadow del volume.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novità: VSS in Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307135"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="3800c-103">Novità: VSS in Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="3800c-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="3800c-104">Windows Server 2008 R2 e Windows 7 introducono le seguenti modifiche al Servizio Copia Shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="3800c-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="3800c-105">Nuove interfacce VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="3800c-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="3800c-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="3800c-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="3800c-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="3800c-108">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="3800c-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="3800c-109">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="3800c-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="3800c-110">Nuove classi VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="3800c-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="3800c-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="3800c-112">Nuove enumerazioni VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="3800c-113">**\_Opzioni di ripristino VSS \_**</span><span class="sxs-lookup"><span data-stu-id="3800c-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="3800c-114">Nuove funzioni VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="3800c-115">**CreateVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="3800c-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="3800c-116">Modifiche all'interfaccia VSS esistente</span><span class="sxs-lookup"><span data-stu-id="3800c-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="3800c-117">Interfaccia [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)</span><span class="sxs-lookup"><span data-stu-id="3800c-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="3800c-118">Metodo aggiunto: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="3800c-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="3800c-119">Traccia e registrazione di eventi VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="3800c-120">A partire da Windows Server 2008 R2 e Windows 7, è possibile usare lo strumento VssTrace, lo strumento Logman o lo strumento tracelog per raccogliere informazioni di traccia per l'infrastruttura VSS.</span><span class="sxs-lookup"><span data-stu-id="3800c-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="3800c-121">Per altre informazioni, vedere [uso degli strumenti di traccia con VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="3800c-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="3800c-122">Risincronizzazione LUN</span><span class="sxs-lookup"><span data-stu-id="3800c-122">LUN Resynchronization</span></span>

<span data-ttu-id="3800c-123">In Windows Server 2008 R2 e Windows 7 i richiedenti VSS possono usare una funzionalità del provider di copie shadow hardware denominata "risincronizzazione LUN".</span><span class="sxs-lookup"><span data-stu-id="3800c-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="3800c-124">Si tratta di uno schema di ripristino rapido che consente a un amministratore dell'applicazione di ripristinare i dati da una copia shadow al numero di unità logica (LUN) originale o a un nuovo LUN.</span><span class="sxs-lookup"><span data-stu-id="3800c-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="3800c-125">La copia shadow può essere un clone completo oppure una copia shadow differenziale.</span><span class="sxs-lookup"><span data-stu-id="3800c-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="3800c-126">In entrambi i casi, al termine dell'operazione di risincronizzazione, il LUN di destinazione avrà lo stesso contenuto del LUN della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="3800c-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="3800c-127">Durante l'operazione di risincronizzazione, l'array esegue una copia a livello di blocco dalla copia shadow al LUN di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3800c-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="3800c-128">Per altre informazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="3800c-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="3800c-129">Risincronizzazione LUN: scenario di ripristino rapido in Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3800c-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="3800c-130">"Modalità di utilizzo delle copie shadow" in [servizio Copia Shadow del volume](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="3800c-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="3800c-131">Problemi comuni di risincronizzazione LUN</span><span class="sxs-lookup"><span data-stu-id="3800c-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="3800c-132">Writer Express</span><span class="sxs-lookup"><span data-stu-id="3800c-132">Express Writers</span></span>

<span data-ttu-id="3800c-133">In Windows Server 2008 R2 e Windows 7, l'interfaccia VSS Express consente a un'applicazione di registrare il percorso dei file di dati senza implementare un VSS writer.</span><span class="sxs-lookup"><span data-stu-id="3800c-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="3800c-134">Per ulteriori informazioni, vedere [servizio Copia Shadow del volume (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="3800c-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="3800c-135">Nuovi writer VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-135">New VSS Writers</span></span>

<span data-ttu-id="3800c-136">In Windows Server 2008 R2 e Windows 7 sono stati introdotti i writer VSS seguenti:</span><span class="sxs-lookup"><span data-stu-id="3800c-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="3800c-137">Writer dei contatori delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="3800c-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="3800c-138">Writer di Utilità di pianificazione</span><span class="sxs-lookup"><span data-stu-id="3800c-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="3800c-139">Writer archivio metadati VSS</span><span class="sxs-lookup"><span data-stu-id="3800c-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="3800c-140">Questi nuovi writer sono documentati in [writer VSS in-box](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="3800c-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
