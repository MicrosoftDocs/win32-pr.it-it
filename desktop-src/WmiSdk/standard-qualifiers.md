---
description: Tutte le implementazioni conformi a CIM devono gestire un set standard di qualificatori.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificatori standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309877"
---
# <a name="standard-qualifiers"></a>Qualificatori standard

Tutte le implementazioni conformi a CIM devono gestire un set standard di qualificatori. Per tutti gli oggetti specifici non sono elencati tutti i qualificatori. In genere, le classi di estensione forniscono qualificatori aggiuntivi per facilitare il provisioning di istanze di classe e altre operazioni sulla classe.

È responsabilità del provider applicare i qualificatori. WMI non impone i qualificatori, ma li utilizza solo per informare l'utente sulla modalità di utilizzo della proprietà.

> [!Note]  
> WMI è conforme alla specifica CIM 2,5.

 

I qualificatori hanno le limitazioni seguenti:

-   Non tutti i qualificatori standard possono essere usati insieme.
-   Non tutti i qualificatori possono essere applicati a tutti i costrutti, ad esempio l'associazione o il riferimento. Queste limitazioni sono identificate nell'elenco si applica a.
-   Per un costrutto specifico, ad esempio un'associazione o un riferimento, l'utilizzo dei qualificatori legali può essere ulteriormente vincolato perché alcuni qualificatori si escludono a vicenda, l'utilizzo di un qualificatore può implicare alcune restrizioni sul valore di un altro e così via. Queste regole di utilizzo sono documentate.
-   I qualificatori legali vengono ereditati solo da entità quali proprietà, metodi, istanze o sottoclassi, non da associazioni o riferimenti. Ad esempio, il qualificatore **maxlen** che si applica alle proprietà non viene ereditato dai riferimenti.

Di seguito sono elencati i qualificatori standard WMI.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Astratta**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi, associazioni, indicazioni

Indica se la classe è astratta e funge solo da base per le nuove classi. Il valore predefinito è **false**. Non è possibile creare istanze di classi astratte. L'assenza di questo qualificatore indica che la classe non è astratta; Pertanto, questo qualificatore è obbligatorio per tutte le classi astratte.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregazione**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: riferimenti

Indica se il riferimento è il componente padre di un'associazione di aggregazione. Il valore predefinito è **false**.

Utilizzo: i **qualificatori aggregazione e** **aggregazione** vengono   **utilizzati insieme per** qualificare l'associazione e il riferimento padre viene specificato dall' **aggregazione** .

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregazione**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: associazioni

Indica se l'associazione è un'aggregazione. Il valore predefinito è **false**. Utilizzato con l' **aggregazione**. Questo qualificatore è obbligatorio per tutte le associazioni di aggregazione.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, riferimenti, metodi

Nome alternativo per una proprietà o un metodo nello schema. Il valore predefinito è **null**.

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, parametri

Tipo della matrice qualificata.

I valori validi sono:

-   contenitore (impostazione predefinita)
-   indicizzati
-   ordered

Utilizzo: applicare questo tipo di qualificatore solo a proprietà e parametri che sono matrici (definite mediante la sintassi della parentesi quadre).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Mappa di posizioni di bit significative in cui ogni posizione significativa può essere "on" o "off". Ogni bit "on" viene mappato a un valore corrispondente nella matrice **BitValues** . Se si dispone di più bit "on", vengono indicati più valori simultanei nella matrice **BitValues** . Il valore predefinito è **null**.

