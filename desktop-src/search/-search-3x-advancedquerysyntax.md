---
description: Advanced Query Syntax (AQS) è la sintassi di query predefinita usata da Windows Ricerca per eseguire query sull'indice e per perfezionare e restringere i parametri di ricerca.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Uso della sintassi di query avanzata a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e480866120289605a7465af96d8aaa8dc2beda
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627227"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Uso della sintassi di query avanzata a livello di codice

Advanced Query Syntax (AQS) è la sintassi di query predefinita usata da Windows Ricerca per eseguire query sull'indice e per perfezionare e restringere i parametri di ricerca. AQS viene utilizzato dagli sviluppatori per compilare query a livello di codice (e dagli utenti per restringere i parametri di ricerca). L'AQS canonico è stato introdotto Windows 7 e deve essere usato in Windows 7 e versioni successive per generare query AQS a livello di codice.

Questo argomento è organizzato come segue:

-   [Informazioni sulla sintassi di query avanzata](#about-advanced-query-syntax)
    -   [esempi](#examples)
    -   [Proprietà](#properties)
-   [Uso di parole chiave nelle lingue locali](#keyword-use-in-local-languages)
-   [Sintassi di query avanzate canoniche in Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [esempi](#examples)
    -   [Operatori di query](#query-operators)
    -   [Eseguire query su valori](#query-values)
-   [Restrizioni di ambito](#scope-restrictions)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-advanced-query-syntax"></a>Informazioni sulla sintassi di query avanzata

Una query è costituita da query di base connesse con AND, OR e NOT, come illustrato nella sintassi di esempio seguente:

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> AQS non fa distinzione tra maiuscole e minuscole, ad eccezione di AND, OR e NOT, che devono essere tutte maiuscole.

 

Se una query ha due o più utilizzi di AND o OR, verrà eseguita l'associazione da sinistra a destra, indipendentemente dal fatto che sia AND o OR. Ovvero, la query "apple AND pear OR prugna" verrà interpretata come se fosse scritta come "(apple AND pear) OR prugna" e la query "apple OR pear AND plum", verrà interpretata come se fosse scritta come "(apple OR pear) AND prugna". Pertanto, se un documento contiene la parola prugna, ma né apple, né pera, la prima query lo restituirà, ma la seconda query non lo restituirà. È quindi consigliabile usare parentesi esplicite per qualsiasi query che combina AND e OR per evitare errori o fraintendenze.

Una query di base cerca gli elementi che soddisfano una restrizione su una proprietà. L'unica parte richiesta di una query di base è la restrizione o il valore di ricerca. Se non si specifica una proprietà, Windows ricerca cerca tutte le proprietà. <restr> rappresenta la restrizione di ricerca.

Sono validi i moduli seguenti per una query di base:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Una proprietà è designata da una parola chiave, ad esempio author o size, o da un nome di proprietà canonico, ad esempio [System.DateModified](../properties/props-system-datemodified.md). I moduli validi per una proprietà sono i seguenti:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Un operatore indica un'operazione, ad esempio < o =. Per un elenco di operatori validi, vedere la sezione Operatori di query più avanti in questo argomento.

Una restrizione di base è una restrizione semplice per una proprietà che può essere scritta senza parentesi:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Una restrizione è un valore di ricerca, ad esempio un valore numerico o un valore stringa, facoltativamente con un operatore . I moduli validi per una restrizione sono i seguenti:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Se non si specifica un operatore, Windows ricerca sceglie l'operatore più appropriato per la query:

-   Per una proprietà stringa, si presuppone l'operatore COP \_ WORD \_ STARTSWITH $<.
-   Per tutte le altre proprietà, si presuppone l'operatore COP \_ EQUAL =.

Per l'uso a livello di codice di AQS, è consigliabile avere sempre un operatore esplicito. Il formato valido per la ricerca di un valore semplice o di un intervallo di valori è il seguente:

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

Un valore semplice può essere costituito da uno dei tipi seguenti:

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a>Esempio

Una query che cerca un documento contenente la fase "last quarter", creato da Theresa o Lee e salvato nella cartella MyDocs, combina tre query di base come segue:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Le tre query di base sono:

-   "last quarter"
-   author:(theresa OR lee)
-   folder:MyDocs

Una query di base che usa la sintassi canonica è:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Proprietà

Le proprietà sono definite da una parola chiave, che può essere un nome di proprietà canonico in Windows 7 e versioni successive. AQS nell'interfaccia Windows può usare l'etichetta anziché il nome canonico della proprietà, ad esempio author anziché [System.Author](../properties/props-system-author.md). In Windows Vista e versioni precedenti era possibile usare etichette in inglese indipendentemente dalla lingua dell'interfaccia utente. In Windows 7 e versioni successive, Windows ricerca riconosce le parole chiave solo nella lingua dell'interfaccia utente predefinita corrente.

### <a name="support-for-custom-properties"></a>Supporto per le proprietà personalizzate

In Windows Vista e versioni precedenti, le proprietà personalizzate non erano disponibili in AQS. In Windows 7 e versioni successive, AQS funziona con proprietà personalizzate registrate con il sistema di proprietà. Per altre informazioni sulla creazione di proprietà personalizzate, vedere [Sistema di proprietà](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Proprietà DateTime in Windows 8

A Windows 8, le proprietà DateTime (ad esempio [System.DateModified](../properties/props-system-datemodified.md)) supportano il formato di data e ora canonico specificato da [ISO-8601,](https://www.w3.org/TR/NOTE-datetime)includendo facoltativamente il fuso orario UTC.

-   **Windows 8 e precedenti, data-ora senza fuso orario UTC:** *AAAA* - *MM* - *GGThh*:*mm*:*ss*

    Questo formato specifica un'ora locale, indipendentemente dalle impostazioni locali dell'utente o del sistema.

-   **Windows 8, data-ora con fuso orario UTC:** *AAAA* - *MM* - *GGThh*:*mm*:*ssTZD*

    Questo formato specifica un'ora nel fuso orario UTC specificato.

## <a name="keyword-use-in-local-languages"></a>Uso di parole chiave nelle lingue locali

In Windows 7 e versioni successive, le parole chiave mnemoniche funzionano solo nella lingua del sistema, ad esempio parole chiave tedesche solo in un sistema operativo tedesco e parole chiave in inglese solo in un sistema operativo in lingua inglese. [System.Author](../properties/props-system-author.md) è una parola chiave canonica e il valore mnemonico per la proprietà System.Author è Author, ad esempio. L'introduzione di parole chiave canoniche compensa il fatto che le parole chiave mnemoniche dell'inglese non sono più universalmente riconosciute in tutti i sistemi operativi indipendentemente dalla lingua, come nel caso di Windows Vista e versioni precedenti.

> [!Note]  
> In Windows 7 e versioni successive, Windows ricerca riconosce le parole chiave solo nella lingua predefinita corrente e non in inglese, a meno che l'inglese non sia l'impostazione predefinita corrente. È consigliabile che gli sviluppatori usino sempre la sintassi canonica in modo che l'applicazione non abbia problemi di linguaggio con le parole chiave.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Sintassi di query avanzate canoniche in Windows 7

La sintassi canonica è stata introdotta per le parole chiave Windows 7. Un esempio di query con una proprietà canonica è `System.Message.FromAddress:=me@microsoft.com` . Quando si codificano query in applicazioni in Windows 7 e versioni successive, è necessario usare la sintassi canonica per generare query AQS a livello di codice. Se non si usa la sintassi canonica e l'applicazione viene distribuita in impostazioni locali o in una lingua dell'interfaccia utente diversa dalla lingua nel codice dell'applicazione, le query non verranno interpretate correttamente.

Le convenzioni per la sintassi delle parole chiave canoniche sono le seguenti:

-   La sintassi canonica per una proprietà è il nome canonico, ad esempio `System.Photo.LightSource` . Per i nomi canonici non viene fatto distinzione tra maiuscole e minuscole.
-   La sintassi canonica per gli operatori booleani è costituita dalle parole chiave AND, OR e NOT in tutte maiuscole.
-   Gli operatori <, >, =e così via, non sono localizzati e fanno quindi parte della sintassi canonica.
-   Se una proprietà ha valori enumerati o intervalli denominati da N₁ a Nk, la sintassi canonica per il valore o l'intervallo I è il nome canonico per P, seguito dal carattere , seguito da N I , come illustrato `P` nell'esempio  \# seguente:<sub></sub>
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` e così via.
-   Per un tipo semantico definito T con valori o intervalli denominati da N₁ a Nk, la sintassi canonica per il valore o l'intervallo *I* è il nome canonico per T, seguito dal carattere , seguito da N I , come illustrato nell'esempio \# seguente:<sub></sub>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Per i valori letterali, ad esempio parole o frasi, la sintassi canonica è la stessa della sintassi normale. Esempi di query con valori letterali nella sintassi canonica sono:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> Non esiste una sintassi canonica per i numeri Windows 7 e versioni successive. Poiché i formati a virgola mobile variano a seconda delle impostazioni locali, l'uso di una query canonica che include una costante a virgola mobile non è supportato. Le costanti integer, al contrario, possono essere scritte usando solo cifre (senza separatori per migliaia) e possono essere usate in modo sicuro nelle query canoniche in Windows 7 e versioni successive.

 

### <a name="examples"></a>Esempio

La tabella seguente illustra alcuni esempi di proprietà canoniche e la sintassi per usarle.



| Tipo di proprietà canonica | Esempio                                                                                     | Sintassi                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore stringa               | [System.Author](../properties/props-system-author.md)<br/>    | Il valore stringa viene cercato nella proprietà author: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Intervallo di enumerazione          | [System.Priority](../properties/props-system-priority.md)             | La proprietà priority può avere un intervallo di valori numerici:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System.IsDeleted](../properties/props-system-isdeleted.md)<br/> | I valori booleani possono essere usati con qualsiasi proprietà booleana:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`E `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numerico                  | [System.Size](../properties/props-system-size.md)<br/>      | Non è possibile scrivere in modo sicuro una query canonica che implica una costante a virgola mobile, perché i formati a virgola mobile variano a seconda delle impostazioni locali. I numeri interi devono essere scritti senza separatori per le migliaia. Ad esempio:<br/>`System.Size:<12345` |



 

Per altre informazioni sulle proprietà canoniche e sul sistema di proprietà in generale, vedere [Proprietà di sistema.](../properties/props.md) In alternativa, fare riferimento ai file di intestazione pubblici.

### <a name="query-operators"></a>Operatori di query

Se una proprietà, p, ha più valori per un elemento, una query AQS per p: restituisce l'elemento se è true per almeno <restr> <restr> uno dei valori.  ( <restr> rappresenta una restrizione).

La sintassi elencata nella tabella seguente è costituita da un operatore, un simbolo dell'operatore, un esempio e una descrizione di esempio. L'operatore e il simbolo possono essere usati in qualsiasi linguaggio e inclusi in qualsiasi query. Non usare gli operatori COP \_ IMPLICIT o COP APPLICATION \_ \_ SPECIFIC. Alcuni operatori hanno simboli intercambiabili.



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Operatore</th>
<th>Simbolo</th>
<th>Esempio</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COP_EQUAL</td>
<td>=<br/></td>
<td>System.FileExtension:= &quot;.txt&quot;<br/></td>
<td>Il valore è la stringa &quot; <em>.txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System.Kind:≠picture<br/> System.Photo.DateTaken:-[] più<br/> System.Kind: &lt; &gt; immagine<br/> Immagine System.Kind:NOT<br/> System.Kind:- -picture<br/></td>
<td>La <a href="/windows/desktop/properties/props-system-kind">proprietà System.Kind</a> non è un'immagine.<br/> La <a href="/windows/desktop/properties/props-system-photo-datetaken">proprietà System.Photo.DateTaken</a> ha un valore .<br/> La <a href="/windows/desktop/properties/props-system-kind">proprietà System.Kind</a> non è un'immagine. <br/> La <a href="/windows/desktop/properties/props-system-kind">proprietà System.Kind</a> non è un'immagine. <br/> Gli operatori NOT double applicati alla stessa proprietà non annullano l'operazione. Di conseguenza, System.Kind:- -picture è equivalente a System.Kind:-picture e System.Kind:NOT picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System.Size: &lt; 1 KB<br/></td>
<td>Questo valore è minore di <em>1 KB.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System.ItemDate: &gt; System.StructuredQueryType.DateTime#Today<br/></td>
<td>Questo valore è maggiore di <em>oggi.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System.Size: &lt; =1kb<br/></td>
<td>Questo valore è minore o uguale a <em>1 KB.</em><br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System.Size: &gt; =1kb<br/></td>
<td>Questo valore è uguale o maggiore di <em>1 KB.</em><br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System.FileName:~ &lt; &quot; C++ Primer&quot;<br/></td>
<td>Trova gli elementi in cui il nome del file inizia con i caratteri &quot; <em>C++ Primer</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System.Photo.CameraModel:~ &gt; non<br/></td>
<td>Trova gli elementi in cui il valore della proprietà termina con i caratteri <em>non</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System.Subject.~=round <br/> System.Search.Autosummary:~~round<br/></td>
<td>Trova un messaggio che contiene questa stringa nell'oggetto e, ad esempio, corrisponderà alle &quot; regole di<em>arrotondamento</em> &quot; g.<br/> Trova tutti gli elementi con un oggetto Autosummary che contiene i caratteri <em>arrotondati a</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System.Author:~! &quot; Sanjay&quot;<br/></td>
<td>Trova gli autori in cui non è presente la sequenza &quot; <em>di caratteri sanjay.</em> &quot;<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System.FileName:~ &quot; Mic?osoft W*d&quot;<br/></td>
<td>Trova i file in cui il nome del file inizia con <em>Mic</em>, seguito da un carattere, seguito da <em>osoft w</em>, seguito da qualsiasi carattere che termina con <em>d</em>. <br/> Il carattere ? i caratteri e * non vengono interpretati letteralmente e funzionano come i caratteri jolly in stile DOS:<br/>
<ul>
<li>? corrisponde a un carattere arbitrario.</li>
<li>* trova zero o più caratteri arbitrari.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System.StructuredQuery.Virtual.From:$= &quot; Sanjay Usds&quot;<br/></td>
<td>Per Windows 7 e versioni successive. Trova la frase &quot; <em>Sanjay Jas</em> &quot; in tutte le proprietà From. La parola <em>Sanjay</em> deve essere seguita dalla <em>parolaUsa .</em><br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System.Author:$<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Per Windows 7 e versioni successive. Trova qualsiasi elemento in cui Author contiene una parola che inizia con i caratteri &quot; <em>San</em> &quot; .<br/> Trova qualsiasi file in cui il nome del file contiene una parola che inizia con <em>micro</em>, seguita da una parola che inizia con <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

); Le parentesi quadre vuote ( \[ \] ) indicano "nessun valore".

Per le proprietà della stringa, l'operazione predefinita è COP \_ WORD STARTS WITH o COP WORD \_ \_ \_ \_ EQUAL.

### <a name="query-values"></a>Valori di query

Nella tabella seguente sono elencati esempi utili di limitazione dei valori di query.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valore/simbolo</th>
<th>Esempi</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>string</td>
<td>auto<br/></td>
<td>Qualsiasi sequenza di caratteri che è possibile cercare. La stringa non deve contenere spazi vuoti o combinazioni di caratteri che fanno parte della sintassi. In questo esempio viene cercata una parola che inizia con <em>auto.</em><br/></td>
</tr>
<tr class="even">
<td>Stringa tra virgolette &quot;&quot;</td>
<td>&quot;Conclusioni: valid &quot; &quot; The blue &quot; &quot; &quot; &quot; team&quot;<br/></td>
<td>Qualsiasi sequenza di caratteri. La stringa non viene interpretata come parte della sintassi.<br/> Le virgolette possono essere incluse in una query se sono doppie. In questo esempio viene eseguita la <em>ricerca &quot; del team &quot; blu</em>.<br/></td>
</tr>
<tr class="odd">
<td>Intero</td>
<td>5678<br/></td>
<td>Usare solo cifre per numeri interi. Non usare separatori per migliaia.<br/></td>
</tr>
<tr class="even">
<td>Numero a virgola mobile</td>
<td>5678.1234<br/></td>
<td>Poiché i formati a virgola mobile variano a seconda delle impostazioni locali, una query canonica non può usare una costante a virgola mobile. L'uso della sintassi canonica con numeri a virgola mobile non è sicuro per la localizzazione. <br/></td>
</tr>
<tr class="odd">
<td>Boolean <strong>true</strong> / <strong>false</strong></td>
<td>System.IsRead:=System.StructuredQueryType.Boolean#True<br/> System.IsEncrypted:-System.StructuredQueryType.Boolean#False<br/></td>
<td>Valore <strong>booleano TRUE.</strong><br/> Valore <strong>booleano FALSE.</strong><br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System.Keywords:=[]<br/></td>
<td>Le parentesi quadre vuote indicano che non è presente alcun valore. In questo esempio vengono trovati tutti gli elementi che non sono stati contrassegnati. <br/></td>
</tr>
<tr class="odd">
<td>Date assolute</td>
<td>System.ItemDate:26/1/2010<br/> SystemDateModified 15/10/2002 19:00<br/></td>
<td>Trova gli elementi con data 26 gennaio 2010.<br/> Trova gli elementi modificati il 15 ottobre 2002 tra le ore 19:00:00 e 19:00:59. <br/>
<blockquote>
[!Note]<br />
Poiché i formati di data (ad esempio i formati a virgola mobile) variano in base alle impostazioni locali, l'uso della sintassi canonica con date assolute non è supportato e non è sicuro per la localizzazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Date relative</td>
<td>System.ItemDate:System.StructuredQueryType.DateTime#Today<br/> System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth<br/> System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear<br/></td>
<td>Trova gli elementi con la data odierna.<br/> Trova gli elementi con una data nel mese successivo.<br/> Trova gli elementi con una data nell'ultimo anno.<br/>
<blockquote>
[!Note]<br />
Oltre a eseguire ricerche in date e intervalli di date specifici, AQS riconosce i valori di data <em></em> relativi (ad esempio <em>today</em>, <em>tomorrow</em>, <em>nextweek,</em> <em>nextmonth)</em>e day (ad esempio martedì o <em>lunedì). Mercoledì</em>) e mese (<em>febbraio</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System.ItemDate:11/05/04..11/10/04 System.Size:5kb.. 10 kb<br/></td>
<td>I punti doppi indicano un intervallo di valori. Trova gli elementi con una data compresa tra il 05/11/04 e il 10/11/04, inclusi.<br/> Trova elementi di dimensioni compresa tra 5 e 10 kb.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Restrizioni di ambito

Gli utenti possono limitare l'ambito delle ricerche a percorsi di cartelle o archivi dati specifici. Ad esempio, se si usano più account di posta elettronica e si vuole limitare una query a Microsoft Outlook o Microsoft Outlook Express, è possibile usare o `System.Search.Store:mapi` `System.Search.Store:oe` rispettivamente. La tabella seguente illustra alcuni esempi di come limitare una ricerca in base all'archivio dati.



| Limitare la ricerca in base all'archivio dati  | Parola chiave | Esempio                                     |
|--------------------------------|---------|---------------------------------------------|
| File                          | file    | System.Search.Store:file                    |
| Outlook                        | Mapi    | System.Search.Store:mapi                    |
| Outlook Express                | Oe      | System.Search.Store:oe                      |
| File offline                  | Csc     | System.Search.Store:csc                     |
| Cartella specifica nell'unità locale | folder  | System.ItemFolderNameDisplay:C:" \\ MyFolder" |



 

## <a name="additional-resources"></a>Risorse aggiuntive

-   In Windows 7 e versioni successive, un'opzione di menu di scelta rapida può essere disponibile a seconda che sia soddisfatta una condizione AQS. Per altre informazioni, vedere "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in Creazione di gestori [del menu di scelta rapida.](../shell/context-menu-handlers.md)
-   Le query AQS possono essere limitate a tipi specifici di file, noti come tipi di file. Per altre informazioni, vedere [Tipi di file e associazioni](../shell/fa-intro.md). Per la documentazione di riferimento sulla proprietà, vedere [System.Kind](../properties/props-system-kind.md)e [System.KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Uso SQL e approcci AQS per eseguire query sull'indice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Esecuzione di query sull'indice con Windows sintassi SQL ricerca](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
