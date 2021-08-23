---
title: Creazione di riconciliatori di valigetta
description: Un riconciliatore di valigetta offre a Briefcase i mezzi per riconciliare versioni diverse di un documento.
ms.assetid: 86d66291-96ae-40ea-98ef-ef263f25aa82
keywords:
- riconciliatori di valigetta
- Riconciliazione
- IReconcilableObject
- IReconcileInitiator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4161796999172e6ee9bc7c403e723f9f8bafe7e876b544888fa5e7105b724f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556941"
---
# <a name="creating-briefcase-reconcilers"></a>Creazione di riconciliatori di valigetta

Un riconciliatore di valigetta offre a Briefcase i mezzi per riconciliare versioni diverse di un documento.

-   [Informazioni sui riconciliatori di valigetta](#about-briefcase-reconcilers)
    -   [Riconciliazione](#reconciliation)
    -   [Creazione di un riconciliatore di valigetta](#creating-a-briefcase-reconciler)
    -   [Interazione dell'utente nella riconciliazione](#user-interaction-in-reconciliation)
    -   [Riconcilio di oggetti incorporati](#reconciling-embedded-objects)
    -   [Residui](#residues)
-   [Informazioni di riferimento su Briefcase Reconciler](#briefcase-reconciler-reference)
    -   [Interfacce e metodi di Briefcase Reconciler](#briefcase-reconciler-interfaces-and-methods)

## <a name="about-briefcase-reconcilers"></a>Informazioni sui riconciliatori di valigetta

Un riconciliatore di valigetta combina diverse versioni di input di un documento per produrre una singola nuova versione di output del documento. Potrebbe essere necessario creare un riconciliatore di valigetta per supportare il tipo di documento. Questa panoramica descrive i riconciliatori di valigetta e spiega come crearli.

Vengono trattati i seguenti argomenti:

-   [Riconciliazione](#reconciliation)
-   [Creazione di un riconciliatore di valigetta](#creating-a-briefcase-reconciler)
-   [Interazione dell'utente nella riconciliazione](#user-interaction-in-reconciliation)
-   [Riconcilio di oggetti incorporati](#reconciling-embedded-objects)
-   [Residui](#residues)

### <a name="reconciliation"></a>Riconciliazione

Un documento è una raccolta di informazioni che possono essere copiate e modificate. Un documento ha versioni diverse se il contenuto di almeno due copie del documento è diverso. La riconciliazione produce una singola versione di un documento di due o più versioni iniziali. In genere, la versione riconciliata è una combinazione di informazioni delle versioni iniziali con le informazioni più recenti o più utili conservate.

La riconciliazione viene avviata da Briefcase quando determina che due o più copie dello stesso documento sono diverse. Briefcase, che funge da iniziatore in questo contesto, individua e avvia il riconciliatore di valigetta associato al tipo di documento specificato. Il riconciliatore confronta i documenti e determina le parti dei documenti da conservare. Alcuni riconciliatori potrebbero richiedere l'interazione dell'utente per completare la riconciliazione. Altri potrebbero completare la riconciliazione senza l'interazione dell'utente. Il riconciliatore può essere contenuto in un'applicazione o essere un'estensione implementata come DLL.

Alcuni riconciliatori di valigetta possono creare residui. Un residuo è un documento, in genere con lo stesso tipo di file del documento iniziale, che contiene informazioni non salvate nella versione unita. I residui vengono in genere usati per offrire agli autori un modo rapido per determinare quali informazioni del documento originale non si trovano nella versione finale unita. Se un riconciliatore supporta i residui, crea un residuo per ognuna delle versioni originali del documento. I residui non vengono creati a meno che non vengano richieste dall'iniziatore.

Alcuni riconciliatori di valigetta lavorano con Briefcase per consentire all'utente di terminare la riconciliazione. Si tratta di una funzionalità importante per un utente che potrebbe decidere che la riconciliazione non deve continuare. Un riconciliatore fornisce in genere un oggetto di terminazione quando la riconciliazione richiede l'interazione dell'utente e potrebbe essere lunga. In alcuni ambienti, un riconciliatore potrebbe consentire la riconciliazione parziale, consentendo a un utente di sospendere temporaneamente una riconciliazione e riprenderla in un secondo momento. La valigetta non supporta attualmente la riconciliazione parziale.

### <a name="creating-a-briefcase-reconciler"></a>Creazione di un riconciliatore di valigetta

È possibile creare un riconciliatore di valigetta implementando le interfacce di riconciliazione. Come minimo, un riconciliatore implementa [**l'interfaccia IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) e [l'interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Come iniziatore, Briefcase determina quando è necessaria la riconciliazione e chiama il metodo [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) per avviare la riconciliazione.

Sebbene [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) offra un ampio set di funzionalità di riconciliazione, nella maggior parte dei casi un riconciliatore di valigetta esegue solo una riconciliazione minima. In particolare, Briefcase non richiede che il riconciliatore supporti la generazione di residui o supporti l'oggetto di terminazione. Inoltre, il riconciliatore esegue una singola riconciliazione dall'alto verso il basso e non deve restituire il valore REC E NOTCOMPLETE, cio' non deve tentare la \_ \_ riconciliazione parziale.

Briefcase fornisce [**l'interfaccia IReconcileInitiator.**](ireconcileinitiator.md) Il riconciliatore di valigetta può usare il metodo [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback) per impostare l'oggetto di terminazione. Briefcase non usa identificatori di versione e pertanto non può fornire versioni precedenti di un documento se un riconciliatore le richiede usando i metodi corrispondenti in **IReconcileInitiator**.

Briefcase passa [**a IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) i moniker di file che rappresentano le versioni del documento da riconciliare. Il riconciliatore di valigetta ottiene l'accesso alle versioni usando il metodo [IMoniker::BindToObject](/windows/win32/api/objidl/nf-objidl-imoniker-bindtoobject) o [IMoniker::BindToStorage.](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage) Quest'ultimo è in genere più veloce ed è consigliato. Il riconciliatore deve rilasciare tutti gli oggetti o le risorse di archiviazione a cui è associato.

Quando il riconciliatore di valigetta usa [IMoniker::BindToStorage,](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage)viene associato all'archiviazione che è un archivio flat (un flusso) o un'archiviazione strutturata definita da OLE. Se il riconciliatore prevede l'archiviazione flat, deve usare IMoniker::BindToStorage per richiedere [l'interfaccia IStream.](/windows/win32/api/objidl/nn-objidl-istream) Se il riconciliatore prevede l'archiviazione strutturata, deve richiedere [l'interfaccia IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) In entrambi i casi, deve richiedere l'accesso diretto (non tradotto) di sola lettura all'archiviazione. L'accesso in lettura/scrittura potrebbe non essere disponibile.

Un riconciliatore briefcase minimo esamina in genere direttamente l'archiviazione delle altre versioni e gestisce gli oggetti incorporati in modo molto primitivo, ad esempio unendo due versioni dell'oggetto includendo entrambe le versioni nella versione di output.

L'iniziatore individua il riconciliatore di valigetta appropriato usando un subset della logica implementata dalla funzione [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile) per determinare il tipo di un determinato file e quindi cerca nel Registro di sistema la classe reconciler associata al tipo di file specificato. La valigetta, come altri componenti di Shell, determina il tipo di un file esclusivamente in base all'estensione del nome file. L'estensione di un file deve avere un tipo di file registrato perché Briefcase richiama un riconciliatore per il file. È necessario impostare una voce del Registro di sistema nel formato seguente durante l'installazione del riconciliatore.

```
CLSID
   {the file CLSID}
      Roles
         Reconciler
            (Default) = {the reconciler-classid}
```

La classe deve essere caricamento rapido, deve essere designata MULTIPLEUSE e, a meno che non vengano forniti i marshalling per l'interfaccia di riconciliazione, deve essere un server in-process (contenuto in una DLL) anziché un server locale (implementato in un \_ file .exe).

### <a name="user-interaction-in-reconciliation"></a>Interazione dell'utente nella riconciliazione

Un riconciliatore di valigetta deve tentare di eseguire la riconciliazione senza l'interazione dell'utente. Più automatizzata è la riconciliazione, migliore sarà la percezione del processo da parte dell'utente.

In alcuni casi, l'intervento dell'utente può essere utile. Ad esempio, un sistema di documenti potrebbe richiedere a un utente di esaminare le modifiche prima di accettare la versione unita di un documento o potrebbe richiedere commenti all'utente che spiegano le modifiche apportate. In questi casi, l'iniziatore, non il riconciliatore di valigetta, è responsabile dell'esecuzione di query sull'utente e dell'esecuzione delle istruzioni dell'utente.

In altri casi, l'intervento dell'utente potrebbe essere necessario, ad esempio quando due versioni sono state modificate in modo incompatibile. In questi casi, l'iniziatore o il riconciliatore di valigetta deve eseguire una query sull'utente per istruzioni su come risolvere il conflitto. In generale, nessun iniziatore può basarsi sul completamento di una riconciliazione senza aspettarsi un'interazione dell'utente. I riconciliatori, d'altra parte, hanno la possibilità di interagire con l'utente per risolvere i conflitti o richiedere all'iniziatore di farlo.

### <a name="reconciling-embedded-objects"></a>Riconcilio di oggetti incorporati

Quando si riconcilia un documento, il riconciliatore di valigetta può diventare un iniziatore se individua un oggetto incorporato di un tipo che non può riconciliare. In questo caso, il riconciliatore deve riconciliare in modo ricorsivo ognuno degli oggetti incorporati e assumersi tutte le responsabilità di un iniziatore.

Per eseguire la ricorsione, il riconciliatore della valigetta carica l'oggetto e esegue query per l'interfaccia appropriata. Il gestore per l'oggetto deve supportare l'interfaccia . Se un metodo dell'interfaccia restituisce il valore OLE E NOTRUNNING, il riconciliatore deve eseguire l'oggetto per \_ \_ eseguire l'operazione. Poiché il codice per gli oggetti incorporati non è sempre disponibile, un riconciliatore deve fornire una soluzione per questa condizione. Ad esempio, il riconciliatore potrebbe includere sia le versioni precedenti che le nuove dell'oggetto incorporato nella versione riconciliata. Il riconciliatore non deve tentare di riconciliare i collegamenti.

L'iniziatore archivia le versioni del documento da unire. In molti casi, l'iniziatore ha accesso all'archiviazione di ogni versione e salva il risultato della riconciliazione usando un'archiviazione simile. A volte, tuttavia, l'iniziatore potrebbe avere un oggetto in memoria per cui non è disponibile alcuna versione permanente. Questa situazione può verificarsi quando un documento contenente oggetti incorporati aperti deve essere riconciliato prima di essere salvato. In questi casi, l'iniziatore salva il risultato della riconciliazione nella versione trovata in memoria.

L'iniziatore usa [l'interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) per associare (caricare) la versione unita. L'iniziatore usa il metodo [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) se è già stata creata una versione iniziale e usa il metodo [IPersistStorage::InitNew](/windows/win32/api/objidl/nf-objidl-ipersiststorage-initnew) per la versione iniziale. Quando viene caricata la versione unita, l'iniziatore usa [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per recuperare l'indirizzo [**dell'interfaccia IReconcilableObject.**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) Questa interfaccia consente all'iniziatore di accedere all'archiviazione dei residui esistenti e consente di creare spazio di archiviazione per eventuali nuovi residui. L'iniziatore indirizza quindi l'interfaccia per eseguire la riconciliazione. L'iniziatore esegue effettivamente una query per [l'interfaccia IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) prima di IPersistStorage. Se il riconciliatore supporta IPersistFile, l'iniziatore modifica la replica tramite i metodi IPersistFile anziché IPersistStorage. Ciò consente la riconciliazione dei file che non vengono archiviati come documenti composti.

Al termine della riconciliazione, l'iniziatore può salvare la versione unita usando [l'interfaccia IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) o [IPersistFile.](/windows/win32/api/objidl/nn-objidl-ipersistfile) Durante la riconciliazione, il riconciliatore di valigetta crea i residui in base alle esigenze e scrive i relativi bit persistenti nell'archiviazione. Se la versione unita è un flusso, l'interfaccia [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) passata a [IPersistStorage::Load](/windows/win32/api/objidl/nf-objidl-ipersiststorage-load) contiene un flusso denominato "Contents" con lo stato di archiviazione impostato su STATEBITS \_ FLAT. È possibile impostare i bit di stato usando il [metodo IStorage::Stat.](/windows/win32/api/objidl/nf-objidl-istorage-stat) Dopo l'unione, l'iniziatore salva la versione unita scrivendo i dati in modo appropriato. Deve garantire che STATEBITS \_ FLAT sia impostato come appropriato per l'archiviazione.

### <a name="residues"></a>Residui

L'iniziatore indica se desidera residui impostando il parametro *pstgNewResidues* su un indirizzo valido quando si chiama il metodo [**IReconcilableObject::Reconcile.**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile) Se il riconciliatore non supporta la creazione di residui, deve restituire immediatamente il valore REC E NORESIDUES, a meno che il parametro dwFlags non specifichi il valore \_ \_ **RECONCILEF \_ NORESIDUESOK.** 

Il riconciliatore di valigetta restituisce i residui all'iniziatore creando nuovi elementi di archiviazione e copiandoli nella matrice a cui punta *pstgNewResidues.* Per i residui di archiviazione strutturata, il riconciliatore copia un'interfaccia [IStorage](/windows/win32/api/objidl/nn-objidl-istorage) e, per i residui di archiviazione flat, copia [un'interfaccia IStream](/windows/win32/api/objidl/nn-objidl-istream) o IStorage con il flag STATEBITS \_ FLAT impostato. Il riconciliatore usa IStorage per creare l'archiviazione necessaria, usando [IStorage::CreateStream](/windows/win32/api/objidl/nf-objidl-istorage-createstream) per creare l'archiviazione flat per un residuo che è un flusso e [IStorage::CreateStorage](/windows/win32/api/objidl/nf-objidl-istorage-createstorage) per creare l'archiviazione strutturata.

L'iniziatore prepara *pstgNewResidues* in modo che non contenga elementi nella parte non riservata dello spazio [dei nomi IStorage.](/windows/win32/api/objidl/nn-objidl-istorage) Il riconciliatore di valigetta inserisce ogni residuo in un elemento il cui nome corrisponde all'ordine della versione iniziale. Ad esempio, il primo residuo è contenuto in "1", il secondo in "2" e così via. Se l'oggetto riconciliato stesso produce un residuo, viene trovato nell'elemento denominato "0".

Il riconciliatore di valigetta esegue il commit di ognuno degli elementi appena creati singolarmente, assicurando che l'iniziatore abbia accesso alle informazioni. Il riconciliatore, tuttavia, non esegue il commit *di pstgNewResidues.* L'iniziatore è responsabile del commit o dell'eliminazione dell'iniziatore.

## <a name="briefcase-reconciler-reference"></a>Riferimento per riconciliatore di valigetta

Questa sezione contiene informazioni sulle interfacce di riconciliazione. Durante la gestione degli errori, un metodo può restituire solo i valori di errore definiti in modo esplicito come possibili valori restituiti. Inoltre, il metodo deve impostare tutte le variabili i cui indirizzi vengono passati come parametri su **NULL** prima di restituire l'errore.

### <a name="briefcase-reconciler-interfaces-and-methods"></a>Interfacce e metodi di Riconciliatore di valigetta

-   [**Oggetto IReconcilableObject**](/windows/win32/api/reconcil/nn-reconcil-ireconcilableobject) 
    -   -   [**IReconcilableObject::GetProgressFeedbackMaxEstimate**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-getprogressfeedbackmaxestimate)
        -   [**IReconcilableObject::Reconcile**](/windows/win32/api/reconcil/nf-reconcil-ireconcilableobject-reconcile)

-   [**IReconcileInitiator**](ireconcileinitiator.md) 
    -   -   [**IReconcileInitiator::SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)
        -   [**IReconcileInitiator::SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback)

-   [**INotifyReplica**](/windows/desktop/api/reconcil/nn-reconcil-inotifyreplica) 
    -   -   [**INotifyReplica::YouAreAReplica**](/windows/desktop/api/reconcil/nf-reconcil-inotifyreplica-youareareplica)

 

 