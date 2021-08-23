---
description: Un provider di copie shadow deve essere conforme alle linee guida per garantire la compatibilità del richiedente.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportamenti obbligatori per i provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97153d3780701fce6edcde4a4a7740ae1d296b58b2bb44ea38c51f3ab1204499
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056389"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportamenti obbligatori per i provider di copie shadow

Un provider di copie shadow deve essere conforme alle linee guida per garantire la compatibilità del richiedente. In fase di esecuzione, un'applicazione di backup o qualsiasi altro richiedente che usa copie shadow deve funzionare correttamente senza conoscere dettagli specifici dell'implementazione del provider.

## <a name="automagic-resource-management"></a>Gestione risorse di Automagic

Il richiedente deve semplicemente aggiungere un volume a un set di copie shadow. Il richiedente può specificare gli attributi della copia shadow, ad esempio **VSS \_ VOLSNAP \_ ATTR \_ TRANSPORTABLE,** **VSS \_ VOLSNAP \_ ATTR \_ DIFFERENTIAL** e/o **VSS \_ VOLSNAP \_ \_ ATTR PLEX** in [**\_ VSS \_ SNAPSHOT \_ CONTEXT.**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Il provider deve rispettare tali attributi. Se non è in grado di rispettare tali attributi, deve indicare che il set di copie shadow non è supportato impostando \* *pbIsSupported* in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) su **FALSE.**

Il provider non deve mai accettare di supportare una copia shadow che non può creare. Se il richiedente non specifica un attributo plex o differenziale, il provider deve includere la logica automagic per l'allocazione dello spazio del sottosistema per la copia shadow e creare la copia shadow usando il metodo più appropriato. Il provider hardware non deve includere un'API specifica del provider per la gestione delle proprietà necessarie della copia shadow.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>I volumi della copia shadow creati Read-Only e nascosti

Il Servizio Copia Shadow del volume imposta flag su ogni LUN interessato in modo che i volumi delle copie shadow risultanti siano nascosti e di sola lettura quando vengono rilevati da un computer che esegue Windows Server 2003. Le lettere di unità e le cartelle montate non vengono assegnate automaticamente. Il Servizio Copia Shadow del volume mantiene questi flag per tutto il ciclo di vita di una copia shadow.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>I LUN della copia shadow dell'hardware devono essere di lettura/scrittura

Il Servizio Copia Shadow del volume supporta le copie shadow hardware solo nei casi in cui il LUN sottostante è mappato come lettura/scrittura. Questa operazione deve essere eseguita prima della creazione della copia shadow. non può essere eseguita dopo il fatto. I provider hardware non devono modificare questi flag. Per altre informazioni sull'uso di questi flag da parte del Servizio Copia Shadow del volume, vedere [Processo di creazione della copia shadow.](the-shadow-copy-creation-process.md)

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>L'importazione automatica di copie shadow hardware non è supportata nel Windows cluster

Windows Servizio cluster non è in grado di supportare LUN con firme duplicate e layout di partizione. I LUN della copia shadow devono essere trasportati in un host esterno al cluster. Per altre informazioni, vedere [Ripristino rapido tramite volumi copiati shadow trasportabili.](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Le copie shadow che contengono dischi dinamici devono essere trasportate in un host diverso

**Prima di Windows Server 2008:** Il supporto nativo per i dischi dinamici non può supportare LUN con firme duplicate e contenuto del database di configurazione. I LUN della copia shadow devono essere trasportati in un host diverso. VsS applica questo comportamento non consentendo l'importazione automatica di copie shadow di dischi dinamici. Un richiedente non deve importare nuovamente una copia shadow trasportabile nello stesso host.

**A partire Windows Server 2008:** Questa limitazione è stata rimossa.

## <a name="providers-are-out-of-process"></a>I provider sono out-of-process

Tutti i provider devono essere implementati come componenti COM out-of-process.

## <a name="time-critical-operations"></a>Time-Critical operazioni

Le operazioni lunghe, ad esempio la sincronizzazione dei plex, devono essere avviate in [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot.**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) Questa funzione deve avviare il lavoro di preparazione asincrona e tornare rapidamente. [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) funge da funzione di "incontro". Il provider può attendere in modo sincrono in questo metodo il completamento delle operazioni di preparazione avviate da **BeginPrepareSnapshot.**

I provider non devono aggiungere ritardi in [**IVssProviderCreateSnapshotSet::P reCommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) [**IVssProviderCreateSnapshotSet::CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)o [**IVssProviderCreateSnapshotSet::P ostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) quando le applicazioni vengono bloccate durante queste chiamate. **CommitSnapshots** dovrebbe restituire entro pochi secondi, perché viene chiamato durante la finestra scaricamento e attesa e il supporto del kernel VSS annulla lo scaricamento e il blocco se il rilascio non viene ricevuto entro 10 secondi, causando l'esito negativo del processo di creazione della copia shadow da parte del Servizio Copia Shadow del volume. Se il provider impiega più di pochi secondi per completare la chiamata, esiste una probabilità elevata che la creazione della copia shadow non riesca.

## <a name="careful-io-during-commitsnapshots"></a>I/O attento durante i commitSnapshots

I provider hardware non devono eseguire operazioni di I/O sui volumi coinvolti nella copia shadow durante [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots). Se sono necessarie operazioni di I/O, i provider non devono avviare alcuna operazione di I/O in un volume originale durante la gestione **del metodo CommitSnapshots.**

Durante [**CommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)i driver di supporto del kernel VSS bloccano l'I/O nei volumi originali di cui viene creata una copia shadow. Se il provider usa L/O sincrono in un volume che si trova nel set di copie shadow, tale I/O verrà bloccato e il processo di commit della copia shadow verrà bloccato. Il provider non deve chiamare api Win32 durante **CommitSnapshot perché** hanno una probabilità elevata di causare I/O e un deadlock. Il timeout del supporto del kernel VSS interromperà questo deadlock dopo 10 secondi, ma ciò causerà l'esito negativo della creazione della copia shadow.

Se è necessario eseguire operazioni di I/O, è necessario eseguire l'operazione in modo asincrono. L'I/O non verrà completato fino a quando tutti i provider non saranno stati restituiti dai relativi [**metodi CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) In generale, è meglio eseguire tali operazioni nella [**chiamata PostCommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots)

## <a name="readwrite-shadow-copy-luns"></a>LUN copia shadow di lettura/scrittura

In questa versione il Servizio Copia Shadow del volume supporta solo LUN di copia shadow di lettura/scrittura anche se i volumi sono esposti come di sola lettura. Il motivo è che il sistema deve modificare le strutture dei dati su disco, ad esempio:

-   Firma del disco, che cambia durante il processo di copia shadow
-   Strutture di dati correlate alle partizioni, incluse quelle che indicano che la partizione è di sola lettura, nascosta, una copia shadow e non deve essere assegnata una lettera di unità.

## <a name="unique-page-83-information"></a>Informazioni univoche sulla pagina 83

Sia il LUN originale che il LUN della copia shadow appena creata devono avere almeno un identificatore di archiviazione univoco nei dati della pagina 83. Almeno un IDENTIFICATORE DI ARCHIVIAZIONE di tipo \_ 1, 2, 3 o 8 e un'associazione 0 devono essere univoci nel LUN originale e nel LUN della copia shadow appena creata.

 

 



