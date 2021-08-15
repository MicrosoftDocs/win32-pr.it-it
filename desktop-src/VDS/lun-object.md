---
description: Oggetto LUN
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: Oggetto LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d315e33b8d253e346b42b01f86a85379aadace73e517a169cc653214a9c674d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347492"
---
# <a name="lun-object"></a>Oggetto LUN

\[A partire Windows 8 e Windows Server 2012, l'interfaccia [COM](virtual-disk-service-portal.md) del servizio disco virtuale viene sostituita dal Windows Archiviazione API Gestione [.](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Un oggetto LUN (numero di unità logica) modella un'unità logica di spazio di archiviazione indirizzabile che viene creata da un provider di hardware ed esata da un sottosistema. Ogni LUN è costituito da almeno un plex LUN, che a sua volta è composto da extent da una o più unità.

## <a name="lun-types"></a>Tipi LUN

VDS supporta cinque tipi di LUN: semplice, con spanning, con striped, con mirroring e striped con parità. I LUN semplici, con spanning e con striped non sono a tolleranza di errore. I LUN con mirroring e parità sono a tolleranza di errore. La parte restante di questa sezione descrive ognuno dei tipi di LUN VDS.

-   Un LUN semplice è un LUN a tolleranza di errore costituito da un singolo extent di unità contigua da una singola unità. L'extent contiguo può essere costituito da un singolo intervallo di blocchi o da più intervalli di blocchi collegati tra loro.
-   Un LUN con spanning è un LUN a tolleranza di errore costituito da più extent non contigui da più unità. I dati vengono scritti in modo lineare in ognuno degli extent nella prima unità fino a quando non vengono riempiti tutti i primi extent dell'unità, quindi in ognuno degli extent nella seconda unità e così via. I LUN con spanning consentono un uso efficiente dello spazio su disco nei sottosistemi costituiti da unità di varie dimensioni.
-   Un LUN con striped è un LUN a tolleranza di errore costituito da più extent contigui interleaved provenienti da più unità. I LUN con striped usano una configurazione RAID-0, in modo che i dati vengono "stripati" ciclicamente tra gli extent nelle unità che contribuiscono. I LUN con striped funzionano meglio con unità della stessa dimensione, modello e produttore.
-   I LUN con mirroring sono LUN a tolleranza di errore che consentono il ripristino di emergenza duplicando i dati in più plex LUN. Ogni plex in un LUN con mirroring contiene una copia dei dati archiviati nel plex originale. Ognuno dei plex si trova in un'unità separata. Tutti i dati scritti in un LUN con mirroring vengono scritti contemporaneamente in ognuno dei relativi plex. In caso di errore di una delle unità che contribuiscono, il plex su tale unità diventa non disponibile, ma il sistema continua a funzionare usando il plex o i plex non interessati. Un LUN con mirroring può avere un numero qualsiasi di plex.
-   I LUN con striping con parità sono LUN a tolleranza di errore che consentono il ripristino di emergenza tramite striping intermittente dei dati di parità tra tre o più unità. In caso di errore di una delle unità che contribuiscono, i dati persi possono essere ricreati dai dati rimanenti e dalla parità.

## <a name="lun-creation"></a>Creazione lun

VDS supporta quattro modelli in base ai quali le applicazioni possono creare LUN: diretto in modo esplicito, parzialmente diretto, automagico e specifico del fornitore. Tutti i provider di hardware devono supportare la creazione di LUN in modo esplicito e parzialmente diretto e sono vivamente invitati a supportare la creazione di LUN automagic. La creazione di LUN specifici del fornitore non rientra nell'ambito di questa guida.

La creazione di LUN indirizzata in modo esplicito consente al chiamante di specificare tutti gli attributi del LUN. La creazione lun parzialmente diretta consente al chiamante di specificare solo gli attributi di particolare interesse e quindi consente al provider di scegliere il resto. La creazione automatica del LUN comporta l'abilitazione del chiamante per specificare semplicemente il tipo e le dimensioni del LUN insieme a un set di "hint automagic" (preferenze predefinite per gli attributi LUN) e quindi consentire al provider di creare automaticamente il LUN.

## <a name="lun-masking"></a>Mascheramento di LUN

VDS supporta l'annullamento del mascheramento LUN per i sottosistemi che offrono questa funzionalità. Tutti i LUN vengono eseguiti nel computer in cui è in esecuzione il provider. L'annullamento del mascheramento LUN consente a un chiamante di "annullare il mascheramento" dei LUN selezionati in altri computer della rete. Se si annulla il mascheramento di un LUN in un computer, il computer ha accesso al LUN. I computer per cui è mascherata una LUN non lo fanno.

Un LUN senza maschera espone entrambe le [**interfacce IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) all'host locale. È possibile usare **IVdsDisk** per aggiungere un LUN a un pacchetto di provider software, creare e rimuovere volumi, assegnare lettere di unità e così via. Per altre informazioni sulle operazioni eseguite su un disco, vedere [l'oggetto disco](disk-object.md).

