---
title: Costanti STGM (ObjBase. h)
description: Flag che indicano le condizioni per la creazione e l'eliminazione di oggetti e modalità di accesso per l'oggetto.
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
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475479"
---
# <a name="stgm-constants"></a>Costanti STGM

Le costanti STGM sono flag che indicano le condizioni per la creazione e l'eliminazione di oggetti e modalità di accesso per l'oggetto. Le costanti STGM sono incluse nelle interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e nelle funzioni [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**, StgCreateDocfileOnILockBytes,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .

Questi elementi vengono spesso combinati usando un operatore **or**. Sono interpretati in gruppi, come indicato nella tabella seguente. Non è possibile usare più di un elemento di un singolo gruppo.

Usare un flag dal gruppo di creazione quando si crea un oggetto, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).

Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.



| Group                      | Flag                         | valore       |
|----------------------------|------------------------------|-------------|
| Access                     | **STGM di \_ lettura**               | 0x00000000L |
|                            | **\_scrittura STGM**              | 0x00000001L |
|                            | **\_ReadWrite STGM**          | 0x00000002L |
| Condivisione                    | **STGM \_ condivisione \_ Nega \_ Nessuna**  | 0x00000040L |
|                            | **STGM \_ condivisione \_ Nega \_ lettura**  | 0x00000030L |
|                            | **STGM \_ condivisione \_ Nega \_ scrittura** | 0x00000020L |
|                            | **STGM \_ condivisione \_ esclusiva**   | 0x00000010L |
|                            | **\_priorità STGM**           | 0x00040000L |
| Creazione                   | **creazione di STGM \_**             | 0x00001000L |
|                            | **STGM \_ convertire**            | 0x00020000L |
|                            | **\_FAILIFTHERE STGM**        | 0x00000000L |
| Transazione             | **STGM \_ Direct**             | 0x00000000L |
|                            | **STGM \_ transazionale**         | 0x00010000L |
| Prestazioni delle transazioni | **STGM \_ NOscratch**          | 0x00100000L |
|                            | **STGM \_ NOsnapshot**         | 0x00200000L |
| SWMR diretto e semplice     | **STGM \_ semplice**             | 0x08000000L |
|                            | **\_SWMR diretto \_ STGM**       | 0x00400000L |
| Elimina al rilascio          | **\_DELETEONRELEASE STGM**    | 0x04000000L |



 

<dl> <dt>

<span id="STGM_READ"></span><span id="stgm_read"></span>**STGM di \_ lettura**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica che l'oggetto è di sola lettura, pertanto non è possibile apportare modifiche. Se, ad esempio, un oggetto flusso viene aperto con **STGM \_ Read**, il metodo [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) può essere chiamato, ma il metodo [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) non può essere. Analogamente, se si apre un oggetto di archiviazione con **STGM \_ Read**, è possibile chiamare i metodi [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) e [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , ma i metodi [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) non possono essere.


</dt> </dl> </dd> <dt>

<span id="STGM_WRITE"></span><span id="stgm_write"></span>**\_scrittura STGM**
</dt> <dd> <dl> <dt>

0x00000001L
</dt> <dt>



Consente di salvare le modifiche apportate all'oggetto, ma non di consentire l'accesso ai relativi dati. Le implementazioni fornite delle interfacce [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) non supportano questa modalità di sola scrittura.


</dt> </dl> </dd> <dt>

<span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**\_ReadWrite STGM**
</dt> <dd> <dl> <dt>

0x00000002L
</dt> <dt>



Consente l'accesso e la modifica dei dati degli oggetti. Se, ad esempio, un oggetto flusso viene creato o aperto in questa modalità, è possibile chiamare sia [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) che **IStream:: Write**. Tenere presente che questa costante non è una semplice operazione binaria **o** con gli elementi **\_ Read** di **STGM \_ Write** e STGM.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ condivisione \_ Nega \_ Nessuna**
</dt> <dd> <dl> <dt>

