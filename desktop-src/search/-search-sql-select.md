---
description: "Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:"
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: Istruzione SELECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306110"
---
# <a name="select-statement"></a>Istruzione SELECT

Di seguito viene illustrata la sintassi di base dell'istruzione SELECT per una query locale:


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



Di seguito viene illustrata la parte della colonna della sintassi dell'istruzione SELECT:


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



Gli identificatori di colonna devono essere colonne di nomi di proprietà valide, separate da virgole. I nomi di colonna validi sono descrizioni di proprietà registrate o sono definiti dallo schema del sistema di proprietà della shell. È possibile selezionare solo le colonne contrassegnate come recuperabili nello schema del sistema di proprietà. Se si usa il caso misto per identificare le proprietà che non sono proprietà definite dal sistema, è necessario racchiudere l'identificatore di colonna tra virgolette doppie. I nomi di proprietà definiti dal sistema includono tutte le proprietà che iniziano con "System" (ad esempio, System. Contact. FirstName) e non richiedono virgolette.

> [!Note]  
> È inoltre possibile racchiudere i nomi delle proprietà definite dal sistema tra virgolette doppie per migliorare la leggibilità. Questa operazione non influisce sulla compatibilità.

 

Quando la query restituisce un documento che non dispone della colonna richiesta, il valore della colonna per il documento è **null**.

È necessario specificare almeno un nome di colonna in un'istruzione SELECT. Nella query Structured Query Language (SQL) è possibile utilizzare l'asterisco ( \* ) per specificare che devono essere restituite tutte le colonne di una tabella. Tuttavia, nessun set definito e fisso di proprietà si applica a tutti i documenti. Per questo motivo, l'asterisco SQL non è consentito nell' <columns> identificatore dell'istruzione SELECT.

## <a name="getting-the-top-n-results"></a>Recupero dei primi n risultati

È possibile specificare un numero massimo di risultati da restituire usando la sintassi TOP:


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a>Cast dei tipi di dati delle colonne

In alcuni casi potrebbe essere necessario eseguire il cast dei dati di tipo stringa estratti da documenti come un altro tipo di dati, in modo da poter effettuare un confronto appropriato. Per ulteriori informazioni, fare riferimento a [cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).

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

 

 



