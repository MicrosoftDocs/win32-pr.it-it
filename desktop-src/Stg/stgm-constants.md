---
title: Costanti STGM (ObjBase.h)
description: Flag che indicano le condizioni per la creazione e l'eliminazione dell'oggetto e le modalità di accesso per l'oggetto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18248e862c3d5981e9c34b29522b1cd75d2b61cf78a52613b3d28a1d2c98b4fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661971"
---
# <a name="stgm-constants"></a>Costanti STGM

Le costanti STGM sono flag che indicano le condizioni per la creazione e l'eliminazione dell'oggetto e delle modalità di accesso per l'oggetto. Le costanti STGM sono incluse nelle interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e nelle funzioni [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)e [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)

Questi elementi vengono spesso combinati usando un **operatore OR.** Vengono interpretati in gruppi come indicato nella tabella seguente. Non è valido usare più di un elemento di un singolo gruppo.

Usare un flag del gruppo di creazione quando si crea un oggetto, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage::CreateStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)

Per altre informazioni sulle transazioni, vedere la sezione Osservazioni.



| Group                      | Flag                         | valore       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM \_ READ**               | 0x00000000L |
|                            | **STGM \_ WRITE**              | 0x00000001L |
|                            | **STGM \_ READWRITE**          | 0x00000002L |
| Condivisione                    | **STGM \_ SHARE \_ DENY \_ NONE**  | 0x00000040L |
|                            | **STGM \_ SHARE \_ DENY \_ READ**  | 0x00000030L |
|                            | **STGM \_ SHARE \_ DENY \_ WRITE** | 0x00000020L |
|                            | **STGM \_ SHARE \_ EXCLUSIVE**   | 0x00000010L |
|                            | **STGM \_ PRIORITY**           | 0x00040000L |
| Creazione                   | **STGM \_ CREATE**             | 0x00001000L |
|                            | **STGM \_ CONVERT**            | 0x00020000L |
|                            | **STGM \_ FAI PIÙ COMPLETO**        | 0x00000000L |
| Transazione             | **STGM \_ DIRECT**             | 0x00000000L |
|                            | **STGM \_ TRANSACTED**         | 0x00010000L |
| Prestazioni delle transazioni | **STGM \_ NOSRATACH**          | 0x00100000L |
|                            | **STGM \_ NOSNAPSHOT**         | 0x00200000L |
| SWMR diretto e semplice     | **STGM \_ SIMPLE**             | 0x08000000L |
|                            | **STGM \_ DIRECT \_ SWMR**       | 0x00400000L |
| Elimina alla versione          | **STGM \_ DELETEONRELEASE**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM \_ READ**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica che l'oggetto è di sola lettura, vale a dire che non è possibile apportare modifiche. Ad esempio, se un oggetto flusso viene aperto con **STGM \_ READ,** è possibile chiamare il metodo [**ISequentialStream::Read,**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) ma non il metodo [**ISequentialStream::Write.**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) Analogamente, se un oggetto di archiviazione aperto con **STGM \_ READ** può essere chiamato il metodo [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) [**e IStorage::OpenStorage,**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) ma non i metodi [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage::CreateStorage.**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM \_ WRITE**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Consente di salvare le modifiche apportate all'oggetto, ma non consente l'accesso ai relativi dati. Le implementazioni fornite delle [**interfacce IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) non supportano questa modalità di sola scrittura.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM \_ READWRITE**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Consente l'accesso e la modifica dei dati dell'oggetto. Ad esempio, se un oggetto flusso viene creato o aperto in questa modalità, è possibile chiamare sia [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) che **IStream::Write**. Tenere presente che questa costante non è una semplice operazione **OR** binaria degli **elementi STGM \_ WRITE** **e STGM \_ READ.**


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ SHARE \_ DENY \_ NONE**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Specifica che alle successive apertura dell'oggetto non viene negato l'accesso in lettura o scrittura. Se non viene specificato alcun flag dal gruppo di condivisione, viene utilizzato questo flag.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ SHARE \_ DENY \_ READ**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto in **modalità STGM \_ READ.** Viene in genere usato in un oggetto di archiviazione radice.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ SHARE \_ DENY \_ WRITE**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto per **l'accesso STGM \_ WRITE** **o STGM \_ READWRITE.** In modalità transazione, la condivisione di **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE** può migliorare significativamente le prestazioni perché non richiedono snapshot. Per altre informazioni sulle transazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ SHARE \_ EXCLUSIVE**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto in qualsiasi modalità. Tenere presente che questo valore non è una semplice operazione **OR** bit per bit dei valori **STGM \_ SHARE DENY \_ \_ READ** e **STGM SHARE DENY \_ \_ \_ WRITE.** In modalità transazione, la condivisione di **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE** può migliorare significativamente le prestazioni perché non richiedono snapshot. Per altre informazioni sulle transazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM \_ PRIORITY**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Apre l'oggetto di archiviazione con accesso esclusivo alla versione di cui è stato eseguito il commit più di recente. Pertanto, gli altri utenti non possono eseguire il commit delle modifiche all'oggetto mentre è aperto in modalità di priorità. Si ottengono vantaggi in termini di prestazioni per le operazioni di copia, ma si impedisce ad altri utenti di eseguire il commit delle modifiche. Limitare il tempo di apertura degli oggetti in modalità di priorità. È necessario specificare **STGM \_ DIRECT** e **STGM \_ READ** con la modalità di priorità e non è possibile **specificare STGM \_ DELETEONRELEASE.** **STGM \_ DELETEONRELEASE è** valido solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) Non è valida quando si apre un oggetto radice esistente, ad esempio con [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Non è inoltre valido quando si crea o si apre un sottoelemento, ad esempio con [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM \_ CREATE**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indica che un oggetto o un flusso di archiviazione esistente deve essere rimosso prima che il nuovo oggetto lo sostituisca. Viene creato un nuovo oggetto quando questo flag viene specificato solo se l'oggetto esistente è stato rimosso correttamente.