0x00000040L
</dt> <dt>



Specifica che le aperture successive dell'oggetto non sono negate per l'accesso in lettura o in scrittura. Se non viene specificato alcun flag dal gruppo di condivisione, viene utilizzato questo flag.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ condivisione \_ Nega \_ lettura**
</dt> <dd> <dl> <dt>

0x00000030L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto in modalità di **\_ lettura STGM** . Viene in genere usato in un oggetto di archiviazione radice.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ condivisione \_ Nega \_ scrittura**
</dt> <dd> <dl> <dt>

0x00000020L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto per l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** . In modalità transazionale, la condivisione della condivisione **STGM \_ \_ Deny \_ Write** o **STGM \_ share \_ Exclusive** può migliorare significativamente le prestazioni, in quanto non richiedono snapshot. Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ condivisione \_ esclusiva**
</dt> <dd> <dl> <dt>

0x00000010L
</dt> <dt>



Impedisce ad altri utenti di aprire successivamente l'oggetto in qualsiasi modalità. Tenere presente che questo valore non è una **semplice operazione or** bit per bit della **\_ condivisione STGM \_ Deny \_ Read** e **STGM \_ share \_ Deny \_ Write** values. In modalità transazionale, la condivisione della condivisione **STGM \_ \_ Deny \_ Write** o **STGM \_ share \_ Exclusive** può migliorare significativamente le prestazioni, in quanto non richiedono snapshot. Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_priorità STGM**
</dt> <dd> <dl> <dt>

0x00040000L
</dt> <dt>



Apre l'oggetto di archiviazione con accesso esclusivo alla versione di cui è stato eseguito il commit più di recente. Di conseguenza, gli altri utenti non possono eseguire il commit delle modifiche all'oggetto mentre è aperto in modalità di priorità. Si ottengono vantaggi in termini di prestazioni per le operazioni di copia, ma si impedisce ad altri utenti di eseguire il commit delle modifiche. Limitare il tempo in cui gli oggetti vengono aperti in modalità di priorità. È necessario specificare **STGM \_ Direct** e **STGM \_ Read** con la modalità Priority e non è possibile specificare **STGM \_ DELETEONRELEASE**. **STGM \_ DELETEONRELEASE** è valido solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Non è valido quando si apre un oggetto radice esistente, ad esempio con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex). Non è inoltre valido quando si crea o si apre un sottoelemento, ad esempio con [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).


</dt> </dl> </dd> <dt>

<span id="STGM_CREATE"></span><span id="stgm_create"></span>**creazione di STGM \_**
</dt> <dd> <dl> <dt>

0x00001000L
</dt> <dt>



Indica che un oggetto o un flusso di archiviazione esistente deve essere rimosso prima che il nuovo oggetto lo sostituisca. Quando questo flag viene specificato solo se l'oggetto esistente è stato rimosso correttamente, viene creato un nuovo oggetto.

Questo flag viene usato durante il tentativo di creazione:

-   Un oggetto di archiviazione su un disco, ma esiste un file con lo stesso nome.
-   Oggetto all'interno di un oggetto di archiviazione, ma esiste un oggetto con il nome specificato.
-   Un oggetto matrice di byte, ma ne esiste uno con il nome specificato.

Questo flag non può essere usato con le operazioni aperte, ad esempio [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).


</dt> </dl> </dd> <dt>

<span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertire**
</dt> <dd> <dl> <dt>

0x00020000L
</dt> <dt>



