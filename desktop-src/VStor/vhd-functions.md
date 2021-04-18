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
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Funzioni disco virtuale

Nei dischi virtuali vengono usate le funzioni seguenti:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In questa sezione

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p></td>
<td><p>Applica uno snapshot del disco virtuale corrente per i file di set VHD.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p></td>
<td><p>Associa un elemento padre a un disco virtuale aperto con il flag di <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p></td>
<td><p>Consente di collegare un disco rigido virtuale (VHD) o un CD o un file di immagine DVD (ISO) individuando un provider VHD appropriato per completare l'allegato.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p></td>
<td><p>Interrompe un'operazione di mirror avviata in precedenza e imposta il mirror come disco virtuale attivo.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p></td>
<td><p>Riduce le dimensioni di un file di archivio di backup del disco rigido virtuale (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p></td>
<td><p>Consente di creare un file di immagine del disco rigido virtuale (VHD) utilizzando parametri predefiniti o un disco virtuale o un disco fisico esistente.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p></td>
<td><p>Elimina uno snapshot da un file di set VHD.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p></td>
<td><p>Elimina i metadati da un disco virtuale.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p></td>
<td><p>Scollega un disco rigido virtuale (VHD) o un CD o un file di immagine DVD (ISO) individuando un provider di dischi virtuali appropriato per eseguire l'operazione.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p></td>
<td><p>Enumera i metadati associati a un disco virtuale.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p></td>
<td><p>Aumenta le dimensioni di un disco rigido virtuale (VHD) fisso o espandibile dinamicamente.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p></td>
<td><p>Restituisce le relazioni tra dischi rigidi virtuali (VHD) o file di immagine CD o DVD (ISO) o i volumi contenuti in tali dischi e il disco o il volume padre.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p></td>
<td><p>Recupera le informazioni su un disco rigido virtuale.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p></td>
<td><p>Recupera i metadati specificati dal disco virtuale.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p></td>
<td><p>Controlla lo stato di un'operazione asincrona del disco rigido virtuale (VHD).</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p></td>
<td><p>Recupera il percorso dell'oggetto dispositivo fisico contenente un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p></td>
<td><p>Unisce un disco rigido virtuale (VHD) figlio in una catena di differenze con uno o più dischi virtuali padre nella catena.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p></td>
<td><p>Avvia un'operazione di mirroring per un disco virtuale.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p></td>
<td><p>Modifica il contenuto interno di un file di disco virtuale. Può essere utilizzato per impostare la foglia attiva o per correggere le voci di snapshot.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p></td>
<td><p>Apre un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO) da usare.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p></td>
<td><p>Recupera le informazioni sulle modifiche apportate alle aree specificate di un disco rigido virtuale (VHD) rilevate dal rilevamento delle modifiche resilienti.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p></td>
<td><p>Rilascia una richiesta SCSI incorporata direttamente a un disco rigido virtuale.</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p></td>
<td><p>Ridimensiona un disco virtuale.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p></td>
<td><p>Imposta le informazioni su un disco rigido virtuale (VHD).</p></td>
</tr>
<tr class="odd">
<td><p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p></td>
<td><p>Imposta un elemento di metadati per un disco virtuale.</p></td>
</tr>
<tr class="even">
<td><p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p></td>
<td><p>Crea uno snapshot del disco virtuale corrente per i file di set VHD.</p></td>
</tr>
</tbody>
</table>

 

 

 
