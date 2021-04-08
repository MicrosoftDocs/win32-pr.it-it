---
description: Questa sezione fornisce un glossario dei termini tecnici usati nella documentazione relativa al servizio dischi virtuali (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossario servizio dischi virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc8804f1aea832f59fcbcab65423e92e134939f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967597"
---
# <a name="virtual-disk-service-glossary"></a><span data-ttu-id="93a13-103">Glossario servizio dischi virtuali</span><span class="sxs-lookup"><span data-stu-id="93a13-103">Virtual Disk Service Glossary</span></span>

<span data-ttu-id="93a13-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93a13-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="93a13-105">Questa sezione fornisce un glossario dei termini tecnici usati nella documentazione relativa al servizio dischi virtuali (VDS).</span><span class="sxs-lookup"><span data-stu-id="93a13-105">This section provides a glossary of technical terms used in the Virtual Disk Service (VDS) documentation.</span></span>

<dl> <dt>

<span data-ttu-id="93a13-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configurazione di automagic**</span><span class="sxs-lookup"><span data-stu-id="93a13-106"><span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**automagic configuration**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-107">Provider RAID hardware che fornisce un set di regole per la scelta del mapping dei blocchi logici LUN in base a attributi semplici.</span><span class="sxs-lookup"><span data-stu-id="93a13-107">Hardware RAID provider that supplies a set of rules for choosing LUN logical block remapping based on simple attributes.</span></span> <span data-ttu-id="93a13-108">I provider di automagic possono anche modificare dinamicamente il mapping per la gestione delle prestazioni o degli errori.</span><span class="sxs-lookup"><span data-stu-id="93a13-108">Automagic providers can also dynamically alter the mapping for performance or fault management.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Suggerimenti per la magia automatica**</span><span class="sxs-lookup"><span data-stu-id="93a13-109"><span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**automagic hints**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-110">Informazioni fornite a un provider di automagic per guidare la configurazione dei blocchi logici LUN.</span><span class="sxs-lookup"><span data-stu-id="93a13-110">Information supplied to an automagic provider to guide the LUN logical block configuration.</span></span> <span data-ttu-id="93a13-111">Gli hint includono informazioni sulla tolleranza di errore desiderata, sull'atomicità fisica e sul modello di accesso I/O previsto.</span><span class="sxs-lookup"><span data-stu-id="93a13-111">Hints include information as to the desired fault tolerance, physical atomicity, and intended I/O access pattern.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco di base**</span><span class="sxs-lookup"><span data-stu-id="93a13-112"><span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**basic disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-113">Disco gestito dal provider software più semplice possibile.</span><span class="sxs-lookup"><span data-stu-id="93a13-113">A disk managed by the simplest possible software provider.</span></span> <span data-ttu-id="93a13-114">Il provider di dischi di base supporta solo i volumi che vengono mappati direttamente alle strutture di dati di configurazione della partizione.</span><span class="sxs-lookup"><span data-stu-id="93a13-114">The basic disk provider supports only volumes that directly map to partition configuration data structures.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**associazione**</span><span class="sxs-lookup"><span data-stu-id="93a13-115"><span id="base.binding"></span><span id="BASE.BINDING"></span>**binding**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-116">Selezione di un set di mapping a risorse fisiche.</span><span class="sxs-lookup"><span data-stu-id="93a13-116">Selecting for a set of mappings to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convertire**</span><span class="sxs-lookup"><span data-stu-id="93a13-117"><span id="base.convert"></span><span id="BASE.CONVERT"></span>**convert**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-118">Processo di conversione di un disco di base in un disco dinamico.</span><span class="sxs-lookup"><span data-stu-id="93a13-118">The process of converting a basic disk to a dynamic disk.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configurazione**</span><span class="sxs-lookup"><span data-stu-id="93a13-119"><span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configuration**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-120">Raccolta dei parametri operativi che forniscono il mapping da un volume, o LUN, alle risorse fisiche.</span><span class="sxs-lookup"><span data-stu-id="93a13-120">A collection of the operating parameters that supply the mapping from a volume, or LUN, to physical resources.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span><span class="sxs-lookup"><span data-stu-id="93a13-121"><span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-122">Programma software che contiene l'intelligence di runtime per un provider hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-122">A software program that contains the runtime intelligence for a hardware provider.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disco**</span><span class="sxs-lookup"><span data-stu-id="93a13-123"><span id="base.disk"></span><span id="BASE.DISK"></span>**disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-124">Un disco fisico o un LUN RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-124">A physical disk or hardware RAID LUN.</span></span> <span data-ttu-id="93a13-125">I dischi sono destinazioni per il carico di I/O di archiviazione di runtime; Plug and Play (PNP) non distingue tra JBOD e lun.</span><span class="sxs-lookup"><span data-stu-id="93a13-125">Disks are targets for runtime storage I/O load; Plug and Play (PNP) does not distinguish between JBOD and LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disco rigido**</span><span class="sxs-lookup"><span data-stu-id="93a13-126"><span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disk platter**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-127">Subset di un pacchetto usato per esportare o importare volumi da un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="93a13-127">A subset of a pack used for exporting or importing volumes from a pack.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**pacchetto di dischi**</span><span class="sxs-lookup"><span data-stu-id="93a13-128"><span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**disk pack**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-129">Vedere *Pack*.</span><span class="sxs-lookup"><span data-stu-id="93a13-129">See *pack*.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**unità**</span><span class="sxs-lookup"><span data-stu-id="93a13-130"><span id="base.drive"></span><span id="BASE.DRIVE"></span>**drive**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-131">Un mandrino del disco fisico all'interno di un sottosistema RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-131">A physical disk spindle within a hardware RAID subsystem.</span></span> <span data-ttu-id="93a13-132">Le unità sono associate a lun dal sottosistema.</span><span class="sxs-lookup"><span data-stu-id="93a13-132">Drives are bound into LUNs by the subsystem.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinamico**</span><span class="sxs-lookup"><span data-stu-id="93a13-133"><span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**dynamic disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-134">Disco gestito da un provider RAID software con supporto per la riconfigurazione flessibile dei volumi.</span><span class="sxs-lookup"><span data-stu-id="93a13-134">A disk managed by a software RAID provider with support for flexible volume reconfiguration.</span></span> <span data-ttu-id="93a13-135">Un disco dinamico utilizza una partizione come contenitore per i volumi. Nessun mapping garantito.</span><span class="sxs-lookup"><span data-stu-id="93a13-135">A dynamic disk uses a partition as a container for volumes; there is no guaranteed mapping.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configurazione esplicita**</span><span class="sxs-lookup"><span data-stu-id="93a13-136"><span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**explicit configuration**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-137">Una configurazione con i parametri, inclusi il tipo di volume e il layout esatto, per una raccolta di volumi di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93a13-137">A configuration with the parameters, including the volume type and the exact layout, for a collection of target volumes.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**esportazione**</span><span class="sxs-lookup"><span data-stu-id="93a13-138"><span id="base.export"></span><span id="BASE.EXPORT"></span>**export**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-139">Operazione di trasferimento di un disco e di tutti i volumi contenuti su tale disco da un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="93a13-139">The act of moving a disk platter and all volumes contained on that platter out of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span><span class="sxs-lookup"><span data-stu-id="93a13-140"><span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-141">Intervallo contiguo di settori logici che contribuiscono a un singolo volume o disco.</span><span class="sxs-lookup"><span data-stu-id="93a13-141">A contiguous range of logical sectors contributing to a single volume or disk.</span></span> <span data-ttu-id="93a13-142">Un extent può anche essere un intervallo di settori non allocati.</span><span class="sxs-lookup"><span data-stu-id="93a13-142">An extent can also be range of unallocated sectors.</span></span> <span data-ttu-id="93a13-143">In genere, un file system Visualizza i dettagli dell'extent per un utente finale.</span><span class="sxs-lookup"><span data-stu-id="93a13-143">Commonly, a file system displays the extent details to an end-user.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabella di partizione GUID (GPT)**</span><span class="sxs-lookup"><span data-stu-id="93a13-144"><span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**GUID Partition Table (GPT)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-145">Strutture usate dal firmware EFI.</span><span class="sxs-lookup"><span data-stu-id="93a13-145">Structures used by EFI firmware.</span></span> <span data-ttu-id="93a13-146">GPT è uno dei due formati di dati di configurazione software di livello più basso usati dal firmware della piattaforma per individuare un sistema operativo di avvio o un'altra immagine eseguibile.</span><span class="sxs-lookup"><span data-stu-id="93a13-146">GPT is one of two lowest level software configuration data formats used by platform firmware to locate a bootable operating system or other executable image.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provider hardware**</span><span class="sxs-lookup"><span data-stu-id="93a13-147"><span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**hardware provider**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-148">Una raccolta di software eseguita nell'host, una scheda bus ed eventualmente un sottosistema di archiviazione esterno che interagisce con la superficie e la gestione dei lun RAID.</span><span class="sxs-lookup"><span data-stu-id="93a13-148">A collection of software that executes on the host, a bus adapter, and possibly an external storage subsystem that works together to surface and manage RAID LUNs.</span></span> <span data-ttu-id="93a13-149">I provider hardware per la maggior parte dei sottosistemi di archiviazione esterni contengono solo software basato su host e modalità utente.</span><span class="sxs-lookup"><span data-stu-id="93a13-149">Hardware providers for most external storage subsystems contain only user-mode, host-based software.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**salute**</span><span class="sxs-lookup"><span data-stu-id="93a13-150"><span id="base.health"></span><span id="BASE.HEALTH"></span>**health**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-151">Stato corrente di gestione degli errori di un volume o di un LUN.</span><span class="sxs-lookup"><span data-stu-id="93a13-151">The current fault-management status of a volume or a LUN.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**Hot Spare**</span><span class="sxs-lookup"><span data-stu-id="93a13-152"><span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**hot sparing**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-153">Aggiunta temporanea di un volume Plex a un volume.</span><span class="sxs-lookup"><span data-stu-id="93a13-153">Temporarily adding a volume plex to a volume.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**importare**</span><span class="sxs-lookup"><span data-stu-id="93a13-154"><span id="base.import"></span><span id="BASE.IMPORT"></span>**import**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-155">Operazione di trasferimento di un disco rigido e di tutti i relativi volumi in un pacchetto esistente.</span><span class="sxs-lookup"><span data-stu-id="93a13-155">The act of moving a disk platter and all its volumes into an existing pack.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un gruppo di dischi (JBOD)**</span><span class="sxs-lookup"><span data-stu-id="93a13-156"><span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**just a bunch of disks (JBOD)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-157">Raccolta di assi fisici senza il controllo coordinato fornito da un dispositivo RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-157">A collection of physical spindles without the coordinated control provided by a hardware RAID device.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**numero blocco logico (LBN)**</span><span class="sxs-lookup"><span data-stu-id="93a13-158"><span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**logical block number (LBN)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-159">Unità più piccola indirizzabile di dati di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93a13-159">The smallest addressable unit of storage data.</span></span> <span data-ttu-id="93a13-160">LBN viene usato con I protocolli di comando di I/O.</span><span class="sxs-lookup"><span data-stu-id="93a13-160">LBN is used with I/O command protocols.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapping del blocco logico**</span><span class="sxs-lookup"><span data-stu-id="93a13-161"><span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**logical block mapping**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-162">Trasformazione dei blocchi logici presentati a un provider a quelli esposti dal provider.</span><span class="sxs-lookup"><span data-stu-id="93a13-162">The transformation of the logical blocks presented to a provider to those exposed by the provider.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**numero di unità logica (LUN)**</span><span class="sxs-lookup"><span data-stu-id="93a13-163"><span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**logical unit number (LUN)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-164">Unità di archiviazione fisicamente indirizzabile come superficie di un sottosistema RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-164">A physically addressable storage unit as surfaced by a hardware RAID subsystem.</span></span> <span data-ttu-id="93a13-165">Questo termine può anche fare riferimento all'identificatore SCSI per l'unità di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="93a13-165">This term can also refer to the SCSI identifier for the storage unit.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Numero LUN**</span><span class="sxs-lookup"><span data-stu-id="93a13-166"><span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**LUN number**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-167">Numero assegnato da un provider hardware VDS a un LUN in una matrice.</span><span class="sxs-lookup"><span data-stu-id="93a13-167">A number that a VDS hardware provider assigns to a LUN in an array.</span></span> <span data-ttu-id="93a13-168">Non corrisponde al "numero di unità logica" nell'indirizzo SCSI del disco.</span><span class="sxs-lookup"><span data-stu-id="93a13-168">This is not the same as the "logical unit number" in the disk's SCSI address.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servizio di gestione**</span><span class="sxs-lookup"><span data-stu-id="93a13-169"><span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**management service**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-170">Un programma software che viene eseguito in base alle esigenze per eseguire la configurazione, il monitoraggio o la gestione degli errori del volume.</span><span class="sxs-lookup"><span data-stu-id="93a13-170">A software program that executes as needed to perform volume configuration, monitoring, or fault handling.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span><span class="sxs-lookup"><span data-stu-id="93a13-171"><span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-172">Volume esposto al sistema operativo e con un nome di volume associato (lettera di unità).</span><span class="sxs-lookup"><span data-stu-id="93a13-172">A volume that is exposed to the operating system and has an associated volume name (a drive letter).</span></span> <span data-ttu-id="93a13-173">Un volume è accessibile da un file system.</span><span class="sxs-lookup"><span data-stu-id="93a13-173">A volume is accessible by a file system.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**mascheramento**</span><span class="sxs-lookup"><span data-stu-id="93a13-174"><span id="base.masking"></span><span id="BASE.MASKING"></span>**masking**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-175">Disco non riconosciuto dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="93a13-175">A disk not recognized by the operating system.</span></span> <span data-ttu-id="93a13-176">Un disco può essere mascherato dal sottosistema RAID hardware, dall'opzione, dalla riserva SCSI da un altro host del computer o dal software nello stack del disco.</span><span class="sxs-lookup"><span data-stu-id="93a13-176">A disk can be masked by the hardware RAID subsystem, switch, SCSI RESERVE by another computer host, or software in the disk stack.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**il partizionamento del record di avvio principale (MBR)**</span><span class="sxs-lookup"><span data-stu-id="93a13-177"><span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**master boot record partitioning (MBR)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-178">MBR è uno dei due formati di dati di configurazione software di livello più basso e viene usato dal firmware BIOS per individuare un'immagine del sistema operativo avviabile.</span><span class="sxs-lookup"><span data-stu-id="93a13-178">MBR is one of two lowest level software configuration data formats, and is used by BIOS firmware to locate a bootable operating system image.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**membro**</span><span class="sxs-lookup"><span data-stu-id="93a13-179"><span id="base.member"></span><span id="BASE.MEMBER"></span>**member**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-180">Raccolta di extent concatenati del disco contenuti in uno o più dischi.</span><span class="sxs-lookup"><span data-stu-id="93a13-180">A collection of concatenated disk extents contained on one more disks.</span></span> <span data-ttu-id="93a13-181">Un disco può contribuire solo a un membro di un volume.</span><span class="sxs-lookup"><span data-stu-id="93a13-181">A disk can contribute to only one member of a volume.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**specchio**</span><span class="sxs-lookup"><span data-stu-id="93a13-182"><span id="base.mirror"></span><span id="BASE.MIRROR"></span>**mirror**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-183">Un mapping del volume o del disco che gestisce due o più copie di dati identiche.</span><span class="sxs-lookup"><span data-stu-id="93a13-183">A volume or disk mapping that maintains two or more identical data copies.</span></span> <span data-ttu-id="93a13-184">Il tipo di mapping è denominato anche RAID Level 1.</span><span class="sxs-lookup"><span data-stu-id="93a13-184">The type of mapping is also called RAID Level 1.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**Pack**</span><span class="sxs-lookup"><span data-stu-id="93a13-185"><span id="base.pack"></span><span id="BASE.PACK"></span>**pack**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-186">Raccolta di volumi logici e dischi sottostanti.</span><span class="sxs-lookup"><span data-stu-id="93a13-186">A collection of logical volumes and underlying disks.</span></span> <span data-ttu-id="93a13-187">Un pacchetto è l'unità di chiusura transitiva per un volume.</span><span class="sxs-lookup"><span data-stu-id="93a13-187">A pack is the unit of transitive closure for a volume.</span></span> <span data-ttu-id="93a13-188">I pacchetti dischi dinamici e i gruppi di dischi sono termini per lo stesso elemento.</span><span class="sxs-lookup"><span data-stu-id="93a13-188">Dynamic disk packs and disk groups are terms for the same item.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**stripe di parità**</span><span class="sxs-lookup"><span data-stu-id="93a13-189"><span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**parity stripe**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-190">Un mapping del volume o del disco che mantiene le informazioni sul controllo di parità e i dati.</span><span class="sxs-lookup"><span data-stu-id="93a13-190">A volume or disk mapping that maintains parity check information as well as data.</span></span> <span data-ttu-id="93a13-191">Ogni fornitore fornisce l'esatto mapping e lo schema di protezione.</span><span class="sxs-lookup"><span data-stu-id="93a13-191">Each vendor supplies the exact mapping and protection scheme.</span></span> <span data-ttu-id="93a13-192">Include RAID 3, 4, 5 e 6.</span><span class="sxs-lookup"><span data-stu-id="93a13-192">Includes RAID 3, 4, 5, and 6.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configurazione parzialmente diretta**</span><span class="sxs-lookup"><span data-stu-id="93a13-193"><span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**partially directed configuration**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-194">Configurazione del volume o del disco non completamente esplicita.</span><span class="sxs-lookup"><span data-stu-id="93a13-194">A volume or disk configuration that is not fully explicit.</span></span> <span data-ttu-id="93a13-195">Il tipo di binding e una raccolta di risorse di destinazione sono specificati. il layout effettivo non è.</span><span class="sxs-lookup"><span data-stu-id="93a13-195">The binding type and a collection of target resources are specified; the actual layout is not.</span></span> <span data-ttu-id="93a13-196">La configurazione parzialmente diretta è la configurazione del volume più comune.</span><span class="sxs-lookup"><span data-stu-id="93a13-196">Partially directed configuration is the most common volume configuration.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partizione**</span><span class="sxs-lookup"><span data-stu-id="93a13-197"><span id="base.partition"></span><span id="BASE.PARTITION"></span>**partition**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-198">Intervallo contiguo di settori logici descritti da una singola voce nella struttura MBR o GPT.</span><span class="sxs-lookup"><span data-stu-id="93a13-198">A contiguous range of logical sectors described by a single entry in the MBR or GPT structure.</span></span> <span data-ttu-id="93a13-199">Nei dischi di base, le partizioni corrispondono direttamente ai volumi semplici.</span><span class="sxs-lookup"><span data-stu-id="93a13-199">On basic disks, partitions directly correspond to simple volumes.</span></span> <span data-ttu-id="93a13-200">Le strutture di partizione vengono condivise tra il firmware della piattaforma BIOS o EFI e un sistema operativo o un'altra immagine di avvio.</span><span class="sxs-lookup"><span data-stu-id="93a13-200">Partition structures are shared between the BIOS or EFI platform firmware and an operating system or other bootable image.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-201"><span id="base.path"></span><span id="BASE.PATH"></span>**percorso**</span><span class="sxs-lookup"><span data-stu-id="93a13-201"><span id="base.path"></span><span id="BASE.PATH"></span>**path**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-202">Il percorso di accesso da un computer a un disco o a un LUN hardware esterno.</span><span class="sxs-lookup"><span data-stu-id="93a13-202">The access path from a computer to a disk or external hardware LUN.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plessi**</span><span class="sxs-lookup"><span data-stu-id="93a13-203"><span id="base.plex"></span><span id="BASE.PLEX"></span>**plex**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-204">Un membro di un volume o LUN con mirroring.</span><span class="sxs-lookup"><span data-stu-id="93a13-204">One member of a mirrored volume or LUN.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-205"><span id="base.port"></span><span id="BASE.PORT"></span>**porta**</span><span class="sxs-lookup"><span data-stu-id="93a13-205"><span id="base.port"></span><span id="BASE.PORT"></span>**port**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-206">Endpoint di un percorso su un disco.</span><span class="sxs-lookup"><span data-stu-id="93a13-206">The endpoint of a path at a disk.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**array di dischi indipendenti (RAID) ridondante**</span><span class="sxs-lookup"><span data-stu-id="93a13-207"><span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**redundant array of independent disks (RAID)**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-208">Raccolta di tecniche per la gestione di più dischi.</span><span class="sxs-lookup"><span data-stu-id="93a13-208">A collection of techniques for managing multiple disks.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servizio di runtime**</span><span class="sxs-lookup"><span data-stu-id="93a13-209"><span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**runtime service**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-210">Programma software che viene eseguito in base a una richiesta di I/O.</span><span class="sxs-lookup"><span data-stu-id="93a13-210">A software program that executes on an I/O-request basis.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco semplice**</span><span class="sxs-lookup"><span data-stu-id="93a13-211"><span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**simple disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-212">Un mandrino non connesso a un controller RAID hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-212">A spindle that is not connected to a hardware RAID controller.</span></span> <span data-ttu-id="93a13-213">Vedere anche solo un gruppo di dischi (JBOD).</span><span class="sxs-lookup"><span data-stu-id="93a13-213">See also Just a Bunch Of Disks (JBOD).</span></span>

</dd> <dt>

<span data-ttu-id="93a13-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provider software**</span><span class="sxs-lookup"><span data-stu-id="93a13-214"><span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-215">Software basato su host che espone volumi logici e opera sui dischi.</span><span class="sxs-lookup"><span data-stu-id="93a13-215">Host-based software that exposes logical volumes and operates on disks.</span></span> <span data-ttu-id="93a13-216">Un provider software include servizi di runtime in modalità kernel, dati di configurazione e servizi di gestione in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="93a13-216">A software provider includes kernel-mode runtime services, configuration data, and user-mode management services.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**intervallo**</span><span class="sxs-lookup"><span data-stu-id="93a13-217"><span id="base.span"></span><span id="BASE.SPAN"></span>**span**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-218">Mapping lineare del volume o del disco di più extent del disco o dell'unità discontinui.</span><span class="sxs-lookup"><span data-stu-id="93a13-218">A volume or disk linear mapping of multiple discontinuous disk or drive extents.</span></span> <span data-ttu-id="93a13-219">Gli extent possono trovarsi in uno o più assi o lun.</span><span class="sxs-lookup"><span data-stu-id="93a13-219">The extents can be on one or more spindles or LUNs.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Spindle**</span><span class="sxs-lookup"><span data-stu-id="93a13-220"><span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**spindle**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-221">Unità fisica di archiviazione su disco.</span><span class="sxs-lookup"><span data-stu-id="93a13-221">A physical unit of disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**sovrapposizione**</span><span class="sxs-lookup"><span data-stu-id="93a13-222"><span id="base.stacking"></span><span id="BASE.STACKING"></span>**stacking**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-223">Operazione di creazione di un volume o un LUN eseguendo più di un'operazione di mapping del blocco logico.</span><span class="sxs-lookup"><span data-stu-id="93a13-223">The act of constructing a volume or LUN by performing more than one logical block mapping operation.</span></span> <span data-ttu-id="93a13-224">Un esempio è un volume con striping con mirroring.</span><span class="sxs-lookup"><span data-stu-id="93a13-224">An example is a mirrored striped volume.</span></span> <span data-ttu-id="93a13-225">Lo stacking più comune si verifica quando il RAID software viene usato in lun costruiti da hardware RAID.</span><span class="sxs-lookup"><span data-stu-id="93a13-225">The most common stacking occurs when software RAID is used across LUNs constructed by hardware RAID.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**striscia**</span><span class="sxs-lookup"><span data-stu-id="93a13-226"><span id="base.stripe"></span><span id="BASE.STRIPE"></span>**stripe**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-227">Un mapping del volume o del disco che interfoliazione gli extent contigui tra più volumi, dischi o unità.</span><span class="sxs-lookup"><span data-stu-id="93a13-227">A volume or disk mapping that interleaves contiguous extents across multiple volumes, disks, or drives.</span></span> <span data-ttu-id="93a13-228">Questo mapping è denominato anche RAID 0.</span><span class="sxs-lookup"><span data-stu-id="93a13-228">This mapping is also called RAID 0.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**stato**</span><span class="sxs-lookup"><span data-stu-id="93a13-229"><span id="base.status"></span><span id="BASE.STATUS"></span>**status**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-230">Disponibilità corrente di un volume, di un disco o di un'unità.</span><span class="sxs-lookup"><span data-stu-id="93a13-230">The current availability of a volume, disk, or drive.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**sottosistema**</span><span class="sxs-lookup"><span data-stu-id="93a13-231"><span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**subsystem**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-232">Creazione di un'istanza del software del provider hardware.</span><span class="sxs-lookup"><span data-stu-id="93a13-232">The instantiation of hardware-provider software.</span></span> <span data-ttu-id="93a13-233">Un sottosistema contiene almeno un controller e un'unità.</span><span class="sxs-lookup"><span data-stu-id="93a13-233">A subsystem contains at least one controller and one drive.</span></span> <span data-ttu-id="93a13-234">Se il sottosistema è esterno al computer, uno o più percorsi di rete connettono il sottosistema al computer.</span><span class="sxs-lookup"><span data-stu-id="93a13-234">If the subsystem is external to the computer, one or more network paths connect the subsystem to the computer.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**stato transizione**</span><span class="sxs-lookup"><span data-stu-id="93a13-235"><span id="base.jello"></span><span id="BASE.JELLO"></span>**transition state**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-236">Stato del mapping logico a fisico in corso di modifica.</span><span class="sxs-lookup"><span data-stu-id="93a13-236">Status of the logical to physical mapping that is undergoing change.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco non inizializzato**</span><span class="sxs-lookup"><span data-stu-id="93a13-237"><span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**uninitialized disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-238">Disco che non è un membro di un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="93a13-238">A disk that is not a member of a pack.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco senza maschera**</span><span class="sxs-lookup"><span data-stu-id="93a13-239"><span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**unmasked disk**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-240">Disco visibile al sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="93a13-240">A disk that is visible to the operating system.</span></span> <span data-ttu-id="93a13-241">Il contenuto di un disco non mascherato è visibile per i responsabili del volume software, i file System e così via.</span><span class="sxs-lookup"><span data-stu-id="93a13-241">The contents of an unmasked disk are visible to software volume managers, file systems, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="93a13-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span><span class="sxs-lookup"><span data-stu-id="93a13-242"><span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="93a13-243">Numero di extent del disco associati in un intervallo pressoché contiguo di blocchi logici.</span><span class="sxs-lookup"><span data-stu-id="93a13-243">A number of disk extents bound into a virtually contiguous range of logical blocks.</span></span> <span data-ttu-id="93a13-244">È possibile accedere a un volume tramite una lettera di unità, una cartella montata o un percorso GUID volume.</span><span class="sxs-lookup"><span data-stu-id="93a13-244">A volume can be accessed through a drive letter, a mounted folder, or a volume GUID path.</span></span>

</dd> </dl>

 

 
