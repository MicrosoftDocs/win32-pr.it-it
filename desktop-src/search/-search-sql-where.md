---
description: Le condizioni che determinano se un documento è incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Clausola WHERE (Windows ricerca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462403"
---
# <a name="where-clause-windows-search"></a>Clausola WHERE (Windows ricerca)

Le condizioni che determinano se un documento è incluso nei risultati restituiti dalla query vengono specificate dalla clausola WHERE. Al livello più alto, la sintassi della clausola WHERE è in due parti:


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



L'alias <gruppo> parte della clausola semplifica le query complesse assegnando un alias a un gruppo di \_ una o più colonne. In questo modo è possibile migliorare la leggibilità delle query complesse che ricercano le stesse informazioni in più colonne specificate dagli URL. Per altre informazioni sugli alias di gruppo, [vedere WITH -- AS Group Alias Predicate](-search-sql-with-as.md).

La <search condition> parte della clausola WHERE è uno o più predicati di ricerca che specificano i criteri di corrispondenza per la ricerca. I predicati di ricerca sono espressioni che asserzioneno alcuni fatti su un valore.

Il risultato di una condizione di ricerca è un valore booleano, **TRUE** se il documento soddisfa le condizioni di ricerca specificate oppure **FALSE** in caso contrario. Se il risultato è **TRUE,** viene restituito il documento. Se il risultato è **FALSE,** il documento non viene restituito. Ai documenti restituiti in una query Windows Ricerca di Microsoft vengono assegnati valori di classificazione in base al livello di corrispondenza delle condizioni di ricerca. Ognuna delle condizioni di ricerca della query può includere una [clausola RANKBY](-search-sql-rankby.md) che supporta la modifica dei valori di classificazione restituiti.

La [funzione ReuseWhere](-search-sql-reusewhere.md) rende più efficienti più query che usano alcune delle stesse condizioni di ricerca. La clausola WHERE in una query specifica il set di elementi che corrispondono in una query. Le query successive possono condividere il lavoro eseguito per l'evaluzione precedente usando la funzione ReuseWhere nella nuova clausola WHERE della query.

## <a name="search-predicates"></a>Predicati di ricerca

Una condizione di ricerca è costituita da uno o più predicati o condizioni di ricerca che descrivono ciò che l'utente sta cercando ,ad esempio WHERE System.DateCreated >'2006-04-19'). I predicati di ricerca possono essere combinati usando gli operatori logici **AND**, **OR** o **NOT**. L'operatore unario **facoltativo NOT** può essere usato solo con **AND** e solo per negare il valore logico di un predicato o di una condizione di ricerca. È possibile usare le parentesi per raggruppare e annidare termini logici.

Nella tabella seguente viene illustrato l'ordine di precedenza per gli operatori logici.



| Order (precedenza) | Operatore logico |
|--------------------|------------------|
| Primo (più alto)    | **NOT**          |
| Secondo             | **AND**          |
| Terzo (più basso)     | **OR**           |



 

Gli operatori logici dello stesso tipo sono associativi e non esiste un ordine di calcolo specificato. Ad esempio, (A **AND** B) **AND** (C **AND** D) può essere calcolato (A **AND** D) **AND** (B **AND** C) senza alcuna modifica nel risultato logico.

> [!IMPORTANT]
>
> Non corretto: WHERE **NOT** CONTAINS ('computer')
>
> Corretto: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')

 

Nelle query complesse può essere necessario mettere in risalto le corrispondenze in alcune colonne rispetto ad altre. Ad esempio, quando si cercano documenti che illustrano la "progettazione software", trovare il termine di ricerca nel titolo del documento è più probabile che sia una buona corrispondenza rispetto a trovare le singole parole nel testo del documento. Per influenzare la classificazione dei documenti in questo modo, il linguaggio di query Di ricerca di Microsoft Windows supporta la ponderazione delle condizioni di ricerca. Per altre informazioni sulla ponderazione delle colonne, vedere [PREDICATO CONTAINS](-search-sql-contains.md) e [PREDICATO FREETEXT](-search-sql-freetext.md).

Esistono tre gruppi di predicati di ricerca Windows ricerca: ricerche full-text, non full-text e di profondità delle cartelle. I predicati di ricerca full-text in genere corrispondono al significato del contenuto, del titolo e di altre colonne e supportano la corrispondenza linguistica , ad esempio forme di parole alternative, frasi e ricerca di prossimità. Al contrario, i predicati di ricerca non full-text corrispondono al valore delle colonne specificate e non includono alcuna elaborazione linguistica speciale, ma in diversi casi offrono criteri di ricerca basati su caratteri. I predicati di profondità delle cartelle limitano l'ambito di ricerca a un percorso specificato.

> [!Note]  
> Se la query restituisce un documento perché un predicato non full-text restituisce **TRUE** per tale documento, il valore di classificazione viene calcolato come 1000. [L'uso della funzione di coercizione rank](-search-sql-rankby.md) può modificare il valore di classificazione.

 

Le tabelle seguenti descrivono i predicati di ricerca full-text, non full-text e di profondità della cartella.



| Predicato full-text                  | Descrizione                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Supporta ricerche complesse di termini nelle colonne di testo del documento (ad esempio, titolo, contenuto). Può cercare forme gonfiate dei termini di ricerca, testare la prossimità dei termini ed eseguire confronti logici. I termini di ricerca possono includere caratteri jolly. |
| [FREETEXT](-search-sql-freetext.md) | Cerca i documenti che corrispondono al significato della frase di ricerca. Parole correlate e frasi simili corrisponderanno, con la colonna di classificazione calcolata in base alla corrispondenza tra il documento e la frase di ricerca. I termini di ricerca non possono includere caratteri jolly.  |



 



| Predicato non full-text                                                    | Descrizione                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | I valori delle colonne vengono confrontati usando criteri di ricerca semplici con caratteri jolly.                                                                                                    |
| [Confronto tra valori letterali](-search-sql-literalvaluecomparison.md)         | I valori delle colonne vengono confrontati con valori stringa, data, timestamp, numerici e altri valori letterali. Questo predicato supporta l'uguaglianza e le disuguaglianze, ad esempio maggiore di e minore di. |
| [Confronti multivalore (ARRAY)](-search-sql-multivaluedcomparisons.md) | Le colonne multivalore vengono confrontate con una matrice multivalore di valori letterali.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | I valori di colonna non definiti per il documento possono essere rilevati usando il predicato **NULL.**                                                                                    |



 



| Profondità cartella                             | Descrizione                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Ambito](-search-sql-folderdepth.md)     | Esegue un attraversamento profondo del percorso specificato, incluse la cartella specifica e tutte le sottocartelle. |
| [Directory](-search-sql-folderdepth.md) | Esegue un attraversamento superficiale del percorso specificato, cercando solo la cartella specifica.            |



 

## <a name="examples"></a>Esempio

Per esempi della clausola WHERE, vedere i singoli argomenti relativi ai predicati collegati nella tabella precedente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Funzione ReuseWhere](-search-sql-reusewhere.md)
</dt> <dt>

[Proprietà del set di righe](-search-sql-rowset-properties.md)
</dt> <dt>

[Clausola FROM](-search-sql-from.md)
</dt> <dt>

[Panoramica della sintassi SQL ricerca](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[WITH -- Predicato alias gruppo AS](-search-sql-with-as.md)
</dt> <dt>

[Predicati SCOPE e DIRECTORY](-search-sql-folderdepth.md)
</dt> <dt>

[Clausola RANK BY](-search-sql-rankby.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Predicati full-text](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Predicati non full-text](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



