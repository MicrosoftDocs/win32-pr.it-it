---
description: 'Altre informazioni su: <span id=vhd.vhd_functions></span> funzioni disco virtuale'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funzioni disco virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f31af2b24a55baa3c64bfe5bd9e09e0b9e2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307115"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span data-ttu-id="49749-103"><span id="vhd.vhd_functions"></span>Funzioni disco virtuale</span><span class="sxs-lookup"><span data-stu-id="49749-103"><span id="vhd.vhd_functions"></span>Virtual Disk Functions</span></span>

<span data-ttu-id="49749-104">Nei dischi virtuali vengono usate le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="49749-104">The following functions are used in Virtual Disks:</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="49749-105"><span id="in_this_section"></span>In questa sezione</span><span class="sxs-lookup"><span data-stu-id="49749-105"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49749-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="49749-106">Topic</span></span></th>
<th><span data-ttu-id="49749-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49749-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49749-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-108"><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-109">Applica uno snapshot del disco virtuale corrente per i file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="49749-109">Applies a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-110"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-111">Associa un elemento padre a un disco virtuale aperto con il flag di <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="49749-111">Attaches a parent to a virtual disk opened with the <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> flag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-112"><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-113">Consente di collegare un disco rigido virtuale (VHD) o un CD o un file di immagine DVD (ISO) individuando un provider VHD appropriato per completare l'allegato.</span><span class="sxs-lookup"><span data-stu-id="49749-113">Attaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate VHD provider to accomplish the attachment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-114"><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-115">Interrompe un'operazione di mirror avviata in precedenza e imposta il mirror come disco virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="49749-115">Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-116"><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-117">Riduce le dimensioni di un file di archivio di backup del disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="49749-117">Reduces the size of a virtual hard disk (VHD) backing store file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-118"><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-119">Consente di creare un file di immagine del disco rigido virtuale (VHD) utilizzando parametri predefiniti o un disco virtuale o un disco fisico esistente.</span><span class="sxs-lookup"><span data-stu-id="49749-119">Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-120"><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-121">Elimina uno snapshot da un file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="49749-121">Deletes a snapshot from a VHD Set file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-122"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-123">Elimina i metadati da un disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-123">Deletes metadata from a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-124"><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-125">Scollega un disco rigido virtuale (VHD) o un CD o un file di immagine DVD (ISO) individuando un provider di dischi virtuali appropriato per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="49749-125">Detaches a virtual hard disk (VHD) or CD or DVD image file (ISO) by locating an appropriate virtual disk provider to accomplish the operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-126"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-127">Enumera i metadati associati a un disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-127">Enumerates the metadata associated with a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-128"><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-129">Aumenta le dimensioni di un disco rigido virtuale (VHD) fisso o espandibile dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="49749-129">Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-130"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-131">Restituisce le relazioni tra dischi rigidi virtuali (VHD) o file di immagine CD o DVD (ISO) o i volumi contenuti in tali dischi e il disco o il volume padre.</span><span class="sxs-lookup"><span data-stu-id="49749-131">Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-132"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-133">Recupera le informazioni su un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-133">Retrieves information about a VHD.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-134"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-135">Recupera i metadati specificati dal disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-135">Retrieves the specified metadata from the virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-136"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-137">Controlla lo stato di un'operazione asincrona del disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="49749-137">Checks the progress of an asynchronous virtual hard disk (VHD) operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-138"><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-139">Recupera il percorso dell'oggetto dispositivo fisico contenente un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO).</span><span class="sxs-lookup"><span data-stu-id="49749-139">Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-140"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-141">Unisce un disco rigido virtuale (VHD) figlio in una catena di differenze con uno o più dischi virtuali padre nella catena.</span><span class="sxs-lookup"><span data-stu-id="49749-141">Merges a child virtual hard disk (VHD) in a differencing chain with one or more parent virtual disks in the chain.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-142"><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-143">Avvia un'operazione di mirroring per un disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-143">Initiates a mirror operation for a virtual disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-144"><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-145">Modifica il contenuto interno di un file di disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-145">Modifies the internal contents of a virtual disk file.</span></span> <span data-ttu-id="49749-146">Può essere utilizzato per impostare la foglia attiva o per correggere le voci di snapshot.</span><span class="sxs-lookup"><span data-stu-id="49749-146">Can be used to set the active leaf, or to fix up snapshot entries.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-147"><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-148">Apre un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO) da usare.</span><span class="sxs-lookup"><span data-stu-id="49749-148">Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-149"><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-150">Recupera le informazioni sulle modifiche apportate alle aree specificate di un disco rigido virtuale (VHD) rilevate dal rilevamento delle modifiche resilienti.</span><span class="sxs-lookup"><span data-stu-id="49749-150">Retrieves information about changes to the specified areas of a virtual hard disk (VHD) that are tracked by resilient change tracking (RCT).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-151"><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-152">Rilascia una richiesta SCSI incorporata direttamente a un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-152">Issues an embedded SCSI request directly to a virtual hard disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-153"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-154">Ridimensiona un disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-154">Resizes a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-155"><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-156">Imposta le informazioni su un disco rigido virtuale (VHD).</span><span class="sxs-lookup"><span data-stu-id="49749-156">Sets information about a virtual hard disk (VHD).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49749-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-157"><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-158">Imposta un elemento di metadati per un disco virtuale.</span><span class="sxs-lookup"><span data-stu-id="49749-158">Sets a metadata item for a virtual disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49749-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="49749-159"><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></span></span></p></td>
<td><p><span data-ttu-id="49749-160">Crea uno snapshot del disco virtuale corrente per i file di set VHD.</span><span class="sxs-lookup"><span data-stu-id="49749-160">Creates a snapshot of the current virtual disk for VHD Set files.</span></span></p></td>
</tr>
</tbody>
</table>

 

 

 
