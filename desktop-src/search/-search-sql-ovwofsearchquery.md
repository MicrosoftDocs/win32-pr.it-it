---
description: Il Windows di Structured Query Language (SQL) è simile a una query SQL standard.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Panoramica della sintassi Windows ricerca SQL ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f34f321bef35ab9f5198345a2630d20b80275b794f53a0c47aabf7667f2e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594741"
---
# <a name="overview-of-windows-search-sql-syntax"></a>Panoramica della sintassi Windows ricerca SQL ricerca

Il Windows di Structured Query Language (SQL) è simile a una query SQL standard. È illustrato nelle due sintassi seguenti:


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

Nell'esempio di query seguente vengono restituiti i valori relativi al numero di pagine e alla data di creazione per tutti i documenti con più di 50 pagine, ordinati in ordine crescente rispetto al numero di pagine.

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

La Windows di query di ricerca supporta molte opzioni, consentendo query più complesse.

Nella tabella seguente vengono descritte le clausole nelle istruzioni SELECT o GROUP ON e le funzionalità supportate.

| Clausola                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [GROUP ON... Oltre...](-search-sql-group-on-over.md) | Specifica come raggruppare i risultati restituiti dalla query. È possibile specificare gli intervalli in base ai quali raggruppare e specificare più di una colonna per il raggruppamento. Ad esempio, è possibile raggruppare i risultati in un intervallo di dimensioni di file (dimensioni < 100, 100 <= dimensioni < 1000; 1000 <= dimensioni) e raggruppamenti annidamento.                                                                                                       |
| [SELECT](-search-sql-select.md)                    | Specifica le colonne restituite dalla query.                                                                                                                                                                                                                                                                                                                                                         |
| [FROM](-search-sql-from.md)                        | Specifica il computer e il catalogo in cui eseguire la ricerca.                                                                                                                                                                                                                                                                                                                                                         |
| [WHERE](-search-sql-where.md)                      | Specifica ciò che costituisce un documento corrispondente. Questa clausola include molte opzioni, consentendo un controllo completo sulle condizioni di ricerca. Ad esempio, è possibile trovare una corrispondenza con parole, frasi, forme di parole flesse, stringhe, valori numerici e bit per bit e matrici multivalore. È anche possibile applicare pesi statistici alle condizioni di corrispondenza e combinare condizioni di corrispondenza con operatori booleani. |
| [ORDER BY](-search-sql-orderby.md)                 | Specifica l'ordinamento per i risultati restituiti dalla query. È possibile specificare più campi in base ai quali vengono ordinati i risultati ed è possibile usare l'ordinamento crescente o decrescente.                                                                                                                                                                                                               |

### <a name="code-samples"></a>Esempi di codice

L'esempio di codice WSSQL illustra come comunicare tra Microsoft OLE DB e Windows ricerca tramite SQL. L'esempio di codice WSOleDB illustra Active Template Library (ATL) OLE DB l'accesso alle applicazioni di ricerca Windows e due metodi aggiuntivi per il recupero dei risultati da Windows ricerca. Entrambi gli esempi sono disponibili in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

## <a name="related-topics"></a>Argomenti correlati

### <a name="reference"></a>Riferimento

[Valori letterali](-search-sql-literals.md)

[Uso delle ricerche localizzate](-search-sql-usinglocsearches.md)

[Informazioni sui valori di pertinenza](-search-sql-understandingrelevancevalues.md)

[Mapping delle proprietà](-search-3x-wds-propertymappings.md)

[Sintassi di ricerca avanzata](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a>Informazioni concettuali

[SQL Estensioni in Microsoft Windows Search](-search-sql-extensions-sps.md)

[SQL Funzionalità non disponibili in Microsoft Windows Search](-search-sql-featuresunavailableinspssearch.md)

[Identificatori](-search-sql-identifiers.md)

[Distinzione tra maiuscole e minuscole nelle ricerche](-search-sql-casesensitivityinsearches.md)

[Riservatezza dei segni diacritici nelle ricerche](-search-sql-accentinsensitivitysearches.md)

[Cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md)

[Mapping dei tipi di dati](-search-sql-datatypemappings.md)
