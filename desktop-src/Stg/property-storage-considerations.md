---
title: Considerazioni sulla Archiviazione proprietà
description: IPropertyStorage ReadMultiple legge tutte le proprietà specificate nella matrice rgpspec, come si trovano nel set di proprietà.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 128c5da70ae08c62660e0177187036fddee6ff27ed1d9971b6f95dea7052ecdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662161"
---
# <a name="property-storage-considerations"></a>Considerazioni sulla Archiviazione proprietà

[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) legge tutte le proprietà specificate nella matrice *rgpspec,* come si trovano nel set di proprietà. Finché viene letta una delle proprietà richieste, una richiesta di recupero di una proprietà che non esiste non è un errore. Questa operazione deve invece determinare la scrittura di VT EMPTY per \_ tale proprietà nella matrice *rgvar* \[ \] in caso di restituzione. Quando nessuna delle proprietà richieste esiste, il metodo deve restituire S FALSE e impostare \_ VT \_ EMPTY in ogni [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Se viene restituito un altro errore, non vengono recuperati valori di proprietà e il chiamante non deve preoccuparsi di rilasciarli.

Il *parametro rgpspec* è una matrice di [**strutture PROPSPEC,**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) che specificano per ogni proprietà l'identificatore di proprietà o, se ne viene assegnato uno, un identificatore di stringa. È possibile eseguire il mapping di una stringa a un identificatore di proprietà chiamando [**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). L'uso degli identificatori di proprietà è tuttavia probabilmente significativamente più efficiente rispetto all'uso di stringhe.

Le proprietà richieste dal nome di stringa (PRSPEC LPWSTR) vengono mappate senza distinzione tra maiuscole e minuscole agli identificatori di proprietà (ID) specificati nel set di proprietà corrente (e in base alle impostazioni locali correnti \_ del sistema).

Quando il tipo di proprietà è VT LPSTR e la proprietà viene letta da un set di proprietà ANSI, vale a dire che la tabella codici per il set di proprietà è impostata su un valore diverso da Unicode, il valore della proprietà usa la stessa tabella codici del set di \_ proprietà. Quando una proprietà LPSTR VT viene letta da un set di proprietà Unicode, il valore della proprietà usa la tabella codici ANSI predefinita corrente del sistema, cio' la tabella codici restituita dalla \_ **funzione GetACP.**

Un [**PROPVARIANT,**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)ad eccezione di quelli che sono puntatori a flussi e archivi, è detto **PROPVARIANT semplice.** Questi **oggetti PROPVARIANT** semplici ricevono i dati in base al valore, quindi una chiamata a [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) fornisce una copia dei dati di cui il chiamante è quindi proprietario. Per creare o aggiornare queste proprietà, chiamare [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

Al contrario, i tipi variant VT \_ STREAM, VT \_ STREAMED \_ OBJECT, VT STORAGE e VT STORED OBJECT sono proprietà \_ \_ non semplici, perché anziché fornire un \_ valore, il metodo recupera un puntatore all'interfaccia indicata, da cui è possibile leggere i dati. Questi tipi consentono l'archiviazione di grandi quantità di informazioni tramite una singola proprietà. Esistono diversi problemi che si verificano nell'uso di proprietà nonsimple.

Per creare queste proprietà, come per le altre proprietà, chiamare [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Invece di chiamare lo stesso metodo per aggiornare, tuttavia, è più efficiente chiamare [**prima IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) per ottenere il puntatore a interfaccia al flusso o all'archiviazione, quindi scrivere dati usando i metodi [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Un flusso o un'archiviazione aperta tramite una proprietà viene sempre aperta in modalità diretta, quindi non viene introdotto un livello aggiuntivo di transazione annidata. Tuttavia, potrebbe essere ancora presente una transazione sull'intero set di proprietà, a seconda di come è stata aperta o creata tramite [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). Inoltre, i tag di accesso e modalità di condivisione specificati quando il set di proprietà viene aperto o creato, vengono passati a flussi o archivi basati su proprietà.

Le durate dei puntatori di flusso o di archiviazione basati su proprietà, anche se teoricamente indipendenti dai puntatori [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) associati, dipendono effettivamente da essi. I dati visibili tramite il flusso o l'archiviazione sono correlati alla transazione nell'oggetto di archiviazione delle proprietà da cui vengono recuperati, proprio come per un oggetto di archiviazione (che supporta [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) con sottoo object di flusso e archiviazione contenuti. Se la transazione nell'oggetto padre viene interrotta, i puntatori [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStorage** esistenti subordinati a tale oggetto non sono più accessibili. Poiché **IPropertyStorage è** l'unica interfaccia nell'oggetto di archiviazione delle proprietà, la durata utile dei puntatori **IStream** e **IStorage** contenuti è vincolata dalla durata dell'interfaccia **IPropertyStorage.**

L'implementazione deve anche gestire la situazione in cui la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite la stessa istanza dell'interfaccia [**IPropertyStorage.**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Ad esempio, nell'implementazione del file composto COM, l'apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta o meno.

Un altro problema riguarda l'apertura multipla in modalità transazione. Il risultato dipende dal livello di isolamento specificato tramite una chiamata ai metodi [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) (metodo [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) o [**Create,**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) tramite i flag STGM) al momento dell'apertura dell'archiviazione delle proprietà.

Se la chiamata per aprire il set di proprietà specifica l'accesso in lettura/scrittura, le proprietà con valori [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)vengono sempre aperte con accesso in lettura/scrittura. I dati possono quindi essere scritti tramite queste interfacce, modificando il valore della proprietà , che è il modo più efficiente per aggiornare queste proprietà. Il valore della proprietà stesso non ha un livello aggiuntivo di annidamento delle transazioni, pertanto le modifiche sono nell'ambito della transazione (se presente) nell'oggetto di archiviazione delle proprietà.

## <a name="storage-and-stream-properties"></a>proprietà Archiviazione e stream

Per scrivere un flusso o un oggetto di archiviazione in un set di proprietà, è necessario che il set di proprietà sia stato creato come non semplice. Per altre informazioni sui set di proprietà semplici e non semplici, vedere la sezione Archiviazione [e Oggetti di](storage-vs--stream-for-a-property-set.md)flusso per un set di proprietà . I tipi di proprietà seguenti, come specificato nel campo *vt* degli elementi della matrice *rgvar,* sono tipi di flusso o di archiviazione: \_ VT STREAM, VT \_ STORAGE, VT \_ STREAMED \_ OBJECT, VT \_ STORED \_ OBJECT.

Per scrivere un flusso o un oggetto di archiviazione come proprietà in un set di proprietà non semplice, chiamare [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Anche se si chiama questo metodo per aggiornare proprietà semplici, non è un modo efficiente per aggiornare gli oggetti di flusso e di archiviazione in un set di proprietà. Questo perché l'aggiornamento di una di queste proprietà tramite una chiamata a **WriteMultiple** crea nell'oggetto di archiviazione delle proprietà una copia dei dati passati e i puntatori [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non vengono mantenuti oltre la durata di questa chiamata. In genere è più efficiente aggiornare direttamente gli oggetti di flusso o di archiviazione chiamando [**prima IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) per ottenere il puntatore di interfaccia al flusso o all'archiviazione, quindi scrivendo i dati tramite i metodi **IStream** o **IStorage.**

Ad esempio, è possibile chiamare [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) per scrivere un flusso **NULL** o un oggetto di archiviazione. L'implementazione creerà quindi un oggetto vuoto nel set di proprietà. È quindi possibile ottenere l'accesso a questo oggetto chiamando [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Dopo aver completato l'aggiornamento di questo oggetto, non è necessario scriverlo nel set di proprietà, perché gli aggiornamenti venivano evasi direttamente nel set di proprietà.

Un flusso o un'archiviazione aperta tramite una proprietà viene sempre aperta in modalità diretta, quindi non viene introdotto un livello aggiuntivo di transazione annidata. Potrebbe essere ancora presente una transazione nell'intero set di proprietà. Ad esempio, se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) è stato ottenuto chiamando [**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) con STGM \_ Flag TRANSACTED impostato nel *parametro grfmode.* Inoltre, un flusso o un archivio basato su proprietà viene aperto in modalità di lettura/scrittura, se possibile, data la modalità nel set di proprietà; In caso contrario, viene usata la modalità di lettura.

Come accennato in precedenza, quando un flusso o un oggetto di archiviazione viene scritto in un set di proprietà con il [**metodo WriteMultiple,**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) viene creata una copia dell'oggetto. Quando viene eseguita una copia di questo tipo su un oggetto flusso, l'operazione di copia inizia in corrispondenza della posizione di ricerca corrente dell'origine. La posizione di ricerca non è definita in caso di errore, ma in caso di esito positivo si trova alla fine del flusso. Il puntatore seek non viene ripristinato nella posizione originale.

Se un flusso o una proprietà di archiviazione è stata letta da un set di proprietà con [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), viene ancora mantenuto aperto e viene eseguita una chiamata successiva a [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) per la stessa proprietà, l'operazione **WriteMultiple** avrà esito positivo. Il flusso o la proprietà di archiviazione aperta in precedenza viene inserita nello stato ripristinato (tutte le chiamate a restituiranno l'errore STG \_ E \_ REVERTED).

Se il [**metodo WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) restituisce un errore durante la scrittura di una matrice di proprietà o anche di singole proprietà non semplici, la quantità di dati effettivamente scritti non è definita.

## <a name="reference-properties"></a>Proprietà riferimento

Se una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) specificata include il flag VT BYREF nel relativo membro \_ **vt,** la proprietà associata è una proprietà di riferimento. Una proprietà di riferimento viene automaticamente dereferenziata prima di scrivere il valore nel set di proprietà. Ad esempio, se il membro **vt** della struttura **PROPVARIANT** specifica un valore di tipo VT BYREF VT I4, il valore effettivo scritto è un \_ \| tipo \_ VT \_ I4. Una chiamata successiva al [**metodo IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) restituisce un valore come VT \_ I4. L'uso delle proprietà di riferimento è simile alla chiamata [della funzione VariantCopyInd.](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libera la variante di destinazione e crea una copia dell'origine VARIANTARG, eseguendo il riferimento indiretto necessario se l'origine è specificata come VT \_ BYREF. Questa funzione è utile quando è necessaria una copia di una variante e per garantire che non sia VT BYREF, ad esempio quando si gestisce gli argomenti in un'implementazione di \_ [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Note per i chiamanti

È consigliabile creare set di proprietà come Unicode, non impostando il flag ANSI PROPSETFLAG nel parametro \_ *grfFlags* di [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). È anche consigliabile evitare l'uso di valori VT LPSTR e usare invece i \_ valori \_ VT LPWSTR. Quando la tabella codici del set di proprietà è Unicode, i valori di stringa VT LPSTR vengono convertiti in Unicode quando vengono archiviati e di nuovo in \_ valori stringa multibyte quando vengono recuperati. Quando la tabella codici del set di proprietà non è Unicode, i nomi delle proprietà, le stringhe BSTR VT e i valori delle proprietà non semplici vengono convertiti in stringhe multibyte quando vengono archiviati e convertiti nuovamente in Unicode quando vengono recuperati, usando la tabella codici ANSI di \_ sistema corrente.

## <a name="notes-to-implementers"></a>Note per gli implementatori

Quando si alloca un identificatore di proprietà, l'implementazione può scegliere qualsiasi valore attualmente non in uso nel set di proprietà per un identificatore di proprietà, purché non sia 0 o 1 o maggiore di 0x80000000, tutti valori riservati. Il *parametro propidNameFirst* stabilisce un valore minimo per gli identificatori di proprietà all'interno del set e deve essere maggiore di 1 e minore di 0x80000000. Vedere la sezione Osservazioni precedente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione di file compositi IPropertyStorage](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[Implementazione del file system IPropertyStorage-NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[Implementazione autonoma di IPropertyStorage](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 