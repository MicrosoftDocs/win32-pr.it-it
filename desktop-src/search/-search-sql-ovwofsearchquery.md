---
description: Il Structured Query Language di Windows Search (SQL) è simile a una query SQL standard.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Panoramica della sintassi SQL di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049385"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Panoramica della sintassi SQL di Windows Search

Il Structured Query Language di Windows Search (SQL) è simile a una query SQL standard. Viene illustrato nelle due sintassi seguenti:


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

Nell'esempio di query seguente vengono restituiti i valori conteggio pagine e Data creazione per tutti i documenti con più di 50 pagine, ordinate in ordine crescente di conteggio delle pagine.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

La sintassi di query di Windows Search supporta molte opzioni, consentendo query più complesse.

Nella tabella seguente viene descritta ogni clausola nelle istruzioni SELECT o GROUP ON e le funzionalità supportate.

| Clausola                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [RAGGRUPPA IN... SOPRA...](-search-sql-group-on-over.md) | Specifica come raggruppare i risultati restituiti dalla query. È possibile specificare gli intervalli in base ai quali raggruppare e specificare più di una colonna per il raggruppamento. È possibile, ad esempio, raggruppare i risultati in base a un intervallo di dimensioni dei file (Size < 100, 100 <= size < 1000; 1000 <= size) e nidificare i raggruppamenti.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Specifica le colonne restituite dalla query.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Specifica il computer e il catalogo in cui eseguire la ricerca.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Specifica ciò che costituisce un documento corrispondente. Questa clausola include molte opzioni, che consentono un controllo completo sulle condizioni di ricerca. Ad esempio, è possibile trovare una corrispondenza con parole, frasi, forme di Word flessori, stringhe, valori numerici e bit per bit e matrici multivalore. È anche possibile applicare pesi statistici alle condizioni di corrispondenza e combinare le condizioni di corrispondenza con gli operatori booleani. |
| [ORDER BY](-search-sql-orderby.md)                 | Specifica l'ordinamento per i risultati restituiti dalla query. È possibile specificare più di un campo in base al quale vengono ordinati i risultati ed è possibile utilizzare l'ordinamento crescente o decrescente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Esempi di codice

Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e Windows Search tramite SQL. Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni Windows Search e due metodi aggiuntivi per recuperare i risultati da Windows Search. Entrambi gli esempi sono disponibili in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[Valori letterali](-search-sql-literals.md)

[Uso di ricerche localizzate](-search-sql-usinglocsearches.md)

[Informazioni sui valori di pertinenza](-search-sql-understandingrelevancevalues.md)

[Mapping delle proprietà](-search-3x-wds-propertymappings.md)

[Sintassi di ricerca avanzata](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Informazioni concettuali

[Estensioni SQL in Microsoft Windows Search](-search-sql-extensions-sps.md)

[Funzionalità SQL non disponibili in Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificatori](-search-sql-identifiers.md)

[Distinzione maiuscole/minuscole nelle ricerche](-search-sql-casesensitivityinsearches.md)

[Distinzione tra segni diacritici nelle ricerche](-search-sql-accentinsensitivitysearches.md)

[Cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md)

[Mapping dei tipi di dati](-search-sql-datatypemappings.md)
