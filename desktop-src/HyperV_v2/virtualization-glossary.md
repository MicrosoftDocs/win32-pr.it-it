---
description: Glossario dei termini usati nella documentazione di Windows Virtualization SDK.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Glossario di Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233314"
---
# <a name="hyper-v-glossary"></a><span data-ttu-id="72703-103">Glossario di Hyper-V</span><span class="sxs-lookup"><span data-stu-id="72703-103">Hyper-V glossary</span></span>

<span data-ttu-id="72703-104">In questo argomento viene fornito un glossario dei termini utilizzati nella documentazione di Windows Virtualization SDK.</span><span class="sxs-lookup"><span data-stu-id="72703-104">This topic provides a glossary of terms used in the Windows Virtualization SDK documentation.</span></span>

<dl> <dt>

<span data-ttu-id="72703-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**associazione**</span><span class="sxs-lookup"><span data-stu-id="72703-105"><span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="72703-106">Processo mediante il quale i servizi e i livelli software sono collegati tra loro.</span><span class="sxs-lookup"><span data-stu-id="72703-106">A process by which software services and layers are linked together.</span></span> <span data-ttu-id="72703-107">Quando viene installato un servizio di rete, vengono stabilite le relazioni di associazione e le dipendenze per i servizi.</span><span class="sxs-lookup"><span data-stu-id="72703-107">When a network service is installed, the binding relationships and dependencies for the services are established.</span></span>

</dd> <dt>

<span data-ttu-id="72703-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Checkpoint**</span><span class="sxs-lookup"><span data-stu-id="72703-108"><span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**checkpoint**</span></span>
</dt> <dd>

<span data-ttu-id="72703-109">Uno snapshot di una macchina virtuale che consente a un amministratore di ripristinare lo stato della macchina virtuale al momento della creazione del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="72703-109">A snapshot of a virtual machine that enables an administrator to roll the virtual machine back to its state at the moment the checkpoint was created.</span></span>

</dd> <dt>

<span data-ttu-id="72703-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**Compact**</span><span class="sxs-lookup"><span data-stu-id="72703-110"><span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**compact**</span></span>
</dt> <dd>

<span data-ttu-id="72703-111">Per ridurre le dimensioni di un disco rigido virtuale a espansione dinamica, rimuovendo lo spazio inutilizzato dal file con estensione vhd.</span><span class="sxs-lookup"><span data-stu-id="72703-111">To reduce the size of a dynamically expanding virtual hard disk by removing unused space from the .vhd file.</span></span>

</dd> <dt>

<span data-ttu-id="72703-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**disco rigido virtuale differenze**</span><span class="sxs-lookup"><span data-stu-id="72703-112"><span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differencing virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="72703-113">Disco rigido virtuale in cui sono archiviate le modifiche apportate a un disco rigido virtuale padre associato allo scopo di mantenere intatto il padre.</span><span class="sxs-lookup"><span data-stu-id="72703-113">A virtual hard disk that stores the changes to an associated parent virtual hard disk for the purpose of keeping the parent intact.</span></span> <span data-ttu-id="72703-114">Il disco differenze è un file con estensione vhd separato associato al file con estensione vhd del disco padre.</span><span class="sxs-lookup"><span data-stu-id="72703-114">The differencing disk is a separate .vhd file that is associated with the .vhd file of the parent disk.</span></span> <span data-ttu-id="72703-115">Le modifiche continuano ad accumularsi nel disco differenze fino a quando non vengono unite al disco padre.</span><span class="sxs-lookup"><span data-stu-id="72703-115">Changes continue to accumulate in the differencing disk until it is merged to the parent disk.</span></span>

</dd> <dt>

