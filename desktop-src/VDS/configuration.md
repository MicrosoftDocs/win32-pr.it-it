---
description: Panoramica della configurazione
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Panoramica della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b742cb5ca2f287cd8b50b9f248d0ebec1174bfd71b59f0630bd9fb98864309c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007951"
---
# <a name="configuration-overview"></a>Panoramica della configurazione

\[A partire da Windows 8 e Windows Server 2012, [l'interfaccia](virtual-disk-service-portal.md) COM del servizio dischi virtuali viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Se non si ha familiarità con gli oggetti definiti da VDS, vedere il [modello a oggetti VDS](vds-object-model.md).

La complessità di configurazione di un disco virtuale può variare da molto semplice a ottimizzata. I dischi virtuali aziendali, senza cura e senza cura definiscono tre prospettive di configurazione tipiche. Ogni prospettiva presenta requisiti leggermente diversi:

-   I dischi virtuali senza cura sono leggermente configurati, ad esempio solo per automatizzare il partizionamento e la formattazione dei nuovi dischi o per creare temporaneamente un volume con mirroring per la migrazione dei dati da un disco a un altro senza tempi di inattività. Tali dischi sono buoni per i computer notebook e altri sistemi con uno o pochi dischi.
-   I dischi virtuali free-from-care offrono spazio di archiviazione che appare auto-configurato, auto-curativo e disponibile; usa volumi con striping e LUN per ottenere prestazioni migliori; usa volumi con mirroring e LUN per ottenere una maggiore disponibilità; e usa i pacchetti per rendere le modalità di errore pulite e contenute. Questo livello di configurazione è ideale quando si sostituiscono dischi di sistema vecchi, piccoli e lenti con dischi nuovi, di grandi dimensioni e veloci. È ideale anche per il mirroring dei dati con lo sparing a caldo automatizzato. Un singolo mandrino di riserva può proteggere molti spindle. Per informazioni dettagliate, vedere [Sparing a caldo.](hot-sparing.md)

    Le reti SAN su scala ridotta dipendono dalla flessibilità e dall'automazione offerte da questo livello di configurazione, così come le appliance NAS (Network Attached Archiviazione). I dischi virtuali free-from-care semplificano l'attività di consolidamento dell'archiviazione delle applicazioni, ad esempio l'archiviazione per SQL e Exchange, senza consolidare i server.

-   Enterprise dischi virtuali contengono configurazioni aziendali molto grandi o complesse con requisiti aggiuntivi specifici del sito o dell'applicazione. Gli amministratori ottimizzano il sottosistema di archiviazione per una singola applicazione che potrebbe essere eseguita solo raramente, ad esempio un processo di creazione di report batch mensile in un sistema di transazioni di gestione degli ordini. Enterprise i dischi virtuali devono essere ridimensionati, mostrare l'attività in tempo reale del sottosistema di archiviazione e soddisfare i requisiti degli amministratori hands-on.

Per altre informazioni su mirror, stripe e altre opzioni di configurazione in VDS, vedere [Associazione di volumi e LUN.](volume-and-lun-binding.md) Una tecnica di configurazione avanzata, denominata stacking, consente di combinare le configurazioni associate a volumi e LUN esistenti. Per informazioni dettagliate, vedere [Stacking della configurazione](configuration-stacking.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Sparing a caldo](hot-sparing.md)
</dt> <dt>

[Associazione di volumi e LUN](volume-and-lun-binding.md)
</dt> <dt>

[Stacking di configurazione](configuration-stacking.md)
</dt> </dl>

 

 