Questo flag viene usato quando si tenta di creare:

-   Un oggetto di archiviazione su un disco, ma esiste un file con tale nome.
-   Oggetto all'interno di un oggetto di archiviazione, ma esiste un oggetto con il nome specificato.
-   Oggetto matrice di byte, ma ne esiste uno con il nome specificato.

Questo flag non può essere usato con operazioni di apertura, ad esempio [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage::OpenStream.**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ CONVERT**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Crea il nuovo oggetto mantenendo i dati esistenti in un flusso denominato "Contents". Nel caso di un oggetto di archiviazione o di una matrice di byte, i dati meno vecchi vengono formattati in un flusso indipendentemente dal fatto che il file o la matrice di byte esistente contenga o meno un oggetto di archiviazione su più livelli. Questo flag può essere usato solo quando si crea un oggetto di archiviazione radice. Non può essere usato all'interno di un oggetto di archiviazione. ad esempio in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Non è inoltre valido usare questo flag e il flag **STGM \_ DELETEONRELEASE** contemporaneamente.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM \_ FAI PIÙ COMPLETO**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Causa l'esito negativo dell'operazione di creazione se esiste un oggetto esistente con il nome specificato. In questo caso, **viene restituito STG \_ E \_ FILEALREADYEXISTS.** Questa è la modalità di creazione predefinita. in altre parole, se non viene specificato alcun altro flag di creazione, **stGM \_ FAI PIÙEFFERE** è implicito.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ DIRECT**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica che, in modalità diretta, ogni modifica a un elemento di archiviazione o flusso viene scritta non appena si verifica. Questa è l'impostazione predefinita se non **viene specificato né STGM \_ DIRECT** né **STGM \_ TRANSACTED.**


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ TRANSACTED**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indica che, in modalità transazione, le modifiche vengono memorizzate nel buffer e scritte solo se viene chiamata un'operazione di commit esplicita. Per ignorare le modifiche, chiamare il [**metodo Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) nell'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) L'implementazione di file compositi COM di **IStorage** non supporta i flussi transazionati, il che significa che i flussi possono essere aperti solo in modalità diretta e non è possibile annullare le modifiche apportate, ma sono supportate le risorse di archiviazione transazione. Analogamente, le implementazioni di file composti, autonomi e NTFS file system [**di IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) non supportano set di proprietà semplici transazionati perché questi set di proprietà vengono archiviati in flussi. È tuttavia supportata la transazione di set di proprietà nonsimple, che possono essere creati specificando il flag **PROPSETFLAG \_ NONSIMPLE** nel parametro *grfFlags* di [**IPropertySetStorage::Create.**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOSRATACH**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indica che, in modalità transazione, un file temporanei temporanei viene in genere usato per salvare le modifiche fino a quando non viene chiamato il metodo **Commit.** Se si **specifica STGM \_ NOSGMCH,** la parte inutilizzata del file originale può essere usata come spazio di lavoro anziché creare un nuovo file a tale scopo. Ciò non influisce sui dati nel file originale e in alcuni casi può comportare un miglioramento delle prestazioni. Non è valido specificare questo flag senza specificare **anche STGM \_ TRANSACTED** e questo flag può essere usato solo in un'apertura radice. Per altre informazioni sulla modalità NoS standby, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOSNAPSHOT**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Questo flag viene usato quando si apre un oggetto di archiviazione con **STGM \_ TRANSACTED** e senza **STGM \_ SHARE \_ EXCLUSIVE** o **STGM \_ SHARE DENY \_ \_ WRITE.** In questo caso, specificando **STGM \_ NOSNAPSHOT** si impedisce all'implementazione fornita dal sistema di creare una copia snapshot del file. Le modifiche apportate al file vengono invece scritte alla fine del file. Lo spazio inutilizzato non viene recuperato a meno che non venga eseguito il consolidamento durante il commit e nel file non sia presente un solo writer corrente. Quando il file viene aperto in modalità senza snapshot, non è possibile eseguire un'altra operazione di apertura senza specificare **STGM \_ NOSNAPSHOT.** Questo flag può essere usato solo in un'operazione di apertura radice. Per altre informazioni sulla modalità NoSnapshot, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ SIMPLE**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Fornisce un'implementazione più rapida di un file composto in un caso limitato, ma usato di frequente. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM \_ DIRECT \_ SWMR**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Supporta la modalità diretta per operazioni su file con scrittura singola e multireader. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM \_ DELETEONRELEASE**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indica che il file sottostante deve essere eliminato automaticamente quando viene rilasciato l'oggetto di archiviazione radice. Questa funzionalità è particolarmente utile per la creazione di file temporanei. Questo flag può essere usato solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) Non è valido quando si apre un oggetto radice, ad esempio con [**StgOpenStorageEx,**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)o quando si crea o si apre un sottoelemento, ad esempio con [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Non è inoltre valido usare questo flag e il flag STGM \_ CONVERT contemporaneamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile combinare questi flag, ma è possibile scegliere un solo flag da ogni gruppo di flag correlati. In genere è necessario specificare un flag da ognuno dei gruppi di accesso e di condivisione per tutte le funzioni e i metodi che usano queste costanti. I flag di altri gruppi sono facoltativi.