<span data-ttu-id="72703-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**disco rigido virtuale a espansione dinamica**</span><span class="sxs-lookup"><span data-stu-id="72703-116"><span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamically expanding virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="72703-117">Disco rigido virtuale che aumenta di dimensioni ogni volta che viene modificato.</span><span class="sxs-lookup"><span data-stu-id="72703-117">A virtual hard disk that grows in size each time it is modified.</span></span> <span data-ttu-id="72703-118">Questo tipo di disco rigido virtuale inizia come file con estensione VHD da 3 KB e può aumentare fino a raggiungere le dimensioni massime specificate al momento della creazione del file.</span><span class="sxs-lookup"><span data-stu-id="72703-118">This type of virtual hard disk starts as a 3 KB .vhd file and can grow as large as the maximum size specified when the file was created.</span></span> <span data-ttu-id="72703-119">L'unico modo per ridurre le dimensioni del file consiste nello azzerare i dati eliminati, quindi compattare il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-119">The only way to reduce the file size is to zero out the deleted data and then compact the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="72703-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**disco rigido virtuale a dimensione fissa**</span><span class="sxs-lookup"><span data-stu-id="72703-120"><span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**fixed-size virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="72703-121">Un disco rigido virtuale con una dimensione fissa determinata e per cui tutto lo spazio viene allocato quando viene creato il disco.</span><span class="sxs-lookup"><span data-stu-id="72703-121">A virtual hard disk with a fixed size that is determined and for which all space is allocated when the disk is created.</span></span> <span data-ttu-id="72703-122">Le dimensioni del disco non cambiano quando i dati vengono aggiunti o eliminati.</span><span class="sxs-lookup"><span data-stu-id="72703-122">The size of the disk does not change when data is added or deleted.</span></span>

</dd> <dt>

<span data-ttu-id="72703-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Macchina virtuale di prima generazione**</span><span class="sxs-lookup"><span data-stu-id="72703-123"><span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Generation 1 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="72703-124">Una macchina virtuale (VM) che contiene lo stesso hardware virtuale presente nelle versioni di Hyper-V precedenti a Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="72703-124">A virtual machine (VM) that contains the same virtual hardware present in versions of Hyper-V prior to Windows 8.1 and Windows Server 2012 R2</span></span>

</dd> <dt>

<span data-ttu-id="72703-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Macchina virtuale di seconda generazione**</span><span class="sxs-lookup"><span data-stu-id="72703-125"><span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Generation 2 virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="72703-126">Una macchina virtuale (VM) che contiene un modello di hardware virtuale semplificato e usa il firmware UEFI anziché il BIOS.</span><span class="sxs-lookup"><span data-stu-id="72703-126">A virtual machine (VM) that contains a simplified virtual hardware model and uses UEFI firmware instead of BIOS.</span></span> <span data-ttu-id="72703-127">In questa VM la maggior parte dei dispositivi emulati viene rimossa, riducendo la complessità della gestione e la superficie di attacco alla sicurezza.</span><span class="sxs-lookup"><span data-stu-id="72703-127">In this VM, most of the emulated devices are removed, which reduces management complexity and security attack surface.</span></span>

</dd> <dt>

<span data-ttu-id="72703-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**sistema operativo guest**</span><span class="sxs-lookup"><span data-stu-id="72703-128"><span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**guest operating system**</span></span>
</dt> <dd>

<span data-ttu-id="72703-129">Il sistema operativo installato nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-129">The operating system running on a virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="72703-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Integration Services**</span><span class="sxs-lookup"><span data-stu-id="72703-130"><span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**integration services**</span></span>
</dt> <dd>

<span data-ttu-id="72703-131">Una raccolta di servizi e driver software che massimizzano le prestazioni e offrono un'esperienza utente migliore all'interno di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-131">A collection of services and software drivers that maximize performance and provide a better user experience within a virtual machine.</span></span> <span data-ttu-id="72703-132">I servizi di integrazione sono disponibili solo per i sistemi operativi guest supportati.</span><span class="sxs-lookup"><span data-stu-id="72703-132">Integration services are only available for supported guest operating systems.</span></span>

