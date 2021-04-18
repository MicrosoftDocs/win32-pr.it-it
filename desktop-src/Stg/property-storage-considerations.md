---
title: Considerazioni sull'archiviazione delle proprietà
description: IPropertyStorage ReadMultiple legge il numero di proprietà specificate nella matrice rgpspec come si trova nel set di proprietà.
ms.assetid: 7540966f-a3b2-46c9-9e04-b15133a517eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aad6aabf8b22a7c01f91a090136e6cc8156c791
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299910"
---
# <a name="property-storage-considerations"></a>Considerazioni sull'archiviazione delle proprietà

[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) legge il numero di proprietà specificate nella matrice *rgpspec* come si trova nel set di proprietà. Se una delle proprietà richieste viene letta, una richiesta di recupero di una proprietà che non esiste non è un errore. Al contrario, questo deve causare \_ la scrittura di un VT vuoto per la proprietà nella matrice *rgvar* al \[ \] ritorno. Quando nessuna delle proprietà richieste esiste, il metodo deve restituire S \_ false e impostare VT \_ Empty in ogni [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant). Se viene restituito un altro errore, non viene recuperato alcun valore di proprietà e il chiamante non deve preoccuparsi di rilasciarlo.

Il parametro *rgpspec* è una matrice di strutture [**Campo PROPSPEC**](/windows/win32/api/propidlbase/ns-propidlbase-propspec) che specifica per ogni proprietà l'identificatore di proprietà o, se ne viene assegnato uno, un identificatore di stringa. È possibile eseguire il mapping di una stringa a un identificatore di proprietà chiamando [**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames). L'uso degli identificatori di proprietà è, tuttavia, molto più efficiente rispetto all'uso di stringhe.

Le proprietà richieste da nome stringa (PRSPEC \_ LPWSTR) vengono mappate senza distinzione tra maiuscole e minuscole a identificatori di proprietà (ID), perché sono specificate nel set di proprietà corrente (e in base alle impostazioni locali correnti del sistema).

Quando il tipo di proprietà è VT \_ LPSTR e la proprietà viene letta da un set di proprietà ANSI, ovvero la tabella codici per il set di proprietà è impostata su un valore diverso da Unicode, il valore della proprietà utilizza la stessa tabella codici del set di proprietà. Quando una \_ Proprietà LPSTR di VT viene letta da un set di proprietà Unicode, il valore della proprietà utilizza la tabella codici ANSI predefinita corrente del sistema, ovvero la tabella codici restituita dalla funzione **GetACP** .

Un [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant), ad eccezione di quelli che sono puntatori a flussi e archivi, viene chiamato semplice **PROPVARIANT**. Questi **PROPVARIANT** semplici ricevono i dati per valore, quindi una chiamata a [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) fornisce una copia dei dati di proprietà del chiamante. Per creare o aggiornare queste proprietà, chiamare [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple).

Al contrario, il flusso VT dei tipi Variant \_ , l' \_ \_ oggetto trasmesso tramite VT, l'archiviazione VT \_ e \_ \_ l'oggetto archiviato VT sono proprietà non semplici, perché invece di fornire un valore, il metodo recupera un puntatore all'interfaccia indicata, da cui i dati possono essere letti. Questi tipi consentono l'archiviazione di grandi quantità di informazioni tramite una singola proprietà. Esistono diversi problemi che si verificano nell'utilizzo di proprietà non semplici.