### <a name="transacted-mode"></a>Modalità transazione

Quando si specifica il flag **STGM \_ DIRECT,** solo una delle seguenti combinazioni di flag può essere specificata dai gruppi di accesso e condivisione.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Tenere presente che la modalità diretta è implicita nell'assenza di **STGM \_ TRANSACTED.** In altre parole, se non si **specifica NÉ STGM \_ DIRECT** né **STGM \_ TRANSACTED,** viene **presupposto STGM \_ DIRECT.**

Quando viene specificato il flag **\_ STGM TRANSACTED,** gli oggetti vengono creati o aperti in modalità transazione. In questa modalità, le modifiche apportate a un oggetto non vengono mantenute fino a quando non ne viene eseguito il commit. Ad esempio, le modifiche apportate a un oggetto di archiviazione transazione non vengono rese persistenti fino a quando non viene chiamato il metodo [**IStorage::Commit.**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) Le modifiche apportate a un oggetto di archiviazione di questo tipo andranno perse se l'oggetto di archiviazione viene rilasciato (versione finale) prima della chiamata al metodo **Commit** o se viene chiamato il metodo [**IStorage::Revert.**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)

Quando un oggetto viene creato o aperto in modalità transazione, l'implementazione deve mantenere sia i dati originali che gli aggiornamenti ai dati, in modo che gli aggiornamenti possano essere ripristinati se necessario. Questa operazione viene in genere eseguita scrivendo le modifiche in un'area scratch fino a quando non ne viene eseguito il commit o creando una copia, denominata snapshot, dei dati di cui è stato eseguito il commit più di recente.

Quando un oggetto di archiviazione radice viene aperto in modalità transazione, è possibile controllare il percorso e il comportamento dei dati dei file scratch e delle copie snapshot per ottimizzare le prestazioni con i flag **STGM \_ NOSNAPCH** e **STGM \_ NOSNAPSHOT.** Un oggetto di archiviazione radice viene ottenuto, ad esempio, dalla funzione [**StgOpenStorageEx.**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) Un oggetto di archiviazione ottenuto dal metodo [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) è un oggetto substorage. In genere, i dati temporanei e gli snapshot vengono archiviati in file temporanei, separati dall'archiviazione.

L'effetto di questi flag dipende dal numero di lettori e/o writer che accedono all'archiviazione radice.

