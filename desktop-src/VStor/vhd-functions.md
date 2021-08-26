---
description: 'Altre informazioni su: <span id=vhd.vhd_functions></span> Funzioni del disco virtuale'
MS-HAID: vhd.vhd\_functions
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Funzioni del disco virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32133e3afa8402de8483a68eb4957b261b46e556
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477217"
---
# <a name="span-idvhdvhd_functionsspanvirtual-disk-functions"></a><span id="vhd.vhd_functions"></span>Funzioni del disco virtuale

Nei dischi virtuali vengono usate le funzioni seguenti:

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In questa sezione


| Argomento | Descrizione | 
|-------|-------------|
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-applysnapshotvhdset"><strong>ApplySnapshotVhdSet</strong></a></p> | <p>Applica uno snapshot del disco virtuale corrente per i file del set di dischi rigidi virtuali.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-addvirtualdiskparent"><strong>AddVirtualDiskParent</strong></a></p> | <p>Collega un elemento padre a un disco virtuale aperto con il flag <strong>OPEN_VIRTUAL_DISK_FLAG_CUSTOM_DIFF_CHAIN.</strong></p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-attachvirtualdisk"><strong>AttachVirtualDisk</strong></a></p> | <p>Collega un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO) individuando un provider di dischi rigidi virtuali appropriato per eseguire l'allegato.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-breakmirrorvirtualdisk"><strong>BreakMirrorVirtualDisk</strong></a></p> | <p>Interrompe un'operazione mirror avviata in precedenza e imposta il mirror come disco virtuale attivo.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-compactvirtualdisk"><strong>CompactVirtualDisk</strong></a></p> | <p>Riduce le dimensioni di un file dell'archivio di backup di un disco rigido virtuale (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk"><strong>CreateVirtualDisk</strong></a></p> | <p>Crea un file di immagine del disco rigido virtuale (VHD), usando i parametri predefiniti o un disco virtuale o un disco fisico esistente.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-deletesnapshotvhdset"><strong>DeleteSnapshotVhdSet</strong></a></p> | <p>Elimina uno snapshot da un file set di dischi rigidi virtuali.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-deletevirtualdiskmetadata"><strong>DeleteVirtualDiskMetadata</strong></a></p> | <p>Elimina i metadati da un disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-detachvirtualdisk"><strong>DetachVirtualDisk</strong></a></p> | <p>Scollega un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO) individuando un provider di dischi virtuali appropriato per eseguire l'operazione.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-enumeratevirtualdiskmetadata"><strong>EnumerateVirtualDiskMetadata</strong></a></p> | <p>Enumera i metadati associati a un disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk"><strong>ExpandVirtualDisk</strong></a></p> | <p>Aumenta le dimensioni di un disco rigido virtuale (VHD) fisso o espandibile dinamicamente.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getstoragedependencyinformation"><strong>GetStorageDependencyInformation</strong></a></p> | <p>Restituisce le relazioni tra dischi rigidi virtuali (VHD) o file di immagine CD o DVD (ISO) o i volumi contenuti all'interno di tali dischi e il relativo disco o volume padre.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskinformation"><strong>GetVirtualDiskInformation</strong></a></p> | <p>Recupera informazioni su un disco rigido virtuale.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata"><strong>GetVirtualDiskMetadata</strong></a></p> | <p>Recupera i metadati specificati dal disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskoperationprogress"><strong>GetVirtualDiskOperationProgress</strong></a></p> | <p>Controlla lo stato di avanzamento di un'operazione asincrona su disco rigido virtuale (VHD).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-getvirtualdiskphysicalpath"><strong>GetVirtualDiskPhysicalPath</strong></a></p> | <p>Recupera il percorso dell'oggetto dispositivo fisico che contiene un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO).</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk"><strong>MergeVirtualDisk</strong></a></p> | <p>Unisce un disco rigido virtuale figlio (VHD) in una catena differenze con uno o più dischi virtuali padre nella catena.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-mirrorvirtualdisk"><strong>MirrorVirtualDisk</strong></a></p> | <p>Avvia un'operazione mirror per un disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-modifyvhdset"><strong>ModifyVhdSet</strong></a></p> | <p>Modifica il contenuto interno di un file su disco virtuale. Può essere usato per impostare la foglia attiva o per correggere le voci dello snapshot.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk"><strong>OpenVirtualDisk</strong></a></p> | <p>Apre un disco rigido virtuale (VHD) o un file di immagine CD o DVD (ISO) per l'uso.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-querychangesvirtualdisk"><strong>QueryChangesVirtualDisk</strong></a></p> | <p>Recupera informazioni sulle modifiche apportate alle aree specificate di un disco rigido virtuale (VHD) rilevate dal rilevamento delle modifiche resilienti.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-rawscsivirtualdisk"><strong>RawSCSIVirtualDisk</strong></a></p> | <p>Esezione di una richiesta SCSI incorporata direttamente a un disco rigido virtuale.</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-resizevirtualdisk"><strong>ResizeVirtualDisk</strong></a></p> | <p>Ridimensiona un disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation"><strong>SetVirtualDiskInformation</strong></a></p> | <p>Imposta le informazioni su un disco rigido virtuale (VHD).</p> | 
| <p><a href="/windows/desktop/api/virtdisk/nf-virtdisk-setvirtualdiskmetadata"><strong>SetVirtualDiskMetadata</strong></a></p> | <p>Imposta un elemento di metadati per un disco virtuale.</p> | 
| <p><a href="/windows/win32/api/virtdisk/nf-virtdisk-takesnapshotvhdset"><strong>TakeSnapshotVhdSet</strong></a></p> | <p>Crea uno snapshot del disco virtuale corrente per i file del set di dischi rigidi virtuali.</p> | 


 

 

 