</dd> <dt>

<span data-ttu-id="72703-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**coppia chiave-valore**</span><span class="sxs-lookup"><span data-stu-id="72703-133"><span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**key-value pair**</span></span>
</dt> <dd>

<span data-ttu-id="72703-134">Set di elementi di dati che contiene un identificatore univoco, denominato chiave, e un valore che rappresenta i dati effettivi della chiave.</span><span class="sxs-lookup"><span data-stu-id="72703-134">A set of data items that contains a unique identifier, called a key, and a value that is the actual data for the key.</span></span>

</dd> <dt>

<span data-ttu-id="72703-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**computer fisico**</span><span class="sxs-lookup"><span data-stu-id="72703-135"><span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physical computer**</span></span>
</dt> <dd>

<span data-ttu-id="72703-136">Un computer basato su hardware, anziché una macchina virtuale basata su software.</span><span class="sxs-lookup"><span data-stu-id="72703-136">A hardware-based computer, as opposed to a software-based virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="72703-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**stato salvato**</span><span class="sxs-lookup"><span data-stu-id="72703-137"><span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**saved state**</span></span>
</dt> <dd>

<span data-ttu-id="72703-138">Modalità di archiviazione di una macchina virtuale in modo che possa essere ripresa rapidamente, in modo analogo a un computer portatile in stato di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="72703-138">A manner of storing a virtual machine so that it can be quickly resumed, similar to a hibernated laptop.</span></span> <span data-ttu-id="72703-139">Quando si inserisce una macchina virtuale in esecuzione in uno stato salvato, Virtual Server e Hyper-V arrestano la macchina virtuale, scrivono i dati presenti in memoria in file temporanei e interrompono il consumo delle risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="72703-139">When you place a running virtual machine in a saved state, Virtual Server and Hyper-V stop the virtual machine, write the data that exists in memory to temporary files, and stop the consumption of system resources.</span></span> <span data-ttu-id="72703-140">Il ripristino di una macchina virtuale da uno stato salvato restituisce la stessa condizione in cui si trovava al momento del salvataggio dello stato.</span><span class="sxs-lookup"><span data-stu-id="72703-140">Restoring a virtual machine from a saved state returns it to the same condition it was in when its state was saved.</span></span>

</dd> <dt>

<span data-ttu-id="72703-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**disco floppy virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-141"><span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtual floppy disk**</span></span>
</dt> <dd>

<span data-ttu-id="72703-142">Una versione basata su file di un disco floppy fisico.</span><span class="sxs-lookup"><span data-stu-id="72703-142">A file-based version of a physical floppy disk.</span></span> <span data-ttu-id="72703-143">Un disco floppy virtuale viene archiviato come file con estensione vfd.</span><span class="sxs-lookup"><span data-stu-id="72703-143">A virtual floppy disk is stored as a file with a .vfd file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="72703-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**disco rigido virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-144"><span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtual hard disk**</span></span>
</dt> <dd>

<span data-ttu-id="72703-145">Supporto di archiviazione per una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-145">The storage medium for a virtual machine.</span></span> <span data-ttu-id="72703-146">Può risiedere in qualsiasi topologia di archiviazione accessibile dal sistema operativo host, tra cui dispositivi esterni, reti dell'area di archiviazione e archiviazione collegata alla rete.</span><span class="sxs-lookup"><span data-stu-id="72703-146">It can reside on any storage topology that the host operating system can access, including external devices, storage area networks, and network-attached storage.</span></span> <span data-ttu-id="72703-147">L'estensione del nome file è VHD.</span><span class="sxs-lookup"><span data-stu-id="72703-147">The file name extension is .vhd.</span></span>

</dd> <dt>

<span data-ttu-id="72703-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**macchina virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-148"><span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtual machine**</span></span>
</dt> <dd>

