---
description: La clausola WHERE in una query specifica un set di elementi in base ai quali confrontare i risultati.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306114"
---
# <a name="reusewhere-function"></a>ReuseWhere (funzione)

La clausola WHERE in una query specifica un set di elementi in base ai [quali](-search-sql-where.md) confrontare i risultati. Le query successive possono condividere il lavoro eseguito per una query precedente utilizzando la funzione ReuseWhere in una nuova clausola WHERE della query. Le query che sfruttano i vantaggi di questa funzione vengono eseguite più velocemente.

## <a name="examples"></a>Esempio

Nello scenario seguente viene illustrato come utilizzare la funzione ReuseWhere:

1.  Eseguire la query seguente:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  Dal set di righe restituito si ottiene un [ID where](-search-sql-rowset-properties.md), *Query1WhereID*.

    Il dove ID è una proprietà del set di righe con propset {aa6ee6b0-e828-11D0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 e il tipo UI4.

3.  Viene eseguita una seconda query con la funzione ReuseWhere, passando il *Query1WhereID* dal passaggio 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

La seconda query è equivalente alla seguente:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



La funzione ReuseWhere può essere utilizzata nella clausola [where](-search-sql-where.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

[Proprietà del set di righe](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