Nel caso di un "writer singolo", viene aperto un oggetto di archiviazione in modalità transazione per l'accesso in scrittura e non possono essere presenti altri accessi al file. In altre parole, il file viene aperto con **STGM \_ TRANSACTED,** l'accesso di **STGM \_ WRITE** o **STGM \_ READWRITE** e la condivisione di **STGM \_ SHARE \_ EXCLUSIVE.** In questo caso, le modifiche apportate all'oggetto di archiviazione vengono scritte nell'area scratch. Quando viene eseguito il commit di tali modifiche, queste vengono copiate nella memoria originale. Pertanto, se non vengono apportate modifiche all'oggetto di archiviazione, non verrà effettuato alcun trasferimento dei dati non necessario.

Nel caso di "più writer", un oggetto di archiviazione transazionale viene aperto per l'accesso in scrittura, ma viene condiviso in , ad esempio per consentire altri writer. In altre parole, l'oggetto di archiviazione viene aperto con **STGM \_ TRANSACTED,** l'accesso di **STGM \_ WRITE** o **STGM \_ READWRITE** e la condivisione di **STGM \_ SHARE DENY \_ \_ READ**. Se invece viene **specificata la condivisione di STGM SHARE DENY \_ \_ \_ NONE,** il caso è "multiple-writer, multiple-reader". In questi casi, durante l'operazione di apertura verrà creato uno snapshot dei dati originali. Pertanto, anche se non viene effettivamente apportata alcuna modifica all'archiviazione e/o non viene effettivamente aperta contemporaneamente da un altro writer, il trasferimento dei dati è comunque necessario durante l'apertura. Di conseguenza, è possibile ottenere le migliori prestazioni in fase di apertura aprendo l'oggetto di archiviazione in modalità **STGM \_ SHARE DENY \_ \_ WRITE** o **STGM SHARE \_ \_ EXCLUSIVE.** Per altre informazioni sul commit delle modifiche quando sono presenti più writer, vedere [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

Nel caso di "writer singolo e lettore multiplo", un oggetto di archiviazione transazionato viene aperto per l'accesso in scrittura, ma condiviso con i lettori. In altre parole, l'oggetto di archiviazione viene aperto dal writer con **STGM \_ TRANSACTED,** l'accesso a **STGM \_ READWRITE** o **STGM \_ WRITE** e la condivisione di **STGM \_ SHARE DENY \_ \_ WRITE.** L'archiviazione viene aperta dai lettori con **STGM \_ TRANSACTED,** l'accesso di **STGM \_ READ** e la condivisione di **STGM \_ SHARE DENY \_ \_ NONE.** In questo caso il writer usa l'area scratch per archiviare le modifiche di cui non è stato eseguito ilcommitted. Come nei casi precedenti, il lettore comporta una perdita di prestazioni in fase di apertura durante la creazione di una copia snapshot dei dati.

In genere, l'area scratch è un file temporaneo, separato dai dati originali. Quando viene eseguito il commit delle modifiche nel file originale, i dati devono essere trasferiti dal file temporaneo. Per evitare questo trasferimento dei dati, è possibile che venga specificato il flag **STGM \_ NOSGMCH.** Quando si specifica questo flag, vengono usate parti del file oggetto di archiviazione per l'area scratch, anziché un file temporaneo separato. Di conseguenza, il commit delle modifiche può essere eseguito rapidamente, perché è necessario un piccolo trasferimento dei dati. Lo svantaggio è che il file di archiviazione può diventare più grande di quanto sarebbe altrimenti, perché deve essere aumentato in modo da essere sufficientemente grande sia per i dati originali che per l'area scratch. Per consolidare i dati e rimuovere questa area non necessaria, riaprire l'archiviazione radice in modalità transazione, ma senza impostare il flag **\_ STGM NOSCRATCH.** Chiamare quindi [**IStorage::Commit con**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) il flag **STGC \_ CONSOLIDATE** impostato.

Anche l'area dello snapshot, come l'area scratch, è in genere un file temporaneo e anche questo può essere interessato da un flag STGM. Specificando il flag **STGM \_ NOSNAPSHOT,** non viene creato un file di snapshot temporaneo separato. Al contrario, i dati originali non vengono mai modificati, anche se sono presenti uno o più writer per oggetto. Quando viene eseguito il commit delle modifiche, vengono aggiunte al file, ma i dati originali rimangono invariati. Questa modalità aumenta l'efficienza perché riduce il tempo di esecuzione eliminando la necessità di creare uno snapshot durante l'operazione di apertura. Tuttavia, l'uso di questa modalità può comportare un file di archiviazione molto grande perché i dati nel file non possono mai essere sovrascritti. Non si tratta di un limite alle dimensioni dei file aperti in modalità NoSnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Direct Single-Writer, Multiple-Reader Mode

