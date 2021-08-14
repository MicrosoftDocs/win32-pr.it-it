---
description: Oggetto Volume Plex
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Oggetto Volume Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140cbf50e1939be7f62499aa90a299e07c157cd22b1a2e039e5e7bb2053b497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603029"
---
# <a name="volume-plex-object"></a>Oggetto Volume Plex

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto volume plex modella un volume plex contenuto in un volume. Solo un volume con mirroring può avere più plex. tutti gli altri tipi di volume hanno un plex. Ogni plex contiene una copia dei dati nel volume. VDS supporta quattro tipi di volumi plex: semplice, con spanning, con striping e con striping con parità. Per una descrizione di ognuno di questi tipi di volume, vedere [l'oggetto volume](volume-object.md).

Esistono due modi per creare un volume con più plex. È possibile usare il [**metodo IVdsPack::CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) per creare direttamente il volume con mirroring oppure usare il metodo [**IVdsVolume::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) per aggiungere un volume a un altro volume. I volumi (e i dischi sottostanti) devono essere nello stesso pacchetto. La figura seguente mostra un esempio di aggiunta di un volume (B) come plex a un altro volume (A) e del volume multiplexed risultante (A). I dati nel volume A rimangono intatti, mentre i dati nel volume B diventano una copia con mirroring dei dati nel volume A.

![Diagramma che mostra due singoli plex, uno con volume semplice A e uno con volume semplice B, uguale a più plex con volume con mirroring A.](images/vdsplex.png)

È possibile eseguire una query per i plex di volume richiamando il [**metodo IVdsVolume::QueryPlexes.**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) È possibile ottenere un puntatore a un plex del volume specifico selezionando l'oggetto plex desiderato dall'enumerazione restituita da **QueryPlexes.** Ad eccezione dell'ultimo plex, i plex esistenti possono essere interrotti o rimossi. Usare [**IVdsVolume::BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) per dividere un plex da un volume e convertire l'oggetto plex interrotto in un oggetto volume. Usare [**IVdsVolume::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) per eliminare completamente il plex. È possibile provare a ripristinare un plex a tolleranza di errore chiamando il metodo [**IVdsVolumePlex::Repair,**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) che sposta i membri non validi in dischi validi.

Oltre a un identificatore di oggetto e a un tipo plex, le proprietà dell'oggetto volume plex includono lo stato, l'integrità e lo stato di transizione del plex. Questo oggetto non ha flag.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Enumerazioni associate                           | [**VDS \_ VOLUME \_ PLEX \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**VDS \_ VOLUME \_ PLEX \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)E [**VDS DISK EXTENT \_ \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Strutture associate                             | [**VDS \_ VOLUME \_ PLEX \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider software](software-provider-objects.md)
</dt> <dt>

[Oggetto Volume](volume-object.md)
</dt> </dl>

 

 