<span data-ttu-id="72703-149">Un computer all'interno di un computer, implementato nel software.</span><span class="sxs-lookup"><span data-stu-id="72703-149">A computer within a computer, implemented in software.</span></span> <span data-ttu-id="72703-150">Una macchina virtuale emula un sistema hardware completo, dal processore alla scheda di rete, in un ambiente software autosufficiente e isolato, consentendo il funzionamento simultaneo di sistemi operativi altrimenti incompatibili.</span><span class="sxs-lookup"><span data-stu-id="72703-150">A virtual machine emulates a complete hardware system, from processor to network card, in a self-contained, isolated software environment, enabling the simultaneous operation of otherwise incompatible operating systems.</span></span> <span data-ttu-id="72703-151">Ogni sistema operativo figlio viene eseguito in una macchina virtuale software isolata.</span><span class="sxs-lookup"><span data-stu-id="72703-151">Each child operating system runs in its own isolated software virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="72703-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**configurazione macchina virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-152"><span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**virtual machine configuration**</span></span>
</dt> <dd>

<span data-ttu-id="72703-153">Configurazione delle risorse assegnate a una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-153">The configuration of the resources assigned to a virtual machine.</span></span> <span data-ttu-id="72703-154">Gli esempi includono dispositivi come dischi e schede di rete, nonché memoria e processori.</span><span class="sxs-lookup"><span data-stu-id="72703-154">Examples include devices such as disks and network adapters, as well as memory and processors.</span></span>

</dd> <dt>

<span data-ttu-id="72703-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Servizio Virtual Machine Management**</span><span class="sxs-lookup"><span data-stu-id="72703-155"><span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Virtual Machine Management Service**</span></span>
</dt> <dd>

<span data-ttu-id="72703-156">Servizio Hyper-V che consente di gestire l'accesso alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="72703-156">The Hyper-V service that provides management access to virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="72703-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**snapshot macchina virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-157"><span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**virtual machine snapshot**</span></span>
</dt> <dd>

<span data-ttu-id="72703-158">Snapshot basato su file dello stato, dei dati del disco e della configurazione di una macchina virtuale in un momento specifico.</span><span class="sxs-lookup"><span data-stu-id="72703-158">A file-based snapshot of the state, disk data, and configuration of a virtual machine at a specific point in time.</span></span>

</dd> <dt>

<span data-ttu-id="72703-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**rete virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-159"><span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtual network**</span></span>
</dt> <dd>

<span data-ttu-id="72703-160">Versione virtuale di uno switch di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="72703-160">A virtual version of a physical network switch.</span></span> <span data-ttu-id="72703-161">Una rete virtuale può essere configurata per fornire accesso alle risorse di rete locali o esterne per una o più macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="72703-161">A virtual network can be configured to provide access to local or external network resources for one or more virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="72703-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Gestione reti virtuali**</span><span class="sxs-lookup"><span data-stu-id="72703-162"><span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network Manager**</span></span>
</dt> <dd>

<span data-ttu-id="72703-163">Servizio Hyper-V usato per creare e gestire reti virtuali.</span><span class="sxs-lookup"><span data-stu-id="72703-163">A Hyper-V service used to create and manage virtual networks.</span></span>

</dd> <dt>

<span data-ttu-id="72703-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**Commuter virtuale**</span><span class="sxs-lookup"><span data-stu-id="72703-164"><span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtual switch**</span></span>
</dt> <dd>

<span data-ttu-id="72703-165">Vedere rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-165">See virtual network.</span></span>

</dd> <dt>

<span data-ttu-id="72703-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Ridimensionamento VHDX**</span><span class="sxs-lookup"><span data-stu-id="72703-166"><span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**VHDX resize**</span></span>
</dt> <dd>

<span data-ttu-id="72703-167">Operazione che compatta o espande un disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="72703-167">The operation that shrinks or expands a virtual hard disk.</span></span>

</dd> </dl>

 

 