Come descritto, è possibile avere un solo writer e più lettori di un oggetto di archiviazione, se tale oggetto viene aperto in modalità transazione. È anche possibile ottenere il case multireader a scrittura singola in modalità diretta, specificando il flag **\_ STGM DIRECT \_ SWMR.**

In **modalità \_ STGM DIRECT \_ SWMR** un chiamante può aprire un oggetto per l'accesso in lettura/scrittura, mentre altri chiamanti hanno contemporaneamente il file aperto per l'accesso in sola lettura. Non è valido usare questo flag in combinazione con il flag **STGM \_ TRANSACTED.** In questa modalità, il writer apre l'oggetto con i flag seguenti:

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ READWRITE** \| **STGM \_ SHARE \_ DENYWRITE**

e ognuno dei lettori apre l'oggetto con questi flag:

**STGM \_ DIRECT \_ SWMR** \| **STGM \_ READ** \| **STGM \_ SHARE DENY \_ \_ NONE**

In questa modalità, per modificare l'oggetto di archiviazione, il writer deve ottenere l'accesso esclusivo all'oggetto. Ciò è possibile quando tutti i lettori lo hanno chiuso. Il writer usa [**l'interfaccia IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) per ottenere questo accesso esclusivo.

### <a name="simple-mode"></a>Modalità semplice

La modalità semplice (**STGM \_ SIMPLE**) è utile per le applicazioni che eseguono operazioni di salvataggio complete. È efficiente, ma ha i vincoli seguenti:

-   Non esiste alcun supporto per le sottocartelle.
-   Non è possibile effettuare il marshalling dell'oggetto di archiviazione e degli oggetti di flusso ottenuti da esso.
-   Ogni flusso ha dimensioni minime. Se al momento del rilascio del flusso vengono scritti meno byte minimi in un flusso, il flusso viene esteso alle dimensioni minime. Ad esempio, le dimensioni minime per una particolare implementazione [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) sono di 4 KB. Viene creato un flusso e vi vengono scritti 1 KB. Alla versione finale di **IStream,** le dimensioni del flusso verranno estese automaticamente a 4 KB. Successivamente, l'apertura del flusso e la chiamata al metodo [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) mostreranno una dimensione di 4 KB.
-   Non tutti i metodi [**di IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) saranno supportati dall'implementazione. Per altre informazioni, vedere [IStorage - Compound File Implementation](istorage-compound-file-implementation.md)e [IStream - Compound File Implementation](istream-compound-file-implementation.md).

[Il marshalling](/windows/desktop/Midl/marshaling-ole-data-types) è il processo di creazione di pacchetti, decompressione e invio di parametri del metodo di interfaccia attraverso i limiti del thread o del processo all'interno di una chiamata di procedura remota (RPC). Per altre informazioni, vedere [Dettagli del marshalling e](../com/marshaling-details.md) [Marshalling dell'interfaccia](../com/interface-marshaling.md).

Quando un oggetto di archiviazione viene ottenuto da un'operazione di creazione in modalità semplice:

-   Gli elementi di flusso possono essere creati, ma non aperti.
-   Quando un elemento di flusso viene creato chiamando [**IStorage::CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)non è possibile creare un altro flusso fino al rilascio dell'oggetto flusso.
-   Dopo aver scritto tutti i flussi, chiamare [**IStorage::Commit per**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) scaricare le modifiche.

Quando un oggetto di archiviazione viene ottenuto da un'operazione Open in modalità semplice:

-   È possibile aprire un solo elemento di flusso alla volta.
-   Non è possibile modificare le dimensioni di un flusso chiamando il metodo [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) o cercando o scrivendo oltre la fine del flusso. Tuttavia, poiché tutti i flussi hanno dimensioni minime, è possibile usare il flusso fino a tale dimensione, anche se in origine sono stati scritti meno dati. Per determinare le dimensioni di un flusso, usare il [**metodo IStream::Stat.**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)

Tenere presente che, se un elemento di archiviazione viene modificato da un oggetto di archiviazione che non è in modalità semplice, non sarà possibile aprire nuovamente tale elemento di archiviazione in modalità semplice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ObjBase.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**Istorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[**StgOpenStorageOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