Per creare queste proprietà, come per le altre proprietà, chiamare [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Anziché chiamare lo stesso metodo per aggiornare, tuttavia, è più efficiente chiamare prima [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) per ottenere il puntatore di interfaccia al flusso o all'archiviazione, quindi scrivere i dati usando i metodi [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Un flusso o una risorsa di archiviazione aperta tramite una proprietà viene sempre aperta in modalità diretta, pertanto non è stato introdotto un ulteriore livello di transazione nidificata. Può tuttavia essere comunque una transazione sulla proprietà impostata nel suo complesso, a seconda della modalità di apertura o creazione tramite [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage). Inoltre, i tag della modalità di accesso e condivisione specificati al momento dell'apertura o della creazione del set di proprietà vengono passati a flussi o archiviazione basati su Proprietà.

Le durate dei puntatori di archiviazione o di flusso basati su proprietà, sebbene teoricamente indipendenti dai puntatori [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) associati, in realtà dipendono da essi. I dati visibili tramite il flusso o l'archiviazione sono correlati alla transazione nell'oggetto di archiviazione della proprietà da cui vengono recuperati, come per un oggetto di archiviazione (che supporta [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)) con oggetti secondari di flusso e di archiviazione contenuti. Se la transazione sull'oggetto padre viene interrotta, i puntatori [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) e **IStorage** esistenti subordinati a tale oggetto non saranno più accessibili. Poiché **IPropertyStorage** è l'unica interfaccia nell'oggetto di archiviazione delle proprietà, la durata utile dei puntatori **IStream** e **IStorage** contenuti è vincolata dalla durata dell'interfaccia **IPropertyStorage** .

L'implementazione deve inoltre gestire la situazione in cui la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite la stessa istanza dell'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Nell'implementazione del file composto COM, ad esempio, l'apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta o meno.

Un altro problema è l'apertura multipla in modalità transazionale. Il risultato dipende dal livello di isolamento specificato tramite una chiamata ai metodi [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) (il metodo [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) o [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , tramite i flag STGM) nel momento in cui è stata aperta l'archiviazione della proprietà.

Se la chiamata per aprire il set di proprietà specifica l'accesso in lettura/scrittura, le proprietà [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)sono sempre aperte con accesso in lettura/scrittura. I dati possono quindi essere scritti tramite queste interfacce, modificando il valore della proprietà, che rappresenta il modo più efficiente per aggiornare queste proprietà. Il valore della proprietà non dispone di un livello aggiuntivo di annidamento delle transazioni, quindi l'ambito delle modifiche viene definito sotto la transazione (se presente) nell'oggetto di archiviazione della proprietà.

## <a name="storage-and-stream-properties"></a>Proprietà di archiviazione e di flusso

Per scrivere un flusso o un oggetto di archiviazione in un set di proprietà, il set di proprietà deve essere stato creato come non semplice. Per ulteriori informazioni sui set di proprietà semplici e non semplici, vedere la sezione intitolata [oggetti di archiviazione e di flusso per un set di proprietà](storage-vs--stream-for-a-property-set.md). I seguenti tipi di proprietà, come specificato nel campo *VT* degli elementi della matrice *rgvar* , sono tipi di flusso o di archiviazione: \_ flusso VT, \_ archiviazione VT, oggetto con \_ flusso VT \_ , \_ oggetto archiviato VT \_ .

Per scrivere un flusso o un oggetto di archiviazione come proprietà in un set di proprietà non semplice, chiamare [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Anche se si chiama questo metodo per aggiornare le proprietà semplici, non si tratta di un modo efficiente per aggiornare gli oggetti flusso e archiviazione in un set di proprietà. Questo perché l'aggiornamento di una di queste proprietà tramite una chiamata a **WriteMultiple** crea nell'oggetto archiviazione proprietà una copia dei dati passati e i puntatori [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non vengono conservati oltre la durata della chiamata. È in genere più efficiente aggiornare direttamente gli oggetti Stream o storage chiamando [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) per ottenere il puntatore di interfaccia al flusso o all'archiviazione, quindi scrivere i dati tramite i metodi **IStream** o **IStorage** .

Ad esempio, è possibile chiamare [**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) per scrivere un flusso **null** o un oggetto di archiviazione. L'implementazione creerà quindi un oggetto vuoto nel set di proprietà. È quindi possibile ottenere l'accesso a questo oggetto chiamando [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). Al termine dell'aggiornamento dell'oggetto, non è necessario scriverlo nel set di proprietà, in quanto gli aggiornamenti venivano inseriti direttamente nel set di proprietà.

Un flusso o una risorsa di archiviazione aperta tramite una proprietà viene sempre aperta in modalità diretta, pertanto non è stato introdotto un ulteriore livello di transazione nidificata. Potrebbe essere ancora presente una transazione per la proprietà impostata nel suo complesso. Ad esempio, se [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) è stato ottenuto chiamando [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) con STGM \_ Flag transazionale impostato nel parametro *grfMode* . Un flusso o una risorsa di archiviazione basata su proprietà viene inoltre aperto in modalità di lettura/scrittura, se possibile, in base alla modalità del set di proprietà. in caso contrario, viene utilizzata la modalità di lettura.

Come indicato in precedenza, quando un flusso o un oggetto di archiviazione viene scritto in una proprietà impostata con il metodo [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) , viene creata una copia dell'oggetto. Quando tale copia viene eseguita su un oggetto flusso, l'operazione di copia inizia in corrispondenza della posizione di ricerca corrente dell'origine. La posizione di ricerca non è definita in caso di errore, ma in caso di esito positivo si trova alla fine del flusso; il puntatore di ricerca non viene ripristinato nella posizione originale.

Se una proprietà di flusso o di archiviazione è stata letta da un set di proprietà con [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple), viene ancora mantenuta aperta e viene eseguita una chiamata successiva a [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) per la stessa proprietà, l'operazione **WriteMultiple** avrà esito positivo. Il flusso o la proprietà di archiviazione precedentemente aperti viene posizionata nello stato Reverted (tutte le chiamate a questo oggetto restituiscono l' \_ errore STG E \_ Reverted).

Se il metodo [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple) restituisce un errore durante la scrittura di una matrice di proprietà o anche di singole proprietà non semplici, la quantità di dati effettivamente scritta non è definita.

## <a name="reference-properties"></a>Proprietà riferimento

Se una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) specificata include il \_ flag ByRef del VT nel membro **VT** , la proprietà associata è una proprietà di riferimento. Una proprietà di riferimento viene automaticamente dereferenziata prima di scrivere il valore nel set di proprietà. Se, ad esempio, il membro **VT** della struttura **PROPVARIANT** specifica un valore di tipo VT \_ ByRef \| VT \_ I4, il valore effettivo scritto è un \_ tipo VT i4. Una chiamata successiva al metodo [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) restituisce un valore come VT \_ i4. L'utilizzo di proprietà di riferimento è simile alla chiamata della funzione [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) . [VariantCopyInd](/windows/win32/api/oleauto/nf-oleauto-variantcopyind) libera la variante di destinazione ed esegue una copia dell'oggetto VARIANTARG di origine, eseguendo il riferimento indiretto necessario se l'origine è specificata come ByRef del VT \_ . Questa funzione è utile quando è necessaria una copia di una variante e per garantire che non sia un VT \_ ByRef, ad esempio quando si gestiscono gli argomenti in un'implementazione di [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke).

## <a name="notes-to-callers"></a>Note per i chiamanti

È consigliabile creare i set di proprietà come Unicode, non impostando il \_ flag ANSI PROPSETFLAG nel parametro *GrfFlags* di [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). È inoltre consigliabile evitare di usare \_ i valori LPSTR di VT e usare \_ invece i valori LPWSTR di VT. Quando la tabella codici del set di proprietà è Unicode, \_ i valori di stringa VT LPSTR vengono convertiti in Unicode quando vengono archiviati e restituiti a valori stringa multibyte quando vengono recuperati. Quando la tabella codici della proprietà impostata non è Unicode, i nomi delle proprietà, le stringhe di tipo VT \_ e i valori di proprietà non semplici vengono convertiti in stringhe multibyte quando vengono archiviati e riconvertiti in Unicode quando vengono recuperati, tutti utilizzando la tabella codici ANSI di sistema corrente.

## <a name="notes-to-implementers"></a>Note per gli implementatori

Quando si alloca un identificatore di proprietà, l'implementazione può scegliere qualsiasi valore non attualmente in uso nel set di proprietà per un identificatore di proprietà, purché non sia 0 o 1 o maggiore di 0x80000000, tutti i quali sono valori riservati. Il parametro *propidNameFirst* stabilisce un valore minimo per gli identificatori di proprietà all'interno del set e deve essere maggiore di 1 e minore di 0x80000000. Vedere la sezione Osservazioni sopra.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[IPropertyStorage-implementazione del file composto](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[IPropertyStorage-implementazione del file system NTFS](ipropertystorage-ntfs-file-system-implementation.md)
</dt> <dt>

[IPropertyStorage-implementazione autonoma](ipropertystorage-stand-alone-implementation.md)
</dt> </dl>

 

 