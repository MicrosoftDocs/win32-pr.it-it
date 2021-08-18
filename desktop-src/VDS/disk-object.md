---
description: Oggetto Disco
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Oggetto Disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5979e6e2e25ee6ded15b987ddbcda0c5c135f92452174853577d7781475c5d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137239"
---
# <a name="disk-object"></a>Oggetto Disco

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto disco modella un disco fisico basato su host. Il provider software in esecuzione nell'host locale può accedere a un LUN come disco quando l'oggetto LUN non viene mascherato nell'host locale. Per altre informazioni sul mascheramento LUN, vedere [l'oggetto LUN](lun-object.md).

Ogni oggetto disco contribuisce esattamente a un oggetto pack. Tuttavia, un disco può contribuire a un numero qualsiasi di volumi all'interno di un pacchetto. È possibile designare un disco come riserva a caldo.

## <a name="partition-to-volume-mapping"></a>Mapping tra partizioni e volumi

Il sistema operativo include il supporto per dischi di base e dinamici. VDS fornisce un provider di base e un provider dinamico per gestire questi tipi di disco. I dischi di base non sono mai a tolleranza di errore. I dischi dinamici possono essere a tolleranza di errore se il sistema operativo consente tale associazione di volumi. I dischi di base e dinamici possono contenere partizioni strutturate in base a uno degli stili di partizione seguenti: MBR (Master Boot Record) o GPT (GUID Partition Table). Il partizionamento MBR include fino a quattro partizioni primarie o tre partizioni primarie più una partizione estesa con unità logiche infinite. Il partizionamento GPT offre fino a 128 partizioni primarie.

La descrizione seguente è di natura generale. Mostra la tipica relazione tra partizioni e volumi, a cui si verificano diverse eccezioni. Per una descrizione dettagliata del mapping tra partizioni e volumi, vedere [**l'interfaccia IVdsAdvancedDisk.**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) Il mapping da partizione a volume varia a seconda del tipo di disco, di base o dinamico.

-   Dischi di base

    Una partizione su un disco di base viene mappata direttamente a un volume, nella maggior parte dei casi, e può essere definita come partizione MBR o GPT. Nella figura seguente viene illustrato il mapping per entrambe le versioni delle partizioni MBR. Nel primo caso, le partizioni (da P1 a P4) vengono mappate direttamente ai volumi (da V1 a V4). Una partizione estesa (Ext) sostituisce P4 nel secondo stile MBR. Il numero di unità logiche all'interno della partizione estesa mappate ai volumi è illimitato.

    ![Mostra due opzioni di mapping per le partizioni M B R.](images/vdsbasicmapping.png)

    Le partizioni GPT (da P1 a P128) nella figura successiva vengono mappate direttamente ai volumi (da V1 a V128), se sono in uso tutte le partizioni disponibili. Un disco GPT non usa una partizione estesa per migliorare l'usabilità.

    ![Mostra una partizione GPT.](images/vdsbasicmappinggpt.png)

-   Dischi dinamici

    Un tipo di partizione speciale in un disco dinamico esegue il mapping a un numero elevato di volumi. Per un limite stimato imposto dal provider dinamico, vedere [l'oggetto pack](pack-object.md). Come illustrato nella figura seguente, all'interno di P1 può essere presente un numero qualsiasi di extent mappati ai volumi.

    ![Mostra un tipo di partizione speciale in un disco dinamico.](images/vdsdynamicmapping.png)

Indipendentemente dal tipo di disco, un disco può contenere uno o più extent del disco. Un extent del disco è un intervallo contiguo di blocchi logici esposti dal disco. Ad esempio, un extent del disco può rappresentare un intero volume, una parte di un volume con spanning, un membro di un volume con striping o un plex di un volume con mirroring.

### <a name="working-with-disks"></a>Uso dei dischi

Usare il [**metodo IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere un disco a un pacchetto esistente. I chiamanti possono ottenere un puntatore a un disco specifico selezionando l'oggetto disco desiderato dall'enumerazione restituita dal [**metodo IVdsPack::QueryDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) Analogamente, è possibile richiamare il [**metodo IVdsDisk::GetPack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) per determinare quale pacchetto contiene un determinato disco.

È possibile spostare un disco da un pacchetto a un altro chiamando il [**metodo IVdsPack::MigrateDisks.**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) VDS non supporta la migrazione di un disco di base tra i pacchetti controllati dal provider di base. È anche possibile spostare un pacchetto in un altro host spostando fisicamente tutti i dischi del pacchetto nel nuovo host. Il pacchetto si sposta con i dischi e viene visualizzato come pacchetto estraneo nel nuovo host. Per istruzioni, vedere [Adding Foreign Disks to a Pack](adding-foreign-disks-to-a-pack.md).

Oltre a un identificatore di oggetto, un nome, un indirizzo, un tipo di dispositivo e un tipo di supporto, le proprietà dell'oggetto disco includono lo stato del disco, l'integrità e i flag; dimensioni in byte, byte per settore, settori per traccia e tracce per cilindro; e il bus e il tipo di partizione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)e [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** [**L'interfaccia IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non è supportata.<br/> **Windows Vista:** [**L'interfaccia IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) non è supportata fino Windows Vista con Service Pack 1 (SP1); usare [**invece IVdsDisk2.**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) [**L'interfaccia IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non è supportata.<br/> **Windows Server 2003:** Le interfacce [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)e [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non sono supportate.<br/> |
| Interfacce che possono essere esposte da questo oggetto     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). Vedere [Oggetto LUN per](lun-object.md) altre interfacce esposte se il disco è un LUN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumerazioni associate                           | [**VDS \_ FLAG \_ DEL DISCO,**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) [**STATO DEL \_ DISCO \_ VDS,**](/windows/desktop/api/Vds/ne-vds-vds_disk_status) [**\_ \_ FLAG DI PARTIZIONE VDS,**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag) [**STILE DI \_ PARTIZIONE \_ VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)E [**TIPO DI EXTENT DEL DISCO VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Strutture associate                             | [**VDS \_ DISK \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), [**VDS DISK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**VDS \_ INPUT \_ DISK**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), VDS PARTITION PROP , VDS PARTITION [**\_ \_ INFO**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop) [**\_ \_ \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**VDS \_ PARTITION INFO \_ \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr)E [**VDS DISK \_ \_ EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider software](software-provider-objects.md)
</dt> <dt>

[Oggetto Pack](pack-object.md)
</dt> <dt>

[Oggetto LUN](lun-object.md)
</dt> <dt>

[Aggiunta di dischi estere a un pacchetto](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

