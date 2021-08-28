---
description: L'oggetto GROUP ON...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: GROUP ON ... OLTRE... Affermazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882013"
---
# <a name="group-on--over--statement"></a>GROUP ON ... OLTRE... Affermazione

L'oggetto GROUP ON... OLTRE... L'istruzione restituisce un set di righe gerarchico in cui i risultati della ricerca sono suddivisi in gruppi basati su una colonna specificata e intervalli di raggruppamento facoltativi. Se si raggruppa la colonna [System.Kind,](../properties/props-system-kind.md) il set di risultati viene diviso in più gruppi: uno per i documenti, uno per le comunicazioni e così via. Se si raggruppa in base a [System.Size](../properties/props-system-size.md) e all'intervallo di gruppi 100 KB, il set di risultati viene diviso in tre gruppi: elementi di dimensioni < 100 KB, elementi di dimensioni >= 100 KB e elementi senza valore di dimensione. È anche possibile aggregare raggruppamenti con funzioni.

In questo argomento vengono trattati gli argomenti seguenti:

-   [Sintassi](#syntax)
-   [Intervalli di gruppi](#group-ranges)
-   [Etichettatura di gruppi](#labeling-groups)
-   [Ordinamento dei gruppi](#ordering-groups)
-   [Annidamento di gruppi](#nesting-groups)
-   [Raggruppamento in base alle proprietà del vettore](#grouping-on-vector-properties)
-   [Altri esempi](#more-examples)
-   [Argomenti correlati](#related-topics)

## <a name="syntax"></a>Sintassi

L'oggetto GROUP ON ... OLTRE... L'istruzione ha la sintassi seguente:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



dove gli intervalli di raggruppamento sono definiti come segue:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



La colonna GROUP ON &lt; può essere un identificatore normale o delimitato per una proprietà &gt; nell'archivio delle proprietà. [](-search-sql-identifiers.md)

L'elemento facoltativo è un elenco di uno o più valori (numero, data o stringa) usati per <group ranges> dividere i risultati in gruppi. identifica <range limit> un punto di divisione nel set di risultati restituito e identifica <label> un'etichetta descrittiva per un gruppo. È possibile dividere il set di risultati in tutti i gruppi necessari.

Il primo gruppo di risultati include gli elementi con il valore minimo possibile per la proprietà specificata, ma senza includere il primo limite di intervallo. È possibile fare riferimento a questo gruppo con la parola chiave MINVALUE. È possibile fare riferimento al secondo gruppo con l'identificatore di limite di intervallo stesso e include gli elementi il cui valore per la proprietà specificata è uguale o maggiore del limite di intervallo. Tutti gli elementi che non hanno un valore per la proprietà specificata vengono restituiti per ultimi e possono essere indicati con la **parola chiave NULL.**

Ad esempio, un limite di intervallo "2006-01-01" per la proprietà [System.DateCreated](../properties/props-system-datecreated.md) divide il set di risultati in elementi con date precedenti al 01/01/2006 (gruppo MINVALUE), elementi con date in data successiva al 01/01/2006 (gruppo 2006-01-01) e elementi senza data (gruppo **NULL).**

All'interno di ogni gruppo, i risultati vengono ordinati in base ai valori nella colonna GROUP ON per impostazione predefinita. La clausola [ORDER BY](-search-sql-orderby.md) facoltativa può contenere un identificatore di direzione di ASC per l'ordine crescente (da basso a alto) o DESC per l'ordine decrescente (dall'alto al basso) e la clausola ORDER IN [GROUP BY](-search-sql-orderingroup.md) può ordinare ogni gruppo usando regole diverse. Per altre [informazioni, vedere la sezione](#ordering-groups) Ordinamento dei gruppi più avanti.

## <a name="group-ranges"></a>Intervalli di gruppi

La tabella seguente illustra come i risultati vengono divisi in gruppi in base ai limiti di intervallo:



| Esempio ( &lt; intervalli &gt; \[ di gruppi di colonne \] )        | Risultato                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System.Size \[ 1000, 5000\]                       | I risultati sono raggruppati in quattro bucket: **MINVALUE:** dimensioni < 1000<br/> **1000:** 1000 <= Dimensioni < 5000<br/> **5000:** Dimensioni >= 5000<br/> **NULL:** Nessun valore per Size<br/>                                                                      |
| System.Author \[ BEFORE('m'),AFTER('r')\]         | I risultati sono raggruppati in quattro bucket: **MINVALUE:** Autore < carattere prima di "m"<br/> **m:** carattere prima di "m" <= autore < carattere dopo "r"<br/> **r:** carattere dopo "r" <= Autore<br/> **NULL:** Nessun valore per Author<br/>      |
| System.Author \[ MINVALUE/'a to l',"m"/'m to z'\] | I risultati sono raggruppati in tre bucket: **a to l:** Author < "m"<br/> **da m a z:** "m" <= Autore <br/> **NULL:** Nessun valore per Author<br/>                                                                                                               |
| System.DateCreated \[ '2005-1-01','2006-6-01'\]   | I risultati sono raggruppati in quattro bucket:<br/> **MINVALUE:** DateCreated < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **NULL:** Nessun valore per DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Errato: `GROUP ON System.Author['m','z','a']`
>
> Corretta: `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Etichettatura di gruppi

Per migliorare la leggibilità, è possibile etichettare i gruppi usando la sintassi seguente:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



L'etichetta è separata dal limite dell'intervallo con una barra ed è racchiusa tra virgolette singole. Se non si specifica un'etichetta, il nome del gruppo è la stringa del limite di intervallo.

Di seguito è riportato un esempio di etichettatura dei gruppi:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



In Windows 7 o versioni successive è anche possibile usare un'etichetta \[ OTHER \] generica per combinare più intervalli di raggruppamento. I risultati di tutti i gruppi identificati con questa etichetta verranno combinati in un unico gruppo con questa etichetta. Questo gruppo di risultati viene restituito dopo tutti gli altri gruppi ad eccezione del **gruppo NULL.** Il **gruppo NULL** contiene i risultati per gli elementi che non hanno un valore per la proprietà specificata. Prima di Windows 7, \[ l'etichetta OTHER \] viene considerata come qualsiasi altra etichetta di gruppo.

Il codice seguente è un esempio dell'uso dell'etichetta OTHER per i gruppi che verranno \[ \] creati in Windows 7 o versioni successive:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



La tabella seguente illustra i gruppi che verrebbero creati dal codice di raggruppamento precedente in Windows 7 o versioni successive.



| Group     | System.Author | System.FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Regina         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| S         | Zara          | amet.docx       |
| \[ALTRO\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Ordinamento dei gruppi

Esistono tre modi per ordinare gli elementi in gruppi:

-   Ordinamento predefinito: se non si specifica diversamente, i risultati vengono ordinati in base ai valori nella colonna GROUP ON, in ordine crescente.
-   ORDER BY: è possibile specificare l'ordine decrescente in una clausola ORDER BY. È necessario ordinare i risultati in base alla colonna GROUP ON.
-   ORDER IN GROUP BY: è possibile specificare un ordine diverso per ogni gruppo. Se si raggruppa in [Base a System.Kind](../properties/props-system-kind.md), è possibile ordinare i documenti in base [a System.Author](../properties/props-system-author.md) e music in base [a System.Musica. Artista.](../properties/props-system-music-artist.md)

Per altre informazioni sull'ordinamento dei risultati, vedere le pagine di riferimento relative alla [clausola ORDER BY](-search-sql-orderby.md) e alla clausola [ORDER IN GROUP.](-search-sql-orderingroup.md)

## <a name="nesting-groups"></a>Annidamento di gruppi

È possibile annidare gruppi con più clausole GROUP ON. L'ordine specificato nella query si riflette direttamente nella gerarchia dei gruppi di output, come illustrato nell'esempio seguente.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System.Kind    | System.Author | System.DateCreated |
|----------------|---------------|--------------------|
| documenti      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| (DIP) interno | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Raggruppamento in base alle proprietà del vettore

Il raggruppamento in base alle proprietà del vettore, che possono contenere uno o più valori contemporaneamente, confronta i valori del vettore singolarmente per impostazione predefinita. Ad esempio, se è presente un documento, Lorem.docx, con la proprietà System.Author impostata su "Theresa; Zara" e un altro documento, Ipsum.docx, con la proprietà System.Author impostata su "Zara", la query restituisce il set di risultati in due gruppi, come illustrato di seguito:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System.FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Come si può vedere, il raggruppamento in base alle proprietà del vettore restituisce righe duplicate. Lorem.docx due volte perché ha due autori.

 

## <a name="more-examples"></a>Altri esempi


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni di aggregazione](-search-sql-aggregates.md)
</dt> <dt>

[Clausola ORDER BY](-search-sql-orderby.md)
</dt> <dt>

[Clausola ORDER IN GROUP](-search-sql-orderingroup.md)
</dt> </dl>

 

 
