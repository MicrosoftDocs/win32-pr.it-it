---
description: In questa sezione viene fornito un glossario dei termini tecnici usati nella documentazione di Virtual Disk Service (VDS).
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 1cf28cfb-ce96-4659-955d-0088bddcb9ce
title: Glossario del servizio Dischi virtuali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7e73e9de8f6c30b69f2e39e78fae36e5c3ea547cccfed2f25f9a15327e3f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602994"
---
# <a name="virtual-disk-service-glossary"></a>Glossario del servizio Dischi virtuali

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

In questa sezione viene fornito un glossario dei termini tecnici usati nella documentazione di Virtual Disk Service (VDS).

<dl> <dt>

<span id="base.automagic_configuration"></span><span id="BASE.AUTOMAGIC_CONFIGURATION"></span>**configurazione automagic**
</dt> <dd>

Provider RAID hardware che fornisce un set di regole per la scelta della modifica del mapping dei blocchi logici LUN in base a attributi semplici. I provider automagic possono anche modificare dinamicamente il mapping per la gestione delle prestazioni o degli errori.

</dd> <dt>

<span id="base.binding_hints"></span><span id="BASE.BINDING_HINTS"></span>**suggerimenti automagic**
</dt> <dd>

Informazioni fornite a un provider automagic per guidare la configurazione del blocco logico LUN. I suggerimenti includono informazioni sulla tolleranza di errore desiderata, sull'atomicità fisica e sul modello di accesso I/O previsto.

</dd> <dt>

<span id="base.basic_disk"></span><span id="BASE.BASIC_DISK"></span>**disco di base**
</dt> <dd>

Un disco gestito dal provider di software più semplice possibile. Il provider di dischi di base supporta solo i volumi di cui viene direttamente mappato il mapping alle strutture dei dati di configurazione della partizione.

</dd> <dt>

<span id="base.binding"></span><span id="BASE.BINDING"></span>**Associazione**
</dt> <dd>

Selezione per un set di mapping alle risorse fisiche.

</dd> <dt>

<span id="base.convert"></span><span id="BASE.CONVERT"></span>**Convertire**
</dt> <dd>

Processo di conversione di un disco di base in un disco dinamico.

</dd> <dt>

<span id="base.configuration"></span><span id="BASE.CONFIGURATION"></span>**Configurazione**
</dt> <dd>

Raccolta dei parametri operativi che forniscono il mapping da un volume, o LUN, alle risorse fisiche.

</dd> <dt>

<span id="base.controller"></span><span id="BASE.CONTROLLER"></span>**Controller**
</dt> <dd>

Programma software che contiene l'intelligence di runtime per un provider di hardware.

</dd> <dt>

<span id="base.disk"></span><span id="BASE.DISK"></span>**Disco**
</dt> <dd>

Disco fisico o LUN RAID hardware. I dischi sono destinazioni per il carico di I/O di archiviazione di runtime. Plug and Play (PNP) non distingue tra JBOD e LUN.

</dd> <dt>

<span id="base.disk_platter"></span><span id="BASE.DISK_PLATTER"></span>**disco piatto**
</dt> <dd>

Subset di un pacchetto utilizzato per l'esportazione o l'importazione di volumi da un pacchetto.

</dd> <dt>

<span id="base.disk_pack"></span><span id="BASE.DISK_PACK"></span>**pacchetto di dischi**
</dt> <dd>

Vedere *pack*.

</dd> <dt>

<span id="base.drive"></span><span id="BASE.DRIVE"></span>**Guida**
</dt> <dd>

Un mandrino del disco fisico all'interno di un sottosistema RAID hardware. Le unità vengono associate ai LUN dal sottosistema.

</dd> <dt>

<span id="base.dynamic_disk"></span><span id="BASE.DYNAMIC_DISK"></span>**disco dinamico**
</dt> <dd>

Disco gestito da un provider RAID software con supporto per la riconfigurazione flessibile dei volumi. Un disco dinamico usa una partizione come contenitore per i volumi. non esiste alcun mapping garantito.

</dd> <dt>