Dopo che un LUN è stato rimosso dal mascheramento in un computer di destinazione o mascherato da un computer di destinazione, la visibilità del LUN su tale computer potrebbe non cambiare fino a quando non viene eseguita una nuova analisi del bus. L'applicazione VDS nel computer di destinazione avvia la nuova analisi del bus chiamando [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). L'avvio della nuova analisi del bus è responsabilità dell'applicazione VDS, non del provider di hardware.

## <a name="lun-multipathing"></a>Percorsi lun

I provider hardware che supportano MPIO (Multipath I/O) possono impostare criteri di bilanciamento del carico nei percorsi tra un LUN e l'host locale. I LUN che supportano questa funzionalità espongono [**l'interfaccia IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) all'host locale.

## <a name="working-with-luns"></a>Uso dei LUN

Usare il [**metodo IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) per creare un nuovo oggetto LUN. È possibile eseguire una query dei LUN esposti da un sottosistema specifico richiamando il [**metodo QueryLuns,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) esposto anche da [**IVdsSubSystem.**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) Un chiamante può ottenere un puntatore a un LUN specifico selezionando l'oggetto LUN desiderato dall'enumerazione restituita da **QueryLuns**. Con un oggetto LUN, è possibile impostare lo stato lun; eseguire una query per tutti i controller attivi, iplex e gli hint automagic; estendere e ridurre il LUN; aggiungere e rimuovere plex; impostare le maschere; applicare hint; ed eliminare il LUN.

Oltre a un identificatore di oggetto, a un nome e a un numero di serie, le proprietà dell'oggetto LUN includono il tipo LUN, le dimensioni, lo stato, l'integrità, lo stato di transizione e i flag; un elenco di annullamento del mascheramento; e un'impostazione di priorità di ricompilazione.

Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.



| Tipo                                                                                              | Elemento                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfacce sempre esposte da questo oggetto                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Le interfacce sempre esposte da questo oggetto in VDS 1.1 e 2.0 Fibre Channel provider | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfacce sempre esposte da questo oggetto solo nei provider iSCSI VDS 1.1 e 2.0         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfacce che possono essere esposte da questo oggetto\*                                                   | [**IVdsMaintenance,**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance) [**IVdsLunMpio,**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)e [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**Windows Server 2008, Windows Vista e Windows Server 2003:** l'interfaccia [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) non è supportata.<br/> |
| Enumerazioni associate                                                                           | [**VDS \_ FLAG \_ LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) e [**STATO LUN \_ VDS \_**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)e [**TIPO \_ LUN \_ VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Strutture associate                                                                             | [**VDS \_ INFORMAZIONI \_ LUN,**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information)PROPRIETÀ LUN [**VDS \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)e [**NOTIFICA \_ LUN \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Vedere [Oggetto disco](disk-object.md) per un'interfaccia aggiuntiva ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) che viene esposta se il LUN non è mascherato come disco nel computer host locale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti provider hardware](hardware-provider-objects.md)
</dt> <dt>

[Oggetto Pack](pack-object.md)
</dt> <dt>

[Oggetto Disco](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Aggiunta di una lettera di unità a un LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

