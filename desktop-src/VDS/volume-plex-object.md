---
description: Oggetto volume Plex
ms.assetid: 9e770bfc-2bcb-45f0-a7fc-ba526349839e
title: Oggetto volume Plex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a858bc6ce98761bb687e8dca473b1b68879da8
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350891"
---
# <a name="volume-plex-object"></a>Oggetto volume Plex

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto volume Plex modella un volume Plex contenuto da un volume. Solo un volume con mirroring può avere più Plex; tutti gli altri tipi di volume hanno un plex. Ogni plex contiene una copia dei dati nel volume. VDS supporta quattro tipi di Plex del volume: semplice, con spanning, con striping e con striping con parità. Per una descrizione di ognuno di questi tipi di volumi, vedere l' [oggetto volume](volume-object.md).

Esistono due modi per creare un volume con più Plex. È possibile utilizzare il metodo [**IVdsPack:: CreateVolume**](/windows/desktop/api/Vds/nf-vds-ivdspack-createvolume) per creare direttamente il volume con mirroring oppure utilizzare il metodo [**IVdsVolume:: AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-addplex) per aggiungere un volume a un altro volume. I volumi e i dischi sottostanti devono trovarsi nello stesso pacchetto. Nella figura seguente viene illustrato un esempio di aggiunta di un volume (B) come plex a un altro volume (A) e il volume multiplex risultante (A). I dati nel volume A rimangono intatti, mentre i dati sul volume B diventano una copia con mirroring dei dati nel volume A.

![Diagramma che mostra due singoli Plex, uno con un volume semplice A e uno con un volume B semplice, uguale a più Plex con il volume speculare A.](images/vdsplex.png)

È possibile eseguire una query per i plex del volume richiamando il metodo [**IVdsVolume:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-queryplexes) . È possibile ottenere un puntatore a un plex del volume specifico selezionando l'oggetto Plex desiderato dall'enumerazione restituita da **QueryPlexes**. Fatta eccezione per l'ultimo plex, i plex esistenti possono essere interrotti o rimossi. Usare [**IVdsVolume:: BreakPlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-breakplex) per suddividere un plex da un volume e convertire l'oggetto Plex rotto in un oggetto volume. Usare [**IVdsVolume:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdsvolume-removeplex) per eliminare completamente il plex. È possibile tentare di ripristinare un plex a tolleranza di errore chiamando il metodo [**IVdsVolumePlex:: Repair**](/windows/desktop/api/Vds/nf-vds-ivdsvolumeplex-repair) , che sposta i membri non validi in dischi corretti.

Oltre a un identificatore di oggetto e un tipo di Plex, le proprietà dell'oggetto volume Plex includono lo stato, l'integrità e lo stato di transizione del Plex. Nessun flag per l'oggetto.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                              | Elemento                                                                                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto | [**IVdsVolumePlex**](/windows/desktop/api/Vds/nn-vds-ivdsvolumeplex).                                                                                                                                          |
| Enumerazioni associate                           | [**VDS \_ \_ \_ Stato del volume Plex**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_status), [**\_ tipo di \_ Plex \_ del volume VDS**](/windows/desktop/api/Vds/ne-vds-vds_volume_plex_type)e [**tipo di \_ \_ extent \_ del disco VDS**](/windows/desktop/api/Vds/ne-vds-vds_disk_extent_type). |
| Strutture associate                             | [**VDS \_ \_ \_ prop del volume Plex**](/windows/desktop/api/Vds/ns-vds-vds_volume_plex_prop).                                                                                                                           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider di software](software-provider-objects.md)
</dt> <dt>

[Oggetto volume](volume-object.md)
</dt> </dl>

 

 