Crea il nuovo oggetto conservando i dati esistenti in un flusso denominato "Contents". Nel caso di un oggetto di archiviazione o di una matrice di byte, i dati obsoleti vengono formattati in un flusso, indipendentemente dal fatto che la matrice di byte o il file esistente contenga attualmente un oggetto di archiviazione a più livelli. Questo flag può essere utilizzato solo quando si crea un oggetto di archiviazione radice. Non può essere usato in un oggetto di archiviazione. ad esempio, in [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Non è inoltre valido utilizzare questo flag e il flag **STGM \_ DELETEONRELEASE** simultaneamente.


</dt> </dl> </dd> <dt>

<span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**\_FAILIFTHERE STGM**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Causa l'esito negativo dell'operazione di creazione se è presente un oggetto esistente con il nome specificato. In questo caso, viene restituito **STG \_ E \_ FILEALREADYEXISTS** . Questa è la modalità di creazione predefinita; ovvero, se non viene specificato nessun altro flag di creazione, **STGM \_ FAILIFTHERE** è implicito.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ Direct**
</dt> <dd> <dl> <dt>

0x00000000L
</dt> <dt>



Indica che, in modalità diretta, ogni modifica apportata a un elemento di archiviazione o flusso viene scritta quando si verifica. Si tratta dell'impostazione predefinita se non viene specificato né **STGM \_ Direct** né **STGM \_ transazionale** .


</dt> </dl> </dd> <dt>

<span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transazionale**
</dt> <dd> <dl> <dt>

0x00010000L
</dt> <dt>



Indica che, in modalità transazionale, le modifiche vengono memorizzate nel buffer e scritte solo se viene chiamata un'operazione di commit esplicita. Per ignorare le modifiche, chiamare il metodo [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) nell'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . L'implementazione del file composto COM di **IStorage** non supporta i flussi transazionali, il che significa che i flussi possono essere aperti solo in modalità diretta e non è possibile ripristinare le modifiche, tuttavia sono supportate le archiviazioni transazionali. Le implementazioni di file composto, autonome e file system NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in modo analogo non supportano i set di proprietà semplici e sottoposti a transazione, perché questi set di proprietà sono archiviati nei flussi. Tuttavia, sono supportate le transazioni di set di proprietà non semplici, che possono essere creati specificando il flag **PROPSETFLAG non \_ semplice** nel parametro *grfFlags* di [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).


</dt> </dl> </dd> <dt>

<span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOscratch**
</dt> <dd> <dl> <dt>

0x00100000L
</dt> <dt>



Indica che, in modalità transazionale, viene in genere utilizzato un file temporaneo temporaneo per salvare le modifiche fino a quando non viene chiamato il metodo **commit** . La specifica di **STGM \_ noscratch** consente di usare come spazio di lavoro la parte inutilizzata del file originale anziché creare un nuovo file a tale scopo. Questa operazione non influisce sui dati nel file originale e in alcuni casi può comportare un miglioramento delle prestazioni. Non è consentito specificare questo flag senza specificare anche **STGM \_ transazionale** e questo flag può essere utilizzato solo in una radice aperta. Per ulteriori informazioni sulla modalità noscratch, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**
</dt> <dd> <dl> <dt>

0x00200000L
</dt> <dt>



Questo flag viene usato per l'apertura di un oggetto di archiviazione con **STGM \_ transazionale** e senza **STGM \_ share \_ Exclusive** o **STGM \_ share \_ Deny \_ Write**. In questo caso, se si specifica **STGM \_ nosnapshot** si impedisce all'implementazione fornita dal sistema di creare una copia snapshot del file. Al contrario, le modifiche apportate al file vengono scritte alla fine del file. Lo spazio inutilizzato non viene recuperato a meno che non venga eseguito il consolidamento durante il commit ed è presente un solo writer corrente sul file. Quando il file viene aperto in modalità senza snapshot, non è possibile eseguire un'altra operazione di apertura senza specificare **STGM \_ nosnapshot**. Questo flag può essere utilizzato solo in un'operazione di apertura radice. Per ulteriori informazioni sulla modalità nosnapshot, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ semplice**
</dt> <dd> <dl> <dt>

0x08000000L
</dt> <dt>



Fornisce un'implementazione più veloce di un file composto in un caso limitato, ma di uso frequente. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**\_SWMR diretto \_ STGM**
</dt> <dd> <dl> <dt>

0x00400000L
</dt> <dt>



Supporta la modalità diretta per le operazioni su file a writer singolo e Multireader. Per altre informazioni, vedere la sezione Osservazioni.


</dt> </dl> </dd> <dt>

<span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**\_DELETEONRELEASE STGM**
</dt> <dd> <dl> <dt>

0x04000000L
</dt> <dt>



Indica che il file sottostante deve essere eliminato automaticamente quando viene rilasciato l'oggetto di archiviazione radice. Questa funzionalità è particolarmente utile per la creazione di file temporanei. Questo flag può essere utilizzato solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Non è valido quando si apre un oggetto radice, ad esempio con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), o quando si crea o si apre un sottoelemento, ad esempio con [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream). Non è inoltre valido utilizzare questo flag e il \_ flag di conversione STGM simultaneamente.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile combinare questi flag, ma è possibile scegliere solo un flag da ogni gruppo di flag correlati. In genere, è necessario specificare un flag da ognuno dei gruppi di accesso e condivisione per tutte le funzioni e i metodi che usano queste costanti. I flag di altri gruppi sono facoltativi.

### <a name="transacted-mode"></a>Modalità transazionale

Quando viene specificato il flag **\_ diretto STGM**, è possibile specificare solo una delle seguenti combinazioni di flag dai gruppi di accesso e condivisione.

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

Tenere presente che la modalità diretta è implicita in assenza di **STGM \_ transazionale**. Ovvero, se non si specifica né **STGM \_ Direct** né **STGM \_ transazionale** , viene utilizzato **STGM \_ Direct** .

Quando viene specificato il flag **\_ transazionale STGM** , gli oggetti vengono creati o aperti in modalità transazionale. In questa modalità le modifiche apportate a un oggetto non vengono mantenute finché non ne viene eseguito il commit. Ad esempio, le modifiche apportate a un oggetto di archiviazione transazionale non vengono rese permanente fino a quando non viene chiamato il metodo [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) . Le modifiche apportate a tale oggetto di archiviazione andranno perse se l'oggetto di archiviazione viene rilasciato (versione finale) prima della chiamata al metodo **commit** o se viene chiamato il metodo [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) .

Quando un oggetto viene creato o aperto in modalità transazionale, l'implementazione deve tenere i dati originali e gli aggiornamenti a questi dati, in modo che gli aggiornamenti possano essere ripristinati, se necessario. Questa operazione viene in genere eseguita scrivendo modifiche a un'area scratch finché non ne viene eseguito il commit oppure creando una copia, denominata snapshot, dei dati di cui è stato eseguito il commit più di recente.

Quando un oggetto di archiviazione radice viene aperto in modalità transazionale, è possibile controllare la posizione e il comportamento dei dati Scratch e delle copie di snapshot per ottimizzare le prestazioni con i flag **STGM \_ noscratch** e **STGM \_ nosnapshot** . Viene ottenuto un oggetto di archiviazione radice, ad esempio, la funzione [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . un oggetto di archiviazione ottenuto dal metodo [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) è un oggetto di archiviazione. In genere, i dati e gli snapshot vengono archiviati in file temporanei, separati dalla risorsa di archiviazione.

L'effetto di questi flag dipende dal numero di lettori e/o writer che accedono all'archiviazione radice.

Nel caso di un singolo writer, viene aperto un oggetto di archiviazione in modalità transazionale per l'accesso in scrittura e non è possibile accedere al file. Ovvero il file viene aperto con **STGM \_ transazionale**, l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** e la condivisione di **STGM \_ share \_ Exclusive**. In questo caso, le modifiche apportate all'oggetto di archiviazione vengono scritte nell'area scratch. Quando si esegue il commit di tali modifiche, queste vengono copiate nella risorsa di archiviazione originale. Di conseguenza, se non vengono apportate modifiche all'oggetto di archiviazione, non sarà necessario alcun trasferimento di dati.

Nel caso di più writer, viene aperto un oggetto di archiviazione transazionale per l'accesso in scrittura, ma è condiviso in tali asway come per consentire altri writer. Ovvero l'oggetto di archiviazione viene aperto con **STGM \_ transazionale**, l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** e la condivisione della **condivisione \_ STGM \_ Deny \_ Read**. Se invece si specifica la condivisione della condivisione **STGM, \_ \_ negare \_** il valore None, il case è "multi-writer, multiple-Reader". In questi casi, durante l'operazione di apertura verrà eseguito uno snapshot dei dati originali. Pertanto, anche se non viene apportata alcuna modifica all'archiviazione e/o non viene effettivamente aperto da un altro writer contemporaneamente, il trasferimento dei dati è ancora necessario durante l'apertura. Di conseguenza, è possibile ottenere le migliori prestazioni in fase di apertura aprendo l'oggetto di archiviazione **nella \_ condivisione STGM \_ Nega \_ scrittura** o **STGM condividono le modalità \_ \_ esclusive** . Per altre informazioni su come viene eseguito il commit delle modifiche quando sono presenti più writer, vedere [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).

Nel caso di un singolo writer e di più lettori, viene aperto un oggetto di archiviazione transazionale per l'accesso in scrittura, ma condiviso con i lettori. Ovvero, l'oggetto di archiviazione viene aperto dal writer con **STGM \_ transazionale**, accesso a **STGM \_ ReadWrite** o **STGM \_ Write** e condivisione di **STGM \_ share \_ Deny \_ Write**. Lo spazio di archiviazione viene aperto dai lettori con **STGM \_ transazionale**, accesso di **STGM \_ Read** e condivisione di **STGM \_ share \_ Deny \_ None**. In questo caso, il writer usa l'area scratch per archiviare le modifiche di cui non è stato eseguito il commit. Come nei casi precedenti, il lettore comporta una riduzione delle prestazioni in fase di apertura mentre viene creata una copia snapshot dei dati.

In genere, l'area scratch è un file temporaneo, separato dai dati originali. Quando viene eseguito il commit delle modifiche nel file originale, i dati devono essere trasferiti dal file temporaneo. Per evitare questo trasferimento dei dati, è possibile specificare il flag **STGM \_ noscratch**. Quando si specifica questo flag, parti del file oggetto di archiviazione vengono utilizzate per l'area scratch, anziché un file temporaneo separato. Di conseguenza, il commit delle modifiche può essere eseguito rapidamente, perché è necessario un piccolo trasferimento dei dati. Lo svantaggio è che il file di archiviazione può diventare più grande di quanto sarebbe altrimenti, perché deve essere cresciuto per essere sufficientemente grande per i dati originali e per l'area scratch. Per consolidare i dati e rimuovere l'area non necessaria, riaprire l'archiviazione radice in modalità transazionale, ma senza impostare il flag **STGM \_ noscratch** . Quindi, chiamare [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) con il flag di **\_ consolidamento STGC** impostato.

Anche l'area snapshot, come l'area scratch, è in genere un file temporaneo, che può anche essere influenzato da un flag STGM. Specificando il flag **STGM \_ nosnapshot** , non viene creato un file di snapshot temporaneo separato. Al contrario, i dati originali non vengono mai modificati, anche se sono presenti uno o più writer per oggetto. Quando viene eseguito il commit delle modifiche, queste vengono aggiunte al file, ma i dati originali rimangono intatti. Questa modalità aumenta l'efficienza perché riduce il tempo di esecuzione eliminando la necessità di creare uno snapshot durante l'operazione di apertura. Tuttavia, l'uso di questa modalità può causare un file di archiviazione molto grande perché i dati nel file non possono mai essere sovrascritti. Non è previsto alcun limite per le dimensioni dei file aperti in modalità nosnapshot.

### <a name="direct-single-writer-multiple-reader-mode"></a>Single-writer diretto, modalità Multiple-Reader

Come descritto, è possibile avere un solo Writer e più lettori di un oggetto di archiviazione, se tale oggetto viene aperto in modalità transazionale. È anche possibile ottenere il case con singolo writer, Multireader in modalità diretta, specificando il flag **\_ \_ SWMR diretto STGM** .

In **modalità \_ \_ SWMR diretta di STGM** è possibile che un chiamante apra un oggetto per l'accesso in lettura/scrittura, mentre altri chiamanti hanno contemporaneamente il file aperto per l'accesso in sola lettura. Non è consentito utilizzare questo flag in combinazione con il flag **\_ transazionale STGM** . In questa modalità, il writer apre l'oggetto con i flag seguenti:

**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**

e ognuno dei lettori apre l'oggetto con i flag seguenti:

**STGM \_ Direct \_ SWMR** \| **STGM \_ Read** \| **STGM \_ share \_ Deny \_ None**

In questa modalità, per modificare l'oggetto di archiviazione, è necessario che il writer ottenga l'accesso esclusivo all'oggetto. Questa operazione è possibile quando tutti i lettori lo hanno chiuso. Il writer usa l'interfaccia [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) per ottenere l'accesso esclusivo.

### <a name="simple-mode"></a>Modalità semplice

La modalità semplice (**STGM \_ Simple**) è utile per le applicazioni che eseguono operazioni di salvataggio complete. È efficiente, ma presenta i vincoli seguenti:

-   Non esiste alcun supporto per le sottoarchiviazioni.
-   Non è possibile effettuare il marshalling dell'oggetto di archiviazione e degli oggetti di flusso ottenuti da esso.
-   Ogni flusso ha una dimensione minima. Se un numero minore di byte minimi viene scritto in un flusso quando il flusso viene rilasciato, il flusso viene esteso alla dimensione minima. Ad esempio, la dimensione minima per una particolare implementazione di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) è 4 KB. Viene creato un flusso e ne viene scritto 1 KB. Al rilascio finale di tale **IStream**, le dimensioni del flusso verranno estesi automaticamente a 4 KB. Successivamente, l'apertura del flusso e la chiamata del metodo [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) mostreranno una dimensione di 4 KB.
-   Non tutti i metodi di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) saranno supportati dall'implementazione di. Per altre informazioni, vedere [implementazione di file compositi IStorage](istorage-compound-file-implementation.md)e [implementazione di un file composto IStream](istream-compound-file-implementation.md).

