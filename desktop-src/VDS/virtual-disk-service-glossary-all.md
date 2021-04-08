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
# <a name="virtual-disk-service-glossary"></a>Glossario servizio dischi virtuali

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Questa sezione fornisce un glossario dei termini tecnici usati nella documentazione relativa al servizio dischi virtuali (VDS).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configurazione di automagic**
</dt> <dd>

Provider RAID hardware che fornisce un set di regole per la scelta del mapping dei blocchi logici LUN in base a attributi semplici. I provider di automagic possono anche modificare dinamicamente il mapping per la gestione delle prestazioni o degli errori.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**Suggerimenti per la magia automatica**
</dt> <dd>

Informazioni fornite a un provider di automagic per guidare la configurazione dei blocchi logici LUN. Gli hint includono informazioni sulla tolleranza di errore desiderata, sull'atomicità fisica e sul modello di accesso I/O previsto.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco di base**
</dt> <dd>

Disco gestito dal provider software più semplice possibile. Il provider di dischi di base supporta solo i volumi che vengono mappati direttamente alle strutture di dati di configurazione della partizione.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**associazione**
</dt> <dd>

Selezione di un set di mapping a risorse fisiche.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**convertire**
</dt> <dd>

Processo di conversione di un disco di base in un disco dinamico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**configurazione**
</dt> <dd>

Raccolta dei parametri operativi che forniscono il mapping da un volume, o LUN, alle risorse fisiche.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**controller**
</dt> <dd>

Programma software che contiene l'intelligence di runtime per un provider hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**disco**
</dt> <dd>

Un disco fisico o un LUN RAID hardware. I dischi sono destinazioni per il carico di I/O di archiviazione di runtime; Plug and Play (PNP) non distingue tra JBOD e lun.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disco rigido**
</dt> <dd>

Subset di un pacchetto usato per esportare o importare volumi da un pacchetto.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**pacchetto di dischi**
</dt> <dd>

Vedere *Pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**unità**
</dt> <dd>

Un mandrino del disco fisico all'interno di un sottosistema RAID hardware. Le unità sono associate a lun dal sottosistema.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinamico**
</dt> <dd>

Disco gestito da un provider RAID software con supporto per la riconfigurazione flessibile dei volumi. Un disco dinamico utilizza una partizione come contenitore per i volumi. Nessun mapping garantito.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configurazione esplicita**
</dt> <dd>

Una configurazione con i parametri, inclusi il tipo di volume e il layout esatto, per una raccolta di volumi di destinazione.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**esportazione**
</dt> <dd>

Operazione di trasferimento di un disco e di tutti i volumi contenuti su tale disco da un pacchetto.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**extent**
</dt> <dd>

Intervallo contiguo di settori logici che contribuiscono a un singolo volume o disco. Un extent può anche essere un intervallo di settori non allocati. In genere, un file system Visualizza i dettagli dell'extent per un utente finale.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabella di partizione GUID (GPT)**
</dt> <dd>

Strutture usate dal firmware EFI. GPT è uno dei due formati di dati di configurazione software di livello più basso usati dal firmware della piattaforma per individuare un sistema operativo di avvio o un'altra immagine eseguibile.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provider hardware**
</dt> <dd>

Una raccolta di software eseguita nell'host, una scheda bus ed eventualmente un sottosistema di archiviazione esterno che interagisce con la superficie e la gestione dei lun RAID. I provider hardware per la maggior parte dei sottosistemi di archiviazione esterni contengono solo software basato su host e modalità utente.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**salute**
</dt> <dd>

Stato corrente di gestione degli errori di un volume o di un LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**Hot Spare**
</dt> <dd>

Aggiunta temporanea di un volume Plex a un volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**importare**
</dt> <dd>

Operazione di trasferimento di un disco rigido e di tutti i relativi volumi in un pacchetto esistente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un gruppo di dischi (JBOD)**
</dt> <dd>

Raccolta di assi fisici senza il controllo coordinato fornito da un dispositivo RAID hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**numero blocco logico (LBN)**
</dt> <dd>

Unità più piccola indirizzabile di dati di archiviazione. LBN viene usato con I protocolli di comando di I/O.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapping del blocco logico**
</dt> <dd>

Trasformazione dei blocchi logici presentati a un provider a quelli esposti dal provider.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**numero di unità logica (LUN)**
</dt> <dd>

Unità di archiviazione fisicamente indirizzabile come superficie di un sottosistema RAID hardware. Questo termine può anche fare riferimento all'identificatore SCSI per l'unità di archiviazione.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Numero LUN**
</dt> <dd>

Numero assegnato da un provider hardware VDS a un LUN in una matrice. Non corrisponde al "numero di unità logica" nell'indirizzo SCSI del disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servizio di gestione**
</dt> <dd>

