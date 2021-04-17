---
description: Le condizioni che determinano se un documento viene incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Clausola WHERE (ricerca di Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306108"
---
# <a name="where-clause-windows-search"></a>Clausola WHERE (ricerca di Windows)

Le condizioni che determinano se un documento viene incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE. Al livello più alto, esistono due parti della sintassi della clausola WHERE:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



L'alias facoltativo del gruppo di <\_> parte della clausola semplifica le query complesse assegnando un alias a un gruppo di una o più colonne. Questo può migliorare la leggibilità di query complesse che cercano le stesse informazioni in più colonne specificate dagli URL. Per ulteriori informazioni sugli alias di gruppo, vedere [con il predicato alias gruppo As](-search-sql-with-as.md).

La <search condition> parte della clausola WHERE è uno o più predicati di ricerca che specificano i criteri di corrispondenza per la ricerca. I predicati di ricerca sono espressioni che asseriscono un certo valore.

Il risultato di una condizione di ricerca è un valore booleano, **true** se il documento soddisfa le condizioni di ricerca specificate; in caso contrario, **false** . Se il risultato è **true**, viene restituito il documento. Se il risultato è **false**, il documento non viene restituito. Ai documenti restituiti in una query di ricerca di Microsoft Windows sono assegnati valori di classificazione in base alle condizioni di ricerca corrispondenti. Ogni condizione di ricerca di query può includere una clausola [RANKBY](-search-sql-rankby.md) che supporta la modifica dei valori di rango restituiti.

La [funzione ReuseWhere](-search-sql-reusewhere.md) esegue più query che utilizzano le stesse condizioni di ricerca più efficienti. La clausola WHERE in una query specifica il set di elementi che corrispondono a una query. Le query successive possono condividere il lavoro eseguito per il valutazione precedente usando la funzione ReuseWhere nella nuova clausola WHERE della query.

## <a name="search-predicates"></a>Cerca predicati

Una condizione di ricerca è costituita da uno o più predicati o da condizioni di ricerca che descrivono ciò che l'utente sta cercando (ad esempio, dove System. DateCreated >' 2006-04-19'). I predicati di ricerca possono essere combinati usando gli operatori logici **and**, **or** o **not**. L'operatore unario facoltativo **not** può essere utilizzato solo con **e** e solo per negare il valore logico di un predicato o di una condizione di ricerca. È possibile usare le parentesi per raggruppare e annidare i termini logici.

Nella tabella seguente viene illustrato l'ordine di precedenza per gli operatori logici.



| Ordine (precedenza) | Operatore logico |
|--------------------|------------------|
| Primo (massimo)    | **NOT**          |
| Second             | **AND**          |
| Terzo (minimo)     | **OR**           |



 

Gli operatori logici dello stesso tipo sono associativi e non esiste alcun ordine di calcolo specificato. È ad esempio possibile calcolare (a **e** B) **e** (c **e** d) (a **e** d) **e** (B **e** C) senza alcuna modifica nel risultato logico.

> [!IMPORTANT]
>
> Errato: WHERE **not** Contains (' computer ')
>
> Corretto: WHERE CONTAINs (' software ') **e not** Contains (' computer ')

 

Nelle query complesse, è consigliabile inserire più enfasi sulle corrispondenze in alcune colonne rispetto alle altre. Ad esempio, durante la ricerca di documenti che discutono "progettazione software", trovare il termine di ricerca nel titolo del documento è più probabile che sia una corrispondenza migliore rispetto alla ricerca delle singole parole nel testo del documento. Per influenzare la classificazione dei documenti in questo modo, il linguaggio di query di ricerca di Microsoft Windows supporta la ponderazione delle condizioni di ricerca. Per ulteriori informazioni sulla ponderazione delle colonne, vedere il predicato [Contains](-search-sql-contains.md) e il [predicato FREETEXT](-search-sql-freetext.md).

Sono disponibili tre gruppi di predicati di ricerca in Windows Search: ricerca full-text, non full-text e profondità cartella. I predicati di ricerca full-text in genere corrispondono al significato del contenuto, del titolo e di altre colonne e supportano la corrispondenza linguistica (ad esempio, moduli Word alternativi, frasi e ricerca vicina). I predicati di ricerca non full-text, invece, corrispondono al valore delle colonne specificate e non includono alcuna elaborazione linguistica speciale, ma in molti casi offrono criteri di ricerca basati su caratteri. I predicati di profondità della cartella limitano l'ambito di ricerca a un percorso specificato.

> [!Note]  
> Se la query restituisce un documento perché un predicato non full-text restituisce **true** per quel documento, il valore di pertinenza viene calcolato come 1000. L'utilizzo della [funzione di coercizione Rank](-search-sql-rankby.md) può modificare il valore di pertinenza.

 

Nelle tabelle seguenti vengono descritti i predicati di ricerca full-text, non full-text e Depth.



| Predicato full-text                  | Descrizione                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Supporta ricerche complesse per i termini nelle colonne di testo del documento, ad esempio titolo, contenuto. Consente di cercare forme flesse dei termini di ricerca, di verificare la vicinanza dei termini e di eseguire confronti logici. I termini di ricerca possono includere caratteri jolly. |
| [FREETEXT](-search-sql-freetext.md) | Cerca i documenti che corrispondono al significato della frase di ricerca. Parole correlate e frasi simili corrisponderanno, con la colonna Rank calcolata in base alla precisione del documento corrispondente alla frase di ricerca. I termini di ricerca non possono includere caratteri jolly.  |



 



| Predicato non full-text                                                    | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | I valori della colonna vengono confrontati usando semplici criteri di ricerca con caratteri jolly.                                                                                                    |
| [Confronto di valori letterali](-search-sql-literalvaluecomparison.md)         | I valori delle colonne vengono confrontati con stringhe, date, timestamp, numerici e altri valori letterali. Questo predicato supporta l'uguaglianza e le disuguaglianze, ad esempio maggiore di e minore di. |
| [Confronti multivalore (matrice)](-search-sql-multivaluedcomparisons.md) | Le colonne multivalore vengono confrontate con una matrice multivalore di valori letterali.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | I valori di colonna non definiti per il documento possono essere rilevati usando il predicato **null** .                                                                                    |



 



| Profondità cartella                             | Descrizione                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [AMBITO](-search-sql-folderdepth.md)     | Esegue un attraversamento profondo del percorso specificato, inclusa la cartella specifica e tutte le sottocartelle. |
| [DIRECTORY](-search-sql-folderdepth.md) | Esegue un attraversamento superficiale del percorso specificato, eseguendo la ricerca solo nella cartella specifica.            |



 

## <a name="examples"></a>Esempio

Per esempi della clausola WHERE, vedere i singoli argomenti del predicato collegati nella tabella precedente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[ReuseWhere (funzione)](-search-sql-reusewhere.md)
</dt> <dt>

[Proprietà del set di righe](-search-sql-rowset-properties.md)
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[Panoramica della sintassi SQL di ricerca](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[CON il predicato alias gruppo AS](-search-sql-with-as.md)
</dt> <dt>

[Predicati di ambito e DIRECTORY](-search-sql-folderdepth.md)
</dt> <dt>

[RANGO per clausola](-search-sql-rankby.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



