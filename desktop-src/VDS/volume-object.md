---
description: Oggetto volume
ms.assetid: 92013015-b0f5-4b92-937b-c2637f65810c
title: Oggetto volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e47092a237e7b0e9441b08c410d95d0836dbdb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319842"
---
# <a name="volume-object"></a>Oggetto volume

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto volume modella un'unità di archiviazione logica creata da un provider software e presentata al file system come disco. Ogni volume è costituito da almeno un volume Plex, che a sua volta è costituito da extent da uno o più dischi.

## <a name="volume-types"></a>Tipi di volume

VDS supporta cinque tipi di volumi: semplice, con spanning, con striping, con mirroring e con striping con parità. I volumi semplici, con spanning e con striping non sono a tolleranza di errore; i volumi con mirroring e parità sono a tolleranza di errore. Nella parte restante di questa sezione vengono descritti i tipi di volume VDS.

-   Un volume semplice è una parte di un disco fisico che funziona come se fosse un'unità fisicamente separata. Un volume semplice può essere costituito da una singola area su un disco o da più aree dello stesso disco collegate tra loro.
-   Un volume con spanning combina aree di spazio non allocato da più dischi in un unico volume logico, consentendo di utilizzare in modo più efficiente tutto lo spazio e tutte le lettere di unità in un sistema a più dischi.
-   Un volume con striping viene creato combinando aree di spazio libero su due o più dischi in un unico volume logico. I volumi con striping usano RAID-0, che esegue lo striping dei dati su più dischi. I volumi con striping non possono essere estesi o speculari e non offrono tolleranza di errore. Se uno dei dischi contenenti un volume con striping ha esito negativo, l'intero volume ha esito negativo. Quando si creano volumi con striping, è preferibile usare dischi di dimensioni, modelli e produttori uguali.
-   Un volume con mirroring è un volume a tolleranza di errore che fornisce la ridondanza dei dati utilizzando due copie, o Plex, del volume per duplicare i dati archiviati nel volume. Tutti i dati scritti nel volume con mirroring vengono scritti in entrambi i plex, che si trovano in dischi fisici distinti. Se si verifica un errore in uno dei dischi fisici, i dati nel disco danneggiato diventano non disponibili, ma il sistema continua a funzionare utilizzando il disco non interessato.
-   Un volume con striping con parità è un volume a tolleranza di errore con dati e parità con striping intermittente in tre o più dischi fisici. Se una parte di un disco fisico ha esito negativo, è possibile ricreare i dati che si trovavano sulla parte non riuscita dai dati e dalla parità rimanenti. Questo tipo di volume, detto anche volume RAID-5, è una soluzione ottimale per la ridondanza dei dati in un ambiente computer in cui la maggior parte delle attività è costituita dalla lettura dei dati.

### <a name="volume-creation"></a>Creazione di volumi

I provider di software di base e dinamici supportano la creazione di volumi parzialmente diretta; un chiamante specifica solo gli attributi che sono di particolare interesse e consente al provider di scegliere il resto. VDS monta automaticamente un volume appena creato, eccetto le piattaforme Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition.

### <a name="working-with-volumes"></a>Utilizzo dei volumi

Creare sempre un volume all'interno dello stesso pacchetto dei dischi che la contribuiscono. Usare il metodo [**IVdsPack:: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) per creare un nuovo oggetto volume. È possibile determinare i volumi contenuti in un pacchetto specifico richiamando il metodo [**QueryVolumes**](/windows/desktop/api/Vds/nf-vds-ivdspack-queryvolumes) , esposto anche da [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack). Un chiamante può ottenere un puntatore a un volume specifico selezionando l'oggetto volume desiderato dall'enumerazione restituita da **QueryVolumes**. Con un oggetto volume è possibile impostare lo stato. eseguire una query per i plex; estendere e compattare il volume; aggiungere, interrompere e rimuovere Plex; ed eliminare il volume.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto volume includono il tipo di volume, le dimensioni, lo stato, l'integrità, lo stato di transizione, i flag e un tipo di file system consigliato.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                                                               |
|---------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsVolume**](/windows/desktop/api/Vds/nn-vds-ivdsvolume), [**IVdsVolumeMF**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf), [**IVdsVolumeMF2**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf2) \* , [**IVdsVolumeOnline**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeonline) \* e [**IVdsVolumeShrink**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeshrink) \* . |
| Enumerazioni associate                           | [**VDS \_ \_Flag del volume**](/windows/desktop/api/Vds/ne-vds-vds_volume_flag), [**\_ \_ stato del volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status), [**\_ \_ tipo di volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_type)e [**\_ \_ \_ tipo di extent del disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type).            |
| Strutture associate                             | [**VDS \_ Volume \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop) e [**la \_ \_ notifica del volume VDS**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification).                                                                                                        |



 

**\* Windows Server 2003:** queste interfacce non sono supportate fino a Windows Vista.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di software](software-provider-objects.md)
</dt> </dl>

 

 
