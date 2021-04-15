---
description: Oggetto disk
ms.assetid: 65e14273-8127-4667-b5c8-362ad54b4782
title: Oggetto disk
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d629f642d83c9e2c6954a4f09fe09091a2bbce9
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104570209"
---
# <a name="disk-object"></a>Oggetto disk

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto disco modella un disco fisico basato su host. Il provider di software in esecuzione nell'host locale può accedere a un LUN come disco quando viene annullato il mascheramento dell'oggetto LUN nell'host locale. Per ulteriori informazioni sulla maschera LUN, vedere l' [oggetto lun](lun-object.md).

Ogni oggetto disco contribuisce esattamente a un oggetto Pack; Tuttavia, un disco può contribuire a un numero qualsiasi di volumi all'interno di un pacchetto. È possibile designare un disco come riserva a caldo.

## <a name="partition-to-volume-mapping"></a>Mapping da partizione a volume

Il sistema operativo include il supporto per dischi di base e dinamici. VDS fornisce un provider di base e un provider dinamico per gestire questi tipi di dischi. I dischi di base non sono mai a tolleranza di errore. I dischi dinamici possono essere a tolleranza di errore se il sistema operativo consente tale associazione di volumi. I dischi di base e dinamici possono contenere partizioni strutturate in base a uno degli stili di partizione seguenti: MBR (master boot record) o GPT (GUID Partition Table). Il partizionamento MBR è costituito da un massimo di quattro partizioni primarie o tre partizioni primarie più una partizione estesa con unità logiche infinite. Il partizionamento GPT fornisce fino a 128 partizioni primarie.

La descrizione che segue è generale per natura. Mostra la relazione tipica tra le partizioni e i volumi, a cui sono associate diverse eccezioni. Per una descrizione dettagliata del mapping da partizione a volume, vedere l'interfaccia [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk) . Il mapping da partizione a volume varia a seconda del tipo di disco, di base o dinamico.

-   Dischi di base

    Una partizione su un disco di base viene mappata direttamente a un volume, nella maggior parte dei casi, e può essere impostata come una partizione MBR o GPT. Nella figura seguente viene illustrato il mapping per entrambe le versioni delle partizioni MBR. Nel primo caso, le partizioni (da P1 a P4) vengono mappate direttamente ai volumi (dalla V1 alla V4). Una partizione estesa (EXT) sostituisce P4 nel secondo stile MBR. Il numero di unità logiche all'interno della partizione estesa con mapping ai volumi è illimitato.

    ![Mostra due opzioni di mapping per le partizioni M B R.](images/vdsbasicmapping.png)

    Le partizioni GPT (da P1 a p128) nell'illustrazione successiva vengono mappate direttamente ai volumi (da V1 a v128), se sono in uso tutte le partizioni disponibili. Un disco GPT non utilizza una partizione estesa come modo per migliorare l'usabilità.

    ![Mostra una partizione GPT.](images/vdsbasicmappinggpt.png)

-   Dischi dinamici

    Un tipo di partizione speciale su un disco dinamico viene mappato a un numero elevato di volumi. Per un limite stimato imposto dal provider dinamico, vedere l' [oggetto Pack](pack-object.md). Come illustrato nella figura seguente, può essere presente un numero qualsiasi di extent all'interno di P1 con mapping ai volumi.

    ![Mostra un tipo di partizione speciale in un disco dinamico.](images/vdsdynamicmapping.png)

Indipendentemente dal tipo di disco, un disco può contenere uno o più extent del disco. Un extent del disco è un intervallo contiguo di blocchi logici esposti dal disco. Un extent del disco, ad esempio, può rappresentare un intero volume, una parte di un volume con spanning, un membro di un volume con striping o un plex di un volume con mirroring.

### <a name="working-with-disks"></a>Uso dei dischi

Usare il metodo [**IVdsPack:: AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) per aggiungere un disco a un pacchetto esistente. I chiamanti possono ottenere un puntatore a un disco specifico selezionando l'oggetto disco desiderato dall'enumerazione restituita dal metodo [**IVdsPack:: QueryDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-querydisks) . Analogamente, è possibile richiamare il metodo [**IVdsDisk:: getpack**](/windows/desktop/api/Vds/nf-vds-ivdsdisk-getpack) per determinare quale pacchetto contiene un disco specificato.

È possibile spostare un disco da un pacchetto a un altro chiamando il metodo [**IVdsPack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) . VDS non supporta la migrazione di un disco di base tra i pacchetti controllati dal provider di base. È anche possibile spostare un pacchetto in un altro host spostando fisicamente tutti i dischi del pacchetto nel nuovo host. Il pacchetto viene spostato con i dischi e viene visualizzato come un pacchetto esterno nel nuovo host. Per istruzioni, vedere [aggiunta di dischi esterni a un pacchetto](adding-foreign-disks-to-a-pack.md).

Oltre a un identificatore di oggetto, un nome, un indirizzo, un tipo di dispositivo e un tipo di supporto, le proprietà dell'oggetto disco includono lo stato, l'integrità e i flag del disco; dimensioni in byte, byte per settore, settori per traccia e tracce per cilindro; e il bus e il tipo di partizione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsAdvancedDisk**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk), [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf), [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)e [**IVdsCreatePartitionEx**](/windows/desktop/api/Vds/nn-vds-ivdscreatepartitionex). **Windows Server 2008:** L'interfaccia [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non è supportata.<br/> **Windows Vista:** L'interfaccia [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline) non è supportata fino a Windows Vista con Service Pack 1 (SP1); in alternativa, usare [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2) . L'interfaccia [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non è supportata.<br/> **Windows Server 2003:** Le interfacce [**IVdsAdvancedDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsadvanceddisk2), [**IVdsDisk2**](/windows/desktop/api/Vds/nn-vds-ivdsdisk2), [**IVdsDiskOnline**](/windows/desktop/api/Vds/nn-vds-ivdsdiskonline), [**IVdsDiskPartitionMF**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf)e [**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2) non sono supportate.<br/> |
| Interfacce che possono essere esposte da questo oggetto     | [**IVdsRemovable**](/windows/desktop/api/Vds/nn-vds-ivdsremovable). (Vedere l' [oggetto lun](lun-object.md) per le interfacce aggiuntive esposte se il disco è un LUN).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Enumerazioni associate                           | [**VDS \_ \_Flag del disco**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag), [**\_ \_ stato del disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_status), [**\_ \_ flag di partizione VDS**](/windows/desktop/api/Vds/ne-vds-vds_partition_flag), [**\_ \_ stile della partizione VDS**](/windows/win32/api/vds/ne-vds-__vds_partition_style)e [**\_ \_ \_ tipo di extent del disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Strutture associate                             | [**VDS \_ DISK \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop), [**VDS \_ disk \_ Notification**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification), [**VDS \_ input \_ disk**](/windows/desktop/api/Vds/ns-vds-vds_input_disk), [**VDS \_ partition \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_partition_prop), [**VDS \_ partition \_ info \_ GPT**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_gpt), [**VDS \_ partition \_ info \_ MBR**](/windows/desktop/api/Vds/ns-vds-vds_partition_info_mbr), and [**VDS \_ disk \_ extent**](/windows/desktop/api/Vds/ns-vds-vds_disk_extent).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di software](software-provider-objects.md)
</dt> <dt>

[Oggetto Pack](pack-object.md)
</dt> <dt>

[LUN (oggetto)](lun-object.md)
</dt> <dt>

[Aggiunta di dischi esterni a un pacchetto](adding-foreign-disks-to-a-pack.md)
</dt> </dl>

 

