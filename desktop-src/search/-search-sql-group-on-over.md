---
description: GRUPPO su...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: RAGGRUPPA IN... SOPRA... Istruzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d7087305f0a5a86f0288ed92ec4bda5b8c882c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128542"
---
# <a name="group-on--over--statement"></a>RAGGRUPPA IN... SOPRA... Istruzione

GRUPPO su... SOPRA... l'istruzione restituisce un set di righe gerarchico in cui i risultati della ricerca sono divisi in gruppi in base a una colonna specificata e a intervalli di raggruppamento facoltativi. Se si raggruppa sulla colonna [System. Kind](../properties/props-system-kind.md) , il set di risultati è diviso in più gruppi: uno per i documenti, uno per le comunicazioni e così via. Se si esegue il raggruppamento in [System. Size](../properties/props-system-size.md) e l'intervallo di gruppi 100 KB, il set di risultati è diviso in tre gruppi: elementi di dimensioni < 100 KB, elementi di dimensioni >= 100 KB ed elementi senza valore size. È anche possibile aggregare i raggruppamenti con funzioni.

In questo argomento vengono illustrati gli argomenti seguenti:

-   [Sintassi](#syntax)
-   [Intervalli di gruppi](#group-ranges)
-   [Assegnazione di etichette ai gruppi](#labeling-groups)
-   [Ordinamento di gruppi](#ordering-groups)
-   [Annidamento di gruppi](#nesting-groups)
-   [Raggruppamento di proprietà vettoriali](#grouping-on-vector-properties)
-   [Altri esempi](#more-examples)
-   [Argomenti correlati](#related-topics)

## <a name="syntax"></a>Sintassi

GRUPPO su... SOPRA... la sintassi dell'istruzione è la seguente:


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



dove gli intervalli di raggruppamento vengono definiti come segue:


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



Il gruppo in <column> può essere un [identificatore](-search-sql-identifiers.md) regolare o delimitato per una proprietà nell'archivio delle proprietà.

Il parametro facoltativo <group ranges> è un elenco di uno o più valori (numero, data o stringa) usati per dividere i risultati in gruppi. <range limit>Identifica un punto di divisione nel set di risultati restituito e <label> identifica un'etichetta intuitiva per un gruppo. È possibile dividere il set di risultati in tutti i gruppi necessari.

Il primo gruppo di risultati include gli elementi con il valore minimo possibile per la proprietà specificata fino al limite del primo intervallo escluso. È possibile fare riferimento a questo gruppo con la parola chiave MINVALUE. Il secondo gruppo è a cui è possibile fare riferimento con l'identificatore di limite intervallo e include gli elementi il cui valore per la proprietà specificata è maggiore o uguale al limite di intervallo. Gli elementi che non dispongono di un valore per la proprietà specificata vengono restituiti per ultimi e possono essere definiti con la parola chiave **null** .

Ad esempio, un limite di intervallo di ' 2006-01-01' per la proprietà [System. DateCreated](../properties/props-system-datecreated.md) divide il set di risultati in elementi con date precedenti a 2006-01-01 (gruppo MinValue), elementi con date in o dopo 2006-01-01 (2006-01-01 gruppo) ed elementi senza data (gruppo **null** ).

All'interno di ogni gruppo, i risultati vengono ordinati in base ai valori nella colonna gruppo per impostazione predefinita. La clausola [Order by](-search-sql-orderby.md) facoltativa può contenere un identificatore di direzione di ASC per Ascending (da basso a alto) o DESC per la decrescente (da alto a basso) e l' [ordine nella clausola Group by](-search-sql-orderingroup.md) può ordinare ogni gruppo usando regole diverse. Per ulteriori informazioni, vedere la sezione [gruppi di ordini](#ordering-groups) riportata di seguito.

## <a name="group-ranges"></a>Intervalli di gruppi

Nella tabella seguente viene illustrato il modo in cui i risultati vengono suddivisi in gruppi in base ai limiti di intervallo:



| Esempio ( <column> \[ intervalli di gruppi \] )        | Risultato                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System. size \[ 1000, 5000\]                       | I risultati sono raggruppati in quattro bucket: **MinValue**: Size < 1000<br/> **1000:** 1000 <= Size < 5000<br/> **5000:** Dimensioni >= 5000<br/> **Valore null:** Nessun valore per le dimensioni<br/>                                                                      |
| System. Author \[ before (' m'), After (' r ')\]         | I risultati sono raggruppati in quattro bucket: **MinValue:** autore < carattere prima di "m"<br/> **m:** carattere prima di "m" <= autore < carattere dopo "r"<br/> **r:** carattere dopo "r" <= autore<br/> **Valore null:** Nessun valore per autore<br/>      |
| System. Author \[ MinValue/' da a l', "m"/da a z '\] | I risultati sono raggruppati in tre bucket: **da a a l:** autore < "m"<br/> **da m a z:** "m" <= autore <br/> **Valore null:** Nessun valore per autore<br/>                                                                                                               |
| System. DateCreated \[ ' 2005-1-01',' 2006-6-01'\]   | I risultati sono raggruppati in quattro bucket:<br/> **MinValue:** DateCreated < 2005-1-01<br/> **2005-1-01:** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01:** DateCreated >= 2006-6-01<br/> **Valore null:** Nessun valore per DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Errata `GROUP ON System.Author['m','z','a']`
>
> Corretto `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Assegnazione di etichette ai gruppi

Per migliorare la leggibilità, è possibile etichettare i gruppi usando la sintassi seguente:


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



L'etichetta è separata dal limite di intervallo con una barra ed è racchiusa tra virgolette singole. Se non si specifica un'etichetta, il nome del gruppo è la stringa limite intervallo.

Di seguito è riportato un esempio di assegnazione di etichette ai gruppi:


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



In Windows 7 o versioni successive è anche possibile usare un' \[ altra etichetta generica \] per combinare più intervalli di raggruppamento. I risultati di tutti i gruppi identificati con questa etichetta verranno combinati in un gruppo con questa etichetta. Questo gruppo di risultati viene restituito dopo tutti gli altri gruppi ad eccezione del gruppo **null** . Il gruppo **null** contiene i risultati per gli elementi che non hanno un valore per la proprietà specificata. Prima di Windows 7 l' \[ altra \] etichetta veniva considerata come qualsiasi altra etichetta di gruppo.

Il codice seguente è un esempio di utilizzo dell' \[ altra \] etichetta per i gruppi che verrebbero creati in Windows 7 o versioni successive:


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



La tabella seguente illustra i gruppi che verrebbero creati dal codice di raggruppamento precedente in Windows 7 o versioni successive.



| Group     | System.Author | System. FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Regina         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| S         | Zara          | amet.docx       |
| \[ALTRI\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Ordinamento di gruppi

Sono disponibili tre modi per ordinare gli elementi nei gruppi:

-   Ordinamento predefinito: se non si specifica diversamente, i risultati vengono ordinati in base ai valori della colonna GROUP ON, in ordine crescente.
-   ORDER BY: è possibile specificare l'ordine decrescente in una clausola ORDER BY. È necessario ordinare i risultati in base alla colonna GROUP ON.
-   ORDER IN GROUP BY: è possibile specificare un ordine diverso per ogni gruppo. Se si esegue il raggruppamento in [System. Kind](../properties/props-system-kind.md), è possibile ordinare i documenti in base a [System. Author](../properties/props-system-author.md) e Music by [System. Music. Artist](../properties/props-system-music-artist.md).

Per ulteriori informazioni sull'ordinamento dei risultati, vedere le pagine di riferimento della clausola [Order by](-search-sql-orderby.md) e [Order in Group](-search-sql-orderingroup.md) .

## <a name="nesting-groups"></a>Annidamento di gruppi

È possibile annidare gruppi con più clausole GROUP ON. L'ordine specificato nella query viene riflesso direttamente nella gerarchia dei gruppi di output, come illustrato nell'esempio seguente.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System. Kind    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| documenti      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| (DIP) interno | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Raggruppamento di proprietà vettoriali

Raggruppamento di proprietà vettoriali, proprietà che possono contenere uno o più valori contemporaneamente, confronta i valori del vettore singolarmente per impostazione predefinita. Se, ad esempio, è presente un documento, Lorem.docx con la proprietà System. Author di "Theresa; Zara "e un altro documento, Ipsum.docx con la proprietà System. Author come" Zara ", la query restituisce il set di risultati in due gruppi, come illustrato di seguito:


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System. FileName |
|---------------|-----------------|
| Teresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Come si può notare, il raggruppamento di proprietà Vector restituisce righe duplicate. Lorem.docx viene visualizzato due volte perché contiene due autori.

 

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

 

 
