---
description: "Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:"
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Istruzione SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1df8cc5f4b6bab673d20c981e44386d3fdbd651b5a2753d8c965ee55023a6562
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118227196"
---
# <a name="select-statement"></a>Istruzione SELECT

Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Di seguito viene illustrata la parte di colonna della sintassi dell'istruzione SELECT:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Gli identificatori di colonna devono essere colonne di nomi di proprietà valide, separate da virgole. I nomi di colonna validi sono descrizioni di proprietà registrate o sono definiti dallo schema del sistema di proprietà della shell. È possibile selezionare solo le colonne contrassegnate come recuperabili nello schema del sistema di proprietà. Se si usa la distinzione tra maiuscole e minuscole per identificare proprietà che non sono proprietà definite dal sistema, è necessario racchiudere l'identificatore di colonna tra virgolette doppie. I nomi delle proprietà definite dal sistema includono tutte le proprietà che iniziano con "System", ad esempio System.Contact.FirstName, e non richiedono le virgolette.

> [!Note]  
> È anche possibile racchiudere i nomi delle proprietà definite dal sistema tra virgolette doppie per una leggibilità. Ciò non influisce sulla compatibilità.

 

Quando la query restituisce un documento che non dispone della colonna richiesta, il valore di tale colonna per il documento è **NULL.**

È necessario specificare almeno un nome di colonna in un'istruzione SELECT. Nella query Structured Query Language (SQL) è possibile usare l'asterisco ( ) per specificare che devono essere restituite tutte \* le colonne di una tabella. Tuttavia, nessun set definito e fisso di proprietà si applica a tutti i documenti. Per questo motivo, l'SQL asterisco non è consentito <columns> nell'identificatore dell'istruzione SELECT.

## <a name="getting-the-top-n-results"></a>Recupero dei primi n risultati

È possibile specificare un numero massimo di risultati da restituire usando la sintassi TOP:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Cast dei tipi di dati delle colonne

A volte potrebbe essere necessario eseguire il cast dei dati stringa estratti dai documenti come un altro tipo di dati in modo da poter eseguire un confronto appropriato. Per altre informazioni, vedere [Cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).

## <a name="examples"></a>Esempio

Negli esempi seguenti vengono restituiti il nome e l'URL dei documenti corrispondenti.


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> </dl>

 

 



