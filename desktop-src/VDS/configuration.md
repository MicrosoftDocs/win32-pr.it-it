---
description: Panoramica della configurazione
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Panoramica della configurazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966612"
---
# <a name="configuration-overview"></a>Panoramica della configurazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Se non si ha familiarità con gli oggetti definiti da VDS, vedere il [modello a oggetti VDS](vds-object-model.md).

La complessità della configurazione di un disco virtuale può variare da molto semplice a ottimizzata. I dischi virtuali dell'organizzazione e della cura gratuita definiscono tre prospettive di configurazione tipiche. Ogni prospettiva presenta requisiti leggermente diversi:

-   I dischi virtuali senza assistenza sono configurati in modo leggero, forse solo per automatizzare il partizionamento e la formattazione dei nuovi dischi o per creare temporaneamente un volume con mirroring per la migrazione dei dati da un disco a un altro senza tempi di inattività. Tali dischi sono utili per i computer notebook e altri sistemi con uno o pochi dischi.
-   I dischi virtuali free-from-Care forniscono archiviazione con configurazione automatica, correzione automatica e disponibilità. USA i volumi con striping e i LUN per ottenere prestazioni migliori. USA volumi e lun con mirroring per ottenere una migliore disponibilità; e usa i pacchetti per rendere le modalità di errore pulita e contenuta. Questo livello di configurazione è ideale quando si sostituiscono dischi di sistema vecchi, piccoli e lenti con nuovi dischi veloci e di grandi dimensioni. È ideale anche per il mirroring dei dati con la disattivazione a caldo automatica: un singolo mandrino di riserva può proteggere molti assi. Per informazioni dettagliate, vedere [Hot Spare](hot-sparing.md).

    I San con scalabilità ridotta dipendono dalla flessibilità e dall'automazione offerti da questo livello di configurazione, così come gli appliance di archiviazione collegata alla rete (NAS). I dischi virtuali free-from-care semplificano l'attività di consolidamento dell'archiviazione dell'applicazione, ad esempio l'archiviazione per SQL e Exchange, senza consolidare i server.

-   I dischi virtuali aziendali contengono configurazioni aziendali molto grandi o complesse con requisiti aggiuntivi specifici del sito o dell'applicazione. Gli amministratori ottimizzano il sottosistema di archiviazione per una singola applicazione che può essere eseguita solo raramente, ad esempio un processo di creazione di report batch mensile in un sistema di transazione per l'esecuzione di ordini. È necessario che i dischi virtuali aziendali siano ridimensionati, mostrino l'attività in tempo reale del sottosistema di archiviazione e soddisfino i requisiti degli amministratori pratici.

Per altre informazioni sui mirror, sulle strisce e sulle altre opzioni di configurazione in VDS, vedere [binding di volumi e lun](volume-and-lun-binding.md). Una tecnica di configurazione avanzata, denominata stacking, consente di combinare le configurazioni associate a volumi e lun esistenti. Per informazioni dettagliate, vedere [stack di configurazione](configuration-stacking.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizio dischi virtuali](virtual-disk-service-portal.md)
</dt> <dt>

[Modello a oggetti VDS](vds-object-model.md)
</dt> <dt>

[Hot Spare](hot-sparing.md)
</dt> <dt>

[Binding di volumi e LUN](volume-and-lun-binding.md)
</dt> <dt>

[Stack di configurazione](configuration-stacking.md)
</dt> </dl>

 

 
