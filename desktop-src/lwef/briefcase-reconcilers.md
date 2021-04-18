---
title: Creazione di riconciliatori di cartelle
description: Un riconciliatore della valigetta fornisce alla valigetta i mezzi per riconciliare le diverse versioni di un documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- riconciliatori di cartelle
- riconciliazione
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b925e7055e15f6c7a49408aa28d147fb2eef5a7e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398868"
---
# <a name="creating-briefcase-reconcilers"></a>Creazione di riconciliatori di cartelle

Un riconciliatore della valigetta fornisce alla valigetta i mezzi per riconciliare le diverse versioni di un documento.

-   [Informazioni sui riconciliatori della cartella](#about-briefcase-reconcilers)
    -   [Riconciliazione](#reconciliation)
    -   [Creazione di un riconciliatore di valigetta](#creating-a-briefcase-reconciler)
    -   [Interazione dell'utente nella riconciliazione](#user-interaction-in-reconciliation)
    -   [Riconciliazione di oggetti incorporati](#reconciling-embedded-objects)
    -   [Residui](#residues)
-   [Riferimento al Riconciliatore di cartelle](#briefcase-reconciler-reference)
    -   [Metodi e interfacce del riconciliatore di cartelle](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Informazioni sui riconciliatori della cartella

Un riconciliatore di cartelle combina diverse versioni di input di un documento per produrre una singola versione di output del documento. Potrebbe essere necessario creare un riconciliatore di valigetta per supportare il tipo di documento. Questa panoramica descrive i riconciliatori della valigetta e spiega come crearli.

Vengono trattati i seguenti argomenti:

-   [Riconciliazione](#reconciliation)
-   [Creazione di un riconciliatore di valigetta](#creating-a-briefcase-reconciler)
-   [Interazione dell'utente nella riconciliazione](#user-interaction-in-reconciliation)
-   [Riconciliazione di oggetti incorporati](#reconciling-embedded-objects)
-   [Residui](#residues)

### <a name="reconciliation"></a>Riconciliazione

Un documento è una raccolta di informazioni che possono essere copiate e modificate. Un documento dispone di versioni diverse se il contenuto di almeno due copie del documento è diverso. La riconciliazione produce una singola versione di un documento da due o più versioni iniziali. In genere, la versione riconciliata è costituita da una combinazione di informazioni delle versioni iniziali con le informazioni più recenti o più utili mantenute.

La riconciliazione viene avviata da sincronia quando determina che due o più copie dello stesso documento sono diverse. La valigetta, che funge da iniziatore in questo contesto, individua e avvia il Riconciliatore di valigetta associato al tipo di documento specificato. Il riconciliatore Confronta i documenti e determina le parti dei documenti da mantenere. Alcuni riconciliatori potrebbero richiedere l'interazione dell'utente per completare la riconciliazione. Altri potrebbero completare la riconciliazione senza interazione dell'utente. Il riconciliatore può essere contenuto all'interno di un'applicazione o essere un'estensione implementata come DLL.

Alcuni riconciliatori della valigetta potrebbero creare i residui. Un residuo è un documento, in genere con lo stesso tipo di file del documento iniziale, che contiene informazioni non salvate nella versione unita. I residui vengono in genere usati per fornire agli autori un modo rapido per determinare quali informazioni del documento originale non sono nella versione finale unita. Se un riconciliatore supporta i residui, viene creato un residuo per ogni versione originale del documento. I residui non vengono creati a meno che non vengano richiesti dall'initiator.

Alcuni riconciliatori di valigetta funzionano con la valigetta per consentire all'utente di terminare la riconciliazione. Si tratta di una funzionalità importante per un utente che può decidere che la riconciliazione non deve continuare. Un riconciliatore in genere fornisce un oggetto di terminazione quando la riconciliazione richiede l'interazione dell'utente e potrebbe essere lunga. In alcuni ambienti un riconciliatore potrebbe consentire la riconciliazione parziale, consentendo a un utente di sospendere temporaneamente una riconciliazione e di riprenderla in un secondo momento. Tuttavia, la cartella non supporta attualmente la riconciliazione parziale.

### <a name="creating-a-briefcase-reconciler"></a>Creazione di un riconciliatore di valigetta

Si crea un riconciliatore di valigetta implementando le interfacce di riconciliazione. Come minimo, un riconciliatore implementa l'interfaccia [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) e l'interfaccia [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Come iniziatore, la cartella di sincronizzazione determina quando è necessaria la riconciliazione e chiama il metodo [**IReconcilableObject:: riconcilia**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) per avviare la riconciliazione.

Sebbene [**IReconcilableObject:: riconcilia**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) fornisca un ampio set di funzionalità di riconciliazione, nella maggior parte dei casi un riconciliatore di valigetta esegue solo la riconciliazione minima. In particolare, per la cartella non è necessario che il riconciliatore supporti la generazione di residui o per supportare l'oggetto di terminazione. Inoltre, il riconciliatore esegue una singola riconciliazione dall'alto verso il basso e non deve restituire il \_ valore REC e \_ non completato, ovvero non deve tentare la riconciliazione parziale.

La cartella fornisce l'interfaccia [**IReconcileInitiator**](ireconcileinitiator.md) . Il riconciliatore della valigetta può usare il metodo [**IReconcileInitiator:: SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) per impostare l'oggetto di terminazione. La cartella non usa gli identificatori di versione e non può, pertanto, fornire versioni precedenti di un documento se un riconciliatore le richiede usando i metodi corrispondenti in **IReconcileInitiator**.

La valigetta passa ai moniker di file [**IReconcilableObject:: riconcilia**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) che rappresentano le versioni del documento da riconciliare. Il riconciliatore della valigetta Ottiene l'accesso alle versioni usando il metodo [IMoniker:: BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) o [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) . Quest'ultimo è in genere più veloce ed è consigliato. Il riconciliatore deve rilasciare tutti gli oggetti o le archiviazioni a cui è associato.

Quando il riconciliatore della valigetta USA [IMoniker:: BindToStorage](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage), viene associato allo spazio di archiviazione che è l'archiviazione Flat (un flusso) o l'archiviazione strutturata definita da OLE. Se il riconciliatore prevede l'archiviazione Flat, deve usare IMoniker:: BindToStorage per richiedere l'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) . Se il riconciliatore prevede l'archiviazione strutturata, deve richiedere l'interfaccia [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . In entrambi i casi, deve richiedere l'accesso diretto (non transazionale) di sola lettura all'archiviazione; l'accesso in lettura/scrittura potrebbe non essere disponibile.

Un riconciliatore di valigetta minimo in genere cerca direttamente nello spazio di archiviazione delle altre versioni e gestisce gli oggetti incorporati in modo molto primitivo, ad esempio unendo due versioni dell'oggetto includendo entrambe le versioni nella versione di output.

L'initiator individua il Riconciliatore di valigetta appropriato usando un subset della logica implementata dalla funzione [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) per determinare il tipo di un determinato file e quindi Cerca nel registro di sistema la classe del riconciliatore associata al tipo di file specificato. La valigetta, analogamente ad altri componenti della shell, determina il tipo di file esclusivamente dall'estensione del nome file. L'estensione di un file deve avere un tipo di file registrato per la cartella per richiamare un riconciliatore per il file. Quando si installa il riconciliatore, è necessario impostare una voce del registro di sistema nel formato seguente.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

La classe deve essere caricamento rapido, deve essere designato come \_ MULTIPLEUSE e, a meno che non vengano forniti i marshalling per l'interfaccia di riconciliazione, deve essere un server in-process (contenuto in una dll) anziché un server locale (implementato in un file exe).

### <a name="user-interaction-in-reconciliation"></a>Interazione dell'utente nella riconciliazione

Un riconciliatore di valigetta deve tentare di eseguire la riconciliazione senza interazione dell'utente. Maggiore è l'automazione della riconciliazione, migliore sarà la percezione dell'utente del processo.

In alcuni casi, l'intervento dell'utente può essere utile. Ad esempio, un sistema di documenti potrebbe richiedere a un utente di rivedere le modifiche prima di accettare la versione unita di un documento o potrebbe richiedere commenti all'utente che spieghi le modifiche apportate. In questi casi, l'iniziatore, non il riconciliatore della valigetta, è responsabile dell'esecuzione di query sull'utente e delle istruzioni dell'utente.

In altri casi, potrebbe essere necessario l'intervento dell'utente, ad esempio quando due versioni sono state modificate in modi incompatibili. In questi casi, il riconciliatore dell'initiator o della valigetta deve eseguire una query sull'utente per istruzioni su come risolvere il conflitto. In generale, nessun iniziatore può basarsi sul completamento di una riconciliazione senza prevedere un'interazione dell'utente. I riconciliatori, d'altra parte, hanno la possibilità di interagire con l'utente per risolvere i conflitti o richiedere l'Initiator a tale scopo.

### <a name="reconciling-embedded-objects"></a>Riconciliazione di oggetti incorporati

Quando si riconcilia un documento, il riconciliatore della valigetta può diventare un iniziatore se individua un oggetto incorporato di un tipo che non può riconciliare. In questo caso, il riconciliatore deve riconciliare in modo ricorsivo ciascuno degli oggetti incorporati e assumere tutte le responsabilità di un iniziatore.

Per eseguire la ricorsione, il riconciliatore della valigetta carica l'oggetto e le query per l'interfaccia appropriata. Il gestore per l'oggetto deve supportare l'interfaccia. Se un metodo dell'interfaccia restituisce il valore OLE \_ E \_ non in esecuzione, il riconciliatore deve eseguire l'oggetto in modo da eseguire l'operazione. Poiché il codice per gli oggetti incorporati non è sempre disponibile, è necessario che un riconciliatore fornisca una soluzione per questa condizione. Ad esempio, il riconciliatore potrebbe includere sia le versioni precedenti che quelle nuove dell'oggetto incorporato nella versione riconciliata. Il riconciliatore non deve tentare la riconciliazione tra i collegamenti.

L'initiator archivia le versioni del documento sottoposte a merge. In molti casi, l'initiator ha accesso all'archiviazione di ogni versione e salva il risultato della riconciliazione usando un'archiviazione simile. In alcuni casi, tuttavia, l'Initiator potrebbe avere un oggetto in memoria per il quale non è disponibile una versione permanente. Questa situazione può verificarsi quando un documento contenente oggetti incorporati aperti deve essere riconciliato prima di essere salvato. In questi casi, l'iniziatore Salva il risultato della riconciliazione nella versione trovata in memoria.

L'initiator utilizza l'interfaccia [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) per associare (caricare) la versione unita. L'initiator usa il metodo [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) se è già stata creata una versione iniziale e usa il metodo [IPersistStorage:: InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) per la versione iniziale. Quando viene caricata la versione unita, l'iniziatore utilizza [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare l'indirizzo dell'interfaccia [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) . Questa interfaccia consente all'initiator di accedere all'archiviazione dei residui esistenti e fornisce un modo per creare spazio di archiviazione per eventuali nuovi residui. Quindi l'initiator indirizza l'interfaccia per eseguire la riconciliazione. L'iniziatore esegue effettivamente una query per l'interfaccia [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) prima di IPersistStorage. Se il riconciliatore supporta IPersistFile, l'initiator manipola la replica tramite IPersistFile anziché i metodi IPersistStorage. Ciò consente la riconciliazione dei file non archiviati come documenti composti.

Al termine della riconciliazione, l'initiator può salvare la versione unita utilizzando l'interfaccia [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) . Durante la riconciliazione, il riconciliatore della valigetta crea i residui in base alle esigenze e scrive i bit persistenti nell'archivio. Se la versione unita è un flusso, l'interfaccia [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) passata a [IPersistStorage:: Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) contiene un flusso denominato "Contents" con lo stato di archiviazione impostato su STATEBITS \_ flat. (È possibile impostare i bit di stato usando il metodo [IStorage:: stat](/windows/win32/api/objidl/nf-objidl-istorage-stat) ). Dopo l'Unione, l'initiator salva la versione unita scrivendo i dati in modo appropriato. È necessario assicurarsi che STATEBITS \_ Flat sia impostato in modo appropriato per l'archiviazione.

### <a name="residues"></a>Residui

L'initiator indica se desidera i residui impostando il parametro *pstgNewResidues* su un indirizzo valido quando si chiama il metodo [**IReconcilableObject:: riconcilia**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) . Se il riconciliatore non supporta la creazione di residui, deve restituire immediatamente il valore REC \_ E \_ noresidus, a meno che il parametro *dwFlags* specifichi il **valore \_ NORESIDUESOK di RECONCILEF** .

Il riconciliatore della valigetta restituisce i residui all'iniziatore creando nuovi elementi di archiviazione e copiando tali elementi nella matrice a cui punta *pstgNewResidues*. Per i residui di archiviazione strutturata, il riconciliatore copia un'interfaccia [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) e, per i residui di archiviazione Flat, copia un'interfaccia [IStream](/windows/win32/api/objidl/nn-objidl-istream) o IStorage con il \_ flag Flat STATEBITS impostato. Il riconciliatore USA IStorage per creare la risorsa di archiviazione necessaria, usando [IStorage:: CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) per creare l'archiviazione flat per un residuo che è un flusso e [IStorage:: CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) per creare un archivio strutturato.

L'iniziatore prepara *pstgNewResidues* in modo che non contenga elementi nella parte non riservata dello spazio dei nomi [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) . Il riconciliatore della valigetta posiziona ogni residuo in un elemento il cui nome corrisponde all'ordine della versione iniziale. Il primo residuo, ad esempio, è contenuto in "1", il secondo in "2" e così via. Se l'oggetto riconciliato produce un residuo, questo viene trovato nell'elemento denominato "0".

Il riconciliatore della valigetta eseguirà il commit di ciascuno degli elementi appena creati, assicurando che l'initiator abbia accesso alle informazioni. Il riconciliatore, tuttavia, non esegue il commit di *pstgNewResidues* stesso. L'iniziatore è responsabile di eseguire il commit di questo o di eliminarlo in altro modo.

## <a name="briefcase-reconciler-reference"></a>Riferimento al Riconciliatore di cartelle

Questa sezione contiene informazioni sulle interfacce di riconciliazione. Quando si gestiscono gli errori, un metodo può restituire solo i valori di errore definiti in modo esplicito come possibili valori restituiti. Inoltre, il metodo deve impostare tutte le variabili i cui indirizzi vengono passati come parametri a **null** prima di restituire l'errore.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Metodi e interfacce del riconciliatore di cartelle

-   [**IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject:: riconcilia**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 