Per ulteriori informazioni, vedere [bitmap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Conversione di un valore di posizione di bit in una **stringa** associata. Il valore predefinito è **null**.

Per ulteriori informazioni, vedere [bitmap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Costruttore**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: metodi

Indica se il metodo crea istanze. Questi metodi non sono limitati a agire su una sola istanza o su una singola classe. Un costruttore può, ad esempio, creare istanze di associazione, nonché istanze della classe che definiscono il costruttore.

Il qualificatore del **Costruttore** è destinato solo alle informazioni e non è previsto che venga utilizzato dal gestore di oggetti. Il gestore di oggetti non deve chiamare i metodi del costruttore quando viene creato un oggetto. Inoltre, quando viene chiamato un costruttore, il gestore di oggetti non deve richiamare alcun metodo del costruttore definito per una classe padre della classe originale. Il valore predefinito è **false**.

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi

Nome del metodo in base al quale vengono create le istanze di questa classe. Il valore è "PutInstance" o il nome di un altro metodo che crea le istanze. Il valore predefinito è **null**.

Utilizzo: questo qualificatore può essere utilizzato solo se il qualificatore **SupportsCreate** è presente.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi

Nome del metodo in base al quale vengono eliminate le istanze di questa classe. Il valore può essere "DeleteInstance" o il nome di un altro metodo che elimina le istanze. Il valore predefinito è **null**.

Utilizzo: questo qualificatore può essere utilizzato solo se il qualificatore **SupportsDelete** è presente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Tipo di dati: **String**

Si applica a: any

Descrizione di un elemento denominato. Il valore predefinito è **null**.

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Distruttore**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: metodi

Indica se il metodo elimina le istanze. I metodi che usano il qualificatore del **distruttore** eliminano l'istanza o le istanze a cui viene applicato il distruttore e non sono vincolate a agire su una sola istanza o classe. Un distruttore, ad esempio, potrebbe eliminare le istanze dell'associazione, nonché le istanze della classe che definiscono il distruttore.

Il qualificatore del **distruttore** è destinato solo alle informazioni e non è previsto che venga utilizzato dal gestore di oggetti. Non è necessario che il gestore di oggetti chiami un metodo con il qualificatore del **distruttore** quando un'istanza viene eliminata. Inoltre, quando viene chiamato un distruttore, il gestore di oggetti non deve richiamare alcun metodo di distruttore definito per una classe padre della classe originale. Il valore predefinito è **false**.

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**
</dt> <dd>

Tipo di dati: **String**

Si applica a: any

Nome visualizzato nell'interfaccia utente anziché il nome effettivo dell'elemento. Il valore predefinito è **null**.

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Tipo di dati: **String**

Si applica a: any

L'elemento di tipo stringa qualificato contiene un'istanza incorporata. Il valore del qualificatore specifica il nome di una classe CIM nello stesso spazio dei nomi della classe che possiede l'elemento Qualified. L'istanza incorporata è un'istanza della classe specificata, incluse le istanze delle relative sottoclassi. Il valore predefinito è **null**.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Calibro**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: any

Indica se la proprietà rappresenta un numero intero non negativo, che può aumentare o diminuire, ma mai superare un valore massimo. Il valore predefinito è **false**.

Il valore massimo della proprietà non può essere maggiore di 2 ^*n* -1. *N* può essere 8, 16, 32 o 64 a seconda del tipo di dati della proprietà a cui viene applicato questo qualificatore. Il valore di un misuratore ha il valore massimo ogni volta che le informazioni modellate sono maggiori o uguali al valore massimo. Se le informazioni modellate successivamente diminuiscono al di sotto del valore massimo, il misuratore diminuisce anche. Questo qualificatore è applicabile solo alle proprietà con tipo di dati Unsigned Integer.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**In**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: parametri

Indica se il parametro viene utilizzato per passare valori a un metodo. Il valore predefinito è **true**.

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In uscita**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: parametri

Indica se il parametro è un parametro di input e di output.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Chiave**](key-qualifier.md)
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: proprietà, riferimenti

Indica se la proprietà fa parte dell'handle dello spazio dei nomi. Se più di una proprietà dispone del qualificatore [**chiave**](key-qualifier.md) , tutte queste proprietà costituiscono collettivamente la chiave (una chiave composta). Quando vengono rilevate insieme, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe. Se questo qualificatore viene inserito in una proprietà, è consentito solo il valore **true** .

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**
</dt> <dd>

Si applica a: Proprietà

Indica che la proprietà è a elevato utilizzo di risorse e richiede molto tempo e memoria del processore. WMI migliora le prestazioni delle query non tentando di restituire le proprietà contrassegnate dal qualificatore **Lazy** .

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: classi, proprietà, associazioni, indicazioni, riferimenti

Set di valori che indicano il percorso di una posizione in cui è possibile trovare ulteriori informazioni sull'origine di una proprietà, una classe, un'associazione, un'indicazione o un riferimento. La stringa di mapping può essere un percorso di directory, un URL, una chiave del registro di sistema, un file di inclusione, un riferimento a una classe CIM o un altro formato. Il valore predefinito è **null**.

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**
</dt> <dd>

Tipo di dati: **int**

Si applica a: riferimenti

Numero massimo di valori che possono essere presenti in un determinato riferimento per ogni set di altri valori di riferimento nell'associazione. Il valore predefinito è **null**. Se, ad esempio, un'associazione mette in correlazione un'istanza alle istanze di B e deve essere presente al massimo un'istanza per ogni istanza B, il riferimento a un oggetto deve avere un massimo di un qualificatore.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Lunghezza massima (in caratteri) di un elemento di dati **stringa** e indica il supporto di matrici a lunghezza fissa.

Se viene rilevata una matrice a lunghezza fissa, il qualificatore **maxlen** contiene la lunghezza fissa trovata durante l'analisi. Se viene rilevata una matrice a lunghezza variabile, questo qualificatore non viene utilizzato. **Maxlen** viene usato per suggerire il numero massimo di elementi che devono essere archiviati in una matrice. Quando si esegue l'override del valore predefinito, è possibile specificare qualsiasi valore di Unsigned Integer (**UInt32**). Il valore **null** (impostazione predefinita) implica una lunghezza illimitata.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Valore massimo dell'oggetto. Il valore predefinito è **null**.

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**
</dt> <dd>

Tipo di dati: **int**

Si applica a: riferimenti

Cardinalità minima del riferimento (il numero minimo di valori che un determinato riferimento può avere per ogni set di altri valori di riferimento nell'associazione). Il valore predefinito è 0.

Se, ad esempio, un'associazione mette in relazione le istanze di in istanze B e deve essere presente almeno un'istanza per ogni istanza B, il riferimento a un oggetto deve avere almeno un qualificatore.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Indica il valore minimo dell'oggetto. Il valore predefinito è **null**.

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: Proprietà

Set di valori che indicano la corrispondenza tra la proprietà di un oggetto e altre proprietà nello schema CIM. Il valore predefinito è **null**.

Le proprietà dell'oggetto vengono identificate utilizzando la sintassi seguente.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Non locali**
</dt> <dd>

Tipo di dati: **String**

Si applica a: riferimenti

Percorso di un'istanza, il cui valore è <*tipologia*>://<*namespacehandle*> il valore predefinito è **null**.

Utilizzo: questo qualificatore non può essere utilizzato con il qualificatore **NonlocalType** .

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Tipo di dati: **String**

Si applica a: riferimenti

Tipo di posizione di un'istanza. Il valore è <namespacetype> . Il valore predefinito è **null**.

Utilizzo: questo qualificatore non può essere utilizzato con il qualificatore non **locale** .

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Tipo di dati: **String**

Si applica a: Proprietà

Valore che indica che la proprietà associata è **null** (la proprietà non ha un valore valido o significativo). Il valore predefinito è **null**.

Le convenzioni e le restrizioni usate per la definizione dei valori **null** sono le stesse applicabili al qualificatore **ValueMap** . Nota non è possibile eseguire l'override di questo qualificatore. Non è ragionevole consentire a una sottoclasse di restituire un valore **null** diverso rispetto a quello della classe padre.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: parametri

Indica se il parametro restituisce valori da un metodo. Il valore predefinito è **false**.

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, metodi, riferimenti

Classe padre o costrutto subordinato (proprietà, metodo o riferimento) sottoposto a override dalla proprietà, dal metodo o dal riferimento con lo stesso nome nella classe derivata. Il valore predefinito è **null**.

Il formato è:

\[<> della *classe* . \] < *costrutto subordinato*>

Se il nome della classe viene omesso, l'override viene applicato al costrutto subordinato nella classe padre nella gerarchia di classi.

Utilizzo: il qualificatore di **override** può fare riferimento a costrutti basati solo sullo stesso Metamodello. Non è consentito modificare il nome o la firma di un costrutto durante un'operazione di sostituzione.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

Si applica a: classi

Indica se il valore della proprietà in una sottoclasse esegue l'override del valore in una classe padre. L'implicazione funzionale è che, se si esegue una query sulla classe padre e se la clausola **where** include questa proprietà, l'elemento padre deve restituire un'istanza con il valore sottoposto a override. Di conseguenza, gestione Windows regola la clausola **where** della query inviata alla classe padre per escludere i riferimenti a questa proprietà.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagate**
</dt> <dd>

Tipo di dati: **String**

Si applica a: Proprietà

Nome della chiave da propagare. Il valore predefinito è **null**.

L'uso di questo qualificatore presuppone l'esistenza di un solo qualificatore vulnerabile su un riferimento che abbia la classe che lo contiene come destinazione. La proprietà associata deve avere lo stesso valore della proprietà indicata dal qualificatore nella classe sull'altro lato dell'associazione debole. Il formato è:

\[<> della *classe* . \] < *costrutto subordinato*>

Utilizzo: quando viene usato il qualificatore **propagato** , il qualificatore della [**chiave**](key-qualifier.md) deve essere specificato con un valore **true**.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Lettura**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica se la proprietà è leggibile. Il valore predefinito è **true**.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obbligatorio**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica se per la proprietà è necessario un valore non null. Il valore predefinito è **false**.

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisione**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi, associazioni, indicazioni, schemi

Numero di revisione secondario dell'oggetto dello schema. Il valore predefinito è **null**.

Usage: il qualificatore di **versione** deve essere presente per fornire il numero di versione principale quando viene usato il qualificatore di **Revisione** .

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, metodi

Nome dello schema in cui è definita la funzionalità. Il valore predefinito è **null**.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Origine**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi, associazioni, indicazioni, riferimenti

Percorso di un'istanza. Il valore predefinito è **null**.

Il valore del qualificatore è <*tipologia*>://<*namespacehandle*>.

Uso: il qualificatore di **origine** non può essere usato con il qualificatore **sourceType** .

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi, associazioni, indicazioni, riferimenti

Tipo di posizione di un'istanza. Il valore di questo qualificatore è <> *tipologia* . Il valore predefinito è **null**.

Utilizzo: non è possibile utilizzare il qualificatore **sourceType** con il qualificatore di **origine** .

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe supporta la creazione di istanze. Il valore predefinito è **false**.

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe supporta l'eliminazione di istanze di. Il valore predefinito è **false**.

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe supporta la modifica (aggiornamento) delle istanze di. Il valore predefinito è **false**.

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: classi

Indica se la classe può disporre di sottoclassi. Il valore predefinito è **false**.

Se viene dichiarata una sottoclasse, il compilatore genera un errore.

Utilizzo: questo qualificatore non può coesistere con il qualificatore **astratto** . Se vengono specificati entrambi i qualificatori **Terminal** e **abstract** , il compilatore genera un errore.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unità**
</dt> <dd>

Tipo di dati: **String**

Si applica a: proprietà, metodi, parametri

Tipo di unità in cui viene espresso l'elemento di dati associato. Il valore predefinito è **null**.

Ad esempio, un elemento di dati di dimensioni potrebbe avere un valore di "bytes" per le **unità**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Set di valori consentiti per una proprietà, un tipo restituito del metodo o un parametro del metodo. Il valore predefinito è **null**.

Usage: questo qualificatore può essere usato da solo o in combinazione con il qualificatore **values** . Se usato in combinazione con il qualificatore **values** , il percorso del valore nella matrice **ValueMap** fornisce la posizione della voce corrispondente nella matrice di **valori** . Usare il qualificatore **ValueMap** solo con valori stringa e interi. La sintassi per la rappresentazione di un valore integer nella matrice della mappa dei valori è digit \[ + \| = \] \[ \* digit \] . Il contenuto, il numero massimo di cifre e il valore rappresentato sono limitati dal tipo della proprietà associata. Ad esempio, Uint8 non può essere firmato, deve essere composto da meno di quattro cifre e deve rappresentare un valore inferiore a 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valori**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Set di valori che converte un valore integer in una stringa associata. Il valore predefinito è **null**.

Questa proprietà specifica inoltre una matrice di valori stringa di cui eseguire il mapping a una proprietà di enumerazione. Questo qualificatore può essere applicato a una proprietà Integer o a una proprietà di stringa e il mapping può essere implicito o esplicito. Se il mapping è implicito, i valori di proprietà Integer o String rappresentano posizioni ordinali nella matrice di **valori** . Se il mapping è esplicito, la proprietà deve essere un numero intero e i valori di proprietà validi sono elencati nella matrice definita dal qualificatore **ValueMap** . Per ulteriori informazioni, vedere [mapping dei valori](value-map.md).

Se non è presente un qualificatore **ValueMap** , la matrice di **valori** viene indicizzata (relativa a zero) utilizzando il valore nella proprietà associata, nel tipo restituito del metodo o nel parametro del metodo. Se è presente un qualificatore **ValueMap** , l'indice dei valori viene definito in base alla posizione del valore della proprietà nella mappa del valore.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione**
</dt> <dd>

Tipo di dati: **String**

Si applica a: classi, schemi, associazioni, indicazioni

Numero di versione principale dell'oggetto dello schema. Il valore predefinito è **null**. Il numero di versione viene incrementato quando vengono apportate modifiche allo schema che modificano l'interfaccia.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Debole**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: riferimenti

Indica se le chiavi della classe a cui si fa riferimento includono le chiavi degli altri partecipanti nell'associazione. Il valore predefinito è **false**.

Questo qualificatore viene utilizzato quando l'identità della classe a cui si fa riferimento dipende dall'identità degli altri partecipanti nell'associazione. Non più di un riferimento a una determinata classe può essere vulnerabile. Le altre classi nell'associazione devono definire una chiave. Le chiavi delle altre classi nell'associazione vengono ripetute nella classe a cui si fa riferimento e sono contrassegnate con un qualificatore **propagato** .

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Scrittura**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica che le applicazioni o gli script possono modificare il valore della proprietà. L'account che esegue l'applicazione deve avere accesso allo spazio dei nomi che contiene le istanze della classe. L'implementazione del provider può anche limitare l'accesso ai dati del provider. Il valore **true** indica che la proprietà è leggibile e scrivibile dai consumer a cui è consentito l'accesso da parte di WMI e del provider. Il valore predefinito è **false**.

Una proprietà che non dispone del qualificatore di **scrittura** può comunque essere scrivibile. L'implementazione del provider può consentire la modifica di qualsiasi proprietà nelle classi del provider, indipendentemente dal fatto che sia presente il qualificatore di **scrittura** .

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica se la proprietà è scrivibile durante la creazione dell'istanza. Questo qualificatore può essere utilizzato insieme al qualificatore **WriteAtCreate** . Il valore predefinito è **false**.

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Tipo di dati: **Boolean**

Si applica a: Proprietà

Indica se la proprietà è scrivibile in caso di aggiornamento dell'istanza. Questo qualificatore può essere utilizzato insieme al qualificatore **WriteAtCreate** . Il valore predefinito è **false**.

</dd> </dl>

## <a name="examples"></a>Esempio

Per ulteriori informazioni sul recupero dei qualificatori, vedere l'esempio di codice PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) nella raccolta TechNet.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Qualificatori WMI](wmi-qualifiers.md)
</dt> <dt>

[Aggiunta di un qualificatore](adding-a-qualifier.md)
</dt> </dl>

 

 