<span id="base.explicit_configuration"></span><span id="BASE.EXPLICIT_CONFIGURATION"></span>**configurazione esplicita**
</dt> <dd>

Configurazione con i parametri, inclusi il tipo di volume e il layout esatto, per una raccolta di volumi di destinazione.

</dd> <dt>

<span id="base.export"></span><span id="BASE.EXPORT"></span>**Esportazione**
</dt> <dd>

L'atto di spostare un disco e tutti i volumi contenuti in tale piatto da un pacchetto.

</dd> <dt>

<span id="base.extent"></span><span id="BASE.EXTENT"></span>**Misura**
</dt> <dd>

Intervallo contiguo di settori logici che contribuiscono a un singolo volume o disco. Un extent può anche essere un intervallo di settori non allocati. In genere, un file system visualizza i dettagli dell'extent per un utente finale.

</dd> <dt>

<span id="base.guid_partition_table_gpt"></span><span id="BASE.GUID_PARTITION_TABLE_GPT"></span>**Tabella di partizione GUID (GPT)**
</dt> <dd>

Strutture usate dal firmware EFI. GPT è uno dei due formati di dati di configurazione software di livello più basso usati dal firmware della piattaforma per individuare un sistema operativo avviabile o un'altra immagine eseguibile.

</dd> <dt>

<span id="base.hardware_provider"></span><span id="BASE.HARDWARE_PROVIDER"></span>**provider di hardware**
</dt> <dd>

Raccolta di software che viene eseguito nell'host, in un adattatore bus ed eventualmente in un sottosistema di archiviazione esterno che funziona insieme per la superficie e la gestione dei LUN RAID. I provider di hardware per la maggior parte dei sottosistemi di archiviazione esterni contengono solo software basato su host in modalità utente.

</dd> <dt>

<span id="base.health"></span><span id="BASE.HEALTH"></span>**Salute**
</dt> <dd>

Stato corrente di gestione degli errori di un volume o di un LUN.

</dd> <dt>

<span id="base.hot_spotting"></span><span id="BASE.HOT_SPOTTING"></span>**sparing a caldo**
</dt> <dd>

Aggiunta temporanea di un volume plex a un volume.

</dd> <dt>

<span id="base.import"></span><span id="BASE.IMPORT"></span>**Importazione**
</dt> <dd>

L'atto di spostare un disco e tutti i relativi volumi in un pacchetto esistente.

</dd> <dt>

<span id="base.JBOD"></span><span id="base.jbod"></span><span id="BASE.JBOD"></span>**solo un gruppo di dischi (JBOD)**
</dt> <dd>

Raccolta di spindle fisici senza il controllo coordinato fornito da un dispositivo RAID hardware.

</dd> <dt>

<span id="base.logical_block_number_LBN"></span><span id="base.logical_block_number_lbn"></span><span id="BASE.LOGICAL_BLOCK_NUMBER_LBN"></span>**Numero di blocco logico (LBN)**
</dt> <dd>

La più piccola unità indirizzabile di dati di archiviazione. LBN viene usato con i protocolli di comando di I/O.

</dd> <dt>

<span id="base.logical_block_mapping"></span><span id="BASE.LOGICAL_BLOCK_MAPPING"></span>**mapping di blocchi logici**
</dt> <dd>

Trasformazione dei blocchi logici presentati a un provider rispetto a quelli esposti dal provider.

</dd> <dt>

<span id="base.logical_Unit_Number_LUN"></span><span id="base.logical_unit_number_lun"></span><span id="BASE.LOGICAL_UNIT_NUMBER_LUN"></span>**numero di unità logica (LUN)**
</dt> <dd>

Unità di archiviazione fisicamente indirizzabile, come indicato da un sottosistema RAID hardware. Questo termine può anche fare riferimento all'identificatore SCSI per l'unità di archiviazione.

</dd> <dt>

<span id="base.LUN_number"></span><span id="base.lun_number"></span><span id="BASE.LUN_NUMBER"></span>**Numero LUN**
</dt> <dd>

