---
description: LUN (oggetto)
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: LUN (oggetto)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad74fa65802adb1439360fb2fcdb423c642ef736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318917"
---
# <a name="lun-object"></a>LUN (oggetto)

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un oggetto LUN (numero di unità logica) modella un'unità logica di spazio di archiviazione indirizzabile creato da un provider hardware ed esposto da un sottosistema. Ogni LUN comprende almeno un PLEX LUN, che a sua volta è costituito da extent di una o più unità.

## <a name="lun-types"></a>Tipi LUN

VDS supporta cinque tipi di LUN: semplice, con spanning, con striping, con mirroring e con striping con parità. I LUN semplici, con spanning e con striping non sono a tolleranza di errore; i LUN con mirroring e parità sono a tolleranza di errore. Nella parte restante di questa sezione vengono descritti i tipi LUN VDS.

-   Un LUN semplice è un LUN a tolleranza di errore costituito da un singolo extent dell'unità contigua da una singola unità. L'extent contiguo può includere un singolo intervallo di blocchi o più intervalli di blocchi collegati tra loro.
-   Un LUN con spanning è un LUN a tolleranza di errore costituito da più extent non contigui provenienti da più unità. I dati vengono scritti in modo lineare in ogni extent della prima unità fino a quando non vengono riempiti tutti gli extent della prima unità, quindi a ogni extent della seconda unità e così via. I LUN con spanning consentono un uso efficiente dello spazio su disco nei sottosistemi che comprendono unità di varie dimensioni.
-   Un LUN con striping è un LUN a tolleranza di errore costituito da diversi extent contigui, Interleaved e contigui da più unità. I LUN con striping usano una configurazione RAID-0, in modo che i dati vengano "con striping" ciclicamente tra gli extent delle unità contribuendo. I LUN con striping funzionano meglio con le unità con le stesse dimensioni, modello e produttore.
-   I LUN con mirroring sono lun a tolleranza di errore che consentono il ripristino di emergenza duplicando i dati in più PLEX LUN. Ogni plex in un LUN con mirroring contiene una copia dei dati archiviati nel Plex originale. Ogni Plex si trova in un'unità separata. Tutti i dati scritti in un LUN con mirroring vengono scritti simultaneamente in ognuno dei relativi Plex. Se una delle unità contribuendo ha esito negativo, il plex su tale unità non sarà più disponibile, ma il sistema continuerà a funzionare usando il plex o i plex non interessati. Un LUN con mirroring può avere un numero qualsiasi di Plex.
-   I LUN con striping con parità sono lun a tolleranza di errore che consentono il ripristino di emergenza tramite lo striping di dati di parità intermittenti in tre o più unità. Se una delle unità contribuendo ha esito negativo, i dati persi possono essere ricreati dai dati e dalla parità rimanenti.

## <a name="lun-creation"></a>Creazione LUN

VDS supporta quattro modelli in base ai quali le applicazioni possono creare LUN: dirette esplicitamente, dirette, automagic e specifiche del fornitore. Tutti i provider di hardware devono supportare la creazione di LUN in modo esplicito e diretto e sono vivamente invitati a supportare la creazione di un LUN con Magic Magic. La creazione di LUN specifici del fornitore esula dall'ambito di questa guida.

La creazione di LUN diretta in modo esplicito consente al chiamante di specificare tutti gli attributi del LUN. La creazione di LUN parzialmente diretta consente al chiamante di specificare solo gli attributi che sono di particolare interesse e quindi consente al provider di scegliere il resto. La creazione di un LUN automatico prevede che il chiamante specifichi semplicemente il tipo e le dimensioni LUN insieme a un set di "suggerimenti automatici" (preferenze predefinite per gli attributi LUN) e quindi consente al provider di creare automaticamente il LUN.

## <a name="lun-masking"></a>Mascheramento di LUN

VDS supporta il mascheramento LUN per i sottosistemi che offrono questa funzionalità. Tutti i LUN vengono esposti al computer in cui è in esecuzione il provider. L'unmascheramento LUN consente a un chiamante di "annullare il mascheramento" dei LUN selezionati in altri computer della rete. Se si annulla il mascheramento di un LUN in un computer, il computer può accedere al LUN. I computer per i quali non è nascosto un LUN.

Un LUN senza maschera espone entrambe le interfacce [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) all'host locale. È possibile usare **IVdsDisk** per aggiungere un LUN a un pacchetto di provider di software, creare e rimuovere volumi, assegnare lettere di unità e così via. Per ulteriori informazioni sulle operazioni eseguite su un disco, vedere l' [oggetto disco](disk-object.md).

Dopo aver annullato il mascheramento di un LUN in un computer di destinazione o mascherato da un computer di destinazione, è possibile che la visibilità del LUN su tale computer non venga modificata fino a quando non viene eseguita una ripetizione dell'analisi del bus. L'applicazione VDS nel computer di destinazione avvia la ripetizione dell'analisi del bus chiamando [**IVdsService:: Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). L'avvio della ripetizione dell'analisi del bus è responsabilità dell'applicazione VDS, non del provider hardware.

## <a name="lun-multipathing"></a>Percorsi multipli LUN

I provider hardware che supportano la funzionalità Multipath I/O (MPIO) possono impostare i criteri di bilanciamento del carico nei percorsi tra un LUN e l'host locale. I LUN che supportano questa funzionalità espongono l'interfaccia [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) all'host locale.

## <a name="working-with-luns"></a>Uso dei lun

Usare il metodo [**IVdsSubSystem:: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) per creare un nuovo oggetto lun. È possibile eseguire una query sui LUN esposti da un sottosistema specifico richiamando il metodo [**QueryLuns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) , esposto anche da [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem). Un chiamante può ottenere un puntatore a un LUN specifico selezionando l'oggetto LUN desiderato dall'enumerazione restituita da **QueryLuns**. Con un oggetto LUN è possibile impostare lo stato LUN; eseguire una query per tutti i controller attivi, i plex e i suggerimenti per la magia automatica; estendere e compattare il LUN; aggiungere e rimuovere Plex; imposta maschere; applica hint; ed eliminare il LUN.

Oltre a un identificatore di oggetto, un nome e un numero di serie, le proprietà dell'oggetto LUN includono il tipo di LUN, le dimensioni, lo stato, l'integrità, lo stato di transizione e i flag. elenco di cui è stato annullato il mascheramento; e un'impostazione della priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                              | Elemento                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Interfacce sempre esposte da questo oggetto in VDS 1,1 e 2,0 Fibre Channel solo provider | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfacce sempre esposte da questo oggetto nei soli provider iSCSI VDS 1,1 e 2,0         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfacce che possono essere esposte da questo oggetto\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)e [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**windows Server 2008, Windows Vista e Windows Server 2003:** l'interfaccia [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) non è supportata.<br/> |
| Enumerazioni associate                                                                           | [**VDS \_ \_Flag lun**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) e [**\_ \_ stato lun VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)e [**\_ \_ tipo lun VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Strutture associate                                                                             | [**VDS \_ \_Informazioni lun**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information), [**porta \_ VDS \_ lun**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)e [**\_ \_ notifica lun VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Vedere [oggetto disco](disk-object.md) per l'interfaccia aggiuntiva ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) che viene esposta se il lun viene annullato come disco nel computer host locale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[Oggetto Pack](pack-object.md)
</dt> <dt>

[Oggetto disk](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Aggiunta di una lettera di unità a un LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

