---
description: La clausola WHERE in una query specifica un set di elementi con cui trovare la corrispondenza dei risultati.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: Funzione ReuseWhere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f073a7ac0d5faf5973d08ff53ccebdacf8bead080a53e2d9a4a6ae9ed5724db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944661"
---
# <a name="reusewhere-function"></a>Funzione ReuseWhere

La [clausola WHERE](-search-sql-where.md) in una query specifica un set di elementi con cui trovare la corrispondenza dei risultati. Le query successive possono condividere il lavoro eseguito per una query precedente usando la funzione ReuseWhere in una nuova clausola WHERE della query. Le query che sfruttano questa funzione vengono eseguite più velocemente.

## <a name="examples"></a>Esempio

Lo scenario seguente illustra come usare la funzione ReuseWhere:

1.  Eseguire la query seguente:
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  Dal set di righe restituito si ottiene un [ID Where](-search-sql-rowset-properties.md), *Query1WhereID*.

    Where ID è una proprietà del set di righe con PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8 e tipo UI4.

3.  Si esegue una seconda query con la funzione ReuseWhere, passando *Query1WhereID* dal passaggio 2:
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

La seconda query è equivalente alla seguente:


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



La funzione ReuseWhere può essere usata nella clausola [WHERE.](-search-sql-where.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Riferimento**
</dt> <dt>

[Clausola WHERE](-search-sql-where.md)
</dt> <dt>

[Proprietà del set di righe](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