Numero assegnato da un provider hardware VDS a un LUN in una matrice. Non corrisponde al "numero di unità logica" nell'indirizzo SCSI del disco.

</dd> <dt>

<span id="base.management_service"></span><span id="BASE.MANAGEMENT_SERVICE"></span>**servizio di gestione**
</dt> <dd>

Programma software che viene eseguito in base alle esigenze per eseguire la configurazione, il monitoraggio o la gestione degli errori del volume.

</dd> <dt>

<span id="base.mapping"></span><span id="BASE.MAPPING"></span>**Mapping**
</dt> <dd>

Volume esposto al sistema operativo a cui è associato un nome di volume (una lettera di unità). Un volume è accessibile da un file system.

</dd> <dt>

<span id="base.masking"></span><span id="BASE.MASKING"></span>**Mascheramento**
</dt> <dd>

Disco non riconosciuto dal sistema operativo. Un disco può essere mascherato dal sottosistema RAID hardware, dal commutatore, da SCSI RESERVE da un altro host del computer o dal software nello stack di dischi.

</dd> <dt>

<span id="base.master_Boot_Record_partitioning_MBR"></span><span id="base.master_boot_record_partitioning_mbr"></span><span id="BASE.MASTER_BOOT_RECORD_PARTITIONING_MBR"></span>**partizionamento dei record di avvio master (MBR)**
</dt> <dd>

MBR è uno dei due formati di dati di configurazione software di livello più basso e viene usato dal firmware del BIOS per individuare un'immagine del sistema operativo di avvio.

</dd> <dt>

<span id="base.member"></span><span id="BASE.MEMBER"></span>**Membro**
</dt> <dd>

Raccolta di extent del disco concatenati contenuti in uno o più dischi. Un disco può contribuire a un solo membro di un volume.

</dd> <dt>

<span id="base.mirror"></span><span id="BASE.MIRROR"></span>**Specchio**
</dt> <dd>

Mapping di volumi o dischi che gestisce due o più copie di dati identiche. Il tipo di mapping è denominato anche RAID Level 1.

</dd> <dt>

<span id="base.pack"></span><span id="BASE.PACK"></span>**branco**
</dt> <dd>

Raccolta di volumi logici e dischi sottostanti. Un pacchetto è l'unità di chiusura transitiva per un volume. I pacchetti di dischi dinamici e i gruppi di dischi sono termini per lo stesso elemento.

</dd> <dt>

<span id="base.parity_stripe"></span><span id="BASE.PARITY_STRIPE"></span>**stripe di parità**
</dt> <dd>

Mapping di volumi o dischi che mantiene le informazioni sul controllo di parità e i dati. Ogni fornitore fornisce lo schema di mapping e protezione esatto. Include RAID 3, 4, 5 e 6.

</dd> <dt>

<span id="base.partially_directed_configuration"></span><span id="BASE.PARTIALLY_DIRECTED_CONFIGURATION"></span>**configurazione parzialmente diretta**
</dt> <dd>

Configurazione del volume o del disco non completamente esplicita. Vengono specificati il tipo di associazione e una raccolta di risorse di destinazione. il layout effettivo non lo è. La configurazione parzialmente diretta è la configurazione del volume più comune.

</dd> <dt>

<span id="base.partition"></span><span id="BASE.PARTITION"></span>**Partizione**
</dt> <dd>

Intervallo contiguo di settori logici descritti da una singola voce nella struttura MBR o GPT. Nei dischi di base le partizioni corrispondono direttamente a volumi semplici. Le strutture di partizione vengono condivise tra il firmware della piattaforma BIOS o EFI e un sistema operativo o un'altra immagine di avvio.

</dd> <dt>

<span id="base.path"></span><span id="BASE.PATH"></span>**Percorso**
</dt> <dd>

Percorso di accesso da un computer a un disco o a un LUN hardware esterno.

</dd> <dt>

<span id="base.plex"></span><span id="BASE.PLEX"></span>**Plex**
</dt> <dd>

Un membro di un volume con mirroring o lun.

</dd> <dt>