Il [marshalling](/windows/desktop/Midl/marshaling-ole-data-types) è il processo di creazione di pacchetti, annullamento del packaging e invio di parametri del metodo di interfaccia attraverso i limiti del thread o del processo all'interno di una chiamata di procedura remota (RPC). Per altre informazioni, vedere [Dettagli di marshalling](../com/marshaling-details.md) e [marshalling dell'interfaccia](../com/interface-marshaling.md).

Quando un oggetto di archiviazione viene ottenuto da un'operazione di creazione in modalità semplice:

-   Gli elementi del flusso possono essere creati, ma non aperti.
-   Quando viene creato un elemento Stream chiamando [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), non è possibile creare un altro flusso fino a quando non viene rilasciato l'oggetto flusso.
-   Dopo la scrittura di tutti i flussi, chiamare [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) per scaricare le modifiche.

Quando un oggetto di archiviazione viene ottenuto da un'operazione di apertura in modalità semplice:

-   È possibile aprire un solo elemento di flusso alla volta.
-   Non è possibile modificare le dimensioni di un flusso chiamando il metodo [**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) oppure cercando o scrivendo oltre la fine del flusso. Tuttavia, poiché tutti i flussi hanno dimensioni minime, è possibile usare il flusso fino a tale dimensione, anche se in origine sono stati scritti meno dati. Per determinare le dimensioni di un flusso, usare il metodo [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .

Tenere presente che, se un elemento di archiviazione viene modificato da un oggetto di archiviazione che non si trova in modalità semplice, non sarà ancora possibile aprire tale elemento di archiviazione in modalità semplice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ObjBase. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
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

 

