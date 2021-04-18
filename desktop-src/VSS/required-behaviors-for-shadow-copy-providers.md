---
description: Un provider di copie shadow deve essere conforme alle linee guida per garantire la compatibilità del richiedente.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportamenti necessari per i provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f451dea7154a313cd64a3a46fbcc3b5fe663ec12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310675"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportamenti necessari per i provider di copie shadow

Un provider di copie shadow deve essere conforme alle linee guida per garantire la compatibilità del richiedente. In fase di esecuzione, un'applicazione di backup o qualsiasi altro richiedente che utilizza copie shadow deve funzionare correttamente senza conoscere i dettagli specifici dell'implementazione del provider.

## <a name="automagic-resource-management"></a>Gestione delle risorse automagiche

È necessario che il richiedente aggiunga semplicemente un volume a un set di copie shadow. Il richiedente può specificare attributi di copia shadow come **VSS \_ VolSnap \_ attr \_ Transportable**, **VSS \_ VolSnap \_ attr \_ differenziale** e/o **VSS \_ VolSnap \_ attr \_** nel [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context). Il provider deve rispettare tali attributi. Se non è possibile rispettare tali attributi, dovrebbe indicare che il set di copie shadow non è supportato impostando \* *PbIsSupported* in [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) su **false**.

Il provider non deve mai accettare di supportare una copia shadow che non è in grado di creare. Se il richiedente non specifica un attributo Plex o differenziale, il provider deve includere la logica di automagic per l'allocazione dello spazio del sottosistema per la copia shadow e creare la copia shadow usando il metodo più appropriato. Il provider hardware non deve includere un'API specifica del provider per la gestione delle proprietà delle copie shadow richieste.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>I volumi creati per le copie shadow sono Read-Only e nascosti

VSS imposta i flag su ogni LUN interessato in modo che i volumi di copia shadow risultanti siano nascosti e in sola lettura quando vengono rilevati da un computer che esegue Windows Server 2003. Le lettere di unità e le cartelle montate non vengono assegnate automaticamente. VSS mantiene questi flag per tutto il ciclo di vita di una copia shadow.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>I LUN della copia shadow hardware devono essere di lettura/scrittura

VSS supporta le copie shadow dell'hardware solo quando il LUN sottostante viene mappato come lettura/scrittura. Questa operazione deve essere eseguita prima della creazione della copia shadow. non può essere eseguita dopo il fatto. I provider hardware non devono modificare questi flag. Per ulteriori informazioni su come VSS utilizza questi flag, vedere [il processo di creazione della copia shadow](the-shadow-copy-creation-process.md).

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>L'importazione automatica delle copie shadow hardware non è supportata nel servizio cluster Windows

Windows Servizio cluster non può contenere lun con firme duplicate e layout di partizione. I LUN delle copie shadow devono essere trasportati in un host esterno al cluster. Per altre informazioni, vedere [ripristino rapido con volumi copiati shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md).

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Le copie shadow contenenti dischi dinamici devono essere trasferite in un host diverso

**Prima di Windows Server 2008:** Il supporto nativo per i dischi dinamici non può contenere lun con firme duplicate e contenuti del database di configurazione. I LUN delle copie shadow devono essere trasportati in un host diverso. Il servizio Copia Shadow del volume impone questo problema senza consentire l'importazione automatica di dischi dinamici. Un richiedente non deve importare nuovamente una copia shadow trasportabile nello stesso host.

**A partire da Windows Server 2008:** Questa limitazione è stata rimossa.

## <a name="providers-are-out-of-process"></a>I provider sono out-of-process

Tutti i provider devono essere implementati come componenti COM out-of-process.

## <a name="time-critical-operations"></a>Operazioni di Time-Critical

Le operazioni lunghe, ad esempio la sincronizzazione di Plex, devono essere avviate in [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot). Questa funzione deve avviare il lavoro di preparazione asincrona e restituire rapidamente. [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) funge da funzione "Rendezvous", il provider può attendere in modo sincrono in questo metodo per il completamento del lavoro di preparazione avviato da **BeginPrepareSnapshot**.

I provider non devono aggiungere ritardi in [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)o [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) perché le applicazioni sono bloccate durante tali chiamate. **CommitSnapshots** deve restituire in pochi secondi, perché viene chiamato durante la finestra di scaricamento e attesa e il supporto del kernel VSS Annulla lo scaricamento e il mantenimento se la versione non viene ricevuta entro 10 secondi, causando il mancato restituzione del processo di creazione della copia shadow da parte di VSS. Se il provider richiede più di alcuni secondi per completare questa chiamata, è molto probabile che la creazione della copia shadow abbia esito negativo.

## <a name="careful-io-during-commitsnapshots"></a>Accuratezza di I/O durante CommitSnapshots

I provider hardware non devono eseguire alcuna operazione di I/O nei volumi necessari per la copia shadow durante [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots). Se sono necessarie operazioni di I/O, i provider non devono avviare alcun I/O su un volume originale gestendo il metodo **CommitSnapshots** .

Durante [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), i driver del supporto del kernel VSS bloccano i/O nei volumi originali di cui viene eseguita la copia shadow. Se il provider utilizza l'I/O sincrono in un volume che si trova nel set di copie shadow, l'I/O verrà bloccato e il processo di commit della copia shadow sarà deadlock. Il provider non deve chiamare alcuna API Win32 durante **CommitSnapshots** poiché avrà una probabilità elevata di causare i/O e un deadlock. Il timeout del supporto del kernel VSS interrompe il deadlock dopo 10 secondi, ma la creazione della copia shadow avrà esito negativo.

Se deve essere eseguito un tentativo di I/O, è necessario eseguirlo in modo asincrono. L'i/O non verrà completato finché non vengono restituiti tutti i provider dai rispettivi metodi [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . In generale, è preferibile eseguire tali operazioni nella chiamata [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) .

## <a name="readwrite-shadow-copy-luns"></a>Lun copia shadow di lettura/scrittura

In questa versione, VSS supporta solo i LUN di copia shadow di lettura/scrittura anche se i volumi sono esposti come di sola lettura. Il motivo è che il sistema deve modificare le strutture dei dati su disco, ad esempio:

-   Firma del disco, che cambia durante il processo di copia shadow
-   Strutture di dati correlate alle partizioni, incluse quelle che indicano che la partizione è di sola lettura, nascosta, una copia shadow e non deve essere assegnata una lettera di unità.

## <a name="unique-page-83-information"></a>Informazioni sulla pagina univoca 83

Sia il lun originale che il LUN della copia shadow appena creato devono avere almeno un identificatore di archiviazione univoco nella pagina 83 dati. Almeno un identificatore di archiviazione \_ con tipo 1, 2, 3 o 8 e un'associazione di 0 devono essere univoci nel LUN originale e nel LUN della copia shadow appena creato.

 

 



