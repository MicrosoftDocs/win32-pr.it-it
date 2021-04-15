---
description: VShadow è uno strumento da riga di comando che è possibile utilizzare per creare e gestire copie shadow del volume.
ms.assetid: 19109f92-b9da-4df7-8628-374e37a3f624
title: Strumento VShadow ed esempio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7a9a697ecdf39f91d43fa0c66faebd37cfbfed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485028"
---
# <a name="vshadow-tool-and-sample"></a><span data-ttu-id="4300b-103">Strumento VShadow ed esempio</span><span class="sxs-lookup"><span data-stu-id="4300b-103">VShadow Tool and Sample</span></span>

<span data-ttu-id="4300b-104">VShadow è uno strumento da riga di comando che è possibile utilizzare per creare e gestire copie shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="4300b-104">VShadow is a command-line tool that you can use to create and manage volume shadow copies.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-105">VShadow è incluso in Microsoft Windows Software Development Kit (SDK) per Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4300b-105">VShadow is included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="4300b-106">VSS 7,2 SDK include una versione di VShadow che viene eseguita solo in Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4300b-106">The VSS 7.2 SDK includes a version of VShadow that runs only on Windows Server 2003.</span></span> <span data-ttu-id="4300b-107">Per informazioni sul download del Windows SDK e di VSS 7,2 SDK, vedere [servizio Copia Shadow del volume](volume-shadow-copy-service-portal.md).</span><span class="sxs-lookup"><span data-stu-id="4300b-107">For information about downloading the Windows SDK and the VSS 7.2 SDK, see [Volume Shadow Copy Service](volume-shadow-copy-service-portal.md).</span></span>

 

<span data-ttu-id="4300b-108">Lo strumento VShadow utilizza opzioni della riga di comando e flag facoltativi per identificare le operazioni da eseguire.</span><span class="sxs-lookup"><span data-stu-id="4300b-108">The VShadow tool uses command-line options and optional flags to identify the work to perform.</span></span> <span data-ttu-id="4300b-109">Quando viene usato senza alcuna opzione della riga di comando, il comando VShadow crea un nuovo set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-109">When used without any command-line options, the VShadow command creates a new shadow copy set.</span></span>

<span data-ttu-id="4300b-110">I comandi VShadow eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4300b-110">VShadow commands perform the following operations:</span></span>