<span id="base.port"></span><span id="BASE.PORT"></span>**Porta**
</dt> <dd>

Endpoint di un percorso in un disco.

</dd> <dt>

<span id="base.redundant_array_of_independent_disks_RAID"></span><span id="base.redundant_array_of_independent_disks_raid"></span><span id="BASE.REDUNDANT_ARRAY_OF_INDEPENDENT_DISKS_RAID"></span>**array ridondante di dischi indipendenti (RAID)**
</dt> <dd>

Raccolta di tecniche per la gestione di più dischi.

</dd> <dt>

<span id="base.runtime_service"></span><span id="BASE.RUNTIME_SERVICE"></span>**servizio di runtime**
</dt> <dd>

Programma software eseguito in base a una richiesta di I/O.

</dd> <dt>

<span id="base.simple_disk"></span><span id="BASE.SIMPLE_DISK"></span>**disco semplice**
</dt> <dd>

Spindle non connesso a un controller RAID hardware. Vedere anche Just a Bunch Of Disks (JBOD).

</dd> <dt>

<span id="base.software_provider"></span><span id="BASE.SOFTWARE_PROVIDER"></span>**provider di software**
</dt> <dd>

Software basato su host che espone volumi logici e opera su dischi. Un provider software include servizi di runtime in modalità kernel, dati di configurazione e servizi di gestione in modalità utente.

</dd> <dt>

<span id="base.span"></span><span id="BASE.SPAN"></span>**Rotazione**
</dt> <dd>

Mapping lineare del volume o del disco di più extent di unità o dischi discontinui. Gli extent possono essere su uno o più spindle o LUN.

</dd> <dt>

<span id="base.spindle"></span><span id="BASE.SPINDLE"></span>**Mandrino**
</dt> <dd>

Unità fisica di archiviazione su disco.

</dd> <dt>

<span id="base.stacking"></span><span id="BASE.STACKING"></span>**Impilamento**
</dt> <dd>

L'azione di costruire un volume o un LUN eseguendo più di un'operazione di mapping dei blocchi logici. Un esempio è un volume con striping con mirroring. Lo stacking più comune si verifica quando il RAID software viene usato tra LUN costruiti da RAID hardware.

</dd> <dt>

<span id="base.stripe"></span><span id="BASE.STRIPE"></span>**Striscia**
</dt> <dd>

Mapping di volumi o dischi che interfolia extent contigui tra più volumi, dischi o unità. Questo mapping è detto anche RAID 0.

</dd> <dt>

<span id="base.status"></span><span id="BASE.STATUS"></span>**Stato**
</dt> <dd>

Disponibilità corrente di un volume, un disco o un'unità.

</dd> <dt>

<span id="base.subsystem"></span><span id="BASE.SUBSYSTEM"></span>**Sottosistema**
</dt> <dd>

Creazione di un'istanza del software del provider hardware. Un sottosistema contiene almeno un controller e un'unità. Se il sottosistema è esterno al computer, uno o più percorsi di rete connettono il sottosistema al computer.

</dd> <dt>

<span id="base.jello"></span><span id="BASE.JELLO"></span>**stato di transizione**
</dt> <dd>

Stato del mapping logico a fisico in fase di modifica.

</dd> <dt>

<span id="base.uninitialized_disk"></span><span id="BASE.UNINITIALIZED_DISK"></span>**disco non inizializzato**
</dt> <dd>

Disco che non è membro di un pacchetto.

</dd> <dt>

<span id="base.unmasked_disk"></span><span id="BASE.UNMASKED_DISK"></span>**disco senza maschera**
</dt> <dd>

Un disco visibile al sistema operativo. Il contenuto di un disco senza maschera è visibile ai gestori di volumi software, ai file system e così via.

</dd> <dt>

<span id="base.volume"></span><span id="BASE.VOLUME"></span>**Volume**
</dt> <dd>

Numero di extent del disco associati a un intervallo di blocchi logici praticamente contigui. È possibile accedere a un volume tramite una lettera di unità, una cartella montata o un percorso GUID del volume.

</dd> </dl>

 

 
