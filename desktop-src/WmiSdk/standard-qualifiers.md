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
ms.openlocfilehash: 67877cfc07a247d6b5e3309270d145bc64fbb814416fa4288c6e85ff2ad2e986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315137"
---
# <a name="standard-qualifiers"></a>Qualificatori standard

Tutte le implementazioni conformi a CIM devono gestire un set standard di qualificatori. Per qualsiasi oggetto specifico non sono elencati tutti i qualificatori. In genere, le classi di estensione forniscono qualificatori aggiuntivi per facilitare il provisioning di istanze di classe e altre operazioni sulla classe.

È responsabilità del provider applicare i qualificatori. WMI non impone qualificatori, ma li usa solo per informare l'utente sull'uso della proprietà.

> [!Note]  
> WMI è conforme alla specifica CIM 2.5.

 

I qualificatori presentano le limitazioni seguenti:

-   Non tutti i qualificatori standard possono essere usati insieme.
-   Non tutti i qualificatori possono essere applicati a tutti i costrutti, ad esempio associazione o riferimento. Queste limitazioni sono identificate nell'elenco Si applica a.
-   Per un costrutto specifico, ad esempio un'associazione o un riferimento, l'uso dei qualificatori legali può essere ulteriormente vincolato perché alcuni qualificatori si escludono a vicenda, l'uso di un qualificatore può implicare alcune restrizioni sul valore di un altro e così via. Queste regole di utilizzo sono documentate.
-   I qualificatori legali vengono ereditati solo da entità quali proprietà, metodi, istanze o sottoclassi, non da associazioni o riferimenti. Ad esempio, il **qualificatore MaxLen** che si applica alle proprietà non viene ereditato dai riferimenti.

Di seguito sono elencati i qualificatori standard WMI.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**astratto**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi, associazioni, indicazioni

Indica se la classe è astratta e funge solo da base per le nuove classi. Il valore predefinito è **FALSE.** Non è possibile creare istanze di classi astratte. L'assenza di questo qualificatore indica che la classe non è astratta. Pertanto, questo qualificatore è obbligatorio per tutte le classi astratte.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregazione**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: riferimenti

Indica se il riferimento è il componente padre di un'associazione di aggregazione. Il valore predefinito è **FALSE.**

Utilizzo: i **qualificatori Aggregazione** **e** Aggregazione vengono usati insieme   **Aggregazione** qualifica l'associazione e **Aggregazione** specifica il riferimento padre.

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregazione**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: associazioni

Indica se l'associazione è un'aggregazione. Il valore predefinito è **FALSE.** Utilizzato con **Aggregate**. Questo qualificatore è obbligatorio per tutte le associazioni di aggregazione.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà, riferimenti, metodi

Nome alternativo per una proprietà o un metodo nello schema. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà, parametri

Tipo della matrice qualificata.

I valori validi sono:

-   bag (impostazione predefinita)
-   indicizzati
-   ordered

Utilizzo: applicare questo tipo di qualificatore solo alle proprietà e ai parametri che sono matrici (definite tramite la sintassi tra parentesi quadre).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Mappa di posizioni di bit significative in cui ogni posizione significativa può essere "on" o "off". Ogni bit "on" viene mappato a un valore corrispondente nella **matrice BitValues.** Con più bit "on", vengono indicati più valori simultanei nella matrice **BitValues.** Il valore predefinito è **NULL.**