-   [<span data-ttu-id="4300b-111">Creazione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-111">Creating a Shadow Copy Set</span></span>](#creating-a-shadow-copy-set)
-   [<span data-ttu-id="4300b-112">Importazione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-112">Importing a Shadow Copy Set</span></span>](#importing-a-shadow-copy-set)
-   [<span data-ttu-id="4300b-113">Esecuzione di query sulle proprietà della copia shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-113">Querying Shadow Copy Properties</span></span>](#querying-shadow-copy-properties)
-   [<span data-ttu-id="4300b-114">Eliminazione di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-114">Deleting Shadow Copies</span></span>](#deleting-shadow-copies)
-   [<span data-ttu-id="4300b-115">Suddivisione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-115">Breaking a Shadow Copy Set</span></span>](#breaking-a-shadow-copy-set)
-   [<span data-ttu-id="4300b-116">Suddivisione di un set di copie shadow tramite il metodo BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="4300b-116">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>](#breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method)
-   [<span data-ttu-id="4300b-117">Esposizione locale di una copia shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-117">Exposing a Shadow Copy Locally</span></span>](#exposing-a-shadow-copy-locally)
-   [<span data-ttu-id="4300b-118">Esposizione di una copia shadow in modalità remota</span><span class="sxs-lookup"><span data-stu-id="4300b-118">Exposing a Shadow Copy Remotely</span></span>](#exposing-a-shadow-copy-remotely)
-   [<span data-ttu-id="4300b-119">Elenco di metadati e stato del writer</span><span class="sxs-lookup"><span data-stu-id="4300b-119">Listing Writer Status and Metadata</span></span>](#listing-writer-status-and-metadata)
-   [<span data-ttu-id="4300b-120">Esecuzione di operazioni di ripristino</span><span class="sxs-lookup"><span data-stu-id="4300b-120">Performing Restore Operations</span></span>](#performing-restore-operations)
-   [<span data-ttu-id="4300b-121">Ripristino di una copia shadow precedente</span><span class="sxs-lookup"><span data-stu-id="4300b-121">Reverting to a Previous Shadow Copy</span></span>](#reverting-to-a-previous-shadow-copy)
-   [<span data-ttu-id="4300b-122">Risincronizzazione di lun</span><span class="sxs-lookup"><span data-stu-id="4300b-122">Resynchronizing LUNs</span></span>](#resynchronizing-luns)

## <a name="creating-a-shadow-copy-set"></a><span data-ttu-id="4300b-123">Creazione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-123">Creating a Shadow Copy Set</span></span>

<span data-ttu-id="4300b-124">**vshadow** \[ \] *Volume* OptionalFlags</span><span class="sxs-lookup"><span data-stu-id="4300b-124">**vshadow** \[OptionalFlags\] *VolumeList*</span></span>

<span data-ttu-id="4300b-125">Questo comando crea un nuovo set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-125">This command creates a new shadow copy set.</span></span>

<span data-ttu-id="4300b-126">*Volume* list è un elenco di nomi di volumi.</span><span class="sxs-lookup"><span data-stu-id="4300b-126">*VolumeList* is a list of volume names.</span></span> <span data-ttu-id="4300b-127">VShadow crea una copia shadow per ogni volume presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="4300b-127">VShadow creates one shadow copy for each volume in the list.</span></span> <span data-ttu-id="4300b-128">Facoltativamente, un nome di volume può terminare con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="4300b-128">A volume name can optionally be terminated with a backslash (\\).</span></span> <span data-ttu-id="4300b-129">Ad esempio, C: e C: \\ sono nomi di volume validi.</span><span class="sxs-lookup"><span data-stu-id="4300b-129">For example, both C: and C:\\ are valid volume names.</span></span> <span data-ttu-id="4300b-130">È inoltre possibile specificare le cartelle montate (ad esempio, C: \\ DirectoryName) o i nomi dei GUID del volume (ad esempio, \\ \\ ? \\ Volume {edbed95e-7e8d-11D8-9D01-505054503030}).</span><span class="sxs-lookup"><span data-stu-id="4300b-130">You can also specify mounted folders (for example, C:\\DirectoryName) or volume GUID names (for example, \\\\?\\Volume{edbed95e-7e8d-11d8-9d01-505054503030}).</span></span>

<span data-ttu-id="4300b-131">*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4300b-131">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4300b-132">Valore del flag facoltativo</span><span class="sxs-lookup"><span data-stu-id="4300b-132">Optional Flag Value</span></span></th>
<th><span data-ttu-id="4300b-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4300b-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4300b-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-134"><span id="-ad"></span><span id="-AD"></span><strong>-ad</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-135">Questo flag facoltativo specifica le copie shadow dell'hardware differenziale.</span><span class="sxs-lookup"><span data-stu-id="4300b-135">This optional flag specifies differential hardware shadow copies.</span></span> <span data-ttu-id="4300b-136">Questo flag e il flag <strong>-AP</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-136">This flag and the <strong>-ap</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-137">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-137">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-138"><span id="-ap"></span><span id="-AP"></span><strong>-AP</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-138"><span id="-ap"></span><span id="-AP"></span><strong>-ap</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-139">Questo flag facoltativo specifica le copie shadow dell'hardware Plex.</span><span class="sxs-lookup"><span data-stu-id="4300b-139">This optional flag specifies plex hardware shadow copies.</span></span> <span data-ttu-id="4300b-140">Questo flag e il flag <strong>-ad</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-140">This flag and the <strong>-ad</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-141">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-141">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span><strong></strong> <strong>-BC =</strong><em>file</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-142"><span id="_-bc_File.xml"></span><span id="_-bc_file.xml"></span><span id="_-BC_FILE.XML"></span> <strong></strong> <strong>-bc=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-143">Questo flag facoltativo specifica le copie shadow non trasferibili e archivia nel file specificato il documento relativo ai componenti di backup.</span><span class="sxs-lookup"><span data-stu-id="4300b-143">This optional flag specifies non-transportable shadow copies and stores the Backup Components Document into the specified file.</span></span> <span data-ttu-id="4300b-144">Questo file può essere utilizzato in un'operazione di ripristino successiva.</span><span class="sxs-lookup"><span data-stu-id="4300b-144">This file can be used in a subsequent restore operation.</span></span> <span data-ttu-id="4300b-145">Questo flag e il flag <strong>-t</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-145">This flag and the <strong>-t</strong> flag are mutually exclusive.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-146">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-146">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-Exec =</strong><em>comando</em></span><span class="sxs-lookup"><span data-stu-id="4300b-147"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span><strong>-exec=</strong><em>Command</em></span></span><br/></td>
<td><span data-ttu-id="4300b-148">Questo flag facoltativo esegue un comando o uno script dopo la creazione delle copie shadow, ma prima che lo strumento VShadow venga chiuso.</span><span class="sxs-lookup"><span data-stu-id="4300b-148">This optional flag executes a command or script after the shadow copies are created but before the VShadow tool exits.</span></span> <span data-ttu-id="4300b-149">Il <em>comando</em> può specificare un comando della shell eseguibile o un file cmd.</span><span class="sxs-lookup"><span data-stu-id="4300b-149"><em>Command</em> can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="4300b-150">Se specifica un comando della shell, non è possibile specificare parametri di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-150">If it specifies a shell command, no command parameters can be specified.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-151">Per motivi di sicurezza e per semplificare l'implementazione, il flag facoltativo <strong>-Exec</strong> non accetterà parametri da passare al comando o allo script.</span><span class="sxs-lookup"><span data-stu-id="4300b-151">For security reasons and to keep the implementation simple, the <strong>-exec</strong> optional flag will not accept parameters to be passed to the command or script.</span></span> <span data-ttu-id="4300b-152">L'intera stringa passata al flag facoltativo <strong>-Exec</strong> viene considerata come un singolo file cmd o exe.</span><span class="sxs-lookup"><span data-stu-id="4300b-152">The entire string passed to the <strong>-exec</strong> optional flag is treated as a single CMD or EXE file.</span></span> <span data-ttu-id="4300b-153">Per ulteriori informazioni su questa limitazione, vedere il codice sorgente di VShadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-153">For more information about this limitation, see the VShadow source code.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-154"><span id="-forcerevert"></span><span id="-FORCEREVERT"></span><strong>-forcerevert</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-155">Questo flag facoltativo specifica che l'operazione di copia shadow deve essere completata solo se è possibile ripristinare tutte le firme del disco.</span><span class="sxs-lookup"><span data-stu-id="4300b-155">This optional flag specifies that the shadow copy operation should be completed only if all disk signatures can be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-156">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-156">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-157"><strong>Windows Server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-157"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-158"><span id="-mask"></span><span id="-MASK"></span><strong>-maschera</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-158"><span id="-mask"></span><span id="-MASK"></span><strong>-mask</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-159">Questo flag facoltativo specifica che i LUN della copia shadow devono essere mascherati dal computer quando il set di copie shadow è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="4300b-159">This optional flag specifies that the shadow copy LUNs should be masked from the computer when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-160">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-160">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-161"><strong>Windows Server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-161"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-162"><span id="-nar"></span><span id="-NAR"></span><strong>-Nar</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-162"><span id="-nar"></span><span id="-NAR"></span><strong>-nar</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-163">Questo flag facoltativo specifica le copie shadow senza ripristino automatico.</span><span class="sxs-lookup"><span data-stu-id="4300b-163">This optional flag specifies shadow copies without auto-recovery.</span></span> <span data-ttu-id="4300b-164">Per ulteriori informazioni su questa opzione, vedere la documentazione relativa al flag di VSS_VOLSNAP_ATTR_NO_AUTORECOVERY dell'enumerazione <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4300b-164">For more information about this option, see the documentation for the VSS_VOLSNAP_ATTR_NO_AUTORECOVERY flag of the <a href="/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes"><strong>_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</strong></a> enumeration.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-Revert</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-165"><span id="-norevert"></span><span id="-NOREVERT"></span><strong>-norevert</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-166">Questo flag facoltativo specifica che le firme del disco non devono essere ripristinate.</span><span class="sxs-lookup"><span data-stu-id="4300b-166">This optional flag specifies that disk signatures should not be reverted.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-167">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-167">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-168"><strong>Windows Server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-168"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-169"><span id="-nw"></span><span id="-NW"></span><strong>-NW</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-169"><span id="-nw"></span><span id="-NW"></span><strong>-nw</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-170">Questo flag facoltativo specifica le copie shadow senza coinvolgere i writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-170">This optional flag specifies shadow copies without involving writers.</span></span> <span data-ttu-id="4300b-171">Per ulteriori informazioni sulle copie shadow senza partecipazione del writer, vedere la pagina relativa ai <a href="shadow-copy-creation-details.md">Dettagli della creazione della copia shadow</a>.</span><span class="sxs-lookup"><span data-stu-id="4300b-171">For more information about shadow copies without writer participation, see <a href="shadow-copy-creation-details.md">Shadow Copy Creation Details</a>.</span></span> <span data-ttu-id="4300b-172">Questo flag e i flag <strong>-Wi</strong> e <strong>-WX</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-172">This flag and the <strong>-wi</strong> and <strong>-wx</strong> flags are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-173"><span id="-p"></span><span id="-P"></span><strong>-p</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-174">Questo flag facoltativo specifica le <a href="vssgloss-p.md"><em>copie shadow permanenti</em></a>.</span><span class="sxs-lookup"><span data-stu-id="4300b-174">This optional flag specifies <a href="vssgloss-p.md"><em>persistent shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-175">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-175">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-176"><span id="-rw"></span><span id="-RW"></span><strong>-RW</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-176"><span id="-rw"></span><span id="-RW"></span><strong>-rw</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-177">Questo flag facoltativo specifica che i LUN della copia shadow devono essere resi di lettura/scrittura quando il set di copie shadow è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="4300b-177">This optional flag specifies that the shadow copy LUNs should be made read/write when the shadow copy set is broken.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-178">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-178">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-179"><strong>Windows Server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-179"><strong>Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-180"><span id="-scsf"></span><span id="-SCSF"></span><strong>-scsf</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-181">Questo flag facoltativo specifica le <a href="vssgloss-c.md"><em>copie shadow accessibili dal client</em></a>.</span><span class="sxs-lookup"><span data-stu-id="4300b-181">This optional flag specifies <a href="vssgloss-c.md"><em>client-accessible shadow copies</em></a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-182">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-182">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script =</strong><em>file</em><strong>. cmd</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-183"><span id="-script_File.cmd"></span><span id="-script_file.cmd"></span><span id="-SCRIPT_FILE.CMD"></span><strong>-script=</strong><em>File</em><strong>.cmd</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-184">Questo flag facoltativo genera un file CMD contenente le variabili di ambiente correlate alle copie shadow create, ad esempio gli ID copia shadow e gli ID del set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-184">This optional flag generates a CMD file containing environment variables related to the created shadow copies, such as shadow copy IDs and shadow copy set IDs.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t =</strong><em>file</em><strong>. XML</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-185"><span id="-t_File.xml"></span><span id="-t_file.xml"></span><span id="-T_FILE.XML"></span><strong>-t=</strong><em>File</em><strong>.xml</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-186">Questo flag facoltativo specifica le copie shadow trasportabili e archivia i componenti di backup del documento nel file specificato dal parametro <em>File.xml</em> .</span><span class="sxs-lookup"><span data-stu-id="4300b-186">This optional flag specifies transportable shadow copies and stores the Backup Components Document into the file specified by the <em>File.xml</em> parameter.</span></span> <span data-ttu-id="4300b-187">Questo file può essere utilizzato in un'operazione di importazione e/o ripristino successiva.</span><span class="sxs-lookup"><span data-stu-id="4300b-187">This file can be used in a subsequent import and/or restore operation.</span></span> <span data-ttu-id="4300b-188">Questo flag e il flag <strong>-BC</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-188">This flag and the <strong>-bc</strong> flag are mutually exclusive.</span></span><br/> <span data-ttu-id="4300b-189"><strong>Windows server 2003, Standard Edition e Windows server 2003, Web Edition:</strong> Le copie shadow trasportabili non sono supportate.</span><span class="sxs-lookup"><span data-stu-id="4300b-189"><strong>Windows Server 2003, Standard Edition and Windows Server 2003, Web Edition:</strong> Transportable shadow copies are not supported.</span></span> <span data-ttu-id="4300b-190">Tutte le edizioni di Windows Server 2003 con Service Pack 1 (SP1) supportano le copie shadow trasportabili.</span><span class="sxs-lookup"><span data-stu-id="4300b-190">All editions of Windows Server 2003 with Service Pack 1 (SP1) support transportable shadow copies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-191"><span id="-tr"></span><span id="-TR"></span><strong>-TR</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-191"><span id="-tr"></span><span id="-TR"></span><strong>-tr</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-192">Questo flag facoltativo specifica che è necessario applicare il ripristino TxF durante la creazione della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-192">This optional flag specifies that TxF recovery should be enforced during shadow copy creation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-193">Questo flag è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-193">This flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-traccia</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-194"><span id="-tracing"></span><span id="-TRACING"></span><strong>-tracing</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-195">Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="4300b-195">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-attesa</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-196"><span id="-wait"></span><span id="-WAIT"></span><strong>-wait</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-197">Questo flag facoltativo fa in modo che lo strumento VShadow attenda la conferma dell'utente prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="4300b-197">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-Wi =</strong><em>writer</em></span><span class="sxs-lookup"><span data-stu-id="4300b-198"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span><strong>-wi=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="4300b-199">Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nella copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-199">This optional flag verifies that the specified writer or component is included in the shadow copy.</span></span> <span data-ttu-id="4300b-200">Il <em>writer</em> può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-200"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="4300b-201">Questo flag e il flag <strong>-NW</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-201">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4300b-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-WX =</strong><em>writer</em></span><span class="sxs-lookup"><span data-stu-id="4300b-202"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span><strong>-wx=</strong><em>Writer</em></span></span><br/></td>
<td><span data-ttu-id="4300b-203">Questo flag facoltativo verifica che il writer o il componente specificato venga escluso dalla copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-203">This optional flag verifies that the specified writer or component is excluded from the shadow copy.</span></span> <span data-ttu-id="4300b-204">Il <em>writer</em> può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-204"><em>Writer</em> can specify a component path, writer name, writer ID, or writer instance ID.</span></span> <span data-ttu-id="4300b-205">Questo flag e il flag <strong>-NW</strong> si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-205">This flag and the <strong>-nw</strong> flag are mutually exclusive.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="importing-a-shadow-copy-set"></a><span data-ttu-id="4300b-206">Importazione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-206">Importing a Shadow Copy Set</span></span>

<span data-ttu-id="4300b-207">**vshadow** \[ OptionalFlags \] **-i =**_file_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="4300b-207">**vshadow** \[OptionalFlags\] **-i=**_File_*_.xml_*</span></span>

<span data-ttu-id="4300b-208">L'opzione della riga di comando **-i** importa un set di copie shadow trasportabili.</span><span class="sxs-lookup"><span data-stu-id="4300b-208">The **-i** command-line option imports a transportable shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-209">Questa opzione della riga di comando è supportata solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-209">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="4300b-210">Il file di *File.xml* deve essere un file di documento dei componenti di backup per un set di copie shadow trasportabili creato con il flag facoltativo **-t** o **-BC** .</span><span class="sxs-lookup"><span data-stu-id="4300b-210">The *File.xml* file must be a Backup Components Document file for a transportable shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="4300b-211">Un set di copie shadow è una [*Copia Shadow persistente*](vssgloss-p.md) se è stata creata con il flag **-p** facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4300b-211">A shadow copy set is a [*persistent shadow copy*](vssgloss-p.md) if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="4300b-212">Se il set di copie shadow trasportabili è non persistente, viene visualizzato per un breve periodo di tempo mentre il comando per la creazione della copia shadow è in esecuzione e viene eliminato automaticamente quando il comando restituisce un risultato.</span><span class="sxs-lookup"><span data-stu-id="4300b-212">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="4300b-213">È possibile importare copie shadow non permanenti solo durante la creazione della copia shadow, creando il set di copie shadow usando il flag facoltativo **-Exec** per eseguire un file cmd che chiama vshadow **-i**.</span><span class="sxs-lookup"><span data-stu-id="4300b-213">You can import nonpersistent shadow copies only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls VShadow **-i**.</span></span>

<span data-ttu-id="4300b-214">Impossibile combinare l'opzione della riga di comando **-i** con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-214">The **-i** command-line option cannot be combined with other command-line options.</span></span>

<span data-ttu-id="4300b-215">*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4300b-215">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="4300b-216">Valore del flag facoltativo</span><span class="sxs-lookup"><span data-stu-id="4300b-216">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="4300b-217">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4300b-217">Description</span></span>                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4300b-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="4300b-218"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="4300b-219">Questo flag facoltativo esegue un comando o uno script dopo l'importazione delle copie shadow ma prima della chiusura dello Strumento VShadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-219">This optional flag executes a command or script after the shadow copies are imported but before the VShadow tool exits.</span></span> <span data-ttu-id="4300b-220">Il *comando* può specificare un comando della shell eseguibile o un file cmd.</span><span class="sxs-lookup"><span data-stu-id="4300b-220">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="4300b-221">Se specifica un comando della shell, non è possibile specificare parametri di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-221">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="4300b-222"><span id="-tracing"></span><span id="-TRACING"></span>**-traccia**</span><span class="sxs-lookup"><span data-stu-id="4300b-222"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="4300b-223">Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="4300b-223">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="4300b-224"><span id="-wait"></span><span id="-WAIT"></span>**-attesa**</span><span class="sxs-lookup"><span data-stu-id="4300b-224"><span id="-wait"></span><span id="-WAIT"></span>**-wait**</span></span><br/>                                                           | <span data-ttu-id="4300b-225">Questo flag facoltativo fa in modo che lo strumento VShadow attenda la conferma dell'utente prima di uscire.</span><span class="sxs-lookup"><span data-stu-id="4300b-225">This optional flag causes the VShadow tool to wait for user confirmation before exiting.</span></span><br/>                                                                                                                                                                          |



 

## <a name="querying-shadow-copy-properties"></a><span data-ttu-id="4300b-226">Esecuzione di query sulle proprietà della copia shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-226">Querying Shadow Copy Properties</span></span>

<span data-ttu-id="4300b-227">**vshadow** **-q**</span><span class="sxs-lookup"><span data-stu-id="4300b-227">**vshadow** **-q**</span></span>

<span data-ttu-id="4300b-228">**vshadow** **-QX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="4300b-228">**vshadow** **-qx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="4300b-229">**vshadow** **-s =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="4300b-229">**vshadow** **-s=**_ShadowCopyId_</span></span>

<span data-ttu-id="4300b-230">L'opzione della riga di comando **-q** elenca le proprietà di tutte le copie shadow nel computer.</span><span class="sxs-lookup"><span data-stu-id="4300b-230">The **-q** command-line option lists the properties of all shadow copies on the computer.</span></span>

<span data-ttu-id="4300b-231">L'opzione della riga di comando **-QX** elenca le proprietà di tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="4300b-231">The **-qx** command-line option lists the properties of all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="4300b-232">L'opzione della riga di comando **-s** elenca le proprietà della copia shadow il cui ID è specificato da *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="4300b-232">The **-s** command-line option lists the properties of the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="4300b-233">Queste opzioni della riga di comando usano una combinazione di [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) e [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) per ottenere le proprietà del set di copie shadow specificato.</span><span class="sxs-lookup"><span data-stu-id="4300b-233">These command-line options use a combination of [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query) and [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties) to get the properties of the given set of shadow copies.</span></span>

<span data-ttu-id="4300b-234">Le opzioni della riga **di comando-q**, **-QX** e **-s** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-234">The **-q**, **-qx**, and **-s** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="deleting-shadow-copies"></a><span data-ttu-id="4300b-235">Eliminazione di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-235">Deleting Shadow Copies</span></span>

<span data-ttu-id="4300b-236">**vshadow** **-da**</span><span class="sxs-lookup"><span data-stu-id="4300b-236">**vshadow** **-da**</span></span>

<span data-ttu-id="4300b-237">**vshadow** **-do**</span><span class="sxs-lookup"><span data-stu-id="4300b-237">**vshadow** **-do**</span></span>

<span data-ttu-id="4300b-238">**vshadow** **-DX =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="4300b-238">**vshadow** **-dx=**_ShadowCopySetId_</span></span>

<span data-ttu-id="4300b-239">**vshadow** **-DS =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="4300b-239">**vshadow** **-ds=**_ShadowCopyId_</span></span>

<span data-ttu-id="4300b-240">Il comando **-da** Elimina tutte le copie shadow nel computer.</span><span class="sxs-lookup"><span data-stu-id="4300b-240">The **-da** command deletes all shadow copies on the computer.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-241">L'opzione della riga di comando **-da** richiede la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4300b-241">The **-da** command-line option requires user confirmation.</span></span>

 

<span data-ttu-id="4300b-242">L'opzione della riga di comando **-do** Elimina la copia shadow meno recente nel computer.</span><span class="sxs-lookup"><span data-stu-id="4300b-242">The **-do** command-line option deletes the oldest shadow copy on the computer.</span></span>

<span data-ttu-id="4300b-243">L'opzione della riga di comando **-dx** Elimina tutte le copie shadow nel set di copie shadow il cui ID è specificato da *ShadowCopySetId*.</span><span class="sxs-lookup"><span data-stu-id="4300b-243">The **-dx** command-line option deletes all shadow copies in the shadow copy set whose ID is specified by *ShadowCopySetId*.</span></span>

<span data-ttu-id="4300b-244">L'opzione della riga di comando **-DS** Elimina la copia shadow il cui ID è specificato da *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="4300b-244">The **-ds** command-line option deletes the shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="4300b-245">Queste opzioni della riga di comando sono utilizzabili solo con [*copie shadow permanenti*](vssgloss-p.md) .</span><span class="sxs-lookup"><span data-stu-id="4300b-245">These command-line options are for use with [*persistent shadow copies*](vssgloss-p.md) only.</span></span> <span data-ttu-id="4300b-246">Non è necessario eliminare in modo esplicito le copie shadow non permanenti perché vengono eliminate automaticamente al termine del comando di creazione VShadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-246">Nonpersistent shadow copies do not need to be explicitly deleted, because they are automatically deleted when the VShadow creation command exits.</span></span>

<span data-ttu-id="4300b-247">Le opzioni della riga di comando **-da**, **-do**, **-DX** e **-DS** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-247">The **-da**, **-do**, **-dx**, and **-ds** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set"></a><span data-ttu-id="4300b-248">Suddivisione di un set di copie shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-248">Breaking a Shadow Copy Set</span></span>

<span data-ttu-id="4300b-249">**vshadow** **-b =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="4300b-249">**vshadow** **-b=**_ShadowCopySetId_</span></span>

<span data-ttu-id="4300b-250">**vshadow** **-BW =**_ShadowCopySetId_</span><span class="sxs-lookup"><span data-stu-id="4300b-250">**vshadow** **-bw=**_ShadowCopySetId_</span></span>

<span data-ttu-id="4300b-251">L'opzione della riga di comando **-b =**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume autonomo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4300b-251">The **-b=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone read-only volume.</span></span>

<span data-ttu-id="4300b-252">L'opzione della riga di comando **-BW =**_ShadowCopySetId_ converte ogni copia shadow nel set di copie shadow in un volume scrivibile autonomo.</span><span class="sxs-lookup"><span data-stu-id="4300b-252">The **-bw=**_ShadowCopySetId_ command-line option converts each shadow copy in the shadow copy set into a stand-alone writable volume.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-253">Le opzioni della riga di comando **-b** e **-BW** sono supportate solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-253">The **-b** and **-bw** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="4300b-254">Per informazioni su come suddividere un set di copie shadow, vedere [interruzioni di copie shadow](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="4300b-254">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

<span data-ttu-id="4300b-255">Dopo che il set di copie shadow è stato danneggiato, il set di copie shadow e le singole copie shadow non esistono più e non possono essere gestiti con i comandi VSS.</span><span class="sxs-lookup"><span data-stu-id="4300b-255">After the shadow copy set is broken, the shadow copy set and the individual shadow copies no longer exist and cannot be managed using VSS commands.</span></span>

<span data-ttu-id="4300b-256">Un set di copie shadow è persistente se è stato creato con il flag **-p** facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4300b-256">A shadow copy set is persistent if it was created with the **-p** optional flag.</span></span> <span data-ttu-id="4300b-257">Se il set di copie shadow trasportabili è non persistente, viene visualizzato per un breve periodo di tempo mentre il comando per la creazione della copia shadow è in esecuzione e viene eliminato automaticamente quando il comando restituisce un risultato.</span><span class="sxs-lookup"><span data-stu-id="4300b-257">If the transportable shadow copy set is nonpersistent, it appears for a short time while the shadow copy creation command is running, and is automatically deleted when the command returns.</span></span> <span data-ttu-id="4300b-258">È possibile interrompere i set di copie shadow non permanenti solo durante la creazione della copia shadow, creando il set di copie shadow usando il flag **-Exec** facoltativo per eseguire un file cmd che chiama **vshadow** **-b** o **vshadow** **-BW**.</span><span class="sxs-lookup"><span data-stu-id="4300b-258">You can break nonpersistent shadow copy sets only during shadow copy creation, by creating the shadow copy set using the **-exec** optional flag to execute a CMD file that calls **vshadow** **-b** or **vshadow** **-bw**.</span></span>

<span data-ttu-id="4300b-259">Le opzioni della riga di comando **-b** e **-BW** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-259">The **-b** and **-bw** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="breaking-a-shadow-copy-set-using-the-breaksnapshotsetex-method"></a><span data-ttu-id="4300b-260">Suddivisione di un set di copie shadow tramite il metodo BreakSnapshotSetEx</span><span class="sxs-lookup"><span data-stu-id="4300b-260">Breaking a Shadow Copy Set Using the BreakSnapshotSetEx Method</span></span>

<span data-ttu-id="4300b-261">**vshadow** **-Bex**</span><span class="sxs-lookup"><span data-stu-id="4300b-261">**vshadow** **-bex**</span></span>

<span data-ttu-id="4300b-262">L'opzione della riga di comando **-Bex** interrompe un set di copie shadow in base alle opzioni specificate dai flag facoltativi **-mask**, **-RW**, **-forcerevert** e **-Revert** .</span><span class="sxs-lookup"><span data-stu-id="4300b-262">The **-bex** command-line option breaks a shadow copy set according to the options specified by the optional **-mask**, **-rw**, **-forcerevert**, and **-norevert** flags.</span></span> <span data-ttu-id="4300b-263">Questa opzione della riga di comando è simile alle opzioni della riga di comando **-b** e **-BW** .</span><span class="sxs-lookup"><span data-stu-id="4300b-263">This command-line option is similar to the **-b** and **-bw** command-line options.</span></span> <span data-ttu-id="4300b-264">L'opzione della riga di comando **-Bex** usa il metodo [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) , mentre le opzioni della riga di comando **-b** e **-BW** usano il metodo [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="4300b-264">The **-bex** command-line option uses the [**IVssBackupComponentsEx2::BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) method, whereas the **-b** and **-bw** command-line options use the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>

<span data-ttu-id="4300b-265">Per informazioni su come suddividere un set di copie shadow, vedere [interruzioni di copie shadow](breaking-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="4300b-265">For information about breaking a shadow copy set, see [Breaking Shadow Copies](breaking-shadow-copies.md).</span></span>

> [!Note]  
> <span data-ttu-id="4300b-266">L'opzione della riga di comando **-Bex** è supportata solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-266">The **-bex** command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="4300b-267">**vshadow** **-Bex** **-mask**</span><span class="sxs-lookup"><span data-stu-id="4300b-267">**vshadow** **-bex** **-mask**</span></span>

<span data-ttu-id="4300b-268">Il flag **-mask** specifica che il lun della copia shadow verrà mascherato dall'host.</span><span class="sxs-lookup"><span data-stu-id="4300b-268">The **-mask** flag specifies that the shadow copy LUN will be masked from the host.</span></span> <span data-ttu-id="4300b-269">Se viene specificato il flag **-mask** , non è possibile specificare i flag **-RW**, **-forcerevert** e **-Revert** .</span><span class="sxs-lookup"><span data-stu-id="4300b-269">If the **-mask** flag is specified, the **-rw**, **-forcerevert**, and **-norevert** flags cannot be specified.</span></span>

<span data-ttu-id="4300b-270">**vshadow** **-Bex** **-RW**</span><span class="sxs-lookup"><span data-stu-id="4300b-270">**vshadow** **-bex** **-rw**</span></span>

<span data-ttu-id="4300b-271">Il flag **-RW** specifica che il lun della copia shadow verrà esposto all'host come volume di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4300b-271">The **-rw** flag specifies that the shadow copy LUN will be exposed to the host as a read/write volume.</span></span>

<span data-ttu-id="4300b-272">**vshadow** **-Bex** **-forcerevert**</span><span class="sxs-lookup"><span data-stu-id="4300b-272">**vshadow** **-bex** **-forcerevert**</span></span>

<span data-ttu-id="4300b-273">Il flag **-forcerevert** specifica che gli identificatori del disco di tutti i LUN della copia shadow verranno ripristinati a quelli dei lun originali.</span><span class="sxs-lookup"><span data-stu-id="4300b-273">The **-forcerevert** flag specifies that the disk identifiers of all of the shadow copy LUNs will be reverted to that of the original LUNs.</span></span> <span data-ttu-id="4300b-274">Tuttavia, se uno dei lun originali è presente nel sistema, l'operazione avrà esito negativo e nessuno degli identificatori verrà ripristinato.</span><span class="sxs-lookup"><span data-stu-id="4300b-274">However, if any of the original LUNs are present on the system, the operation will fail and none of the identifiers will be reverted.</span></span> <span data-ttu-id="4300b-275">Questo flag e il flag **-Revert** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-275">This flag and the **-norevert** flag are mutually exclusive.</span></span>

<span data-ttu-id="4300b-276">**vshadow** **-Bex** **-Revert**</span><span class="sxs-lookup"><span data-stu-id="4300b-276">**vshadow** **-bex** **-norevert**</span></span>

<span data-ttu-id="4300b-277">Il flag **-Revert** specifica che nessuno degli identificatori del disco lun della copia shadow verrà ripristinato.</span><span class="sxs-lookup"><span data-stu-id="4300b-277">The **-norevert** flag specifies that none of the shadow copy LUN disk identifiers will be reverted.</span></span> <span data-ttu-id="4300b-278">Questo flag e il flag **-forcerevert** si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="4300b-278">This flag and the **-forcerevert** flag are mutually exclusive.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="4300b-279">Esposizione locale di una copia shadow</span><span class="sxs-lookup"><span data-stu-id="4300b-279">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="4300b-280">**vshadow** **-El =**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span><span class="sxs-lookup"><span data-stu-id="4300b-280">**vshadow** **-el=**_ShadowCopyId_*_,_*_LocalEmptyDirectory_</span></span>

 <span data-ttu-id="4300b-281">**vshadow** **-El =**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span><span class="sxs-lookup"><span data-stu-id="4300b-281">**vshadow** **-el=**_ShadowCopyId_*_,_*_UnusedDriveLetter_</span></span>

<span data-ttu-id="4300b-282">L'opzione della riga di comando **-El** assegna una cartella montata o una lettera di unità a una copia shadow permanente.</span><span class="sxs-lookup"><span data-stu-id="4300b-282">The **-el** command-line option assigns a mounted folder or a drive letter to a persistent shadow copy.</span></span> <span data-ttu-id="4300b-283">Si noti che il contenuto del volume resterà di sola lettura, a meno che non venga successivamente chiamato **vshadow** **-BW** per interrompere il set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-283">Note that the volume contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-284">Le copie shadow non permanenti e le [*copie shadow accessibili dal client*](vssgloss-c.md) non possono essere esposte localmente.</span><span class="sxs-lookup"><span data-stu-id="4300b-284">Nonpersistent shadow copies and [*client-accessible shadow copies*](vssgloss-c.md) cannot be exposed locally.</span></span>

 

<span data-ttu-id="4300b-285">Se, ad esempio, {edbed95e-7e8d-11D8-9D01-505054503030} è il GUID di una copia shadow persistente esistente e X: è una lettera di unità inutilizzata, il comando seguente espone la copia shadow in X:</span><span class="sxs-lookup"><span data-stu-id="4300b-285">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and X: is an unused drive letter, the following command exposes the shadow copy under X:</span></span>

<span data-ttu-id="4300b-286">**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, x:**</span><span class="sxs-lookup"><span data-stu-id="4300b-286">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},x:**</span></span>

<span data-ttu-id="4300b-287">Nell'esempio seguente viene illustrato come esporre la stessa copia shadow nella cartella montata C: \\ ShadowCopies \\ June23:</span><span class="sxs-lookup"><span data-stu-id="4300b-287">The following example shows how to expose the same shadow copy under the mounted folder C:\\ShadowCopies\\June23:</span></span>

<span data-ttu-id="4300b-288">**mkdir c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="4300b-288">**mkdir c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="4300b-289">**vshadow** **-El = {edbed95e-7e8d-11D8-9D01-505054503030}, c: \\ ShadowCopies \\ June23**</span><span class="sxs-lookup"><span data-stu-id="4300b-289">**vshadow** **-el={edbed95e-7e8d-11d8-9d01-505054503030},c:\\ShadowCopies\\June23**</span></span>

<span data-ttu-id="4300b-290">Non è possibile combinare l'opzione della riga di comando **-El** con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-290">The **-el** command-line option cannot be combined with other command-line options.</span></span>

## <a name="exposing-a-shadow-copy-remotely"></a><span data-ttu-id="4300b-291">Esposizione di una copia shadow in modalità remota</span><span class="sxs-lookup"><span data-stu-id="4300b-291">Exposing a Shadow Copy Remotely</span></span>

<span data-ttu-id="4300b-292">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_</span><span class="sxs-lookup"><span data-stu-id="4300b-292">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_</span></span>

 <span data-ttu-id="4300b-293">**vshadow** **-er =**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span><span class="sxs-lookup"><span data-stu-id="4300b-293">**vshadow** **-er=**_ShadowCopyId_*_,_*_UnusedShareName_*_,_*_PathFromRootOnShadow_</span></span>

<span data-ttu-id="4300b-294">L'opzione della riga di comando **-er** assegna un nome di condivisione di sola lettura alla directory radice (o a una sottodirectory) dalla copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-294">The **-er** command-line option assigns a read-only share name to the root directory (or a subdirectory) from the shadow copy.</span></span> <span data-ttu-id="4300b-295">Si noti che il contenuto della condivisione rimarrà di sola lettura, a meno che non venga successivamente chiamato **vshadow** **-BW** per interrompere il set di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-295">Note that the share contents will remain read-only unless you subsequently call **vshadow** **-bw** to break the shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-296">Le [*copie shadow accessibili dal client*](vssgloss-c.md) non possono essere esposte in remoto.</span><span class="sxs-lookup"><span data-stu-id="4300b-296">[*Client-accessible shadow copies*](vssgloss-c.md) cannot be exposed remotely.</span></span>

 

<span data-ttu-id="4300b-297">Se, ad esempio, {edbed95e-7e8d-11D8-9D01-505054503030} è il GUID di una copia shadow persistente esistente e la condivisione \_ 123 è un nome di condivisione non usato, il comando seguente espone la copia shadow in share \_ 123:</span><span class="sxs-lookup"><span data-stu-id="4300b-297">For example, if {edbed95e-7e8d-11d8-9d01-505054503030} is the GUID of an existing persistent shadow copy, and share\_123 is an unused share name, the following command exposes the shadow copy under share\_123:</span></span>

<span data-ttu-id="4300b-298">**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, condivisione \_ 123**</span><span class="sxs-lookup"><span data-stu-id="4300b-298">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123**</span></span>

<span data-ttu-id="4300b-299">Nell'esempio seguente viene illustrato come esporre solo un sottoalbero (denominato "Folder1 \\ Cartella2") della stessa copia shadow nella stessa condivisione:</span><span class="sxs-lookup"><span data-stu-id="4300b-299">The following example shows how to expose only a subtree (named "Folder1\\Folder2") of the same shadow copy under the same share:</span></span>

<span data-ttu-id="4300b-300">**vshadow** **-er = {edbed95e-7e8d-11D8-9D01-505054503030}, share \_ 123, Folder1 \\ Cartella2**</span><span class="sxs-lookup"><span data-stu-id="4300b-300">**vshadow** **-er={edbed95e-7e8d-11d8-9d01-505054503030},share\_123,Folder1\\Folder2**</span></span>

<span data-ttu-id="4300b-301">Non è possibile combinare l'opzione della riga di comando **-er** con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-301">The **-er** command-line option cannot be combined with other command-line options.</span></span>

## <a name="listing-writer-status-and-metadata"></a><span data-ttu-id="4300b-302">Elenco di metadati e stato del writer</span><span class="sxs-lookup"><span data-stu-id="4300b-302">Listing Writer Status and Metadata</span></span>

<span data-ttu-id="4300b-303">**vshadow** **-WS**</span><span class="sxs-lookup"><span data-stu-id="4300b-303">**vshadow** **-ws**</span></span>

<span data-ttu-id="4300b-304">**vshadow** **-WM**</span><span class="sxs-lookup"><span data-stu-id="4300b-304">**vshadow** **-wm**</span></span>

<span data-ttu-id="4300b-305">**vshadow** **-wm2**</span><span class="sxs-lookup"><span data-stu-id="4300b-305">**vshadow** **-wm2**</span></span>

<span data-ttu-id="4300b-306">**vshadow** **-WM3**</span><span class="sxs-lookup"><span data-stu-id="4300b-306">**vshadow** **-wm3**</span></span>

<span data-ttu-id="4300b-307">L'opzione della riga **di comando-WS** enumera i writer del servizio Copia Shadow del volume attualmente in esecuzione nel computer e ne descrive lo stato.</span><span class="sxs-lookup"><span data-stu-id="4300b-307">The **-ws** command-line option enumerates the VSS writers that are currently running on the computer and describes their state.</span></span> <span data-ttu-id="4300b-308">Questo comando è l'equivalente del comando [vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="4300b-308">This command is the equivalent of the [Vssadmin list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754968(v=ws.11)) command.</span></span> <span data-ttu-id="4300b-309">Esistono sei possibili valori di stato: stabile, non riuscito, sconosciuto, in attesa di blocco, bloccato e in attesa del completamento.</span><span class="sxs-lookup"><span data-stu-id="4300b-309">There are six possible state values: Stable, Failed, Unknown, Waiting for freeze, Frozen, and Waiting for completion.</span></span>

<span data-ttu-id="4300b-310">L'opzione della riga di comando **-WM** elenca un riepilogo dei metadati del writer, inclusi i volumi interessati.</span><span class="sxs-lookup"><span data-stu-id="4300b-310">The **-wm** command-line option lists a summary of the writer metadata, including the affected volumes.</span></span>

<span data-ttu-id="4300b-311">L'opzione della riga di comando **-wm2** elenca tutti i metadati del writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-311">The **-wm2** command-line option lists all writer metadata.</span></span>

<span data-ttu-id="4300b-312">L'opzione della riga di comando **-WM3** elenca tutti i metadati del writer in formato XML non elaborato.</span><span class="sxs-lookup"><span data-stu-id="4300b-312">The **-wm3** command-line option lists all writer metadata in raw XML format.</span></span>

<span data-ttu-id="4300b-313">**Windows Vista e Windows Server 2003:** L'opzione della riga di comando **-WM3** non è supportata.</span><span class="sxs-lookup"><span data-stu-id="4300b-313">**Windows Vista and Windows Server 2003:** The **-wm3** command-line option is not supported.</span></span>

<span data-ttu-id="4300b-314">È possibile utilizzare queste informazioni per determinare i volumi da includere nel set di copie shadow del volume.</span><span class="sxs-lookup"><span data-stu-id="4300b-314">You can use this information to determine which volumes to include in the volume shadow copy set.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-315">Se lo stato del writer è stabile o in attesa del completamento, è possibile considerare che il writer è in uno stato stabile, pronto per il backup successivo.</span><span class="sxs-lookup"><span data-stu-id="4300b-315">If the writer state is Stable or Waiting for completion, the writer can be considered to be in a stable state, ready for the next backup.</span></span>

 

<span data-ttu-id="4300b-316">Le opzioni della riga **di comando-WS**, **-WM**, **-wm2** e **-WM3** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-316">The **-ws**, **-wm**, **-wm2**, and **-wm3** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

## <a name="performing-restore-operations"></a><span data-ttu-id="4300b-317">Esecuzione di operazioni di ripristino</span><span class="sxs-lookup"><span data-stu-id="4300b-317">Performing Restore Operations</span></span>

<span data-ttu-id="4300b-318">**vshadow** \[ OptionalFlags \] **-r =**_file_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="4300b-318">**vshadow** \[OptionalFlags\] **-r=**_File_*_.xml_*</span></span>

<span data-ttu-id="4300b-319">**vshadow** \[ OptionalFlags \] **-RS =**_file_*_. XML_*</span><span class="sxs-lookup"><span data-stu-id="4300b-319">**vshadow** \[OptionalFlags\] **-rs=**_File_*_.xml_*</span></span>

<span data-ttu-id="4300b-320">L'opzione della riga di comando **-r** esegue un'operazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4300b-320">The **-r** command-line option performs a restore operation.</span></span>

<span data-ttu-id="4300b-321">L'opzione della riga di comando **-RS** esegue un'operazione di ripristino simulato.</span><span class="sxs-lookup"><span data-stu-id="4300b-321">The **-rs** command-line option performs a simulated restore operation.</span></span>

<span data-ttu-id="4300b-322">Il file di *File.xml* deve essere un file di documento dei componenti di backup per un set di copie shadow creato con il flag facoltativo **-t** o **-BC** .</span><span class="sxs-lookup"><span data-stu-id="4300b-322">The *File.xml* file must be a Backup Components Document file for a shadow copy set that was created with the **-t** or **-bc** optional flag.</span></span>

<span data-ttu-id="4300b-323">Le opzioni della riga di comando **-r** e **-RS** si escludono a vicenda e non possono essere combinate con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-323">The **-r** and **-rs** command-line options are mutually exclusive and cannot be combined with other command-line options.</span></span>

<span data-ttu-id="4300b-324">*OptionalFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4300b-324">*OptionalFlags* is a bitmask of optional flag values from the following table.</span></span>



| <span data-ttu-id="4300b-325">Valore del flag facoltativo</span><span class="sxs-lookup"><span data-stu-id="4300b-325">Optional Flag Value</span></span>                                                                                                            | <span data-ttu-id="4300b-326">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4300b-326">Description</span></span>                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4300b-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-Wi =**_writer_</span><span class="sxs-lookup"><span data-stu-id="4300b-327"><span id="-wi_Writer"></span><span id="-wi_writer"></span><span id="-WI_WRITER"></span>**-wi=**_Writer_</span></span><br/>             | <span data-ttu-id="4300b-328">Questo flag facoltativo verifica che il writer o il componente specificato sia incluso nel ripristino.</span><span class="sxs-lookup"><span data-stu-id="4300b-328">This optional flag verifies that the specified writer or component is included in the restore.</span></span> <span data-ttu-id="4300b-329">Il *writer* può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-329">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                    |
| <span data-ttu-id="4300b-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-WX =**_writer_</span><span class="sxs-lookup"><span data-stu-id="4300b-330"><span id="-wx_Writer"></span><span id="-wx_writer"></span><span id="-WX_WRITER"></span>**-wx=**_Writer_</span></span><br/>             | <span data-ttu-id="4300b-331">Questo flag facoltativo verifica che il writer o il componente specificato venga escluso dal ripristino.</span><span class="sxs-lookup"><span data-stu-id="4300b-331">This optional flag verifies that the specified writer or component is excluded from the restore.</span></span> <span data-ttu-id="4300b-332">Il *writer* può specificare un percorso componente, un nome di writer, un ID writer o un ID istanza writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-332">*Writer* can specify a component path, writer name, writer ID, or writer instance ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="4300b-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-Exec =**_comando_</span><span class="sxs-lookup"><span data-stu-id="4300b-333"><span id="-exec_Command"></span><span id="-exec_command"></span><span id="-EXEC_COMMAND"></span>**-exec=**_Command_</span></span><br/> | <span data-ttu-id="4300b-334">Questo flag facoltativo esegue un comando o uno script tra gli eventi di pre-ripristino e post-ripristino inviati ai writer.</span><span class="sxs-lookup"><span data-stu-id="4300b-334">This optional flag executes a command or script between the pre-restore and post-restore events that are sent to the writers.</span></span> <span data-ttu-id="4300b-335">Il *comando* può specificare un comando della shell eseguibile o un file cmd.</span><span class="sxs-lookup"><span data-stu-id="4300b-335">*Command* can specify an executable shell command or a CMD file.</span></span> <span data-ttu-id="4300b-336">Se specifica un comando della shell, non è possibile specificare parametri di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-336">If it specifies a shell command, no command parameters can be specified.</span></span><br/> |
| <span data-ttu-id="4300b-337"><span id="-tracing"></span><span id="-TRACING"></span>**-traccia**</span><span class="sxs-lookup"><span data-stu-id="4300b-337"><span id="-tracing"></span><span id="-TRACING"></span>**-tracing**</span></span><br/>                                                  | <span data-ttu-id="4300b-338">Questo flag facoltativo genera un output dettagliato che può essere utilizzato per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="4300b-338">This optional flag generates verbose output that can be used for troubleshooting.</span></span><br/>                                                                                                                                                                                       |



 

## <a name="reverting-to-a-previous-shadow-copy"></a><span data-ttu-id="4300b-339">Ripristino di una copia shadow precedente</span><span class="sxs-lookup"><span data-stu-id="4300b-339">Reverting to a Previous Shadow Copy</span></span>

<span data-ttu-id="4300b-340">**vshadow** **-Revert =**_ShadowCopyId_</span><span class="sxs-lookup"><span data-stu-id="4300b-340">**vshadow** **-revert=**_ShadowCopyId_</span></span>

> [!Note]  
> <span data-ttu-id="4300b-341">Questa opzione della riga di comando è supportata solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-341">This command-line option is supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="4300b-342">**Windows server 2008 e Windows server 2003:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-342">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="4300b-343">L'opzione **-Revert** Command-line ripristina un volume alla precedente copia shadow il cui ID è specificato da *ShadowCopyId*.</span><span class="sxs-lookup"><span data-stu-id="4300b-343">The **-revert** command-line option reverts a volume to the previous shadow copy whose ID is specified by *ShadowCopyId*.</span></span>

<span data-ttu-id="4300b-344">Impossibile combinare l'opzione **-Revert** dalla riga di comando con altre opzioni della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4300b-344">The **-revert** command-line option cannot be combined with other command-line options.</span></span>

## <a name="resynchronizing-luns"></a><span data-ttu-id="4300b-345">Risincronizzazione di lun</span><span class="sxs-lookup"><span data-stu-id="4300b-345">Resynchronizing LUNs</span></span>

<span data-ttu-id="4300b-346">**vshadow** **-addresync =**_ShadowCopyId_ **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="4300b-346">**vshadow** **-addresync=**_ShadowCopyId_ **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="4300b-347">**vshadow** **-addresync =**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-Resync =**_BCDFileName_ \[ OptionalResyncFlags\]</span><span class="sxs-lookup"><span data-stu-id="4300b-347">**vshadow** **-addresync=**_ShadowCopyId_*_,_* *TargetVolumeDriveLetter* **-resync=**_BCDFileName_ \[OptionalResyncFlags\]</span></span>

<span data-ttu-id="4300b-348">L'opzione della riga di comando **-addresync** specifica i volumi da includere in un'operazione di risincronizzazione LUN.</span><span class="sxs-lookup"><span data-stu-id="4300b-348">The **-addresync** command-line option specifies the volumes to be included in a LUN resynchronization operation.</span></span> <span data-ttu-id="4300b-349">Il parametro *ShadowCopyId* specifica l'identificatore della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-349">The *ShadowCopyId* parameter specifies the identifier of the shadow copy.</span></span> <span data-ttu-id="4300b-350">Il parametro facoltativo *TargetVolumeDriveLetter* specifica il volume di destinazione in cui deve essere copiato il contenuto del volume della copia shadow.</span><span class="sxs-lookup"><span data-stu-id="4300b-350">The optional *TargetVolumeDriveLetter* parameter specifies the destination volume where the contents of the shadow copy volume are to be copied.</span></span>

<span data-ttu-id="4300b-351">L'opzione della riga di comando **-Resync** avvia un'operazione di risincronizzazione LUN.</span><span class="sxs-lookup"><span data-stu-id="4300b-351">The **-resync** command-line option initiates a LUN resynchronization operation.</span></span> <span data-ttu-id="4300b-352">Al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN del volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4300b-352">After the operation is complete, the signature of each target LUN should be identical to that of the target volume LUN.</span></span> <span data-ttu-id="4300b-353">Il parametro *BCDFileName* specifica il nome del file XML che contiene il documento del componente di backup.</span><span class="sxs-lookup"><span data-stu-id="4300b-353">The *BCDFileName* parameter specifies the name of the XML file that contains the Backup Component Document.</span></span>

> [!Note]  
> <span data-ttu-id="4300b-354">Le opzioni della riga di comando **-addresync** e **-Resync** sono supportate solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-354">The **-addresync** and **-resync** command-line options are supported only on Windows server operating systems.</span></span>

 

<span data-ttu-id="4300b-355">**Windows server 2008 e Windows server 2003:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-355">**Windows Server 2008 and Windows Server 2003:** Not supported.</span></span>

<span data-ttu-id="4300b-356">*OptionalResyncFlags* è una maschera di maschera dei valori facoltativi dei flag della tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4300b-356">*OptionalResyncFlags* is a bitmask of optional flag values from the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4300b-357">Valore del flag facoltativo</span><span class="sxs-lookup"><span data-stu-id="4300b-357">Optional flag value</span></span></th>
<th><span data-ttu-id="4300b-358">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4300b-358">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4300b-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-359"><span id="-revertsig"></span><span id="-REVERTSIG"></span><strong>-revertsig</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-360">Questo flag facoltativo specifica che, al termine dell'operazione, la firma di ogni LUN di destinazione deve essere identica a quella del LUN originale utilizzato per creare la copia shadow, non il LUN del volume di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4300b-360">This optional flag specifies that after the operation is complete, the signature of each target LUN should be identical to that of the original LUN that was used to create the shadow copy, not the target volume LUN.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-361">Il flag <strong>-revertsig</strong> è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-361">The <strong>-revertsig</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-362"><strong>Windows server 2008 e Windows server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-362"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4300b-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span><span class="sxs-lookup"><span data-stu-id="4300b-363"><span id="-novolcheck"></span><span id="-NOVOLCHECK"></span><strong>-novolcheck</strong></span></span><br/></td>
<td><span data-ttu-id="4300b-364">Questo flag facoltativo specifica che il servizio VSS non deve verificare la presenza di volumi non selezionati che verrebbero sovrascritti dall'operazione di risincronizzazione LUN.</span><span class="sxs-lookup"><span data-stu-id="4300b-364">This optional flag specifies that the VSS service should not check for unselected volumes that would be overwritten by the LUN resynchronization operation.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4300b-365">Il flag <strong>-novolcheck</strong> è supportato solo nei sistemi operativi Windows Server.</span><span class="sxs-lookup"><span data-stu-id="4300b-365">The <strong>-novolcheck</strong> flag is supported only on Windows server operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="4300b-366"><strong>Windows server 2008 e Windows server 2003:</strong> Non supportato.</span><span class="sxs-lookup"><span data-stu-id="4300b-366"><strong>Windows Server 2008 and Windows Server 2003:</strong> Not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 
