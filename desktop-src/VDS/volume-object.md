---
description: Oggetto Volume
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Oggetto Volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87887dae233a47ef168546bb4d0bab93389ab72e0e0617b64ea0c80fbfab0e83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125391"
---
# <a name="volume-object"></a>Oggetto Volume

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto volume modella un'unità di archiviazione logica creata da un provider di software e presentata al file system come disco. Ogni volume è costituito da almeno un volume plex, che a sua volta è costituito da extent da uno o più dischi.

## <a name="volume-types"></a>Tipi di volume

VDS supporta cinque tipi di volume: semplice, con spanning, con striping, con mirroring e con striping con parità. I volumi semplici, con spanning e con striping non sono a tolleranza di errore. I volumi con mirroring e parità sono a tolleranza di errore. La parte restante di questa sezione descrive ognuno dei tipi di volume VDS.

-   Un volume semplice è una parte di un disco fisico che funziona come se fosse un'unità fisicamente separata. Un volume semplice può essere costituito da una singola area in un disco o da più aree dello stesso disco collegate tra loro.
-   Un volume con spanning combina aree di spazio non allocato da più dischi in un unico volume logico, consentendo di usare in modo più efficiente tutto lo spazio e tutte le lettere di unità in un sistema con più dischi.
-   Un volume con striping viene creato combinando aree di spazio libero su due o più dischi in un unico volume logico. I volumi con striping usano RAID-0, che consente di eseguire lo striping dei dati su più dischi. I volumi con striping non possono essere estesi o con mirroring e non offrono tolleranza di errore. Se uno dei dischi contenenti un volume con striping ha esito negativo, l'intero volume ha esito negativo. Quando si creano volumi con striping, è meglio usare dischi della stessa dimensione, modello e produttore.
-   Un volume con mirroring è un volume a tolleranza di errore che fornisce la ridondanza dei dati usando due copie, o plex, del volume per duplicare i dati archiviati nel volume. Tutti i dati scritti nel volume con mirroring vengono scritti in entrambi i plex, che si trovano in dischi fisici separati. Se si verifica un errore in uno dei dischi fisici, i dati sul disco non riuscito diventano non disponibili, ma il sistema continua a funzionare usando il disco non interessato.
-   Un volume con striping con parità è un volume a tolleranza di errore con dati e parità con striping intermittente tra tre o più dischi fisici. Se si verifica un errore in una parte di un disco fisico, è possibile ricreare i dati nella parte non riuscita dai dati rimanenti e dalla parità. Questo tipo di volume (detto anche volume RAID-5) è una buona soluzione per la ridondanza dei dati in un ambiente computer in cui la maggior parte delle attività consiste nella lettura dei dati.

### <a name="volume-creation"></a>Creazione del volume

I provider di software di base e dinamici supportano la creazione di volumi indirizzati parzialmente; un chiamante specifica solo gli attributi di particolare interesse e consente al provider di scegliere il resto. VDS monta automaticamente un volume appena creato, ad eccezione delle piattaforme Windows Server 2003, edizione Enterprise e Windows Server 2003, Datacenter Edition.

### <a name="working-with-volumes"></a>Uso dei volumi

Creare sempre un volume all'interno dello stesso pacchetto dei dischi che contribuiscono a esso. Usare il [**metodo IVdsPack::CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) per creare un nuovo oggetto volume. È possibile determinare i volumi contenuti in un pacchetto specifico richiamando il [**metodo QueryVolumes,**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) esposto anche da [**IVdsPack.**](/windows/desktop/api/Vds/nn-vds-ivdspack) Un chiamante può ottenere un puntatore a un volume specifico selezionando l'oggetto volume desiderato dall'enumerazione restituita da **QueryVolumes**. Con un oggetto volume è possibile impostare lo stato. query per i plex; estendere e ridurre il volume; aggiungere, interrompere e rimuovere i plex; ed eliminare il volume.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto volume includono il tipo di volume, le dimensioni, lo stato, l'integrità, lo stato di transizione, i flag e un tipo di file system consigliato.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsVolume,**](/windows/desktop/api/Vds/nn-vds-ivdsvolume) [**IVdsVolumeMF,**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf) [**IVdsVolumeMF2,**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* e [**IVdsVolumeShrink.**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* |
| Enumerazioni associate                           | [**VDS \_ FLAG \_ DI VOLUME,**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag) [**STATO \_ VOLUME \_ VDS,**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) [**TIPO DI \_ VOLUME \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)e TIPO DI [**EXTENT DISCO VDS \_ \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Strutture associate                             | [**VDS \_ VOLUME \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) e [**VDS VOLUME \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification).                                                                                                        |



 

**\* Windows Server 2003:** queste interfacce non sono supportate fino Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider software](software-provider-objects.md)
</dt> </dl>

 

 