Per altre informazioni, vedere [BitMap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Conversione di un valore di posizione di bit in una stringa **associata.** Il valore predefinito è **NULL.**

Per altre informazioni, vedere [BitMap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Costruttore**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: metodi

Indica se il metodo crea istanze. Questi metodi non sono vincolati ad agire su una singola istanza o su una singola classe. Ad esempio, un costruttore può creare istanze di associazione e istanze della classe che definisce il costruttore.

Il **qualificatore** Costruttore è destinato solo alle informazioni e non è previsto che sia agito dal gestore di oggetti. Il gestore oggetti non deve chiamare i metodi del costruttore quando viene creato un oggetto . Inoltre, quando viene chiamato un costruttore, il gestore oggetti non deve richiamare alcun metodo costruttore definito per qualsiasi classe padre della classe originale. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi

Nome del metodo con cui vengono create le istanze di questa classe. Il valore è "PutInstance" o il nome di un altro metodo che crea le istanze. Il valore predefinito è **NULL.**

Utilizzo: questo qualificatore può essere usato solo se è presente il qualificatore **SupportsCreate.**

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi

Nome del metodo in base al quale vengono eliminate le istanze di questa classe. Il valore è "DeleteInstance" o il nome di un altro metodo che elimina le istanze. Il valore predefinito è **NULL.**

Utilizzo: questo qualificatore può essere usato solo se è presente il qualificatore **SupportsDelete.**

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: any

Descrizione di un elemento denominato. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Distruttore**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: metodi

Indica se il metodo elimina le istanze. I metodi che usano il qualificatore **distruttore** eliminano le istanze a cui viene applicato il distruttore e non sono vincolati ad agire su una singola istanza o classe. Ad esempio, un distruttore potrebbe eliminare le istanze di associazione e le istanze della classe che definisce il distruttore.

Il **qualificatore distruttore** è destinato solo alle informazioni e non è previsto che sia agito dal gestore oggetti. Non è obbligatorio che il gestore di oggetti chiami un metodo con il **qualificatore Distruttore** quando un'istanza viene eliminata. Inoltre, quando viene chiamato un distruttore, il gestore oggetti non deve richiamare alcun metodo del distruttore definito per qualsiasi classe padre della classe originale. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: any

Nome visualizzato nell'interfaccia utente anziché il nome effettivo dell'elemento. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: any

L'elemento di tipo stringa completo contiene un'istanza incorporata. Il valore del qualificatore specifica il nome di una classe CIM nello stesso spazio dei nomi della classe proprietaria dell'elemento completo. L'istanza incorporata è un'istanza della classe specificata, incluse le istanze delle relative sottoclassi. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**misuratore**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: any

Indica se la proprietà rappresenta un numero intero non negativo, che può aumentare o diminuire, ma non superare mai un valore massimo. Il valore predefinito è **FALSE.**

Il valore massimo della proprietà non può essere maggiore di 2^*n* - 1. *N* può essere 8, 16, 32 o 64 a seconda del tipo di dati della proprietà a cui viene applicato questo qualificatore. Il valore di un misuratore ha il valore massimo ogni volta che le informazioni modellate sono maggiori o uguali a tale valore massimo. Se le informazioni modellate successivamente diminuiscono al di sotto del valore massimo, anche il misuratore diminuisce. Questo qualificatore è applicabile solo alle proprietà con un tipo di dati Integer senza segno.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**Pollici**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: parametri

Indica se il parametro viene utilizzato per passare valori a un metodo. Il valore predefinito è **TRUE.**

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: parametri

Indica se il parametro è sia un parametro di input che di output.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Chiave**](key-qualifier.md)
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà, riferimenti

Indica se la proprietà fa parte dell'handle dello spazio dei nomi. Se più proprietà hanno il [**qualificatore Key,**](key-qualifier.md) tutte queste proprietà formano collettivamente la chiave (una chiave composta). Quando vengono riunite, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe. Se questo qualificatore viene inserito in una proprietà, è consentito solo il **valore TRUE.**

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Pigro**
</dt> <dd>

Si applica a: proprietà

Indica che la proprietà è a elevato utilizzo di risorse per restituire e richiede molto tempo e memoria del processore. WMI migliora le prestazioni delle query non tentando di restituire le proprietà contrassegnate con il qualificatore **Lazy.**

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: classi, proprietà, associazioni, indicazioni, riferimenti

Set di valori che indicano un percorso in cui è possibile trovare altre informazioni sull'origine di una proprietà, una classe, un'associazione, un'indicazione o un riferimento. La stringa di mapping può essere un percorso di directory, un URL, una chiave del Registro di sistema, un file di inclusione, un riferimento a una classe CIM o un altro formato. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Massimo**
</dt> <dd>

Tipo di dati: **int**

Si applica a: riferimenti

Numero massimo di valori che un determinato riferimento può avere per ogni set di altri valori di riferimento nell'associazione. Il valore predefinito è **NULL.** Ad esempio, se un'associazione mette in relazione istanze A a istanze B e deve essere presente al massimo un'istanza A per ogni istanza B, il riferimento ad A deve avere un massimo di un qualificatore.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Lunghezza massima (in caratteri) di un **elemento di** dati stringa e indica il supporto di matrici a lunghezza fissa.

Se viene rilevata una matrice a lunghezza fissa, il qualificatore **MaxLen** contiene la lunghezza fissa trovata durante l'analisi. Se viene rilevata una matrice a lunghezza variabile, questo qualificatore non viene usato. **MaxLen** viene usato per suggerire il numero massimo di elementi che devono essere archiviati in una matrice. Quando si esegue l'override del valore predefinito, è possibile specificare qualsiasi valore intero senza segno (**uint32**). Il valore **NULL** (impostazione predefinita) implica una lunghezza illimitata.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**Maxvalue**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Valore massimo dell'oggetto . Il valore predefinito è **NULL.**

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Minimo**
</dt> <dd>

Tipo di dati: **int**

Si applica a: riferimenti

Cardinalità minima del riferimento (numero minimo di valori che un determinato riferimento può avere per ogni set di altri valori di riferimento nell'associazione). Il valore predefinito è 0.

Ad esempio, se un'associazione mette in relazione le istanze A con le istanze B e deve essere presente almeno un'istanza A per ogni istanza B, il riferimento ad A deve avere almeno un qualificatore.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**Minvalue**
</dt> <dd>

Tipo di dati: **int**

Si applica a: proprietà, metodi, parametri

Indica il valore minimo dell'oggetto . Il valore predefinito è **NULL.**

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà

Set di valori che indicano la corrispondenza tra la proprietà di un oggetto e altre proprietà nello schema CIM. Il valore predefinito è **NULL.**

Le proprietà dell'oggetto vengono identificate usando la sintassi seguente.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Non locale**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: riferimenti

Posizione di un'istanza, il cui valore è <*namespacetype*>://<*namespacehandle*> Il valore predefinito è **NULL.**

Utilizzo: questo qualificatore non può essere usato con il **qualificatore NonlocalType.**

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: riferimenti

Tipo di posizione di un'istanza. Il valore è <namespacetype> . Il valore predefinito è **NULL.**

Utilizzo: questo qualificatore non può essere usato con il **qualificatore non** locale.

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**Nullvalue**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà

Valore che indica che la proprietà associata è **NULL** (la proprietà non ha un valore valido o significativo). Il valore predefinito è **NULL.**

Le convenzioni e le restrizioni usate per definire i **valori NULL** sono le stesse applicabili al qualificatore **ValueMap.** Si noti che questo qualificatore non può essere sottoposto a override. Non è ragionevole consentire a una sottoclasse di restituire un **valore NULL** diverso da quello della classe padre.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Cambio**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: parametri

Indica se il parametro restituisce valori da un metodo. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**prevalere**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà, metodi, riferimenti

Classe padre o costrutto subordinato (proprietà, metodo o riferimento) sottoposto a override dalla proprietà, dal metodo o dal riferimento dello stesso nome nella classe derivata. Il valore predefinito è **NULL.**

Il formato è:

\[<*classe*>. \] < *costrutto subordinato*>

Se il nome della classe viene omesso, l'override si applica al costrutto subordinato nella classe padre nella gerarchia di classi.

Utilizzo: il **qualificatore Override** può fare riferimento a costrutti basati solo sullo stesso meta model. Non è consentito modificare il nome o la firma di un costrutto durante un'operazione di override.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**
</dt> <dd>

Si applica a: classi

Indica se il valore della proprietà in una sottoclasse esegue l'override del valore in una classe padre. L'implicazione funzionale è che, se si esegue una query sulla classe padre e se la clausola **WHERE** include questa proprietà, l'elemento padre deve restituire un'istanza con il valore sottoposto a override. Di conseguenza, gestione Windows regola la clausola **WHERE** della query inviata alla classe padre per escludere i riferimenti a questa proprietà.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagate**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà

Nome della chiave da propagare. Il valore predefinito è **NULL.**

L'uso di questo qualificatore presuppone l'esistenza di un solo qualificatore debole in un riferimento con la classe contenitore come destinazione. La proprietà associata deve avere lo stesso valore della proprietà denominata dal qualificatore nella classe sull'altro lato dell'associazione debole. Il formato è:

\[<*classe*>. \] < *costrutto subordinato*>

Utilizzo: quando si **usa il qualificatore Propagated,** il [**qualificatore Key**](key-qualifier.md) deve essere specificato con il valore **TRUE**.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Leggere**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà

Indica se la proprietà è leggibile. Il valore predefinito è **TRUE.**

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obbligatorio**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà

Indica se per la proprietà è necessario un valore non Null. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisione**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi, associazioni, indicazioni, schemi

Numero di revisione secondario dell'oggetto schema. Il valore predefinito è **NULL.**

Utilizzo: il **qualificatore Di** versione deve essere presente per specificare il numero di versione principale quando viene usato il **qualificatore** Revisione.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà, metodi

Nome dello schema in cui è definita la funzionalità. Il valore predefinito è **NULL.**

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**fonte**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi, associazioni, indicazioni, riferimenti

Posizione di un'istanza di . Il valore predefinito è **NULL.**

Il valore del qualificatore è <*namespacetype*>://<*namespacehandle*>.

Utilizzo: il **qualificatore Source** non può essere usato con il **qualificatore SourceType.**

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**Sourcetype**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi, associazioni, indicazioni, riferimenti

Tipo di posizione di un'istanza. Il valore di questo qualificatore è <*namespacetype>.* Il valore predefinito è **NULL.**

Utilizzo: il **qualificatore SourceType** non può essere usato con il **qualificatore Source.**

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe supporta la creazione di istanze. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe supporta l'eliminazione di istanze. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe supporta la modifica (aggiornamento) delle istanze. Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: classi

Indica se la classe può avere sottoclassi. Il valore predefinito è **FALSE.**

Se viene dichiarata una sottoclasse, il compilatore genera un errore.

Utilizzo: questo qualificatore non può coesistere con il **qualificatore Abstract.** Se vengono specificati **entrambi i qualificatori Terminal** e **Abstract,** il compilatore genera un errore.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unità**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: proprietà, metodi, parametri

Tipo di unità in cui viene espresso l'elemento di dati associato. Il valore predefinito è **NULL.**

Ad esempio, un elemento di dati size potrebbe avere un valore "bytes" per **Units**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Set di valori consentiti per una proprietà, un tipo restituito di metodo o un parametro di metodo. Il valore predefinito è **NULL.**

Utilizzo: questo qualificatore può essere usato da solo o in combinazione con il **qualificatore Values.** Se usato in combinazione con il qualificatore **Values,** la posizione del valore nella matrice **ValueMap** fornisce la posizione della voce corrispondente nella matrice **Values.** Usare il **qualificatore ValueMap** solo con valori stringa e integer. La sintassi per rappresentare un valore intero nella matrice di mapping dei valori è \[ + \| = \] digit \[ \* digit \] . Il contenuto, il numero massimo di cifre e il valore rappresentato sono vincolati dal tipo della proprietà associata. Ad esempio, uint8 potrebbe non essere firmato, deve essere minore di quattro cifre e deve rappresentare un valore minore di 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valori**
</dt> <dd>

Tipo di dati: **matrice di stringhe**

Si applica a: proprietà, metodi, parametri

Set di valori che traslano un valore intero in una stringa associata. Il valore predefinito è **NULL.**

Questa proprietà specifica anche una matrice di valori stringa di cui eseguire il mapping a una proprietà di enumerazione. Questo qualificatore può essere applicato a una proprietà integer o a una proprietà stringa e il mapping può essere implicito o esplicito. Se il mapping è implicito, i valori delle proprietà integer o stringa rappresentano le posizioni ordinali nella **matrice Values.** Se il mapping è esplicito, la proprietà deve essere un numero intero e i valori validi della proprietà sono elencati nella matrice definita dal qualificatore **ValueMap.** Per altre informazioni, vedere [Mappa valori](value-map.md).

Se non è presente un qualificatore **ValueMap,** la matrice **Values** viene indicizzata (relativa a zero) usando il valore nella proprietà associata, nel tipo restituito del metodo o nel parametro del metodo. Se è **presente un qualificatore ValueMap,** l'indice dei valori viene definito dalla posizione del valore della proprietà nella mappa valori.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione**
</dt> <dd>

Tipo di dati: **stringa**

Si applica a: classi, schemi, associazioni, indicazioni

Numero di versione principale dell'oggetto schema. Il valore predefinito è **NULL.** Il numero di versione viene incrementato quando vengono apportate modifiche allo schema che modificano l'interfaccia.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Debole**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: riferimenti

Indica se le chiavi della classe a cui si fa riferimento includono le chiavi degli altri partecipanti all'associazione. Il valore predefinito è **FALSE.**

Questo qualificatore viene usato quando l'identità della classe a cui si fa riferimento dipende dall'identità degli altri partecipanti all'associazione. Non più di un riferimento a una determinata classe può essere debole. Le altre classi nell'associazione devono definire una chiave. Le chiavi delle altre classi nell'associazione vengono ripetute nella classe a cui si fa riferimento e contrassegnate con un **qualificatore propagato.**

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Scrivere**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà

Indica che le applicazioni o gli script possono modificare il valore della proprietà. L'account che esegue l'applicazione deve avere accesso allo spazio dei nomi che contiene le istanze della classe . L'implementazione del provider può anche limitare l'accesso ai dati del provider. Il valore **TRUE** indica che la proprietà è leggibile e scrivibile dai consumer a cui è consentito l'accesso da WMI e dal provider. Il valore predefinito è **FALSE.**

Una proprietà che non dispone del **qualificatore Write** può comunque essere scrivibile. L'implementazione del provider può consentire la modifica di qualsiasi proprietà nelle classi del provider, indipendentemente dal fatto che il **qualificatore Write** sia presente.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà

Indica se la proprietà è scrivibile durante la creazione dell'istanza. Questo qualificatore può essere usato insieme al **qualificatore WriteAtCreate.** Il valore predefinito è **FALSE.**

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Tipo di dati: **booleano**

Si applica a: proprietà

Indica se la proprietà è scrivibile in fase di aggiornamento dell'istanza. Questo qualificatore può essere usato insieme al **qualificatore WriteAtCreate.** Il valore predefinito è **FALSE.**

</dd> </dl>

## <a name="examples"></a>Esempio

Per altre informazioni sul recupero di qualificatori, vedere l'esempio di codice [di PowerShell Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in TechNet Gallery.

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

 

 