Un programma software che viene eseguito in base alle esigenze per eseguire la configurazione, il monitoraggio o la gestione degli errori del volume.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**mapping**
</dt> <dd>

Volume esposto al sistema operativo e con un nome di volume associato (lettera di unità). Un volume è accessibile da un file system.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**mascheramento**
</dt> <dd>

Disco non riconosciuto dal sistema operativo. Un disco può essere mascherato dal sottosistema RAID hardware, dall'opzione, dalla riserva SCSI da un altro host del computer o dal software nello stack del disco.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**il partizionamento del record di avvio principale (MBR)**
</dt> <dd>

MBR è uno dei due formati di dati di configurazione software di livello più basso e viene usato dal firmware BIOS per individuare un'immagine del sistema operativo avviabile.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**membro**
</dt> <dd>

Raccolta di extent concatenati del disco contenuti in uno o più dischi. Un disco può contribuire solo a un membro di un volume.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**specchio**
</dt> <dd>

Un mapping del volume o del disco che gestisce due o più copie di dati identiche. Il tipo di mapping è denominato anche RAID Level 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**Pack**
</dt> <dd>

Raccolta di volumi logici e dischi sottostanti. Un pacchetto è l'unità di chiusura transitiva per un volume. I pacchetti dischi dinamici e i gruppi di dischi sono termini per lo stesso elemento.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**stripe di parità**
</dt> <dd>

Un mapping del volume o del disco che mantiene le informazioni sul controllo di parità e i dati. Ogni fornitore fornisce l'esatto mapping e lo schema di protezione. Include RAID 3, 4, 5 e 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configurazione parzialmente diretta**
</dt> <dd>

Configurazione del volume o del disco non completamente esplicita. Il tipo di binding e una raccolta di risorse di destinazione sono specificati. il layout effettivo non è. La configurazione parzialmente diretta è la configurazione del volume più comune.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**partizione**
</dt> <dd>

Intervallo contiguo di settori logici descritti da una singola voce nella struttura MBR o GPT. Nei dischi di base, le partizioni corrispondono direttamente ai volumi semplici. Le strutture di partizione vengono condivise tra il firmware della piattaforma BIOS o EFI e un sistema operativo o un'altra immagine di avvio.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**percorso**
</dt> <dd>

Il percorso di accesso da un computer a un disco o a un LUN hardware esterno.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**plessi**
</dt> <dd>

Un membro di un volume o LUN con mirroring.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**porta**
</dt> <dd>

Endpoint di un percorso su un disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**array di dischi indipendenti (RAID) ridondante**
</dt> <dd>

Raccolta di tecniche per la gestione di più dischi.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servizio di runtime**
</dt> <dd>

Programma software che viene eseguito in base a una richiesta di I/O.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco semplice**
</dt> <dd>

Un mandrino non connesso a un controller RAID hardware. Vedere anche solo un gruppo di dischi (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provider software**
</dt> <dd>

Software basato su host che espone volumi logici e opera sui dischi. Un provider software include servizi di runtime in modalità kernel, dati di configurazione e servizi di gestione in modalità utente.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**intervallo**
</dt> <dd>

Mapping lineare del volume o del disco di più extent del disco o dell'unità discontinui. Gli extent possono trovarsi in uno o più assi o lun.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Spindle**
</dt> <dd>

Unità fisica di archiviazione su disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**sovrapposizione**
</dt> <dd>

Operazione di creazione di un volume o un LUN eseguendo più di un'operazione di mapping del blocco logico. Un esempio è un volume con striping con mirroring. Lo stacking più comune si verifica quando il RAID software viene usato in lun costruiti da hardware RAID.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**striscia**
</dt> <dd>

Un mapping del volume o del disco che interfoliazione gli extent contigui tra più volumi, dischi o unità. Questo mapping è denominato anche RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**stato**
</dt> <dd>

Disponibilità corrente di un volume, di un disco o di un'unità.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**sottosistema**
</dt> <dd>

Creazione di un'istanza del software del provider hardware. Un sottosistema contiene almeno un controller e un'unità. Se il sottosistema è esterno al computer, uno o più percorsi di rete connettono il sottosistema al computer.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**stato transizione**
</dt> <dd>

Stato del mapping logico a fisico in corso di modifica.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco non inizializzato**
</dt> <dd>

Disco che non è un membro di un pacchetto.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco senza maschera**
</dt> <dd>

Disco visibile al sistema operativo. Il contenuto di un disco non mascherato è visibile per i responsabili del volume software, i file System e così via.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**volume**
</dt> <dd>

Numero di extent del disco associati in un intervallo pressoché contiguo di blocchi logici. È possibile accedere a un volume tramite una lettera di unità, una cartella montata o un percorso GUID volume.

</dd> </dl>

 

 
