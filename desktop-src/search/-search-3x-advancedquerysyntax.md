---
description: La sintassi di query avanzata (AQS) è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Uso della sintassi avanzata delle query a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306194"
---
# <a name="using-advanced-query-syntax-programmatically"></a>Uso della sintassi avanzata delle query a livello di codice

La sintassi di query avanzata (AQS) è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca. AQS viene usato dagli sviluppatori per compilare query a livello di codice (e dagli utenti per restringere i parametri di ricerca). AQS canonico è stato introdotto in Windows 7 e deve essere usato in Windows 7 e versioni successive per generare query AQS a livello di codice.

Questo argomento è organizzato nel modo seguente:

-   [Informazioni sulla sintassi avanzata delle query](#about-advanced-query-syntax)
    -   [esempi](#examples)
    -   [Proprietà](#properties)
-   [Utilizzo delle parole chiave nelle lingue locali](#keyword-use-in-local-languages)
-   [Sintassi avanzata delle query canoniche in Windows 7](#canonical-advanced-query-syntax-in-windows-7)
    -   [esempi](#examples)
    -   [Operatori di query](#query-operators)
    -   [Valori di query](#query-values)
-   [Limitazioni dell'ambito](#scope-restrictions)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="about-advanced-query-syntax"></a>Informazioni sulla sintassi avanzata delle query

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
> AQS non fa distinzione tra maiuscole e minuscole, ad eccezione di AND, OR e NOT, che deve essere in lettere maiuscole.

 

Se una query ha due o più utilizzi di AND o OR, verranno associati da sinistra a destra, indipendentemente dal fatto che sia e o o. Ovvero, la query "Apple, pera o prugna" verrà interpretata come se fosse scritta come "(Apple e pera) o prugna" e la query "Apple, pera e Plum" verrà interpretata come se fosse scritta come "(Apple o pera) e Plum". Quindi, se un documento contiene la parola prugna ma né Apple, né Pear, la prima query lo restituirà ma la seconda query non verrà eseguita. È quindi consigliabile usare le parentesi esplicite per qualsiasi query che mescoli AND e OR per evitare errori o interpretazioni errate.

Una query di base cerca gli elementi che soddisfano una restrizione su una proprietà. L'unica parte obbligatoria di una query di base è la restrizione o il valore di ricerca. Se non si specifica una proprietà, la ricerca di Windows Cerca tutte le proprietà. <restr> rappresenta la restrizione di ricerca.

I seguenti formati per una query di base sono validi:

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

Una proprietà viene designata da una parola chiave, ad esempio Author o size, oppure da un nome di proprietà canonico, ad esempio [System. DateModified](../properties/props-system-datemodified.md). I moduli validi per una proprietà sono i seguenti:

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

Un operatore indica un'operazione come < o =. Per un elenco degli operatori validi, vedere la sezione operatori di query più avanti in questo argomento.

Una restrizione di base è una restrizione semplice su una proprietà che può essere scritta senza parentesi:

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

Una restrizione è un valore di ricerca, ad esempio un valore numerico o un valore stringa, facoltativamente con un operatore. I moduli validi per una restrizione sono i seguenti:

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

Se non si specifica un operatore, Windows Search sceglie l'operatore più appropriato per la query:

-   Per una proprietà di stringa, \_ \_ viene utilizzato l'operatore di Word STARTSWITH $<.
-   Per tutte le altre proprietà, \_ viene utilizzato l'operatore COP EQUAL =.

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

Una query che cerca un documento che contiene la fase "ultimo trimestre", creata da Theresa o Lee, e che è stata salvata nella cartella documenti, combina tre query di base come segue:

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

Le tre query di base sono:

-   "ultimo trimestre"
-   autore: (Theresa o Lee)
-   cartella: docs

Una query di base che usa la sintassi canonica è:

``` syntax
System.Size:>1kb
```

### <a name="properties"></a>Proprietà

Le proprietà sono definite da una parola chiave, che può essere un nome di proprietà canonico in Windows 7 e versioni successive. AQS nell'interfaccia utente di Windows può usare l'etichetta anziché il nome della proprietà canonica, ad esempio Author anziché [System. Author](../properties/props-system-author.md). In Windows Vista e versioni precedenti era possibile usare le etichette inglesi indipendentemente dalla lingua dell'interfaccia utente. In Windows 7 e versioni successive, Windows Search riconosce le parole chiave solo nella lingua predefinita dell'interfaccia utente corrente.

### <a name="support-for-custom-properties"></a>Supporto per proprietà personalizzate

In Windows Vista e versioni precedenti, le proprietà personalizzate non erano disponibili in AQS. In Windows 7 e versioni successive, AQS funziona con proprietà personalizzate registrate con il sistema di proprietà. Per ulteriori informazioni sulla creazione di proprietà personalizzate, vedere [System Property](../properties/building-property-handlers.md).

### <a name="datetime-properties-in-windows-8"></a>Proprietà DateTime in Windows 8

A partire da Windows 8, le proprietà DateTime (ad esempio [System. DateModified](../properties/props-system-datemodified.md)) supportano il formato di data e ora canonico specificato da [ISO-8601](https://www.w3.org/TR/NOTE-datetime), includendo facoltativamente il fuso orario UTC.

-   **Windows 8 e versioni precedenti, data e ora senza fuso orario UTC:** *aaaa* - *mm* - *GGThh*:*mm*:*SS*

    Questo formato specifica un'ora locale, indipendentemente dall'utente o dalle impostazioni locali del sistema.

-   **Windows 8, data/ora con fuso orario UTC:** *aaaa* - *mm* - *GGThh*:*mm*:*ssTZD*

    Questo formato specifica un'ora al fuso orario UTC specificato.

## <a name="keyword-use-in-local-languages"></a>Utilizzo delle parole chiave nelle lingue locali

In Windows 7 e versioni successive, le parole chiave mnemonico funzionano solo nel linguaggio di sistema, ad esempio parole chiave tedesche solo in un sistema operativo tedesco e parole chiave inglesi solo in un sistema operativo in lingua inglese. [System. Author](../properties/props-system-author.md) è una parola chiave canonica e il valore mnemonico per la proprietà System. Author è, ad esempio, Author. L'introduzione di parole chiave canoniche compensa il fatto che le parole chiave in lingua inglese non sono più universalmente riconosciute in tutti i sistemi operativi indipendentemente dalla lingua, come nel caso di Windows Vista e versioni precedenti.

> [!Note]  
> In Windows 7 e versioni successive, Windows Search riconosce solo le parole chiave nella lingua predefinita corrente e non in inglese, a meno che l'inglese non sia l'impostazione predefinita corrente. Si consiglia agli sviluppatori di usare sempre la sintassi canonica, in modo che l'applicazione non abbia problemi di lingua con le parole chiave.

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a>Sintassi avanzata delle query canoniche in Windows 7

La sintassi canonica è stata introdotta per le parole chiave in Windows 7. Un esempio di query con una proprietà canonica è `System.Message.FromAddress:=me@microsoft.com` . Quando si codificano query in applicazioni in esecuzione in Windows 7 e versioni successive, è necessario usare la sintassi canonica per generare query AQS a livello di codice. Se non si usa la sintassi canonica e l'applicazione viene distribuita in una lingua locale o dell'interfaccia utente diversa da quella del codice dell'applicazione, le query non verranno interpretate correttamente.

Le convenzioni per la sintassi delle parole chiave canoniche sono le seguenti:

-   La sintassi canonica per una proprietà è il nome canonico, ad esempio `System.Photo.LightSource` . I nomi canonico non fanno distinzione tra maiuscole e minuscole
-   La sintassi canonica per gli operatori booleani è costituita dalle parole chiave AND, OR e NOT, in lettere maiuscole.
-   Gli operatori <, >, = e così via, non sono localizzati e quindi fanno anche parte della sintassi canonica.
-   Se una proprietà `P` ha enumerato i valori o gli intervalli denominati N ₁ tramite NK, la sintassi canonica per il valore o l'intervallo di *i* TH è il nome canonico per P, seguito dal carattere \# , seguito da N <sub>i</sub>, come illustrato nell'esempio seguente:
    -   `System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` e così via.
-   Per un tipo semantico definito T con valori o intervalli denominati N ₁ tramite NK, la sintassi canonica per il valore o l'intervallo di *i* TH è il nome canonico per T, seguito dal carattere \# , seguito da N <sub>i</sub>, come illustrato nell'esempio seguente:
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   Per i valori letterali come parole o frasi, la sintassi canonica è identica a quella della normale sintassi. Esempi di query con valori letterali nella sintassi canonica sono:
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> Non esiste alcuna sintassi canonica per i numeri in Windows 7 e versioni successive. Poiché i formati a virgola mobile variano tra le impostazioni locali, l'uso di una query canonica che prevede una costante a virgola mobile non è supportato. Le costanti integer possono invece essere scritte usando solo cifre (nessun separatore per migliaia) e possono essere usate in modo sicuro nelle query canoniche in Windows 7 e versioni successive.

 

### <a name="examples"></a>Esempio

Nella tabella seguente vengono illustrati alcuni esempi di proprietà canoniche e la sintassi per utilizzarli.



| Tipo di proprietà canonica | Esempio                                                                                     | Sintassi                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Valore stringa               | [System.Author](../properties/props-system-author.md)<br/>    | Il valore della stringa viene cercato nella proprietà Author: <br/>`System.Author:Jacobs`                                                                                                                                                              |
| Intervallo di enumerazione          | [System. Priority](../properties/props-system-priority.md)             | La proprietà Priority può avere un intervallo di valori numerici:<br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| Boolean                    | [System. undeleted](../properties/props-system-isdeleted.md)<br/> | I valori booleani possono essere usati con qualsiasi proprietà booleana:<br/>`System.IsDeleted:System.StructuredQueryType.Boolean#True`, e `System.IsDeleted:System.StructuredQueryType.Boolean#False`                                                             |
| Numerico                  | [System. size](../properties/props-system-size.md)<br/>      | Non è possibile scrivere in modo sicuro una query canonica che prevede una costante a virgola mobile, perché i formati a virgola mobile variano tra le impostazioni locali. I numeri interi devono essere scritti senza separatori per le migliaia. Ad esempio:<br/>`System.Size:<12345` |



 

Per ulteriori informazioni sulle proprietà canoniche e sul sistema di proprietà in genere, vedere [proprietà di sistema](../properties/props.md). In alternativa, fare riferimento ai file di intestazione pubblica.

### <a name="query-operators"></a>Operatori di query

Se una proprietà, p, ha più valori per un elemento, una query AQS per p: <restr> restituisce l'elemento se <restr> è **true** per almeno uno dei valori. ( <restr> rappresenta una restrizione).

La sintassi elencata nella tabella seguente è costituita da un operatore, un simbolo dell'operatore, un esempio e una descrizione di esempio. L'operatore e il simbolo possono essere utilizzati in qualsiasi linguaggio e inclusi in qualsiasi query. Non usare gli \_ operatori specifici dell'applicazione COP o COP \_ \_ . Alcuni operatori hanno simboli intercambiabili.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
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
<td>System. FileExtension: = &quot; . txt&quot;<br/></td>
<td>Il valore è String &quot; <em>. txt</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_NOTEQUAL</td>
<td>≠<br/> -<br/> &lt;&gt;<br/> NOT<br/> - -<br/></td>
<td>System. Kind: immagine ≠<br/> System. Photo. DateTaken:-[] ¹<br/> System. Kind: &lt; &gt; immagine<br/> System. Kind: non immagine<br/> System. Kind:--immagine<br/></td>
<td>La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine.<br/> Il valore della proprietà <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> è.<br/> La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine. <br/> La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine. <br/> Gli operatori Double non applicati alla stessa proprietà non vengono annullati. System. Kind:--Picture, quindi, è equivalente a System. Kind:-Picture e System. Kind: NOT Picture.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHAN</td>
<td>&lt;<br/></td>
<td>System. Size: &lt; 1 KB<br/></td>
<td>Questo valore è minore di <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHAN</td>
<td>&gt;<br/></td>
<td>System. ItemDate: &gt; System. StructuredQueryType. DateTime # today<br/></td>
<td>Questo valore è maggiore di <em>oggi</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_LESSTHANOREQUAL</td>
<td>&lt;=<br/> ≤<br/></td>
<td>System. Size: &lt; = 1 KB<br/></td>
<td>Questo valore è minore o uguale a <em>1 KB</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_GREATERTHANOREQUAL</td>
<td>&gt;=<br/> ≥<br/></td>
<td>System. Size: &gt; = 1 KB<br/></td>
<td>Questo valore è uguale o maggiore di <em>1 KB</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_STARTSWITH</td>
<td>~&lt;<br/></td>
<td>System. FileName: ~ Nozioni di &lt; &quot; primo in C++&quot;<br/></td>
<td>Trova gli elementi in cui il nome del file inizia con i caratteri C++ nozioni di &quot; <em>fondo</em> &quot; .<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_ENDSWITH</td>
<td>~&gt;<br/></td>
<td>System. Photo. CameraModel: ~ &gt; non<br/></td>
<td>Trova gli elementi in cui il valore della proprietà termina con i caratteri <em>non</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_VALUE_CONTAINS</td>
<td>~=<br/> ~~<br/></td>
<td>System. Subject. ~ = Round <br/> System. search. AutoSummary: ~ ~ Round<br/></td>
<td>Trova un messaggio con questa stringa nell'oggetto e corrisponde a &quot; g regole<em>arrotondate</em> , &quot; ad esempio.<br/> Trova tutti gli elementi con un riepilogo che contiene i caratteri <em>arrotondati</em>.<br/></td>
</tr>
<tr class="even">
<td>COP_VALUE_NOTCONTAINS</td>
<td>~!<br/></td>
<td>System. Author: ~! &quot; Sanjay&quot;<br/></td>
<td>Trova gli autori che non hanno la sequenza di caratteri &quot; <em>Sanjay</em> &quot; .<br/></td>
</tr>
<tr class="odd">
<td>COP_DOSWILDCARDS</td>
<td>~ <br/></td>
<td>System. FileName: ~ &quot; MIC? osoft W * d&quot;<br/></td>
<td>Trova i file in cui il nome del file inizia con <em>MIC</em>, seguito da un carattere, seguito da <em>osoft w</em>, seguito da tutti i caratteri che terminano con <em>d</em>. <br/> Il carattere ? e * i caratteri non vengono interpretati letteralmente e funzionano come i caratteri jolly di tipo DOS:<br/>
<ul>
<li>? corrisponde a un carattere arbitrario.</li>
<li>* trova la corrispondenza di zero o più caratteri arbitrari.</li>
</ul></td>
</tr>
<tr class="even">
<td>COP_WORD_EQUAL</td>
<td>$=<br/> $$<br/></td>
<td>System. StructuredQuery. Virtual. from: $ = &quot; Sanjay Jacobs&quot;<br/></td>
<td>Per Windows 7 e versioni successive. Trova la frase &quot; <em>Sanjay Jacobs</em> &quot; in tutte le proprietà di. La parola <em>Sanjay</em> deve essere seguita dalla parola <em>Jacobs</em>.<br/></td>
</tr>
<tr class="odd">
<td>COP_WORD_STARTSWITH</td>
<td>$<<br/></td>
<td>System. Author: $<&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td>Per Windows 7 e versioni successive. Trova un elemento in cui l'autore contiene una parola che inizia con i caratteri &quot; <em>San</em> &quot; .<br/> Trova tutti i file in cui il nome file contiene una parola che inizia con <em>micro</em>, seguita da una parola che inizia con <em>exe</em>.<br/></td>
</tr>
</tbody>
</table>



 

¹ parentesi quadre vuote ( \[ \] ) indica "nessun valore".

Per le proprietà di stringa l'operazione predefinita è COP \_ Word \_ inizia \_ con o COP \_ Word \_ Equal.

### <a name="query-values"></a>Valori di query

Nella tabella seguente sono elencati alcuni esempi utili di come è possibile limitare i valori di query.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Qualsiasi sequenza di caratteri in cui è possibile cercare. La stringa non deve contenere spazi vuoti o combinazioni di caratteri che fanno parte della sintassi. Questo esempio cerca una parola che inizia con <em>auto</em>.<br/></td>
</tr>
<tr class="even">
<td>Stringa tra virgolette &quot;&quot;</td>
<td>&quot;CONCLUSIONI: valido &quot; &quot; il &quot; &quot; Blue &quot; &quot; Team&quot;<br/></td>
<td>Qualsiasi sequenza di caratteri. La stringa non viene interpretata come parte della sintassi.<br/> Le virgolette possono essere incluse in una query se sono raddoppiate. In questo esempio viene eseguita <em>la ricerca del &quot; Blue &quot; Team</em>.<br/></td>
</tr>
<tr class="odd">
<td>Integer</td>
<td>5678<br/></td>
<td>Usare solo cifre per numeri interi. Non usare alcun separatore per le migliaia.<br/></td>
</tr>
<tr class="even">
<td>Numero a virgola mobile</td>
<td>5678,1234<br/></td>
<td>Poiché i formati a virgola mobile variano tra le impostazioni locali, una query canonica non può utilizzare una costante a virgola mobile. L'uso della sintassi canonica con numeri a virgola mobile non è sicuro per la localizzazione. <br/></td>
</tr>
<tr class="odd">
<td>Booleano <strong>true</strong> / <strong>false</strong></td>
<td>System. noread: = System. StructuredQueryType. Boolean # true<br/> System. IsEncrypted:-System. StructuredQueryType. Boolean # false<br/></td>
<td>Valore booleano <strong>true</strong> .<br/> Valore booleano <strong>false</strong> .<br/></td>
</tr>
<tr class="even">
<td>[]</td>
<td>System. Keywords: = []<br/></td>
<td>Le parentesi quadre vuote indicano che non esiste alcun valore. In questo esempio vengono trovati tutti gli elementi che non sono stati contrassegnati. <br/></td>
</tr>
<tr class="odd">
<td>Date assolute</td>
<td>System. ItemDate: 1/26/2010<br/> SystemDateModified 10/15/2002 19:00<br/></td>
<td>Trova gli elementi con una data di 26 gennaio 2010.<br/> Trova gli elementi modificati il 15 ottobre 2002 tra le ore 19:00:00 e 19:00:59. <br/>
<blockquote>
[!Note]<br />
Poiché i formati di data, ad esempio i formati a virgola mobile, variano tra le impostazioni locali, l'uso della sintassi canonica con date assolute non è supportato e non è sicuro per la localizzazione.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Date relative</td>
<td>System. ItemDate: System. StructuredQueryType. DateTime # today<br/> System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth<br/> System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear<br/></td>
<td>Trova gli elementi con la data odierna.<br/> Trova gli elementi con una data nel mese successivo.<br/> Trova gli elementi con una data nell'ultimo anno.<br/>
<blockquote>
[!Note]<br />
Oltre a eseguire ricerche in base a intervalli di date e date specifici, AQS riconosce i valori relativi alla data, ad esempio <em>Today</em>, <em>Tomorrow</em>, <em>NEXTWEEK</em>, <em>NEXTMONTH</em>, e Day, ad esempio <em>Tuesday</em> o <em>Monday. Mercoledì</em>) e mese (<em>febbraio</em>).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>..</td>
<td>System. ItemDate: 11/05/04.. 11/10/04 System. Size: 5 KB.. 10kb<br/></td>
<td>I punti doppi indicano un intervallo di valori. Trova gli elementi con una data compresa tra 11/05/04 e 11/10/04 inclusi.<br/> Trova gli elementi compresi tra 5 e 10KB.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a>Limitazioni dell'ambito

Gli utenti possono limitare l'ambito delle proprie ricerche a percorsi di cartelle o archivi dati specifici. Se, ad esempio, si utilizzano più account di posta elettronica e si desidera limitare una query a Microsoft Outlook o Microsoft Outlook Express, è possibile `System.Search.Store:mapi` utilizzare `System.Search.Store:oe` rispettivamente o. La tabella seguente illustra alcuni esempi di come limitare una ricerca in base all'archivio dati.



| Limita la ricerca per archivio dati  | Parola chiave | Esempio                                     |
|--------------------------------|---------|---------------------------------------------|
| File                          | file    | System. search. Store: file                    |
| Outlook                        | MAPI    | System. search. Store: MAPI                    |
| Outlook Express                | OE      | System. search. Store: OE                      |
| File offline                  | CSC     | System. search. Store: CSC                     |
| Cartella specifica nell'unità locale | folder  | System. ItemFolderNameDisplay: C: " \\ cartella" |



 

## <a name="additional-resources"></a>Risorse aggiuntive

-   In Windows 7 e versioni successive, può essere disponibile un'opzione di menu di scelta rapida a seconda che venga soddisfatta una condizione AQS. Per ulteriori informazioni, vedere "recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata" nella sezione [creazione di gestori di menu di scelta rapida](../shell/context-menu-handlers.md).
-   Le query AQS possono essere limitate a specifici tipi di file, noti come tipi di file. Per altre informazioni, vedere [tipi di file e associazioni](../shell/fa-intro.md). Per la documentazione di riferimento della proprietà, vedere [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
